# Introduction into automated systems
## Automation
**Automation** is the way to have tasks performed automatically by electrical appliances, machinery or technical installations.

## Parts of an automated system
In order to achieve this, these devices need following items:
* **Senses** to observe the actual state
* **Power** that is adjustable to obtain a desired state
* A **brain** to process the senses and to control the power

The artificial senses are called **sensors** and they are assembled from mechanical and electronic components. There main goal is to convert a physical condition to an electrical signal.

The controllable power components are called **actuators**. The are also assembled from mechanical and electronic components and they are often extended with additional hydraulic, pneumatic or electrical components to control high powers.

The **programmable brain** is a combination of processors and electronic memories to process the sensors, connected on inputs, and to control the actuators, connected on outputs. It is extended with an electrical power supply connection, a communication port and connections for additional equipment. The collection of it all is called a Central Processing Unit (CPU).

## Programmble logic controller
PLC stand for **Programmble Logic Controller** and it is mainly used in technical installations for B2B (Business-to-business) solutions. Therefore PLC's are installed into electrical cabinets and they are manufactured only by a few constructors such as Siemens, Beckhoff, Schneider-Electric, Allen-Bradley and Omron.
Each constructor has more than one PLC series to have a solution for each automation project.

![Siemens S7-1200 PLC](../Ex01/Images/Siemens_S7_1200_PLC.jpg)

It is possible to extended a CPU with extra sensors and/or actuators by adding modules. Each constructor has a catalog with additional modules for their PLC's. The PLC used on the PLC board is a **Siemens PLC from the S7-1200 family** with 3 additional modules: at the left a 24VDC power supply and an Ethernet switch. In the middle an analog output signal board.

For Siemens modules can each module be recognized by means of its abbreviations.

| Abbreviation | Declaration |
| :--- | :--- |
| AC/DC/RLY | PLC 230VAC power supply / 24VDC inputs / relay outputs |
| DC/DC/DC | PLC 24VDC power supply / 24VDC inputs / transistor outputs |
| AI | Analog Input |
| AQ | Analog Output |
| CPU | Central Processor Unit |
| CSM | Compact Switch Module |
| DI | Digital Input |
| DQ | Digital Output |
| IO | Inputs & Outputs |
| LINK | Indication of connection state by LED beside LINK text |
| NC | Normally closed |
| NO | Normally open |
| RLY | Relay |
| PM | Power module |
| SB | Signal Board |
| SM | Signal Module |
