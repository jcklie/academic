---
title: "Cash Clash - Our Ludum Dare 44 Game"
date: 2019-05-01
tags: ["godot", "ldjam", "programming"]
---

Over the years, I heard a lot about Game Jams, online competitions in which you need to develop a game from scratch including assets in a limited time frame, often a weekend. I always wanted to participate in one, but life always got in the way. For the [Ludum Dare 44](https://ldjam.com/events/ludum-dare/44/), which took place from Saturday April 27th to Tuesday April 30th, 2019, I finally decided to attend no matter what. A colleague of mine, *mbugert*, participated in previous installations and we agreed to join forces this time. I was happy that I can follow him and leverage his experience.

<p align="center">
<img src="https://raw.githubusercontent.com/jcklie/ludum-dare-44/master/menu/splash_screen.png"/>
</p>

Game Jams are virtual events, everyone can work wherever he or she wants and finally submit the game online over the internet. While this is nice, [a department of my university](https://www.kom.tu-darmstadt.de/news-events/game-jams/ludum-dare-44/) hosts a place where you can collaborate with other people, sit and collaborate. They also sponsor water, breakfast and we ordered lunch together.

For the game programming itself, I prepared some frameworks: for an all-in-one game engine, I wanted to use [Godot](https://godotengine.org/) as I heard a lot good about it (Unity in faster and easier). As a backup, I looked into [PyGame](https://www.pygame.org). I was told that one should be familiar with the tools beforehand, as time is scarce during the competition so I dabbled with both before.

Every Ludum Dare, a topic is selected. The topic this time was *"Your life is currency"*. When I first heard it on the first morning of the event, I thought that the most obvious game would circle around *"deals with the devil"*, that is sacrificing things like hitpoints for upgrades. As I did not want to follow the obvious, I played with the idea to misinterpred it so that your game character *is a currency*, e.g. you play as a Euro, Yen or Dollar sign.

With this idea, I went to the home for the weekend in the university. I met a new friend there, *tomatenbrei* and we talked about the topic, what we prepared and more. *mbugert* then also arrived and we brainstormed more. The other teams also pregrouped mostly and had their own twist on the topic. You can find their games [here](https://www.kom.tu-darmstadt.de/news-events/game-jams/ludum-dare-44/). We decided to group together as a team of three. Our final idea was a multiplayer arena top down shooter where you play as a currency symbol. From our manual:

> You and other currencies move around in an arena, firing bullets and dodging enemy projectiles. Besides regular movement, you can also utilize a dash skill to surprise your opponent.
>
> The strength of your weapons and your own armor scales in real time with the currency strength. The current timepoint is highlighted with a white vertical line and you can see some seconds into the future to plan your next strategic steps.
>
> It is also possible to change your currency. This is possible in one of the exchange stops which are spread over the map. When you switch to a better currency, you will loose health (but gain weapon strength and armor) - switching to a worse currency will increase your health but lower your strength and armor. But keep in mind that the currencies values keep changing! However, you will keep the health you gained.
>
> The game always uses three player characters, each playing as an individual currency. In the main menu, you can define how many of them are controlled by humans. You can only change to other currencies which are not already taken by other players.
>
> Hint: When you play the game for the first time, you should definitely start it in three players mode - even when you want to play alone. The AI is quite powerful and would most likely frustrate you when you directly fight against it. In your next rounds, you can decrease the number of human players to two such that the AI takes over a single player character. If you feel prepared enough after some training, you can switch to the true single player mode.

*mbugert* also brought two Steam controllers which we would use for the multiplayer part. For single player, we wanted to integrate a simple AI.

## The competition

On the first day, I drew the tiles, weapons bullets and the first map in the first hour of the game jam. Of course, we said "we would change it later", but later turned out to be never. Both of my team mates had not worked with Godot up till then, so they started the day with tutorials. Then, *mbugert* rendered the currency symbols with [OpenSCAD](https://www.openscad.org/) and Python magic in 16 directions. Afterwards, he integrated these assets and their rotation into the game. *tomatenbrei* started the AI until it could walk around and implemented the currency chart. I implemented the basic controls and shooting and dashing. We did not work too late; I was home at around 10. When I was home, I added the particle blood effect on hit for fun. The game for me was already fun, as you could run around as a currency symbol and shoot things .

On the second day, I was really tired and did not do that well. I added the cross bow, fixed the collosion (I really do not like collision layers) and fixed some bugs. *mbugert* did nice weapon audio, death and win jingles and improved the characters. *tomatenbrei* improved the AI so it did not run into things and started to add the damage scaling.

On the third day, it felt like I was working on this game forever. The time passes so quickly, and the two days before felt identical. *mbugert* added the currency conversion in a heroic effort. *tomatenbrei* made the AI shoot and had to make it deliberately worse, as it would kill you instantly otherwise. He also wrote the README and prepared our submission. At the end, I did the game cycle of starting and winning the game, menu and added the steam controller support. The game was fun and played nicely at that point in the evening, and we decided to not crunch. Finally we polished the game a bit, created some additional maps and then went home - 9 hours before the deadline. The other teams stayed longer, I really admire the tenacity, I was really weary after just three days of game jam.

## Aftermath

We used Godot for the first time in a real game. I found it much easier to get started than Unity. The scripting is nice, the UI is good and intuitive, it is fast and there are many resources on the Internet to help you. The controller integration was really easy, it was fun to play with three players and shoot each other.

The export to an executable itself was really easy. Sadly, we did not manage to get a good WebGL export, as it would lag. After the competition, I was told by other participants on how to do that, the more you now.

What we did not like is Godot together with Git, as Godot generated Ids for everything. If two people work on the same scene, then ids after a merge point to different things, breaking lots of stuff. Besides that, I really liked the engine.

In retrospective, the programming and collaboration went really smooth, we had enough to do and split the work so that nobody was under- or overworked. We were really to meet *tomatenbrei* at the  event, as he did the AI alone; without it, the game would be multiplayer (with game controllers!) only, not so good for other people to try out. One problem was that our team did not have a graphics person. That is why I did the menu and tile set, which is really ugly. Three days of game development sound easier than it is, I gladly anticipated that and had vacation at home afterwards.

You can find our game on the [LD44 website](https://ldjam.com/events/ludum-dare/44/cash-clash) and the source code on [Github](https://github.com/jcklie/ludum-dare-44). After we submitted our game, we rated other games, as then your game gets more exposure on the competitions' website. Now we wait 3 weeks for our score.

You can find a gameplay video on YouTube, where I play against some AI players.

<iframe align="middle" width="560" height="315" src="https://www.youtube.com/embed/Ydjk-2oP6GQ" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

## Update

Our results are in:

<table class="-items">
    <tr><td>Overall:</td> <td><strong>708</strong><sup>th</sup> (3.29 average from 33 ratings)<td></tr>
    <tr><td>Fun:</td> <td><strong>314</strong><sup>th</sup> (3.548 average from 33 ratings)<td></tr>
    <tr><td>Innovation:</td> <td><strong>373</strong><sup>rd</sup> (3.323 average from 33 ratings)<td></tr>
    <tr><td>Theme:</td> <td><strong>551</strong><sup>st</sup> (3.359 average from 34 ratings)<td></tr>
    <tr><td>Graphics:</td> <td><strong>958</strong><sup>th</sup> (2.672 average from 34 ratings)<td></tr>
    <tr><td>Audio:</td> <td><strong>626</strong><sup>th</sup> (2.65 average from 32 ratings)<td></tr>
    <tr><td>Humor:</td> <td><strong>354</strong><sup>th</sup> (3.161 average from 33 ratings)<td></tr>
    <tr><td>Mood:</td> <td><strong>777</strong><sup>th</sup> (3 average from 32 ratings)<td></tr>
</table>
<br />

In total, [2538 submissions were received](https://ldjam.com/events/ludum-dare/44/stats). People commented overall very kindly and we are around top 15% in *Fun*, *Humor* and *Innovation*. *Overall* is top 30%. I am really happy with this verdict for my first verdict, as we tried to make something besides the obvious topic interpretation. I feel bad that I ruined our *Graphics* rating, as I did the ugly tiles. If we did not have the rendered currency symbols by *mbugert*, then I do not want to imagine how bad the score for that would be.