# TAG naming convention
_____________________________________
## General
The use of a naming convention is used to increase the readability of the software. TAG and block names are constructed with capital and small letters where
* The name is assembled with one or more words
* Each word starts with a capital letter
* Words can be reduced by the use of abbreviations

## Programming blocks
### Structure
The name of a programming block is constructed with the use of ANSI/ISA S88 standard, as showed in the next table.

| Block type | _     | S88 Type  | _    | Block description  |
| :---:      | :---: |:---:      |:---: | :---               |

It starts with the block type abbreviation, followed by an underscore and it finish with an S88 abbreviation and block description.

The S88 type abbreviation is not used with global data blocks (DBs).

### Block type abbreviation
| Block type | Description |
| :---: | :--- |
| FC | Function |
| FB | Function block |
| OB | Program organization unit |
| DB | Global data block |
| ID | Instance data block  |

### S88 abbreviation
| S88 abbreviation | Description |
| :---: | :--- |
| CM | Control module |
| EM | Equipment module |
| PE | Procedure element |

Notes on ANSI/ISA S88
* A control module is a function block (FB) which processed signals from inputs or controls output signals.
* An equipment is a function (FC) which represent a collection of physical elements that have an physical relationship.
* A procedure element is function block (FB) that represents a strategy (GRAFCET, flowchart, PID controller, etc.).

### Examples
| Block type | _     | S88 Type  | _    | Block description  |
| :---:      | :---: | :---:     |:---: | :---               |
| DB         | _     |           |      | Alarms             |
| DB         | _     |           |      | HMI1               |
| FB         | _     | CM        | _    | AI                 |
| FB         | _     | CM        | _    | DI                 |
| FB         | _     | CM        | _    | Lamp               |
| FB         | _     | CM        | _    | DOL                |
| FB         | _     | CM        | _    | DOLRev             |
| FC         | _     | EM        | _    | CC                 |
| FB         | _     | PE        | _    | StartStop          |
| FB         | _     | PE        | _    | CRNLoad            |

| Example         | Description |
| :---            | :--- |
| DB_Alarms       | Alarms & events data block |
| DB_HMI1         | Interface data block HMI1 |
| FB_CM_AI        | Control module of a analog input |
| FB_CM_DI        | Control module of a digital input |
| FB_CM_Lamp      | Control module of a digital lamp |
| FB_CM_DOL       | Control module of a direct online motor with 1 speed and 1 rotating direction |
| FB_CM_DOLRev    | Control module of a direct online motor with 1 speed and 2 rotating directions |
| FB_PE_StartStop | Procedure element start-stop |
| FB_PE_CRNLoad   | Procedure element to load a crane |
| FC_EM_CC        | Equipment module of the control cabinet |

## PLC TAGs
### Structure
The name of a PLC TAG is constructed as showed in the next table.
| Prefix | Physical name | _ | Type name | Function | _ | Suffix |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: |

### Prefix
The prefix gives the function of the absolute address.

| Prefix | Description |
| :---: | :--- |
| i | Input |
| o | Output |
| m | Memory flag |

### Physical names
The physical name is an abbreviation that refers to the name of that part of the installation that combines multiple physical parts.
The use of an unique number after the abbreviation is allowed.

| Prefix  | Description |
| :---:    | :--- |
| BLT     | Belt conveyor |
| BOX     | Electrical distribution box |
| CC      | Control cabinet |
| CHN     | Chain conveyor |
| CRN     | Crane |
| CW      | City water  |
| DR      | Door |
| DRN     | Drain |
| FRK     | Forks |
| GRP     | Gripper |
| GATE    | Gate |
| LFT     | Lift |
| OP      | Operator panel |
| PnP     | Pick & Place robot |
| PRT     | Port |
| PSH     | Pusher |
| ROL     | Roll conveyor |
| RW      | Rain water |
| SRT     | Sorter |
| T       | Tank |
| TR      | Transfer (roll to chain) |
| TT      | Turntable |

### Type name
The type name refers to the type of sensor (e.t. actuator) that is connected to the input (e.t. output). Therefore it is always used by input & output TAGs.

The use of the type name is only used by flags if there is a connection to a sensor (e.t. actuator).

| Type name | Description |
| :---:     | :--- |
| BCD       | BCD device |
| Dis       | Display device |
| Btn       | Button |
| Pot       | Potentiometer |
| Con       | Contactor |
| Lmp       | Lamp or LED |
| Mcb       | Motor circuit breaker |
| Rel       | Relay |
| Sel       | Selector Switch |
| Sen       | Sensor (General) |
| Vlv       | Valve |
| Clck      | Only in the case of clock memory bits/byte |
| Ne        | Only in the case of a falling edge (negative) memory bits |
| Po        | Only in the case of a rising edge (positive) memory bits |
| Sys       | Only in the case of system memory bits/byte |
|           | No abbreviation with flags if there is no relation to a sensor or actuator |

### Function
The function gives information about the function of the TAG. The next table shows different kind of options where it is allowed to combine multiple functions.

| Function| Description | Function| Description |
| :---: | :--- |:---: |:--- |
| Start | Start | Stop | Stop |
| Startup | Starting up | Started| Started |
| Stopped | Stopped | Reset | Reset |
| Err | Error or fault | Gen | General |
| Mode | Mode of action | Opt | Option |
| Aut | Automatic | Hand | Hand or manual |
| OK | OK | NOK | NOK |
| Fw | Forward | Bw | Backward |
| Rev | Reverse | Test | Test |
| On | On | Off | Off |
| Le | Left | Ri | Right |
| Up | Up(ward) | Down | Down(ward) |
| Open | Open | Close| Close|
| Lo | Low | Hi | High |
| Lim | Limit | Enb | Enable |
| Vol | Volume| Pres | Pressure |
| Temp | Temperature | Flow | Flow |
| Vac | Vacuum | Level | Level |
| Spd  | Speed  | Telrup | Teleruptor |
| TRUE | TRUE | FALSE | FALSE |
| 1   | TRUE  | 0   | FALSE  |
| Box | Box | Pal | Pallet |
| 1Hz | Frequency 1 HZ | 2Hz | Frequency 2 Hz |
| Ems | Emergency stop | Move | Move action |
| Fill | Fill action | Empty | Empty action |
| PV | Process value | SP | Setpoint |
| LMN | Loop manipulated value | Db | Deadband |
| Cmd | Command | ... | ... |

### Suffix (option)
The suffix is an option that:
* Gives information about the SI units.
* Gives the relationship to the electrical drawings

| Prefix | Description                      |
| :---:  | :---                             |
| mm     | Distance or level in millimeters |
| m      | Distance or level in meters      |
| m_s    | Speed in meters/second           |
| l      | Volume in litres                 |
| l_u    | Volume in liters/hour            |
| B1     | Electrical reference -B1         |
| K1     | Electrical reference -K1         |
| S1     | Electrical reference -S1         |
| U1     | Electrical reference -U1         |
| Q1     | Electrical reference -Q1         |

### Examples
Structure examples of TAGs.

| Prefix | Physical name | _     | Type name | Function     | _     | Suffix |
| :---:  | :---:         | :---: | :---:     | :---:        | :---: | :---:  |
| i      | CC            | _     | Btn       | Start        | _     | S1     |
| i      | CC            | _     | Btn       | Stop         | _     | S2     |
| i      | CC            | _     | Rel       | Ems          | _     | K1     |
| o      | CC            | _     | Lmp       | Start        | _     | H1     |
| o      | T10           | _     | Sen       | Level        | _     | B21    |
| m      | T10           | _     |           | Level & PV   | _     | mm     |
| m      | T10           | _     |           | Vol & PV     | _     | l      |
| m      |               |       | Gen       | Startup      |       |        |
| m      |               |       | Gen       | Started      |       |        |

TAGs examples with description.

| Examples | Description |
| :---: | :--- |
| iCC_BtnStart_S1 | Start pushbutton (-S1) on the control cabinet |
| iCC_BtnStop_S2 | Stop pushbutton (-S2) on the control cabinet |
| iCC_RelEms_K1 | Emergency stop relay (-K1) in the control cabinet |
| oCC_LmpStart_H1 | Start lamp (-H1) on the control cabinet |
| oT10_SenLevel_B21 | Level sensor (-B21) on tank T10 |
| mT10_LevelPV_mm | Actual level of tank T10 [mm] |
| mT10_VolPV_l | Actual volume of tank T10 [l] |
| mGenStartup | Installation is starting up |
| mGenStarted | Installation started |
