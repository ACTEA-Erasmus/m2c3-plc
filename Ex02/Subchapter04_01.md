# The railroad bridge project
_____________________________________
## Overview
-   The [first goal](Ex02/Subchapter04_01.md) is to configure and to download the hardware of a PLC device
-   The [second goal](Ex02/Subchapter04_02.md) is to debug hardware errors
-   The [third goal](Ex02/Subchapter04_03.md) is to create and to download basic software, according IEC 61131-3
-   The [fourth goal](Ex02/Subchapter04_04.md) is to debug software errors and programming faults
-   The [last goal](Ex02/Subchapter04_05.md) is to deliver a working project

Back to the [project scope](Ex02/Subchapter04.md).

## Goal 1 : Configure the hardware
### Create a new TIA Portal project
>Project name : Task1-BasicProgramming
Author : *Your name*
Comment : Project railroad bridge

### Add a PLC-device
CPU settings:
>*Type* : See available CPU
*System byte* : %MB254
*Clock memory byte* : %MB255
*Digital input start address* : %IB0
*Output start address* : %QB0
*Analog input start address* : %IB64
*IP-address* : 192.168.0.30
*IP-address subnet mask* : 255.255.255.0

Signal board settings:
>*Type* : SB1231 1x12BIT - 6ES7 232-4HA30-0XB0
*Analog output start address* : %QB80
*Analog output signal* : Voltage

Digital input settings:
>*Type* : SM1221 DI8x24VDC - 6ES7 221-1BF30-0XB0
*Digital input start address* : %IB8

### Add software blocks
Add next *Functions* (FC) into PLC_1 in the FBD program language:
>-   FC_Sign1
>-   FC_Sign2

Add both Functions into *Organization block* Main [OB1] in separated networks:
>-   Open *Organization block* Main [OB1] by double-click
>-   Drag-and-drop *Function* FC_Sign1 into network 1
>-   Drag-and-drop *Function* FC_Sign2 into network 2

**Download the hardware** configuration into the available CPU. When the device configuration was downloaded successfully; start the download of the software into the CPU. We do this to remove any existing software in the CPU.