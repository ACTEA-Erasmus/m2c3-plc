# The railroad bridge project
_____________________________________
## Overview
-   The [first goal](Ex02/Subchapter04_01.md) is to configure and to download the hardware of a PLC device
-   The [second goal](Ex02/Subchapter04_02.md) is to debug hardware errors
-   The [third goal](Ex02/Subchapter04_03.md) is to create and to download PLC software, according IEC 61131-3
-   The [fourth goal](Ex02/Subchapter04_04.md) is to debug software errors and programming faults
-   The [last goal](Ex02/Subchapter04_05.md) is to deliver a working project

## Scope
Create a solution for a railroad bridge with traffic lights which control the traffic under the bridge. The lane under the bridge is reduced to 1 lane.

![Railroad bridge](Ex02/Images/Railroad_with_signs.jpg)

The traffic lights are equipped with a selector switch for 2 operation modes:
-   ON : Normal operation : Traffic is controlled by the traffic lights
-   OFF : Emergency operation : Flashing orange lights, other lights are off

An output has to be activated in case of an software program error where the
functionality of the lamps “freezes” in normal operation (=Lamps do not change any more during 30 s or more). This output is connected with the management system of the road manager.
