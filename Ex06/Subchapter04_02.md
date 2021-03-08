
![ACTEA](../Logo_ACTEA_2.png)
_____________________________________
# Emergency stop circuits
-   The [first goal](Ex06/Subchapter04_01.md) is to wire the electrical circuit for a direct online motor starter with safety relay logic.
-   The [second goal](Ex06/Subchapter04_02.md)  is to program and test PLC software for a direct online motor starter with safety relay logic.

Back to the [project scope](Ex06/Subchapter04.md).

## Goal 2 : Program and test PLC software for a direct online motor starter with safety relay logic
**Step 1 :** Create a new TIA Portal project
```javascript
Project name  : Ex6-SafetyCircuits
Author        : Your name
Comment       : Emergency stop circuits
```

**Step 2 :** Add a PLC-device with next CPU settings
```javascript
Type                          : See available CPU
System byte                   : %MB254
Clock memory byte             : %MB255
Digital input start address   : %IB0
Output start address          : %QB0
Analog input start address    : %IB64
IP-address                    : 192.168.0.30
IP-address subnet mask        : 255.255.255.0
```

**Step 3 :** Add next *Functions* (FC) into PLC_1 in the FBD program language:
```javascript
FC_DOL_EMS
```

**Step 4 :** Add the Function into *Organization block* Main [OB1]:
```javascript
FC_DOL_EMS into network 1
```

**Step 5 :** Create the necessary PLC Tags:
```javascript
iCC_BtnStop_S1 - BOOL - %I 0.0 - Stop button
iCC_BtnStart_S3 - BOOL - %I 0.2 - Start buttons
iCC_RlyEms_KES - BOOL - %I 1.0 - Safety relay OK
iCC_McbMot_QM1 - BOOL - %I 1.1 - Motor circuit breaker
iCC_ConMot_KM1 - BOOL - %I 1.2 - Feedback signal contactor
oCC_LmpStart_H1 - BOOL - %Q 0.0 - Lamp start
oCC_LmpStop_H3 - BOOL - %Q 0.2 - Lamp stop
oCC_ConMot_KM1 - BOOL - %Q 0.6 - Contactor motor
mMotStarted - BOOL - %M 0.0 - Motor started
```

<details>
	<summary>Click here to download the Ms Excel TAG List</summary><!-- Empty line after this one needed, do not delete! -->

<br>
Download file <a href="./Ex06/Documents/Actea_Ex6_Taglist.xlsx">here</a>.</p>

  </details><!-- Empty line after this one needed, do not delete! -->
<br>

**Step 6 :** Program in FC_DOL_EMS the software to start & stop the motor. Do not forget to program the lamps.
```javascript
Network 1 : Start-stop circuit "mMotStarted"
Start circuit = Start button
Stop circuit = Stop button AND Motor circuit breaker
```
```javascript
Network 2 : activate motor "oCC_ConMot_KM1 "
```
```javascript
Network 3 : Start lamp "oCC_LmpStart_H1"
Use the contactor feedback signal to (de)activate the lamp
```
```javascript
Network 4 : Stop lamp "oCC_LmpStop_H3"
Use the contactor feedback signal to (de)activate the lamp.
The lamp must flash with a Frequency of 1 Hz in cause of an emergency stop.
```

**Step 7 :** Download the software and test it
__Start-stop the motor__
1) Switch on the motor circuit breaker
2) Start the motor by pushing and release the green button
3) Motor is started, the green lamp is ON while the red lamp is OFF
4) Stop the motor by pushing and release the red button
5) Motor is stopped, the green lamp is OFF while the red lamp is ON

__Emergency stop__
1) Switch on the motor circuit breaker
2) The motor is stopped (if not stop the motor with the stop button)
2) Start the motor by pushing and release the green button
3) Push on the emergency stop
4) The motor is stopped
5) Deactivate the emergency stop buttons
6) Reset the safety relay with the black reset buttons
7) Restart the motor

<details>
	<summary>Click here to download the TIA Portal Exercise project solution</summary><!-- Empty line after this one needed, do not delete! -->

<br>
Download file <a href="./Ex06/Documents/ACTEA_Ex6.zap15_1">here</a>.</p>

  </details><!-- Empty line after this one needed, do not delete! -->
