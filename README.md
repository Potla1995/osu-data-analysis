# Rhythm games - player and beatmap analysis
(A project proposal for TDI Fellowship Program)
## What is a rhythm game?
+ A game where a song/music plays in the background,
+ Objects appear on the screen in rhythm to the music,
+ The player is supposed to hit the objects at the correct times.
+ Scores may depend on how _accuractely_ the player hits the object.

### Examples
Guitar Hero, Beat Saber, Piano Tiles, osu!, Sound Voltex, Cytus, Bang Dream,... and the list continues.

## What kind of data is available?
There are basically two types of data we can get a hold of.
### 1. Beatmap Data
A beatmap is something like a musical score, that represents the music. Mathematically, it's a map $f:[0,t]\to \mathbb N^2$, where $f(t)$ represents the position of an object at time $t$.

Every game has beatmaps for different songs, on which players compete.
### 2. Player Data
Whenever a player plays a beatmap, the game captures details such as:
+ Player's trajectory/cursor movement
+ Player's hit times

## What can we deduce from all these data?
There are two sides to this project: the beatmap side and the player side.

For a few reasons, we choose the rhythm game _osu!_ to perform the analysis:
+ _osu!_ is free to play,
+ All its data is available online or can be scraped using their API,
+ All the beatmap data are text files which can be easily read.

### 1. Beatmap Side
A preliminary analysis of this can be found [in this notebook](./osu-beatmap-data.ipynb). Basically the following information is analyzed:
+ Calculation of difficulty of beatmaps, using a classifier from [this repo](https://github.com/Potla1995/POT_Bot).
+ A plot of the beatmap difficulty showing that on average, they get harder with time.

The following could be directions for this part of the project:
+ Create a beatmap classifier of some sort using machine learning, that classifies "good" maps from "bad" maps.
+ Create an automated beatmap generator using machine learning, that can produce human-like beatmaps from any given music.

### 2. Player Side
This is more of an uncharted territory for me.

The data for this can be obtained using an API or from the specific game company by requesting for replay data of players on different beatmaps.

Things that can be deduced from such data possibly include answers to questions in Human-Computer Interaction, for example:
+ How does a player perceive a beatmap?
+ How long is a player's attention span before potentially messing up at some point of the song?
+ There is a lot of spatial and temporal information available for each player. How does that relate to reaction times and memory?
+ After what point do nerves kick in for players?
+ Maybe later on, there can be eye and hand tracking mechanisms. What kind of insight do these additional input give on human perception and reaction?

## Who are we aiming at with this project?
All rhythm game companies, basically. Such as Cytus, Bandai Namco, SEGA, etc. etc.
