12/10/2014
�i����Servo Control (PID�bFPGA�W����)
5�bclosed-loop�AV-command���� (Axis 1-5�A���Ĥ��b�S���w�qI/O�A���w�d)
�Q��sbRIO-9626 Analog Output (�u���|��channel AO�A�ҥH�u��4�b)
�C�b�㦳Find Limit/Home�\��
No encoder feedback (�����ӥi�H�[)
No Position Capture/Breakpoint (�����ӥi�H�[)

Reset Position�n�p�ߡA���M�|��following error�C
SOP:
1. ����ʱNAO�k�s (�Q��AO Override ���s)
2. ��Encoder�MTrajectory���k�s
3. �A��AO�񱼡A�^�kPID Control�C


11/05/2014

���P����cUMI-01�O�l��compile�������C
��z�Fcode�Mproject�A�H�etest code�����C
�������\��]�A:
5�bopen-loop�AP-command���� (Axis 1-5�A���Ĥ��b�S���w�qI/O�A���w�d)
�C�b�㦳Find Limit/Home�\��
No encoder feedback (�����ӥi�H�[)
No Position Capture/Breakpoint (�����ӥi�H�[)

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