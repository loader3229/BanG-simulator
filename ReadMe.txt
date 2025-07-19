BanG! Simulator 2.7 - 6th Anniversary Version
Made using GameMaker 8.x

music file path = data\music\bgm[ID].ogg / data\music\bgm[ID].mp3
score file path = data\score\[ID]ex.txt / data\score\[ID]sp.txt

use https://loader3229.github.io/BanGConverter to download and convert charts, support official and bestdori community charts

For Expert charts, just type ID. For Special charts, type ID and +, example: 123+ will load SP chart for ID=123.
ID can contain alphabets and numbers.

[Effect]
Place effect files to data\effect\normal, data\effect\flick and data\effect\slide.

[Note Format]
Normal Note Format
beat/notetype/lanenumber
ex) 8/2/1	<- flick at beat 8 on 1st lane

Normal Note Types
0 music (use 0/0/0)
1 normal
2 flick
3 slide a start
4 slide a among
5 slide a end
6 slide b start
7 slide b among
8 slide b end
9 old long note (deprecated)
10 fever single
11 skill note
12 slide a end flick
13 slide b end flick
14 catch note (2.7)
15 slide a end among (2.7)
16 slide b end among (2.7)
20 bpm change (beat/20/bpm) ex) 5/20/160		<- change bpm at beat 5 to bpm 160
21 long note start
25 long note end
26 long note end with flick
31 long note start with skill (1.30)
32 long note end with skill (1.30)
33 slide a start with skill (1.30)
34 slide a end with skill (1.30)
35 slide b start with skill (1.30)
36 slide b end with skill (1.30)
40 alternative skill note using skill2.wav  (2.7)
41 slide a among hidden (2.0)
42 slide b among hidden (2.0)
51 directional flick left width 1 (2.0)
52 directional flick left width 2 (2.0)
53 directional flick left width 3 (2.0)
54 directional flick left width 4 (2.0)
55 directional flick left width 5 (2.0)
56 directional flick left width 6 (2.0)
57 directional flick left width 7 (2.0)
58 directional flick left width 8 (2.3)
59 directional flick left width 9 (2.3)
61 directional flick right width 1 (2.0)
62 directional flick right width 2 (2.0)
63 directional flick right width 3 (2.0)
64 directional flick right width 4 (2.0)
65 directional flick right width 5 (2.0)
66 directional flick right width 6 (2.0)
67 directional flick right width 7 (2.0)
68 directional flick right width 8 (2.3)
69 directional flick right width 9 (2.3)

Universal Slide Note Format
beat/notetype/slideid/lanenumber
ex) 8/71/2/1	<- slide ID 2 start at beat 8 on 1st lane
ex) 9/73/3/4	<- slide ID 3 end at beat 9 on 4th lane

Universal Slide Note Types
71 universal slide start (2.3)
72 universal slide among (2.3)
73 universal slide end (2.3)
74 universal slide end flick (2.3)
75 universal slide start skill (2.3)
76 universal slide end skill (2.3)
77 universal slide among hidden (2.3)
78 universal slide end among (2.7)

new note types in version 2.6-2.7
100 timing group start  (2.6) (ex. 0/100)
101 timing group normal (2.6)
102 timing group flick (2.6)
103 timing group universal slide start (2.6)
104 timing group universal slide among (2.6)
105 timing group universal slide end (2.6)
106 timing group universal slide end flick (2.6)
107 timing group universal slide among hidden (2.6)
108 timing group universal slide end among (2.7)
109 timing group skill (2.7)
110 timing group scrolling speed change (2.6)


[Chart Format]

1.offset
2.bpm
3.notes
....
....

ex)
46		<- note offset
131		<- song bpm
0/0/0		<- music start at beat 0
8/1/3		<- normal note at beat 8 on 3rd lane
8.5/1/6		<- normal note at beat 8.5 on 6th lane
8.75/1/6
9.25/1/1
10/1/6
10.25/1/6
10.75/1/1


setting.ini explaining

[Coord]
Topx=622		<- top x value
Topdistance=6		<- top distance between lanes
Topy=20			<- top y value
Botx=197		<- bottom x value
Botdistance=147		<- bottom distance between lanes
Boty=589		<- bottom y value
[Display]
Windowx=1280		<- window width (please always set to 1280)
Windowy=720		<- window height (please always set to 720)
Notesize=71		<- (2.3 update) note size (71 = 100%, 142 = 200%)
Notespeed=6		<- (2.3 update) note speed (not the GBP note speed, please go to bottom to find the corresponding note speed)
FPS=60			<- (2.7 update) target fps of the program. usually 60hz
[Music]
Sevol=40		<- sound effect volume
Musicvol=100		<- music volume
Offset=46		<- music offset
SEOffset=0		<- sound effect offset
[Settings]
Color=1			<- (2.3 update) color change when note is not fit by 1/GrayNoteMultiplier beat line
GrayNoteMultiplier=2    <- (2.3 update) 
Sameline=1		<- if two notes are in same timing, make a line (not support old longnote 9)
Mirror=0		<- (2.4 update) mirror the chart
ScoreCalculateType=0	<- (2.0 update) 0 for bandori-standard, 1 for arcaea, 2 for standard, 3 for bandori-new
ShowHidden=0		<- (2.2 update) show hidden slide among
Font=5			<- (2.3 update) 0 for MS Gothic, 3 for CN Server Font, 5 for Arial
ScoreFont=3		<- (2.3 update) 0 for MS Gothic, 1 for JP/EN Server Font, 3 for CN Server Font, 5 for Arial. When using JP/EN server font, maximum score display digits is 8, otherwise is 11.
ScoreDisplay=0		<- (2.4 update) if 1, The displayed score will have 2 decimal digits.
MV=0			<- (2.4 update) if 1, Enable Image-Based MV Mode.
PlayLine=0		<- (2.4 update) if 0, no playline will be displayed, otherwise data\playline\[ID].png will be displayed. Recommanded: 0 for normal mode, 1 for MV mode.
MVAlpha=0.3		<- (2.4 update) set the alpha of the MV. (0.0-1.0)
[Effect]		<- effect config
EffectEnable=1		<- if 0, no effect. if 1, enable image based effect
Size=0.71		<- effect image size multiplier
Normalx=300		<- center position of x in normal effect image
Normaly=589		<- y
Flickx=300		<- flick x
Flicky=589		<- flick y
Slidex=200
Slidey=589
Amongx=300		<- does not use for now
Amongy=589		<- does not use for now

[BandoriNewCalculation] <- (2.2 update) use the real calculation formula of BanG Dream! GBP APP (medley live is not supported)
Type=0                  <- (2.2 update) if 0, use floating-point calculation. if 1, use integer calculation as BanG Dream! GBP APP does.
Power=250000            <- (2.2 update) the power of your band
Difficulty=29           <- (2.2 update) the difficulty of the chart
SkillType=0             <- (2.4 update) if 0, skill notes use the same skill. if 1, first 5 skill notes will use the 1st-5th skills. 2 is averaged mode.
SkillTime=7             <- (2.2 update) the time of each skill (encore skill if SkillType is not 0), in seconds
SkillEffect=100         <- (2.2 update) the Score UP effect of each skill (encore skill if SkillType is not 0), in percent.
SkillTime1=7            <- (2.4 update) the time of the 1st skill, in seconds
SkillEffect1=100        <- (2.4 update) the Score UP effect of the 1st skill, in percent.
SkillTime2=7            <- (2.4 update) the time of the 2nd skill, in seconds
SkillEffect2=100        <- (2.4 update) the Score UP effect of the 2nd skill, in percent.
SkillTime3=7            <- (2.4 update) the time of the 3rd skill, in seconds
SkillEffect3=100        <- (2.4 update) the Score UP effect of the 3rd skill, in percent.
SkillTime4=7            <- (2.4 update) the time of the 4th skill, in seconds
SkillEffect4=100        <- (2.4 update) the Score UP effect of the 4th skill, in percent.
SkillTime5=7            <- (2.4 update) the time of the 5th skill, in seconds
SkillEffect5=100        <- (2.4 update) the Score UP effect of the 5th skill, in percent.

normal, gray, flick, slide, skill note sprite from https://github.com/BandoriDatabase/bangdream-data-viewer
directional note sprite from https://bestdori.com/



2.x Changelog by loader3229/qq1010903229

2.0 - New Note Types in GBP Version 5.0 Support
    - Note movement now based on time instead of tick, so the lag is reduced
    - Added Score Display (Types: Bandori-Standard, Arcaea)
    - The simulator now uses CN Server Font

2.1 - Performance Improvement
    - Added NPS Display
    - New Score Calculation Type: Standard
    - Fix a bug in chart 359+ (HELL! or HELL? SP)

2.2 - BanG! Simulator 3rd Anniversary! New opening page added!
    - Added Time, Progress Bar and Score Bar Display
    - Added Maximum and Average NPS Display
    - New Score Calculation Type: Bandori-New
    - Hidden slide among showing
    - Moving arrow added on directional notes
    - Added Font Change
    - Increased maximum score display digits to 10
    - New Chart Downloader!
    - Fixed some bugs

2.3 - Added Universal Slides! Now you can use more than 2 slides at the same time!
    - Non-Integer note lanes (0.0-8.0) support! (Any note type except directional)
    - The opening page now display options
    - The opening page now display Equivalent GBP Note Speed/Size
    - Note Speed range is now 0.0-1000.0 (Equivalent GBP Note Speed range (Estimation) 1.0-12.1)
    - More Font Changes
    - Fixed some bugs (such as directional note effect volume is not affected by effect volume options)

2.4 - BanG! Simulator 4th Anniversary!
    - Image-Based MV Mode Is Added! Now you can use MV in the simulator. Read mv\readme.txt for more details.
    - Added Mirror
    - More Score Display Options
    - Note Speed range is now 0.0-10000.0 (Equivalent GBP Note Speed range (Estimation) 1.0-13.0)
    - Fixed some bugs

2.5.0 - Added SE Offset Setting, MV Offset Setting and MV Playing Mode (for testing MV Configuration, or for anyone who likes just watching MV). Read mv\readme.txt for more details.
    - Fixed some bugs

2.6.0 - BanG! Simulator 4.5th Anniversary!
    - Added Timing Groups
    - Fixed some bugs

2.7 - New Note Types!
      - Updated Bass and Sin-Bass to latest version


This table is calculated using 60FPS.
BanGSim 2.3+ Note Speed   GBP Note Speed (Estimation)
0                         1.0
0.01                      1.6
0.02                      2.1
0.05                      3.2
0.1                       4.3
0.2                       5.5
0.5                       6.9
1                         7.9
2                         8.7
3                         9.1
4                         9.4
5                         9.6
6                         9.7
7                         9.8
8                         9.9
9                         10.0
11                        10.1
13                        10.2
16                        10.3
19                        10.4
23                        10.5
28                        10.6
35                        10.7
45                        10.8
60                        10.9
80                        11.0
100                       11.1
125                       11.2
150                       11.3
200                       11.4
250                       11.5
300                       11.6
400                       11.7
500                       11.8
600                       11.9
800                       12.0
1000                      12.1
1300                      12.2
1600                      12.3
2000                      12.4
2500                      12.5
5000                      12.8
10000                     13.0