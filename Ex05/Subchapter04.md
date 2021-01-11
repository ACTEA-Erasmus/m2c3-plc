# Basic motor software circuits
_____________________________________
## Overview
-   The [first goal](../Ex05/Subchapter04_01.md) is to wire the electrical circuit for a direct online motor starter
-   The [second goal](../Ex05/Subchapter04_02.md)  is to program and test PLC software for a direct online motor starter
- The [third goal](../Ex05/Subchapter04_03.md) is to wire the electrical circuit for a direct reverse online motor starter
-   The [Last goal](../Ex05/Subchapter04_04.md)  is to program and test PLC software for a direct reverse online motor starter

## Scope : DOL - Direct online motor starter
A three-phase asynchronous motor must be switched on and off using a pushbutton. The power circuit is made with a contactor. The control function must be implemented with a PLC.

- The motor is turned on by pressing the green button %I 0.2 and is turned off by pressing the red button %I 0.0
- When the motor is running, the green lamp %Q 0.0 is ON and the red lamp %Q 0.2 is OFF.
- When the motor is stopped, the red lamp is ON and the green lamp is OFF.
- The feedback of the circuit breaker and power contactor should be used for the programming logic.

## Scope : ROL - Direct reverse online motor starter
A three-phase asynchronous motor must be switched on and off using buttons. The power circuit is made with contactors. The motor can rotate in both directions. The control function must be implemented with a PLC.

- The direction of rotation is selected by using one of the green buttons %I 0.2 or %I 0.3.
- For safety reasons, the control circuits of the two contactors must lock each other using auxiliary contacts.
- The direction of rotation cannot be changed during operation: to change the direction of rotation, the motor must first be stopped.
- The direction of rotation is shown by the green lamps %Q 0.0 and %Q 0.1.
- When the motor is stopped the red lamp %Q 0.2 is lit.
- The motor is stopped by pressing the red button %I 0.0.
- The feedback of the circuit breaker and power contactor should be used for the programming logic.
