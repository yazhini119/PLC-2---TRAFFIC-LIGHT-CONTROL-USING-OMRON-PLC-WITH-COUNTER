# PLC-2---TRAFFIC-LIGHT-CONTROL-USING-OMRON-PLC-WITH-COUNTER

## Aim
To design and implement a Traffic Light Control System using Omron PLC with Timer and Counter instructions.

## Objective
1.	To understand PLC timer operation.
2.	To learn counter instructions in Omron PLC.
3.	To implement sequential traffic signal control.
4.	To restart the process automatically after a delay.

## Apparatus Required
•	Omron PLC (CP1E/CP1L)
•	CX-Programmer Software

## Theory
Traffic signals control the movement of vehicles and pedestrians. In this experiment, the lamps operate sequentially:
•	Red Lamp ON for 5 seconds
•	Yellow Lamp ON for 5 seconds
•	Green Lamp ON for 5 seconds
One complete cycle is counted by a PLC counter.
The sequence repeats only 5 times.
After completion of 5 cycles, the system waits for 10 seconds and automatically starts again.

## Procedure
1.	Connect PLC hardware.
2.	Assign I/O addresses.
3.	Create ladder logic using timers and counter.
4.	Download the program to PLC.
5.	Switch PLC to RUN mode.
6.	Press Start Switch.
7.	Observe traffic light sequence.
8.	Verify counter operation.
9.	Verify automatic restart after 10 seconds.

## I/O Address Assignment
Inputs
Device	Address
Start Switch	0.00
Outputs
Device	Address
Red Lamp	100.00
Yellow Lamp	100.01
Green Lamp	100.02
Internal Bits
Function	Address
Run Bit	W0.00
Step 1	W0.01
Step 2	W0.02
Step 3	W0.03

## Operating Sequence
Initial Delay
Start Switch ON
Wait 2 seconds
### Step 1
Red Lamp ON
Time = 5 sec
### Step 2
Red Lamp OFF
Yellow Lamp ON
Time = 5 sec
### Step 3
Yellow Lamp OFF
Green Lamp ON
Time = 5 sec
### Step 4
Green Lamp OFF
Counter increments by 1
### Step 5
If Counter < 5
Repeat cycle
### Step 6
If Counter = 5
Wait 10 seconds
Reset Counter
Restart from Step 1

## Flow Chart
START
  |
  
2 sec Delay
  |
  
Red ON (5 sec)
  |
  
Yellow ON (5 sec)
  |
  
Green ON (5 sec)
  |
  
Counter +1
  |
Counter = 5 ?
  |
 No --------> Repeat Cycle
  |
 Yes
  |
10 sec Delay
  |
Counter Reset
  |
Restart


Timing Table
Operation	Time
Initial Delay	2 sec
Red Lamp	5 sec
Yellow Lamp	5 sec
Green Lamp	5 sec
Total Cycle Time	15 sec
Number of Cycles	5
Restart Delay	10 sec



## Output

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/4718198b-a8d3-40eb-a5cc-9512a94dfeec" />















## Result
The traffic light control system was successfully implemented using Omron PLC. The Red, Yellow and Green lamps operated sequentially with 5-second intervals. The cycle repeated 5 times using a counter and automatically restarted after a 10-second delay.

