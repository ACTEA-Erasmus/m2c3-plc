![](../Ad03/Images/Logo_Siemens_TIA_Portal.jpg)
_____________________________________
# Hardware
Double click in the **Project view** on "Add new device" and select the S7-1200 CPU if you want to add a PLC to your project.

![Select CPU](../Ad03/Images/TIA_select_CPU.jpg)

Configure the device by double-click on “Device configuration” and selecting the CPU in the Device view.

![Open Device configuration](../Ad03/Images/TIA_Open_Device_configuration.jpg)

# Add modules to a PLC Device
A PLC Device can be expanded with additional modules such as:
* Digital input modules to process digital sensors
* Digital output modules to control digital actuators
* Analog input modules to process analog sensors
* Analog output modules to control analog actuators
* Industrial network modules to process communication through Profibus, ProfiNET, etc.
* Other modules such as ..

![Add modules](../Ad03/Images/Add_modules.jpg)

The Siemens S7-1200 CPU is foreseen with an extra location for modules in the middle of the CPU. Additional modules for this location are called boards.

Modules and boards can be added to a PLC device by opening the "Device configuration" and to drag a module from the catalog to the CPU.
Allowed locations in the PLC rack are showed with a blue rectangle.

![Add modules](../Ad03/Images/TIA_Add_modules.jpg)

Each module and device can be configured in the "Properties" window of the "Device configuration" by selecting the item. Also some internal parts of a device can be configured this way.

For example: The ProfiNET/Ethernet port can be configured in the "Properties" window after selecting it.

![Ethernet port configuration](../Ad03/Images/Config_ethernet_port.jpg)

**Remark**: Create a subnet if the CPU is not networked.

![](../Ad03/Images/Not_networked.jpg)

# Download hardware
Each change in the "Device configuration" must be transferred to the CPU. This is done by downloading the hardware. Compile your project before a download to check on faults.

A hardware download can be started from the toolbar

![Hardware download](../Ad03/Images/TIA_HW_download.jpg)
