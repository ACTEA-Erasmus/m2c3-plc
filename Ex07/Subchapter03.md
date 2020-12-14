# Introduction into analog IO
_____________________________________
## Analog inputs
### Analog conversion
The artificial senses of a machine or installation, called **sensors**, transmit the current status of the machine or technical installation to the processing unit of the PLC via the PLC inputs.

A **sensor** measures a certain physical quantity and converts it into an electrical signal so that it can be processed by an electronic device. The electrical signal is converted by PLC input modules into a signal consisting of “0” and “1”. Such a signal is called a digital signal because it changes in stages (through the “0” and “1”).

![Analog to digital conversion](../Ex07/Images/AD.jpg)

The electrical signal is called an analog signal as it can take any value (the number of digits after the decimal point is in theory infinitely long).

![Analog vs Digital](../Ex07/Images/analog_vs_digital.jpg)

However, in automated systems one will define digital and analog signals according to the different states of the electrical signal:
- Electrical signals with stepless state between 2 extreme limits, which are converted into a series of “0” and “1” and are called **analog input signals**
- Electrical signals with 2 states that are converted to a logic “0” or a logic “1” are called **digital input signals**

![Analog vs Digital](../Ex07/Images/analog_vs_digital_detail.jpg)

### Analog sensors
Within the EU, electrical input signals are determined by standards and guidelines. The list below provides an overview of commonly used electrical signals in automated systems:
- 24 VDC & 0 VDC for digital signals
- 0 .. 20 mA / 4 .. 20 mA for analog current signals
- 0 .. 10 V for analog tension signals
- Pt100 resistor measurement for analog temperature signals

![Analog vs Digital](../Ex07/Images/sitrans_p200.jpg)
_Siemens SITRANS P200 Pressure sensor_

Because a digital signal changes stepwise, some information is lost during the conversion of analog input signals. In addition, analog input signals will always work between 2 extreme values, namely the min. and max. measuring limit. The difference between the max. limit and the min. limit is called the nominal measuring range.

![Measuring range](../Ex07/Images/measuring_range.jpg)

### Analog input modules
Analog signals are processed by analog input modules or by analog inputs integrated into the CPU. Analog input modules are available in modules with 2, 4, or 8 analog inputs and are often indicated with the abbreviation **AI**.

![Analog input module](../Ex07/Images/ai_module.jpg)


| Bit        | 15                 | 14    | 13   | 12   | 11   | 10   | 9   | 8   | 7   | 6  | 5  | 4  | 3  | 2  | 1  | 0  |
|-------------|--------------------|-------|------|------|------|------|-----|-----|-----|----|----|----|----|----|----|----|
| Weight     | S                  | 2<sup>14   | 2<sup>13  | 2<sup>12  | 2<sup>11  | 2<sup>10  | 2<sup>9  | 2<sup>8  | 2<sup>7  | 2<sup>6 | 2<sup>5 | 2<sup>4 | 2<sup>3 | 2<sup>2 | 2<sup>1 | 2<sup>0 |
| Numeric | \+/-               | 16384 | 8192 | 4096 | 2048 | 1024 | 512 | 256 | 128 | 64 | 32 | 16 | 8  | 4  | 2  | 1  |

Typical for these modules:
- They produce a serie of 16 BITs. This is called a **WORD** and the combination is called "input word"
- An input word uses the datatype **INT** a can therefore create values between -32768 and +32767
- The measuring range is narrowed to -27648 and +27648 to allow a certain overrange
- Input modules come with a resolution which determines how many bits are used

| **Resolution in bits** | **Accuracy** | **Analog value**  |
| :-------------------: | :----------------: | :-----------------: |
| 8                     | 128                | S000 0000 1xxx xxxx |
| 9                     | 64                 | S000 0000 01xx xxxx |
| 10                    | 32                 | S000 0000 001x xxxx |
| 11                    | 16                 | S000 0000 0001 xxxx |
| 12                    | 8                  | S000 0000 0000 1xxx |
| 13                    | 4                  | S000 0000 0000 01xx |
| 14                    | 2                  | S000 0000 0000 001x |
| 15                    | 1                  | S000 0000 0000 0001 |

The "unused" BITs are showed with an x and have the value "0" in case of a positive number.
The influence ont the accuracy is showed in the figure below.

![Resolution](../Ex07/Images/resolution.jpg)

### Process analog inputs in software
It is advisable to convert analog values to the measuring unit of the sensor.
The table below shows de conversion of a Siemens STIRAN P200 pressure sensor with a measuring range from 0 .. 4 bar g and an electrical signal from 4 .. 20 mA.

|       | Sensor | Electrical signal | AD conversion |  Software REAL value |
| :---: | :---: | :---: | :---: | :---: |
| Max.  | 4 bar | 20 mA | 27648 | **4.0** "bar" |
| Measured value | 2 bar | 12 mA | 13824 | **2.0** "bar" |
| Min.  | 0 bar | 4 mA  | 0     | **0.0** "bar" |

Conversion of analog inputs is done by the NORM_X and the SCALE_X instruction.

The **NORM_X** instruction converts an INT number limited between a min. and a max. value to a REAL number between 0.0 and 1.0 (or 0% to 100%).

![Normalization](../Ex07/Images/norm.jpg)

The **SCALE_X** instruction converts a REAL number limited between 0% and 100% to a REAL number between a min. and a max. value.

![Scale](../Ex07/Images/scale.jpg)


## Analog outputs
