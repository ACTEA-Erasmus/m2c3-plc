# Introduction into Siemens TIA Portal
_____________________________________
## First steps


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

![Hardware download](../Ex02/Images/TIA_HW_Download.jpg)

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
![Add function](../Ex02/Images/TIA_Add_FC.jpg)

### Function Blocks [FB]

### Data Blocks [FB]

## PLC TAGs
BOOL, BYTE, WORD, DWORD & LWORD

## Download software

![Sofware download](../Ex02/Images/TIA_SW_Download.jpg)

## Debugging
### Hardware
| **Icon** | **Description**   |
|:--------:|:------------------|
| ![](../Ex02/Images/Icon_no_error.jpg) | No error          |
| ![](../Ex02/Images/Icon_Maintenance_needed.jpg)| Maintenance needed |
| ![](../Ex02/Images/Icon_Maintenance_necessary.jpg) | Maintenance necessary |
| ![](../Ex02/Images/Icon_error.jpg) | Error, maintenance necessary |
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
It is possible to create a backup of your project by archiving it. An **archive** is a TIA Portal ZIP file a can only be opened by retrieving the file.

| **File type** | **Description**                                                    |
|---------------|--------------------------------------------------------------------|
| .ZAP15_1      | TIA Portal ZIP archive of a V15.1 project                          |
| .ZAL15_1      | TIA Portal ZIP archive of a V15.1 library                          |
| .AP15_1       | TIA Portal project V15.1 <sup>(1)</sup> |
| .AL15_1       | TIA Portal library V15.1 <sup>(1)</sup> |

<sup>(1)</sup> *!! Cannot be used as standalone file !!*
