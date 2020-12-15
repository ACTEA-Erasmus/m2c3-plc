![Factory IO](../Ex03/Images/logo_fio.png)
_____________________________________
# The Pusher Game
## Overview
-   The [first goal](../Ex03/Subchapter04_01.md) is to recognize the working principles
-   The [second goal](../Ex03/Subchapter04_02.md) is to define the Factory IO & PLC Tags
-   The [third goal](../Ex03/Subchapter04_03.md) is to create and to download the PLC hardware
-   The [fourth goal](../Ex03/Subchapter04_04.md) is to create and to download the PLC software, according IEC 61131-3
-   The [last goal](../Ex03/Subchapter04_05.md) is to is to deliver a working project

Back to the [project scope](../Ex03/Subchapter04.md).

## Goal 3 : Configure the hardware
**Step 1 :** Create a new TIA Portal project
```javascript
Project name  : Ex3-PusherGame
Author        : Your name
Comment       : Project The Pusher Game
```

**Step 2 :** Add a PLC-device with next CPU settings
```javascript
Type                          : See available CPU
System byte                   : %MB254
Clock memory byte             : %MB255
Digital input start address   : %IB0 (DO NOT USE %IB10!)
Output start address          : %QB0
Analog input start address    : %IB64
Analog output start address   : %QB80
IP-address                    : 192.168.0.30
IP-address subnet mask        : 255.255.255.0
```

**Step 3 :** Add next *Functions* (FC) into PLC_1 in the LAD program language:
```javascript
FC_CC
FC_CamController
FC_Pusher1
FC_Pusher2
FC_Pusher3
FC_Pusher4
```

**Step 4 :** Add the Functions into *Organization block* Main [OB1] in separated networks:
```javascript
FC_CC into network 1
FC_CamController into network 2
FC_Pusher1 into network 3
FC_Pusher2 into network 4
FC_Pusher3 into network 5
FC_Pusher4 into network 6
```

**Step 5 :** **Download the hardware** configuration into the available CPU. When the device configuration was downloaded successfully; start the download of the software into the CPU. We do this to remove any existing software in the CPU.
