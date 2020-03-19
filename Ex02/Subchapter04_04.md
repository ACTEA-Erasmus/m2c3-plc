# The railroad bridge project
_____________________________________
## Overview
-   The [first goal](Ex02/Subchapter04_01.md) is to configure and to download the hardware of a PLC device
-   The [second goal](Ex02/Subchapter04_02.md) is to debug hardware errors
-   The [third goal](Ex02/Subchapter04_03.md) is to create and to download basic software, according IEC 61131-3
-   The [fourth goal](Ex02/Subchapter04_04.md) is to debug software errors and programming faults
-   The [last goal](Ex02/Subchapter04_05.md) is to deliver a working project

Back to the [project scope](Ex02/Subchapter04.md).

## Goal 4 : Debug software
Go online (do *not* download the software) and check in the “*Project tree*” the
map “*Program blocks*” on *online* and *offline* differences

The next table shows the online diagnostic icons. Mark those icons which are
visible in your “*Online view*”.

| **Icon** | **Description**                                                   | **Present (Y/N)** |
|----------|-------------------------------------------------------------------|-------------------|
|          | Software error, **can be showed in combination with other icons** |                   |
|          | There is a difference between the online and offline block        |                   |
|          | Block only exist in the online version                            |                   |
|          | Block only exist in the offline version                           |                   |
|          | The offline and online blocks are equal                           |                   |


There should be a difference between the *online* and o*ffline* version.

Call the *Function* FC_Normal in the *Organization block* Main [%OB1] and
download the software to the device. Check the functionality of both warning
lamps (orange lamps).
-   Use the “*Monitoring on/off*” function in the “*Online view*” of the
    “*Program blocks*”
-   Change the state of the selector switch
-   Both the orange lamps should be blinking if the selector switch has the
    state OFF