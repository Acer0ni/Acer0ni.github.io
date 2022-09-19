+++
title = "SY0-601 Training Course"
date = "2022-09-19T15:22:17-07:00"
author = "Larry Flint"
authorTwitter = "0xaceroni" #do not include @
cover = ""
tags = ["", ""]
keywords = ["", ""]
description = ""
showFullContent = false
readingTime = true
draft=false
+++

Well, long time no see. Sorry for the lack of posting, but I had some personal things come up. My Monday started strong, or so I thought. I sat down and wrote a solution I was 100% would work for [Add Border](https://app.codesignal.com/arcade/intro/level-4/ZCD7NQnED724bJtjN/solutions), only to be met by an error I had never seen before `circular reference detected`. I looked it up only to find that it's usually caused by improper keys, or trying to serialize to JSON improperly, neither of which I was doing in this case. I spent the rest of the time allocated trying to figure it out, before shooting a message to a friend asking for help. About an hour later, he pointed out I was accidentally trying to append a list to itself and that was my problem.

Coursework was a weird little today, I started with one course before meeting a paywall after about an hour. I messaged the friend who set up this crash course and mentioned it, and he told me I should be taking week seven and take the class that I took yesterday. So I did, and rejoined my good friend professor Messor with the [SY0-601 Training Course](https://www.professormesser.com/security-plus/sy0-601/sy0-601-video/sy0-601-comptia-security-plus-course/). I didn't get to finish it being about an hour behind at this point, but luckily as much of the security adjacent stuff and the actual security course I took last week it was a lot of reviews. We went over the many types of attacks today, and told some stories about major viruses or attacks as he went. My favorite was the guy who lost the one-letter Twitter name because the attacker managed to get the last four digits of his CC number, then used that information to control his domains with his registrar, and held them ransom for control over the Twitter account. In the end, Twitter gave the account back but I thought it was a brilliant piece of social engineering.
