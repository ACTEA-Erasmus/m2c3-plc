# The watertank project
_____________________________________
-   The [first goal](Ex07/Subchapter04_01.md) is to program the AD conversion of an analog input
-   The [second goal](Ex07/Subchapter04_02.md) is to program a high level alarm control circuit
-   The [third goal](Ex07/Subchapter04_03.md) is to program start-stop control circuit
-   The [fourth goal](Ex07/Subchapter04_04.md) is to control the level
-   The [last goal](Ex07/Subchapter04_05.md) is to deliver a working project

Back to the [project scope](Ex07/Subchapter04.md).

## Goal 2 : To program a high level alarm control circuit
**Step 1 :** Program in FC_T1 an alarm control circuit in network 3. Activate the alarm if the level is higher than 2500 mm.

```javascript
//Used Tags in this chapter
iCC_BtnReset_S5 - BOOL - %I 0.4 - Reset button
mA001 - BOOL - %M 0.0 - Alarm high level exceeded
mT1_SenLev_mm - REAL - %MD2 - Level tank 1 [mm]
```
**Step 2 :** Download the software and test the alarm by manually controlling the valves in Factory IO.

**Step 3 :** Test the AD conversions of the previous goal.
