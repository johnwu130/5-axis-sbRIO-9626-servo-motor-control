# 5-axis-sbRIO-9626-servo-motor-control
Code for doing servo motor control on NI sbRIO targets

This LabVIEW code was written to provide a basis for customers wanting to use sbRIO for multi-axis servo control applications.  This code provides a good transition into the high-volume deployment phase, if the user was previously prototyping with cRIO and NI-9514 modules.
 
Hardware:
sbRIO-9626
NI 9694 RMC Breakout Board (or some other RMC breakout board)
Servo Motor and Drive
 
Software:
LabVIEW 2014, Real-Time 2014, FPGA 2014
SoftMotion 2014
 
Notes and Features:
1. "Test Panel"-like operation directly from RT UI.  You can pick which axis to move, the kind of move to execute (i.e. vel move, rel pos move, etc.) and define the parameters of the move.
2. No limit switch functionality in this bitfile, but can be added in the future.
3. Encoder feedback and PID loop stable for all 5 axes.
4. The FPGA is big enough to support up to 5 axes, but the sbRIO-9626 only has 4 AO channels.  Code can be easily compiled for other targets.

Demo Instructions: (See attached doc)

Demo Video:
https://www.youtube.com/watch?v=tIiUsSXaO4g
