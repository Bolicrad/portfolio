---
title: Retrieve Dev Story
date: 2021-11-04 16:17:47
urlname: Retrieve
tags: Game
categories: Portfolio
cover: https://img.itch.zone/aW1hZ2UvNDYxMjQzLzI1Nzg0NTQucG5n/original/nRAH4c.png
thumbnail: https://img.itch.zone/aW1nLzI1Nzg0NjAucG5n/original/BEN8Mr.png
---

This game was originated in a 7 day game gev camp in late July 2019. 

I can still remember at that summer, I was still a curious, passionate, and enthusiastic rookie game developer, full of creativity. I didn't have much experience in game programming at that time. But actually, that's why I dare to take the role of "Programmer" in game dev camp: not realized how hard it is to become a real game engineer in the industry. 

## Ver. 0.1: Born from a wish

My teammates are mainly hardcore gamers. We adimired our game experience in childhood, missed the feeling of taking adventure in the delicate pixel worlds, and wished to bring such feeling to modern gamers. That's the motivation for our first  design decision: making a 2D pixel styled platformer adventure game.

<!-- more -->

During the week, I was focused on coding for the camera following mechanic (later solved by Unity plugin Cinemachine), implementing controller input frameworks, learning how to code for the bosses' AI (with hand written state machine), and preparing slides for pitching in the mid night before the due. It was the first time I felt like myself was burned out, in game development. 

![](/gallery/Retrieve1.JPG)

Unfortunately developing a platformer game is not such simple as playing Super Mario Bros. Our product after the week was not so ideal, that I once believed that it was final form of the game, and the team should seperate and keep walking on each one's own path. I took a flight from Beijing to Shanghai, then to Irvine, California for a summer session. 

But before we go, I and my friend Daemon Pan decided to submit it to the Tencent Competetion. This decision finally gave our project a possibility to be retrieved.

## Ver. 0.2: Rush, Game Developers!

When it was near the end of my summer school in UCI, A good news came out to me: Retrieve, the demo we submitted to Tencent, passed the first round filtering and entered the second round competetion. I canceled all my previous schedules after flying back to China, then on late August, I immediately rushed to Hangzhou, where we decided to gather again.

###### This round we reconstructed the whole project: 

* Art: Our artists' productivity cannot support keeping the pre-painted level arts, so we decided to shift into Tiled Map. I intergrated the unity 2d tilemap expansion into our project, then learned the rules of how tilemap distributes, instructed the art team to develop our first set of tiles.

* Design: I decided to utilize a Zelda approach to design the whole level structure of the game. We set 3 different themed sub-worlds, each has a boss in the end of the level. After collect 3 gems from 3 worlds, the secret portal to the fianl boss would open at the central room.

* Code: My hand written state machine is not stable enough for AIs, and it was frustrating when I want to create some cross-frame logics. Thus a replaced the AI framework into a coroutine based system, inspired by [a blog](https://www.gamedeveloper.com/programming/beyond-the-state-machine) from Jean Simonet. I then created 9 different kinds of normal enemies AI under the new framework and reconstructed all the 5 bosses' AI. The efficiency was totolly differernt.


![](/gallery/Retrieve2.JPG)

The strength of development was extremely strong in this phase: Our work hour usually extended to 3-4 am, no rest on weekends, either. I celebrated my 22th birthday in the hotel, and turned back into development after finished the cake. The word label on the corner of the cake said: "Wish you can win a reward!". Such kind of work style made 2 of our artists exited the project after this phase. Later in the middle of September, I and Daemon finished the second version of Retrieve, on the attic of his home.

## Ver. 0.3: From a demo into a game

5 Days before October 2019, we were told to entered the third round of the competetion, which means no more than 15 other teams are competing with us. In the meanwhile, we could forsee that this would probably our last version, because other teams were also hardworking, and we weren't the most talented nor experienced one. This situation led us to the last design decision: Make it a game, with complete level structure, user interface and storytelling elements.  We gathered in Hangzhou again before October 1, 2019, which should have been a week long holiday. Luckily, an new artist Chuxian joined us this time and helped us reproduced 4 sets of more exquisite tiles.

![](/gallery/Retrieve3.JPG)

###### In this phase I have done the following works:

* Art: I once again instructed the new artists about how to create tiled map, such as which side of the block should be continous, which side should be unique. We even rebuild the moving platform assets under this rule, evolved out art style for 8-bit into 16 bit.

* Design: In this cycle I decide add some Rougelike element to the levels before the boss room: We don't want to make it a Cuphead-like. I designed several "level Chuncks", and randomly combine those prefabs into a whole level. That inhereits the idea of how spelunky generates it level.

* Code: I coded for the level generate system mentioned before, and worked on the cutscene manga system, which give this game a narrative. Rest of time I devoted in debug or minor systems.

As we predicted, the game was not able to enter the top 6. But Later we were still be issued an exellence award, the proof of the Top 16 of this year. Because we all had to start prepareing the appication for the master's program from November, the development was stopped. I was so proud of the product we created, and really appreciated everyone who devoted to this project.

#### Finally we had a game like this:

{% youtuber video tu9jHgyxQGw %}
{% endyoutuber %}

## Postmorterm from 2021

I recently downloaded it from itch.io, to play the game again and write something for this new portfolio site. I found some obvious weakness, form both player and developer's perspective:

#### * The jumping action was poor designed.
