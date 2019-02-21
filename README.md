# Data Analysis of the Secret Skirmish

[Original reddit thread](https://www.reddit.com/r/FortniteCompetitive/comments/asa8vy/data_analysis_of_the_secret_skirmish_full/)

Analysis was done in Python with Pandas and Matplotlib.
The data can be found [here](SecretSkirmishKillFeed.csv).

I recently discovered that the killfeed for the Secret Skirmish Solos event was broadcasted, so in this thread, I try to present this data in a meaningful way. The hardest part was definitely gathering the data. The killfeed VODs were not saved, so I had to go through Twitch Clips and Myth's stream to manually collect the data. In total, it took me 6 hours to collect everything. It wasn't fun, but someone had to do it.

As a disclaimer, I'm not a stats or data science guy by any means, but I'm trying to get better at it. So, feel free to leave some criticism or suggestions on other data I could present.

# Full Standings

First, I calculated the standings of all the players. I believe that this was shown only for Top 20 and without detail. 

[Full Standings](https://imgur.com/a/CKfZSiJ)

First thing to note is that Saf has more kills and a better avg. placement than Bizzle, the winner. Had Saf gotten 1 more point, he would've won. Just shows how clutch Bizzle's second win was. 
Highest placing EU player: Pate1k (6th). Highest placing controller player: Flossen (39th). Highest placing free agent: Kyzui (4th). Other notable placings are Nickmercs at 90th and Chap at 89th. Ghost members somehow manages to consistently place next to each other. Sean, Aydan, Kayuun, Dmo and Thwifo ranked 63, 64, 66, 67, and 68th, respectively. XXIF and TriggySoars completely tied, so I flipped a coin to decide who gets 59th. XXIF won.

[Top 10 Avg. Placement](https://imgur.com/LzgFqTO)

[Bottom 10 Avg. Placement](https://imgur.com/MjzVQ5M)


Overall, Saf has the best average placement, averaging 14th place. His landing spot was the oasis close to Westworld. Nickmers had the worst, averaging 89th. He dropped Shifty Shafts rather than Tilted for this entire series, and died to Tocata 3 times early game. Nickmercs, Chap, Slobings, Aydan, and Overpeek never made it past the 2nd circle.

Also, notice how low average placement is not a good indicator of how well you'll place in this format. We will try to fix this by applying another format to the results in a later section.

[Top 10 Most Kills](https://imgur.com/jmR7dO3)

Saf wins this category with 20 total kills. Only 3 players did not get a single kill (Lyricen, Overpeek and Dark). 

Notice how 9 of the top 10 killers make it to Top 10 overall. This implies that total kills are a good indicator of how well you'll place in this format.

# Playstyles

We can try to infer the playstyles of the top 20 Players by looking at how their kills are distributed across early, mid, and late-game. In the following graph, black dots represent kills and red dots represent deaths. Each box represents the distribution of kills across storm phases for each player.

[Distribution of Kills across Storm Phases for Top 20 Players](https://imgur.com/X3FNzS6)

Bizzle (17 kills) and Saf (20 kills) consistenly made it to end game and were actively getting kills during all phases of the game. Vivid (17 kills) suffered from 2 early/mid game deaths, putting him behind Saf and Bizzle. Just goes to show the importance of being strong in all 3 phases of the game consistently. 

For example, Vinny1x (5 kills) played purely for late game, with 0 early game kills and 5 total kills overall. His strong late game put him on the board, but it wasn't enough to get top 10.

On the other hand, roatdw had the strongest early game. 9 of his kills were before 3rd circle. He was able to get 18th without a single placement point and only made it to late game once (anyone know where he landed?). As we can see, roatdw's strong early game singlehandely put him in Top 20, but his early deaths prevented him from placing top 10.

Pate1k (16 kills) also went for a lot of early game kills, but, unlike roatdw, managed to survive long enough to get a couple of mid and late-game kills, placing him in 6th place overall.

Vicaros (8 kills) died 4 times in early game without scoring a single point, but his top 3 7-kill game was enough to put him on the board. As they say, all it takes is one game. 

The same could be said about 72hrs (13th). He only made it to top 10 once, the game he won, and didn't do so well for the rest of the tournament.


# Point System

Recently, there's been a lot of criticism of the current point system. I can certainly see why. Many players such as Fulmer, Bowman and Naga Ops did not place despite having more kills and better average placement than many players in Top 20 (Zayt, Blind, Vicaros). They simply did not get their kills in the right order or placed just outside the unforgiving placement point thresholds.

I decided to apply a different point system to the results to see how it would've played out. I applied the point system outlined in [this thread](https://www.reddit.com/r/FortniteCompetitive/comments/aog6g0/alternative_point_system/) by /u/IvoAlbino, because it seems to be well received. Under this system, every kill is rewarded and more placement points are given. 

> (KILLS \* PLACEMENT FACTOR**) + PLACEMENT POINTS

> Kills: 10 points per kill

>Placements

> 50th - 26th: 10 points

> 25th - 21st: 20 points

> 20th - 16th: 30 points

> 15th - 11th: 40 points

> 10th - 6th: 50 points

> 5th - 2nd: 60 points

> 1st: 80 points

> **Placement Factor:

> 100th - 76th: * 1.5

> 75th - 51st: * 1.5

> 50th - 26th: * 1.6

> 25th - 21st: * 1.6

> 20th - 16th: * 1.7

> 15th - 11th: * 1.7

> 10th - 6th: * 1.8

> 5th - 2nd: * 2.0

> 1st: * 2.5
​

Here are the results:

[Full Standings Under IvoAlbino's Point System](https://imgur.com/a/LleMWQy)

Some obvious observations are Saf at 1st, Tfue at 4th and Psalm at 11th. Zexrow, LeNain, Mmaetoss and Fulmer enter the top 20. LeNain (5 kills, avg. placement: 19) benefitted the most from this format, jumping from 37th to 16th. roatdw, Vicaros, 72hrs and Blind are kicked out of the top 20. roatdw suffered the most out of this format, going from 18th to 36th place. His aggressive playstyle does not work out in this format. 

[Top 10 Avg. Placement](https://imgur.com/wXQVuB4)

Notice how avg. placements now becomes a better indicator of how well you'll place in this format. They all make top 20, except Anthony whose great placements are not enough to balance his lack of kills.

[Top 10 Kills](https://imgur.com/DjpIa8l)

Your total kills still remain a great indicator of how high you'll place, but it's less forgiving to players such as roatdw, who don't play the survival game.

[Secret Skirmish Results under ESL Katowice ruleset](https://imgur.com/a/h3FYHBz)

With the ESL Katowice Tournament coming up in 2 weeks, we can analyze what types of playstyles will give pros the better chance of placing high.

As we can see, there's a way higher emphasis on placement. Players with great placement and low kills (Zexrow, Mmateoss, Vinny1x and Lenain) all jumped to Top 10. Ideally, you obviously want to get both a really good avg. placement and high number of kills, but if you have to choose, definitely go for placement. You can get 50 kills, without any placements points and you still probably won't get top 10. 

# Weapons

[Weapon Distribution](https://imgur.com/8Bxg0ht) (max and min represent max and min distance kill)

#### Fun Facts

- Surprisingly, there was not a single RPG kill, unless somehow RPG counts as a Grenade. 
- roatdw was the player who died to the plane turret. Perhaps, as karma for pushing 72hrs twice with a plane during the pop up cup. 
- Tendons died to InstantEnvironmental?? I don't know what that is, but if I had to guess, it's the storm surge.
- Vinny1x killed himself the most. Died 2 times to FallDamage and once to zone.
- Aspect had the most shotgun kills (11).
- Saf had the most Rifle kills (11).
- Morgausse's only kill was also the farthest kill in the entire tournament (242m pistol kill on Nistic).
- Tfue and Bizzle had the most weapon variety (6 kills with 6 different weapons). 
Bizzle's  weapons: Sniper, Rifle, Shotgun, Smg, FallDamage, Pistol. 
Tfue's weapons: Trap, Shotgun, Rifle, GrenadeLauncher, FallDamage, Smg.
- Poach died twice to Vivid and once to 72hrs.

I also calculated the average kill distance for players with more than 5 kills.

[Highest avg. distance (Kills)](https://imgur.com/mK1PEzy)

[Lowest avg. distance (Kills)](https://imgur.com/7OsukQn)

The data makes sense for players like Bizzle and Tfue who usually play for high ground and third party kills. 

# Storm Phases

[Player count across Storm Phases for each Match](https://imgur.com/KlRFJF0)

Not a lot of interesting info here. The deadliest zone is zone #1. Second deadliest is zone #6. Top 10 usually happens in Zone #7 and Zone #8. In my opinion, it's kind of harsh that a lot of players who make it this far do not get rewarded at all. It takes 20+ minutes to reach Zone #7, yet dying at 11th is equivalent to dying at 100th. 

I wanted to create a graph of player count vs. time, but I was not able to get the time data for all the kills. I tried doing player count vs. storm phase, but it turned out pretty ugly and did not show anything meaningful.

# The End

Anyway, that's it for now. I hope some of it was insightful, or at least entertaining. Let me know if there's anything I missed, anything I got wrong or anything else you'd like to see.


