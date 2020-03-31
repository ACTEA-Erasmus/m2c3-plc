<img src="/Ex02/Images/Logo_Siemens_TIA_Portal.jpg" style="position:absolute;top:0px;right:0px;" />

# Introduction into Siemens TIA Portal
_____________________________________
## About Siemens TIA Portal
With SIMATIC TIA Portal users configure, program, test and diagnose the basic, advanced, distributed controllers and HMI panels, whether it is PLC- or PC-based, incl. software controllers.
SIMATIC TIA Portal can be expand with supplements for configure, test and diagnose applications such as drives, network applications, ... .

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
Start TIA Portal by double-clicking the icon.

TIA Portal can be started in 2 views where it is possible to switch between views:
* Portal view : Run through a wizard to add a device (**Default view**)
* Project view : To program and add devices (**Preferred view**)


## Create a new Project

![New TIA Project](../Ex02/Images/TIA_new_project.jpg)

## PLC Hardware
### Add a new PLC Device
![Select CPU](../Ex02/Images/TIA_select_CPU.jpg)

Configure the device by double-click on “Device configuration” and selecting the CPU in the Device view. The properties can be configured in the Properties view.

![Open Device configuration](../Ex02/Images/TIA_Open_Device_configuration.jpg)

### Add modules to a Device
Add the signal board and the signal module with drag-and-drop from the hardware catalog to the device. Allowed locations in the rack are showed with a blue rectangle.

![Add modules](../Ex02/Images/TIA_Add_modules.jpg)

### Download hardware

![Hardware download](../Ex02/Images/TIA_HW_download.jpg)

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

<details>
  <summary>Click to expand!</summary>

  tested

</details>

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
