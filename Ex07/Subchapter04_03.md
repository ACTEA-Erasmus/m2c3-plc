
![ACTEA](../Logo_ACTEA_2.png)
_____________________________________
# The watertank project
-   The [first goal](Ex07/Subchapter04_01.md) is to program the AD conversion of an analog input
-   The [second goal](Ex07/Subchapter04_02.md) is to program a high level alarm control circuit
-   The [third goal](Ex07/Subchapter04_03.md) is to program start-stop control circuit
-   The [fourth goal](Ex07/Subchapter04_04.md) is to control the level
-   The [last goal](Ex07/Subchapter04_05.md) is to deliver a working project

Back to the [project scope](Ex07/Subchapter04.md).

## Goal 3 : To program start-stop control circuit
**Step 1 :** Program in FC_CC a start-stop control circuit in network 1. Do not forget forget to program the start lamp.

```javascript
//Used Tags in this chapter
iCC_BtnStop_S1 - BOOL - %I 0.0 - Stop button
iCC_BtnStart_S3 - BOOL - %I 0.2 - Start button
mGenStarted - BOOL - %M 30.0 - Installation started
oCC_LmpStart_H1 - BOOL - %Q 0.0 - Lamp start
```

**Step 2 :** Download the software and test the start-stop control circuit. Do not forget to deactive the manually controlled valves in Factory IO from the previous goal; actuators may not be FORCED (Forced Tags are showed with a blue color).
