
![ACTEA](../Logo_ACTEA_2.png)
_____________________________________
# Emergency stop circuits
## Overview
-   The [first goal](Ex06/Subchapter04_01.md) is to wire the electrical circuit for a direct online motor starter with safety relay logic.
-   The [second goal](Ex06/Subchapter04_02.md)  is to program and test PLC software for a direct online motor starter with safety relay logic.

# Scope
A three-phase asynchronous motor must be switched on and off using buttons. The power circuit is made with a contactor. The control function must be implemented with a PLC while also include the safety relay logic.

- The motor is turned on by pressing the green button %I 0.2 and is turned off by pressing the red button %I 0.0
- When the motor is running, the green lamp %Q 0.0 is ON and the red lamp %Q 0.2 is OFF.
- When the motor is stopped, the red lamp is ON and the green lamp is OFF.
- The safety relay is used when the switch is on NS1 position.
- When the safety condition is FALSE, then yellow lamp %Q 0.4 must be ON.
- In order to reset the safety loop, there must be connection between Y1 and Y2 and S1 button must be pressed.
- If the safety relay condition is ok, then the OUT led ,from the front of the safety relay, should lit and the motor can be started.
