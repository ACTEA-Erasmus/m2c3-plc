![](../Ex02/Images/Logo_Siemens_TIA_Portal.jpg)
_____________________________________
# Add a new PLC Device to a project
## Portal view
The project will be created after pushing the "Create" button and opened. The menu "Start", "First steps" will open automatically.

![First steps](../Ex02/Images/First_steps.jpg)

Push "Configure a device" in "Start" > "First steps" and switch to the "Add new device" menu.

![Add new device](../Ex02/Images/Add_new_device.jpg)

Select the S7-1200 CPU for your project and click on "Add".

![Select new device](../Ex02/Images/Select_new_device.jpg)

## Project view
Double click on "Add new device" and select the S7-1200 CPU for your project.

![Select CPU](../Ex02/Images/TIA_select_CPU.jpg)

Configure the device by double-click on “Device configuration” and selecting the CPU in the Device view. The properties can be configured in the Properties view.

![Open Device configuration](../Ex02/Images/TIA_Open_Device_configuration.jpg)

# Add modules to a PLC Device
A PLC Device can be expanded with additional modules such as:
* Digital input modules to process digital sensors
* Digital output modules to control digital actuators
* Analog input modules to process analog sensors
* Analog output modules to control analog actuators
* Industrial network modules to process communication through Profibus, ProfiNET, etc.
* Other modules such as ..

![Add modules](../Ex02/Images/Add_modules.jpg)

The Siemens S7-1200 CPU is foreseen with an extra location for modules in the middle of the CPU. Additional modules for this location are called boards.

Modules and boards can be added to a PLC device by opening the "Device configuration" and to drag a module from the catalog to the CPU.
Allowed locations in the PLC rack are showed with a blue rectangle.

![Add modules](../Ex02/Images/TIA_Add_modules.jpg)

Each module and device can be configured in the "Properties" window of the "Device configuration" by selecting the item. Also some internal parts of a device can be configured this way.

For example: The ProfiNET/Ethernet port can be configured in the "Properties" window after selecting it.

![Ethernet port configuration](../Ex02/Images/Config_ethernet_port.jpg)

Remark: Create a subnet if the CPU is not networked.

![](../Ex02/Images/Not_networked.jpg)

# Download hardware
Each change in the "Device configuration" must be transferred to the CPU. This is done by downloading the hardware. Compile your project before a download to check on faults.

A hardware download can be started from the toolbar

![Hardware download](../Ex02/Images/TIA_HW_download.jpg)
