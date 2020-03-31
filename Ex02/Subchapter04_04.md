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
**Step 1 :** Go online (do *__not__* download the software) and check in the “*Project tree*” the map “*Program blocks*” on *online* and *offline* differences.

The next table shows the online diagnostic icons.

| **Icon** | **Description**                                                   |
|:---------:|-------------------------------------------------------------------|
| ![](../Ex02/Images/Icon_soft_error.jpg)| Software error, **can be showed in combination with other icons** |
| ![](../Ex02/Images/Icon_soft_diff.jpg) | There is a difference between the online and offline block        |
| ![](../Ex02/Images/Icon_soft_online.jpg) | Block only exist in the online version                            |
| ![](../Ex02/Images/Icon_soft_offline.jpg) | Block only exist in the offline version                           |
| ![](../Ex02/Images/Icon_soft_ok.jpg) | The offline and online blocks are equal                           |

There should be a difference between the *online* and *offline* version.

**Step 2 :** Solve the software difference by:

```javascript
- Call the Function "FC_Normal" in the Organization block "Main" [%OB1]
- Download the software to the device
```

**Step 3 :** Check the functionality of both warning lamps (orange lamps)

```javascript
- Use the “Monitoring on/off” function in the “Online view” of the “Program blocks”
- Change the state of the selector switch
- Both the orange lamps should be blinking if the selector switch has the state OFF
```
