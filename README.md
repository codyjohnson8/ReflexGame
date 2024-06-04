# ReflexGame
This Arduino Reflex Game challenges players to complete simple tasks displayed on the serial monitor within a specified time limit. Failure to complete the task in time results in a loss. As you progress through the rounds, the difficulty increases as the allotted time to respond decreases. 

To begin the game, press either the left or right button. The monitor will then prompt you with one of three commands: "tap it," "cover it," or "sing it," each requiring a specific action on the Arduino. Successfully completing each task earns you a point, but also reduces the time you have to respond in subsequent rounds.

The game continues until you successfully complete 30 rounds, at which point you win. Good luck!

User Input Controls
Left Button (Pin 4):
Function: Starts the game, triggers specific game actions.

Right Button (Pin 5):
Function: Starts the game, triggers specific game actions.

Tap Interrupt Sensor (Accelerometer):
Function: Detects taps as part of the "Tap it!" command.
Raw Range: Dependent on the accelerometer’s sensitivity setting (set to LIS3DH_RANGE_8_G).

Light Sensor:
Function: Measures light intensity for the "Cover it!" command.
Raw Range: 0 (no light) to 1023 (maximum light).

Microphone (Sound Sensor):
Function: Detects sound levels for the "Sing it!" command.
Raw Range: Measured in sound, typically from 0 dB to over 100 dB.

Defined Rules
Starting the Game:
Press either the left or right button to start the game.
The game begins with an delay of 3 seconds.

Game Commands:
The game displays commands on the serial monitor:
"Tap it!": Requires a tap detected by the accelerometer.
"Cover it!": Requires the light sensor to drop in light (covering the sensor).
"Sing it!": Requires a sound level above a certain threshold.

Scoring and Progression:
Successfully completing a task scores a point.
The time to respond decreases as the score increases.
The game ends when the player scores 30 points.

Game Failure:
Failing to complete a task within the given time results in a loss.
The game displays a failure message and resets the score.

Winning the Game:
Successfully scoring 30 points results in a win.
The game plays a congratulatory message and resets for a new game.

Sensors Used
Accelerometer (Tap Sensor):
Function: Detects taps for "Tap it!" command.
Raw Range: Varies based on configuration, set to detect a significant tap.

Light Sensor:
Function: Measures ambient light levels for the "Cover it!" command.
Raw Range: 0 to 1023.

Microphone (Sound Sensor):
Function: Measures sound pressure levels for the "Sing it!" command.
Raw Range: 0 dB to over 100 dB.





