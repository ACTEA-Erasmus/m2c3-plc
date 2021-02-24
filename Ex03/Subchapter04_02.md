![Factory IO](../Ex03/Images/logo_fio.png)
_____________________________________
# The Pusher Game
## Overview
-   The [first goal](Ex03/Subchapter04_01.md) is to recognize the working principles
-   The [second goal](Ex03/Subchapter04_02.md) is to define the Factory IO & PLC Tags
-   The [third goal](Ex03/Subchapter04_03.md) is to create and to download the PLC hardware
-   The [fourth goal](Ex03/Subchapter04_04.md) is to create and to download the PLC software, according IEC 61131-3
-   The [last goal](Ex03/Subchapter04_05.md) is to is to deliver a working project

Back to the [project scope](Ex03/Subchapter04.md).

## Goal 2 : Define Tags
**Step 1 :** Select in the Factory IO scene the correct I/O driver.
```javascript
TIP : Look at the PLC Type on the PLC Board
TIP : You have to stop the Factory IO RUN mode
```

**Step 2 :** Configure the I/O driver.
```javascript
Host address                    : 192.168.0.30
Network adapter                 : Your local LAN card
Numerical Data Type             : DWORD
Bool Inputs offset              : 10
Bool Inputs count               : 16
Bool Outputs offset             : 0
Bool Outputs count              : 16
DWORD Inputs offset             : 100
DWORD Inputs count              : 8
DWORD Outputs offset            : 100
DWORD Outputs count             : 8
```

**Step 3 :** Start mapping the actuators and sensors.
```javascript
TIP : Drag and drop the sensors and actuators to the host.
TIP : Do not forget to map the "Factory I/O (reset)" input
```

**Step 4 :** Export the tags to a XML file with the export button (at the bottom right with an up arrow). The file is saved to **This pc > My Documents > Factory IO**

![Factory IO](../Ex03/Images/export_tags.jpg)

**Step 4 :** Save the Factory IO scene.
