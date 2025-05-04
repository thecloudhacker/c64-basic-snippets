# The Drone

You're in the middle of a psychadellic happening with your C64.
A tonal drone and regular ticking while colours shift on your screen and the famous maze pattern appears. 
Just a bit of fun really, testing out cycling of colours and audio output while plugging screens in.

## Code
```
10 POKE 641,1
20 PRINT CHR$(147)
30 A=0
40 B=1
50 BG=(15*RND(1))
60 FG=(15*RND(1))
70 POKE 54274,B:POKE 54275,A
80 POKE 54296,15
90 POKE 54273,28:POKE 54272,49
100 POKE 54278,240
110 POKE 54276,65
120 FOR T=1 TO 500:NEXT
130 POKE 54276,64
140 POKE 54296,0
150 PRINT CHR$(205.5+RND(1));
160 POKE 53280,BG
170 POKE 53281,FG
180 GOTO 50
200 REM TO CEASE AUDIO RUN POKE 54296,0
```

