
![ACTEA](/Logo_ACTEA_2.png)
_____________________________________
# The watertank project
-   The [first goal](Ex07/Subchapter04_01.md) is to program the AD conversion of an analog input
-   The [second goal](Ex07/Subchapter04_02.md) is to program a high level alarm control circuit
-   The [third goal](Ex07/Subchapter04_03.md) is to program start-stop control circuit
-   The [fourth goal](Ex07/Subchapter04_04.md) is to control the level
-   The [last goal](Ex07/Subchapter04_05.md) is to deliver a working project

Back to the [project scope](Ex07/Subchapter04.md).

## Goal 5 : Deliver a working project
- **Step 1 :** Compile the hardware with a rebuild all command
- **Step 2 :** Compile the software with a rebuild all command
- **Step 3 :** Download hardware and software to the PLC_1
- **Step 4 :** Test the Project

__Normal functionallity__
1. Start the watertank installation
2. Change the setpoint below the high level alarms
3. Check the level control (does it maintain the level?)
4. Repeat these steps by changing the setpoint (always below the alarm level)

__High level alarm__
1. Start the watertank installation
2. Change the setpoint above the high level alarms
3. Check the level control (does it fill above the high level?)
4. The alarm must be activated if the level is too high!
5. Does the inlet valve closes?
6. Can you reset the alarm if the level is too high? No!
7. Can you reset the alarm if the level is below the alarm level? Yes!
8. Can you program the red error lamp so this will light on if there is a level alarm?

<details>
	<summary>Click here to download the TIA Portal Exercise project solution</summary><!-- Empty line after this one needed, do not delete! -->

<br>
Download file <a href="./Ex07/Documents/Ex7_Watertank.zap15_1">here</a>.</p>

  </details><!-- Empty line after this one needed, do not delete! -->
