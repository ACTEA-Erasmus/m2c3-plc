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
**Step 1 :** Create a new TIA Portal project
```javascript
Project name  : Task1-BasicProgramming
Author        : Your name
Comment       : Project railroad bridge
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

**Step 3 :** Add a signal board and configure it:
```javascript
Type                          : SB1231 1x12BIT - 6ES7 232-4HA30-0XB0
Analog output start address   : %QB80
Analog output signal          : Voltage
```

**Step 4 :** Add a digital input module and configure it:
```javascript
Type                          : SM1221 DI8x24VDC - 6ES7 221-1BF30-0XB0
Digital input start address   : %IB8
```

**Step 5 :** Add next *Functions* (FC) into PLC_1 in the FBD program language:
```javascript
FC_Sign1
FC_Sign2
```

**Step 6 :** Add both Functions into *Organization block* Main [OB1] in separated networks:
```javascript
FC_Sign1 into network 1
FC_Sign2 into network 2
```

**Step 7 :** **Download the hardware** configuration into the available CPU. When the device configuration was downloaded successfully; start the download of the software into the CPU. We do this to remove any existing software in the CPU.
