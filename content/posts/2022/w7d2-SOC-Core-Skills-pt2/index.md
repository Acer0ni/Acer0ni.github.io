+++
title = "Antisyphon's SOC Core Skills day two"
date = "2022-09-13T15:42:56-07:00"
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

I finally did it! After learning last, I solved [reverseInParentheses](https://app.codesignal.com/arcade/intro/level-3/9DgaPsE2a7M6M2Hu6) night I could just use .extends to get my reverse string back into the stack. but even after I replaced all of the parentheses s with empty strings there was sometimes an opening parenthesis left behind. I spent most of the time trying to bug fix this as in my head it worked perfectly, after about 3 hours, while I was supposed to be practicing for my A+ cert, of printing out strings and reading what functions do through vs codes little tooltips I realized that my problem was with the range function the ending spot is exclusive but the starting is inclusive, I lowered the ending spot by one and it passed with flying colors!

Today I continued [SOC Core Skills ](https://www.antisyphontraining.com/soc-core-skills-w-john-strand/) with John Strand where we started our morning by talking briefly about the different CLIs and some of the basic commands to navigate with them. the cool thing today in a lab was that we infected our VMs with a malicious file. Then it talked us through how to use netstat and wmic to track it down as if we were security professionals which can be done by looking at all of your open ports with `netstat - naob` to find the PID and then using wmic with the pic to dig deeper into the data, funnily enough, the lab does not go over removing or stopping the malware so it still currently running on my VM.
