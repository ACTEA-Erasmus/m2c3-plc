![](../Ad03/Images/Logo_Siemens_TIA_Portal.jpg)
_____________________________________
# Hardware
Double click in the **Project view** on "Add new device" and select the S7-1200 CPU if you want to add a PLC to your project.

![Select CPU](../Ad03/Images/TIA_select_CPU.jpg)

Double-click on “Device configuration” in the device tree to add and configure device modules.

![Open Device configuration](../Ad03/Images/TIA_Open_Device_configuration.jpg)

The TIA Portal project view contains different items. They can be switched on or off in the "View" menu.
1. Menu bar
2. Toolbar
3. Project tree
4. Editor area
5. Inspector window
6. Task card

![](../Ad03/Images/TIA_overview.jpg)

The editor area contains the opened editors. The organization of these windows can be controlled by the "Window" menu in the menu bar.
The contents of the inspector window and task card depends on the selected item(s) in the Editor window.

# Add modules to a PLC Device
A PLC device can be expanded with additional modules such as:
* Digital input modules to process digital sensors
* Digital output modules to control digital actuators
* Analog input modules to process analog sensors
* Analog output modules to control analog actuators
* Industrial network modules to process communication through Profibus, ProfiNET, etc.
* Other modules ...

![Add modules](../Ad03/Images/Add_modules.jpg)

It is necessary to add the PLC device modules in the "Device configuration" so it match with the real situation. Also the configuration of the addresses can be done in the "Device configuration". It requires to open the "Device overview".

![](../Ad03/Images/Device_configuration.jpg)

**Remark:** To show and hide the Device overview, you must click the small arrow next to "Device data" on the right side of the hardware configuration.

![](../Ad03/Images/Show_device_data.jpg)

Modules and boards can be added to a PLC device by drag a module from the catalog and to drop it into the CPU. Allowed drop locations are showed with a blue rectangle.

![Add modules](../Ad03/Images/TIA_Add_modules.jpg)

**Remark:** The Siemens S7-1200 CPU is foreseen with an extra location for modules in the middle of the CPU. Additional modules for this location are called boards.

# Configure modules
Each module and device can be configured in the "Properties" window of the "Device configuration" by selecting the item. Also some internal parts of a device can be configured this way.

For example: The ProfiNET/Ethernet port can be configured in the "Properties" window after selecting it.

![Ethernet port configuration](../Ad03/Images/Config_ethernet_port.jpg)

**Remark**: Create a subnet if the CPU is not networked.

![](../Ad03/Images/Not_networked.jpg)

# Download hardware
Each change in the "Device configuration" must be transferred to the CPU. This is done by downloading the hardware. Compile your project before a download to check on faults.

A hardware download can be started from the toolbar.

![Hardware download](../Ad03/Images/TIA_HW_download.jpg)
