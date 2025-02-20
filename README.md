Molly Fry & Aidan Munns

This is a car alarm and automatic windshield wiper control system. When the driver sits down in the car, a welcome message is displayed. When both a driver and a passenger are sitting in the car, and both are wearing seat belts, ignition is allowed to begin. When the ignition button is pressed under these conditions, the engine starts. While the engine is running, the user has the 
option to select the wiper mode from the options HI, LO, INT, and OFF. If HI is selected then the wipers turn on, moving between 0 and 67 degrees at a rate of 40 rpm, with no hesitation at any point. If LO is selected then the wipers turn on, moving between 0 and 67 degrees at a rate of 30 rpm, with no hesitation at any point. If INT is selected then the wipers turn on, moving between 0 and 67 degrees at a rate of 30 rpm, but hesitating for a chosen time interval every time it reaches the 0 degree position. The user can choose between time intervals of 3, 6, and 8 seconds. If OFF is selected then the wipers do not move from their position of 0 degrees. When the engine is turned off, or when OFF is selected, then the windshield wiper completes its cycle of movement and returns to the 0 degree position, becoming stationary. 

We chose to use a positional servo motor for our windshield wipers, as opposed to a continuous servo motor. We made this choice because it seemed more manageable to code, and because it consistently reached the desired angle and accurate position in a way that the continuous servo had trouble achieving. 

IGNITION SUBSYSTEM:
| Specifications | Test Result | Comments |
| :---         |     :---:      |          ---: |
|Enable engine start while both seats are occupied and seatbelts fastened. Otherwise print appropriate error message.| Pass | All error messages are displayed on the serial monitor depending on which error occurred. |
|Start the engine (light the blue LED, turn off Green) when ignition is enabled (green LED) and ignition button is pressed  (before the button is released).|Pass| Serial Monitor will display: Engine Started  |
| Keep the engine running even if the driver/passenger should unfasten belt and exit the vehicle.|  Pass | |
| When the engine is running, stop the engine once the ignition button has been pushed and then released. | Pass | Serial Monitor will display: Engine Stopped |

WINDSHIELD WIPER SUBSYSTEM:

|                     Specification                    |  Test Result  |                       Comment                      |
| ---------------------------------------------------- | ------------- |----------------------------------------------------|
| While the engine is running, the user selects the wiper mode| Pass          | These mode are selected by the potentiometer and displayed on the LCD   |
|If the user selects LO the wiper moves at 30 rpm |  Pass         |    |
| If the user selects HI the wiper moves at 40rpm | Pass | | |
| If the user selects INT the wiper moves according to the selected interval. Either 3, 6, or 8 seconds   | Pass          | Interval displayed as slow, medium, or high on the LCD|
|Wiper initializes to 0 degrees when the system turns on| Pass | |
| Wiper turns off and returns to 0 degrees when OFF is selected| Pass| |
