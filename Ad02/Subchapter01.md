# TAG naming convention
## General
The use of a naming convention is used to increase the readability of the software.
TAG and block names are constructed with capital and small letters where
* The name is assembled with one or more words
* Each word starts with a capital letter
* Words can be reduced by the use of abbreviations

## Programming blocks
The name of a programming block is constructed as showed in the next table.
| Block type | _ | Block description |

It starts with the block type abbreviation, followed by an underscore and it finish with a block description.


| Block type | Description |
| :--- | :--- |
| FC | Function |
| FB | Function block |
| OB | Organization block |
| DB | Data block |

| Example | Description |
| :--- | :--- |
| FC_CC | Function which contain the software of the control cabinet equipment |
| DB_Alarms | Alarms & events data block |
| DB_HMI1 | Interface data block for HMI1 |


## PLC TAGs
The name of a PLC TAG is constructed as showed in the next table.
| Prefix | Physical name | _ | Type | Function | _ | Suffix |

The prefix gives the function of the absolute address.
| Prefix | Description |
| :--- | :--- |
| i | Input |
| o | Output |
| m | Flag  (merker) |

| Example | Description |
| :--- | :--- |
| iCC_BtnStart_S1 | Start pushbutton (-S1) on the control cabinet |
| iCC_BtnStop_S2 | Stop pushbutton (-S2) on the control cabinet |
| iCC_RelEms_K1 | Emergency stop relay (-K1) in the control cabinet |
| oCC_LmpStart_H1 | Start lamp (-H1) on the control cabinet |
| oT10_SenLevel_S21 | Level sensor (-S21) on tank T10 |
| mT10_LevelX_mm | Actual level of tank T10 [mm] |
| mT10_VolX_l | Actual volume of tank T10 [l] |
| mStartup | Installation is starting up |
| mStarted | Installation started |
