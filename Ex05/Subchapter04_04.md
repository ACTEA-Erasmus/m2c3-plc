# Basic motor software circuits
_____________________________________
-   The [first goal](../Ex05/Subchapter04_01.md) is to wire the electrical circuit for a direct online motor starter
-   The [second goal](../Ex05/Subchapter04_02.md)  is to program and test PLC software for a direct online motor starter
- The [third goal](../Ex05/Subchapter04_03.md) is to wire the electrical circuit for a direct reverse online motor starter
-   The [Last goal](../Ex05/Subchapter04_04.md)  is to program and test PLC software for a direct reverse online motor starter

Back to the [project scope](../Ex05/Subchapter04.md).

## Goal 4 : Program and test PLC software for a direct reverse online motor starter
**Step 1 :** Add next *Functions* (FC) into PLC_1 in the FBD program language:
```javascript
FC_DOR
```

**Step 2 :** Add the Function into *Organization block* Main [OB1]:
```javascript
FC_DOR into network 2
```

**Step 3 :** Disable the Function of the DOL motor into *Organization block* Main [OB1]:
```javascript
FC_DOL into network 1 -> Add system bit "AlwaysFALSE" to the EN-input of FC_DOL
```

**Step 4 :** Update PLC Tags:
```javascript
iCC_BtnStop_S1 - BOOL - %I 0.0 - Stop button
iCC_BtnStartFw_S3 - BOOL - %I 0.2 - Start button forward
iCC_BtnStartBw_S4 - BOOL - %I 0.2 - Start button Backward
iCC_McbMot_QM1 - BOOL - %I 1.1 - Motor circuit breaker
iCC_ConMotFw_KM1 - BOOL - %I 1.2 - Feedback signal contactor forward
iCC_ConMotBw_KM2 - BOOL - %I 1.4 - Feedback signal contactor backward
oCC_LmpStartFw_H1 - BOOL - %Q 0.0 - Lamp start forward
oCC_LmpStartBw_H2 - BOOL - %Q 0.1 - Lamp start backward
oCC_LmpStop_H3 - BOOL - %Q 0.2 - Lamp stop
oCC_ConMotFw_KM1 - BOOL - %Q 0.6 - Contactor motor forward
oCC_ConMotBw_KM2 - BOOL - %Q 0.6 - Contactor motor backward
mMotStartedFw - BOOL - %M 0.0 - Motor started forward
mMotStartedBw - BOOL - %M 0.0 - Motor started backward
```

**Step 5 :** Program in FC_DOR the software to start & stop the motor. Do not forget to program the lamps.
```javascript
Network 1 : Start-stop circuit forward "mMotStartedFw"
Start circuit = Start button forward AND NOT backward started
Stop circuit = Stop button AND Motor circuit breaker
```

```javascript
Network 2 : Start-stop circuit backward "mMotStartedFw"
Start circuit = Start button backward AND NOT forward started
Stop circuit = Stop button AND Motor circuit breaker
```

```javascript
Network 3 : activate motor "oCC_ConMotFw_KM1 " and "oCC_LmpStartFw_H1"
```

```javascript
Network 4 : activate motor "oCC_ConMotBw_KM2 "  and "oCC_LmpStartBw_H2"
```

**Step 6 :** Download the software and test it
__Start-stop the motor forward__
1) Switch on the motor circuit breaker
2) Start the motor forwards by pushing and release the green forward button
3) Motor is started, the green lamp forward is ON while the red lamp is OFF
4) Stop the motor by pushing and release the red button
5) Motor is stopped, the green lamp is OFF while the red lamp is ON

__Start-stop the motor backward__
1) Switch on the motor circuit breaker
2) Start the motor backwards by pushing and release the green backward button
3) Motor is started, the green lamp backward is ON while the red lamp is OFF
4) Stop the motor by pushing and release the red button
5) Motor is stopped, the green lamp is OFF while the red lamp is ON

__Changing the motor direction__
1) Switch on the motor circuit breaker
2) Start the motor forwards by pushing and release the green forward button
3) Motor is started, the green lamp forward is ON while the red lamp is OFF
4) Press the green backward buttons
5) It is not allowed that the motor stops or change direction. You first have to press the stop button

__The stop priority__
1) Switch on the motor circuit breaker
2) The motor is stopped (if not stop the motor with the stop button)
2) Push simultanious on a start and stop button
3) Motor may not start! Stop has priority over start!

__Motor circuit breaker__
1) Switch on the motor circuit breaker
2) The motor is stopped (if not stop the motor with the stop button)
2) Start the motor
3) Deactivate the motor circuit breaker
4) Motor is stopped
5) Switch on the motor circuit breaker. It is not allowed that the motor restart (you must push on start)
6) Start the motor
