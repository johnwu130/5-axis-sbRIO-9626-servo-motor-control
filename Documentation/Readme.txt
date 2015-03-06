12/10/2014
進版到Servo Control (PID在FPGA上面做)
5軸closed-loop，V-command控制 (Axis 1-5，但第五軸沒有定義I/O，先預留)
利用sbRIO-9626 Analog Output (只有四個channel AO，所以只有4軸)
每軸具有Find Limit/Home功能
No encoder feedback (但未來可以加)
No Position Capture/Breakpoint (但未來可以加)

Reset Position要小心，不然會有following error。
SOP:
1. 先手動將AO歸零 (利用AO Override 按鈕)
2. 把Encoder和Trajectory都歸零
3. 再把AO放掉，回歸PID Control。


11/05/2014

為星協科技cUMI-01板子所compile的版本。
整理了code和project，以前test code拿掉。
此版本功能包括:
5軸open-loop，P-command控制 (Axis 1-5，但第五軸沒有定義I/O，先預留)
每軸具有Find Limit/Home功能
No encoder feedback (但未來可以加)
No Position Capture/Breakpoint (但未來可以加)

8/25/2014

Updated for LabVIEW 2014.


6/03/2014

*8-Axis (Manual).vi
*8-Axis (Producer Consumer - PC).vi

No Changes


*8-Axis Roadshow Demo.vi

Added 3 sequences to program.  Auto cycles.

*8-Axis Roadshow Demo KNR-IPAD.vi

Testing version for KNR daughterboard.  Motor is 1600 cts/rev.

*8-Axis Roadshow Demo WPC-IPAD.vi
*8-Axis (Manual) WPC.vi

Final version for WPC daughterboard.  Motor is 200 cts/rev.


*8-Axis RS Coordinate Move (bad).vi

This is an attempt to use coordinate (vector) moves to make
multiple axes move simultaneously.  It works, but every time when
we switch from individual axis control to vector control, the position
resets to 0!  This behavior is only seen when SoftMotion is deployed to 
RT and UDV axes.  This is not seen when just using simulated axes on RT.
This remains an open issue to investigate.


Consumer Loop includes new cases, "Reset" and 'Coordinate Move".
"Stop" case also stop coordinate moves, if any.



John Wu