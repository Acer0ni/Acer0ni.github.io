+++
title = "Alien invasion"
date = "2022-07-07T12:35:47-07:00"
author = "Larry Flint"
authorTwitter = "0xaceroni" #do not include @
cover = ""
tags = ["", ""]
keywords = ["", ""]
description = ""
showFullContent = false
readingTime = true
draft=true
+++

Well, this project started as a way for me to continue my python ,a tutorial i found in [Python crash course](https://nostarch.com/pythoncrashcourse2e) by Eric Matthes. the idea started to form as the tutorial walked me through setting up a highscores for the game, but a problem that bugged me immediately was that there was no persistence there so as soon as you exited the app the highscores were gone forever and you would never be able to brag to your friends about your sweet new score. after the tutorial was finished i went back and refactored it to save the highscores locally but that still seemed hollow to me in todays connected world.

so after a little research on how bigger games handle this problem i started writing a server that takes care of authorization and keeps track of the highscores with plenty of ideas for the future.

I started with the server first, that being the part that i had done before and honestly not too much to say about it. i used djangos user models to keep track of the users and cookie based authentication which did most of the brunt of the work work for me. as i moved back to the game, honestly i was at a loss. i knew exactly as much of Pygame as the tutorial had taught me, which unfortunately for me was not the same knowledge i needed to do what i wanted to do. i spent a few days thinking about the overall design of the game and how i could slip a login screen into it without refactoring the whole thing.Once i felt i had a clear path i jumped in and started coding. at the end of the project it ended up pretty much how i had planned in the begining.

While the coding of the project went well the deployment was rocky, because the server was going to be hosted remotly i decided the dockerifying it would be the simpliest path. Docker is a great tool that i have used once before and was happy to get some more experience with so that part was pretty straight forward.Pairing it with nginx so that it could talk to the container took me a awhile and i needed a fair bit of help to get it done.

I thought deploying the game would be easy. Until i started writing the readme for the repo and as i write my technical docs as if i was explaining them to my grandma i knew i was losing a lot of potential users if my install instructions included the command line. I looked around and found Pyisntaller and learned how to use that. After two days of making sure i have the right python version installed and studying which flags to use to get a single exectuble i finally had it. an executable for mac's and windows or i thought i did. i moved the binary to my wifes computer and tried to run it. only to be met with a windows defender alert. a packager that pyinstaller uses was flagged as malware. I decided that i had sunk enough time into this part of the project and decided to try and do a binary in a later version
