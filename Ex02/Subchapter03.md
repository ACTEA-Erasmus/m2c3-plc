![](../Ex02/Images/Logo_Siemens_TIA_Portal.jpg)
_____________________________________
## Siemens TIA Portal
With SIMATIC TIA Portal users configure, program, test and diagnose basic, advanced, distributed controllers and HMI panels, whether it is PLC- or PC-based, incl. software controllers. SIMATIC TIA Portal can be expand with supplements for configure, test and diagnose applications such as drives, network applications, ... .

![Hardware overview TIA Portal](../Ex02/Images/TIA_HW_Overview.jpg)

SIMATIC TIA Portal is one of the core products of the TIA Portal engineering framework seamlessly integrated into one platform by using shared services as well as data.

## Siemens TIA Portal licensing
| **TIA Portal Basic** | **TIA Portal Professional** | **TIA Portal Options** |
|:--------------------:|:---------------------------:|:----------------------:|
| ![](../Ex02/Images/TIA_Basic.jpg) | ![](../Ex02/Images/TIA_Professional.jpg) | ![](../Ex02/Images/TIA_Options.jpg) |
| The subset of TIA Portal controller software for the basic controller S7-1200 | The comprehensive software solution for programming the controllers S7-1200, S7-1500, S7-300 and S7-400 with a fixed number of integrated functions | Functional supplements to the standard controller software, e.g. for failsafe applications or technological tasks |
| **Basic license** | **Professional license** | **Optional licenses**  |

Educational institutes benefit from special conditions such as **educational licenses** which are Professional licenses limited in time (356-days).

![Educational license](../Ex02/Images/Edu_license.jpg)

## TIA Portal versions
The TIA Portal platform is constantly evolving, resulting in different versions over the years. Upward compatibility from older versions is only possible according to the schedule below.

![TIA versions](../Ex02/Images/TIA_Versions.jpg)

Downward compatibility is not supported.

## TIA Portal icons
TIA Portal can be started by double-clicking the TIA Portal icon. A new set of icons come with the installation of TIA Portal.

| **Icon** | **Description**   |
|:--------:|:------------------|
| ![Icon_TIA_V15_1](../Ex02/Images/Icon_TIA_V15_1.jpg)  | To start TIA Portal V15.1 |
| ![Icon_TIA_Updater](../Ex02/Images/Icon_TIA_Updater.jpg)  | To start the TIA Portal updater for installing updates |
| ![Icon_TIA_Lic_manager](../Ex02/Images/Icon_TIA_Lic_manager.jpg)  | To open the license manager |
| ![Icon_TIA_Simulator](../Ex02/Images/Icon_TIA_Simulator.jpg) | To start the PLC simulator for S7-1200 & S7-1500 CPU’s |
| ![Icon_TIA_Project](../Ex02/Images/Icon_TIA_Project.jpg) | A TIA Portal file |
| ![Icon_TIA_Communications](../Ex02/Images/Icon_TIA_Communications.jpg) | To open the PC communication settings necessary for HMI simulation with a CPU where administration rights are necessary<sup>1</sup> |

<sup> 1 Can be started from: "C:\Program Files\Common Files\Siemens\CommunicationSettings\CommunicationSettings.exe" </sup>

## Start TIA Portal
TIA Portal can be started, by double-clicking its icon, in 2 views:
- Portal view : Run through a wizard to add a device (**Default view**)
- Project view : To program and add devices (**Preferred view**)

The portal view provides a task-oriented view of the tools for working on the
project. Here, you can quickly decide what you want to do and open the tool for the task at hand. If necessary, a change to the project view takes place
automatically for the selected task.

![Portal view](../Ex02/Images/TIA_Portal_View.jpg "Portal View")

The project view is used for hardware configuration, programming, creation of the visualization and many other tasks.

By default, the project view displays the menu bar with the toolbars at the top, the project tree with all components of a project on the left and the so-called task cards with instructions and libraries, for example, on the right.

If an element (for example, the device configuration) is selected in the project tree, it is displayed in the center and can be worked on there.

![Project view](../Ex02/Images/TIA_Project_View.jpg "Project View")

It is possible to switch between the 2 views by means of clicking the text "Project view" or "Portal view" at the bottom left.

## Create a new Project in TIA Portal
A new project can be created in Portal or Project view.

Portal view  |  Project view
:--:|:--:
"Create new Project"  |  "Project" > "New..."
![Create new TIA Project](../Ex02/Images/Create_new_project.jpg) | ![New TIA Project](../Ex02/Images/TIA_new_project.jpg)

## Add a new PLC Device to a project
### Portal view
The project will be created after pushing the "Create" button and opened. The menu "Start", "First steps" will open automatically.

![First steps](../Ex02/Images/First_steps.jpg)

Push "Configure a device" in "Start" > "First steps" and switch to the "Add new device" menu.

![Add new device](../Ex02/Images/Add_new_device.jpg)

Select the S7-1200 CPU for your project and click on "Add".

![Select new device](../Ex02/Images/Select_new_device.jpg)

### Project view
Double click on "Add new device" and select the S7-1200 CPU for your project.

![Select CPU](../Ex02/Images/TIA_select_CPU.jpg)

Configure the device by double-click on “Device configuration” and selecting the CPU in the Device view. The properties can be configured in the Properties view.

![Open Device configuration](../Ex02/Images/TIA_Open_Device_configuration.jpg)

## Add modules to a PLC Device
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

### Download hardware
Each change in the "Device configuration" must be transferred to the CPU. This is done by downloading the hardware.

Before you download the configuration, you should save your project by clicking the ![](../Ex02/Images/Save_project.jpg) button. The next step is to compile your CPU with the device configuration, first select the "CPU_1215C [CPU1215C DC/DC/DC]" folder and click the ![](../Ex02/Images/Compile_icon.jpg) "Compile" icon.

> **Note:**
> "Save project" should be used repeatedly when working on a project since this does not happen automatically. A prompt to save the project only occurs when the TIA Portal is closed.

If the project was compiled without errors, you see the following screen.

![](../Ex02/Images/No_errors.jpg)

To download your entire CPU, select the → "CPU_1215C [CPU1215C DC/DC/DC]" folder and click the ![](../Ex02/Images/Download_icon.jpg) "Download to device" button.

![](../Ex02/Images/Download_all.jpg)

The manager for configuring the connection properties (extended download) opens.

![](../Ex02/Images/Extended_download.jpg)

First, the interface must be correctly selected. This happens in three steps.
> **Step 1**: Type of the PG/PC interface → PN/IE
> ![](../Ex02/Images/Download_step1.jpg) <br>
> **Step 2**: PG/PC interface  → Select your network card
> ![](../Ex02/Images/Download_step2.jpg) <br>
> **Step 3**: Connection to interface/subnet → "PN/IE_1"
> ![](../Ex02/Images/Download_step3.jpg) <br>


## PLC software
Software code can be programmed into 'Program blocks' in 5 programming languages:
* Function Block Diagram (FBD)
* Ladder (LAD)
* Sequential Function Chart (SFC)
* Structured Text (ST)
* Structured Control language (SCL)

FBD, LAD and SFC are graphical based programming languages. This means that instructions are figures which can be connected. Each

### Organization blocks [OB]

### Functions [FC]
![Add function](../Ex02/Images/TIA_add_FC.jpg)

### Function Blocks [FB]

### Data Blocks [FB]

## PLC TAGs
BOOL, BYTE, WORD, DWORD & LWORD

## Download software

![Sofware download](../Ex02/Images/TIA_SW_download.jpg)

## Debugging
### Hardware
| **Icon** | **Description**   |
|:--------:|:------------------|
| ![](../Ex02/Images/Icon_No_error.jpg) | No error          |
| ![](../Ex02/Images/Icon_Maintenance_needed.jpg)| Maintenance needed |
| ![](../Ex02/Images/Icon_Maintenance_necessary.jpg) | Maintenance necessary |
| ![](../Ex02/Images/Icon_Error.jpg) | Error, maintenance necessary |
| ![](../Ex02/Images/Icon_device_deactivated.jpg) | The device or module is deactivated |
| ![](../Ex02/Images/Icon_device_not_reached.jpg) | The device or module cannot be reached |
| ![](../Ex02/Images/Icon_device_no_iodata.jpg) | No input and/or output data available |
| ![](../Ex02/Images/Icon_device_no_diagdata.jpg) | There is no diagnostic data available because the online and offline configurations are different |
| ![](../Ex02/Images/Icon_device_not_compatible.jpg) | The device or module is available but is not compatible |
| ![](../Ex02/Images/Icon_device_state_unkown.jpg) | There is a connection with the device or module but state is unknown |
| ![](../Ex02/Images/Icon_device_diag_notallowed.jpg) | There is a connection with the device or module but diagnostic is not allowed |
| ![](../Ex02/Images/Icon_device_hardware_fault.jpg) | Hardware fault, **can be showed in combination with other icons** |

## Software
| **Icon** | **Description**                                                   |
|:---------:|-------------------------------------------------------------------|
| ![](../Ex02/Images/Icon_soft_error.jpg)| Software error, **can be showed in combination with other icons** |
| ![](../Ex02/Images/Icon_soft_diff.jpg) | There is a difference between the online and offline block        |
| ![](../Ex02/Images/Icon_soft_online.jpg) | Block only exist in the online version                            |
| ![](../Ex02/Images/Icon_soft_offline.jpg) | Block only exist in the offline version                           |
| ![](../Ex02/Images/Icon_soft_ok.jpg) | The offline and online blocks are equal                           |

## Backup
It is possible to create a backup of your project by archiving it.
An **archive** is a TIA Portal ZIP file a can only be opened by retrieving the file.

| **File type** | **Description**                                                    |
|---------------|--------------------------------------------------------------------|
| .ZAP15_1      | TIA Portal ZIP archive of a V15.1 project                          |
| .ZAL15_1      | TIA Portal ZIP archive of a V15.1 library                          |
| .AP15_1       | TIA Portal project V15.1 <sup>(1)</sup> |
| .AL15_1       | TIA Portal library V15.1 <sup>(1)</sup> |

<sup>1</sup> *!! Cannot be used as standalone file !!*
