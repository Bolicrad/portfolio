---
title: Retrieve Dev Story
date: 2021-11-04 16:17:47
urlname: Retrieve
toc: true
tags: Game
categories: Portfolio
cover: https://img.itch.zone/aW1hZ2UvNDYxMjQzLzI1Nzg0NTQucG5n/original/nRAH4c.png
thumbnail: https://img.itch.zone/aW1nLzI1Nzg0NjAucG5n/original/BEN8Mr.png
---

This game was originated in a 7-day game dev camp in late July 2019. 

I can still remember that summer when I was still a curious, passionate, and enthusiastic rookie game developer, full of creativity. I didn’t have much experience in game programming at that time. But actually, that’s why I dare to take the role of “Programmer” of a game dev camp: not realizing how hard it is to become a real game engineer in the industry. 

## Ver. 0.1: Born from a wish

My teammates are mainly hardcore gamers. We admired our game experience in childhood, missed the feeling of taking an adventure in the delicate pixel worlds, and wished to bring such sense to modern gamers. That’s the motivation for our first design decision: making a 2D pixel-styled platformer adventure game.

<!-- more -->

During the week, I was focused on coding for the camera following mechanic (later solved by Unity plugin Cinemachine), implementing controller input frameworks, learning how to code for the bosses’ AI (with handwritten state machine), and preparing slides for pitching in the midnight before the due. It was the first time I felt like I was burned out in game development.

![](/gallery/Retrieve1.JPG)

Unfortunately, developing a platformer game is not as simple as playing Super Mario Bros. Our product after the week was not so ideal that I once believed it was the final form. The team should separate and keep walking on each one’s path. For a summer session, I took a flight from Beijing to Shanghai, then to Irvine, California. But before we went, my friend Daemon Pan and I decided to submit it to the Tencent Competition. This decision finally gave our project a possibility to be retrieved.

## Ver. 0.2: Rush, Game Developers!

When it was near the end of my summer school in UCI, A good news came out to me: Retrieve, the demo we submitted to Tencent, passed the first round filtering and entered the second round competition. I canceled all my previous schedules after flying back to China. Then in late August, the second day after I went back to China, I immediately rushed to Hangzhou, where we decided to gather again.

###### This round we reconstructed the whole project: 

* Art: Our artists’ productivity cannot support keeping the pre-painted level arts, so we shifted into Tiled Map. I integrated the unity 2d tilemap expansion into our project, then learned the rules of how tilemap distributes, instructed the art team to develop our first set of tiles.

* Design: I decided to utilize a Zelda approach to design the whole level structure of the game. We set 3 different themed sub-worlds. Each has a boss at the end of the level. After collecting three gems from 3 worlds, the secret portal to the final boss would open in the central room.

* Code: My handwritten state machine is not stable enough for AIs, and it was frustrating when I wanted to create some cross-frame logic. Thus a replaced the AI framework into a coroutine-based system, inspired by [a blog](https://www.gamedeveloper.com/programming/beyond-the-state-machine) from Jean Simonet. I then made 9 different kinds of regular enemies AI under the new framework and reconstructed all the 5 bosses’ AI. The efficiency was totally different.


![](/gallery/Retrieve2.JPG)

The development strength was extreme in this phase: Our work hour was usually extended to 3-4 am, with no rest on weekends. I celebrated my 22nd birthday in the hotel and turned back into development after finishing the cake. The word label on the corner of the cake said: “Wish you can win a reward!”. Such kind of work style made 2 of our artists exit the project after this phase. Later in the middle of September, Daemon and I finished the second version of Retrieve on the attic of his home.

## Ver. 0.3: From a demo into a game

5 days before October 2019, we were informed that we entered the third round of the competition, which means no more than 15 other teams are competing with us. Meanwhile, we could foresee that this would probably be our last version because other teams were hardworking, and we weren’t the most talented or experienced. This situation led us to one last design decision: Make it a game with complete structure, user interface, and storytelling elements. We gathered in Hangzhou again before October 1, 2019, which should have been a week-long holiday. Luckily, a new artist Chuxian joined us and helped us reproduce 4 sets of more exquisite tiles.

![](/gallery/Retrieve3.JPG)

###### In this phase, I have done the following works:

* Art: I again instructed the new artist about creating a tiled map, such as determining which side of the block should be continuous and which side should be unique. Under this rule, we even rebuilt the moving platform assets and evolved our art style from 8-bit into 16 bit.

* Design: In this cycle, I decided to add some Roguelike elements to the levels before the boss room: We don’t want to make it Cuphead-like. I designed several “level Chunks” and randomly combined those prefabs into a whole level. That inherits the idea of how Spelunky generates its level.

* Code: I coded for the level generate system mentioned before and worked on the cutscene manga system, which gives this game a narrative—the rest of the time to debug or work on minor systems.

As we predicted, the game was not able to enter the top 6. But Later, we were still be issued an excellence award, the proof of the Top 16 of this year. Because we all had to start preparing the application for the master’s program in November, the development was stopped. I was so proud of the product we created and appreciated everyone who devoted to this project.

#### Finally, we had a game like this:

{% youtuber video tu9jHgyxQGw %}
{% endyoutuber %}

## Postmorterm from 2021

I recently downloaded it from itch.io, to play the game again and write something for this new portfolio site. I found some obvious weakness, form both player and developer's perspective:

#### 1. The jumping action was poor designed.

I cannot remember clearly how this fuction was crafted, but jumping in this game is not powerful, but sometimes frustrating. We have many platforms that the player need to use double jump, but actually the character itself cannot jump twice after once performed wall-jump. It is a bug in design that we did not provide such affordance, but most players have this instinct from their experience in SMB or Celeste. We should have consider this and do some special coding in profile.

#### 2. The Level-size/player-size ratio was too small.

The level chunks I created in the 0.3 version was not well tested. Some paths are only 3-block high, but our character have 2 block size. Considering better user experience, we should have made the level scale at least twice larger. The path from the start to the end of a paticular level was too long, either. The level generating principle was still cool, but specific data settings should be reconsidered. 

#### 3. The sword attack was weakened too much.
At the time we made the decision to make combining 4 elements into 10 magics, we were thinking about making this new feature the main way to defeat most enemies. But according to my recent test, this change made it impossible for regular-leveled players to beat up the bosses. We need to reconsider the system balancing.

#### 4. The Tiled Map has tiny seams among each block.

Minor tech error on rendering, but must have some way to solve.

#### To conclude, I have to say, as my fisrt completed game project, though Retrieve has a lot of design defects and engineering problems, it's still means a lot to me, and have the potential to be refined, or remastered in the future.

#### [Download from itch.io](https://mcatin.itch.io/retrieve)