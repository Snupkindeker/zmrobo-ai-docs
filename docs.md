## Overview

This is the ultimate documentation to writing code for ZMROBO robots via RoboEXP software. The documentation is meant to be used by language models to be more competent in this topic.

ZMROBO is a Chinese robotics company founded in 2002. They sell parts and building kits for people to build robots and other smart creations. Most parts have their analogs in LEGO MINDSTORMS EV3, but ZMROBO ones are bigger by 50% (1.5x).

### Part categories

ZMROBO parts can be split into different categories by their purpose and appearance.

#### 1. Motors

The **motors** category has a self-explanatory name. Here's the full table of their specifications:

| №   | Model          | Description                         | Working torque | Stopping torque | Encoder resolution (CPR) | Speed (RPM) | Voltage, V | Rotation range | Size, cm     | Note                                                           |
| --- | -------------- | ----------------------------------- | -------------- | --------------- | ------------------------ | ----------- | ---------- | -------------- | ------------ | -------------------------------------------------------------- |
| 1   | JMP-BE-2115    | Pump motor                          | -              | -               | -                        | -           | 5          | -              | 7 x 5 x 3    | Suction pressure - 60 kPa<br>Working t° 5-45°C.                |
| 2   | JMP-BE-3568A/B | High-speed motor                    | 10             | -               | 780                      | 300-340     | 5-7.2      | -              | 9 x 4 x 3    | Fast, but weak.                                                |
| 3   | JMP-BE-3569A/B | Low-speed motor                     | 25             | -               | 2048                     | 100         | 5-7.2      | -              | 9 x 4 x 3    | Slow, but powerful.                                            |
| 4   | JMP-BE-3570A   | Large motor                         | 21             | -               | 360                      | 170-190     | 4.8-8.4    | -              | 12 x 5.5 x 4 | -                                                              |
| 5   | JMP-BE-3571A   | Medium motor                        | 10             | -               | 360                      | 260-280     | 5-7.2      | -              | 8 x 4 x 3    | -                                                              |
| 6   | JMP-BE-3578A   | Medium motor, no encoder, 3.7V      | 4              | 18              | -                        | 140         | 3-4.2      | -              | 7 x 4 x 3    | A compact motor, no encoder.                                   |
| 7   | JMP-BE-3579A   | Medium motor, 7.4V                  | 8.5            | >=34            | 360                      | 160-180     | 7.4-8.4    | -              | 7 x 4 x 3    | A compact motor.                                               |
| 8   | JMP-BE--3581A  | Medium motor, 3.7V                  | 4              | 18              | 360                      | 140         | 3-4.2      | -              | 7 x 4 x 3    | A compact motor.                                               |
| 9   | JMP-BE-3582A   | Large motor, 7.4V                   | >=30           | -               | 360                      | 190-210     | 7.4-8.4    | -              | 7 x 5 x 3    | A compact motor.                                               |
| 10  | JMP-BE-9520    | Digital servo (competition version) | 79             | -               | 4096                     | 68          | 5-9        | 0-359°         | 7 x 5 x 3    | Can work as a slow gear motor.<br>**Plugs into sensor ports!** |
| 11  | JMP-BE-9523    | Gear motor (competition version)    | 20             | -               | 2048                     | 200         | 4.8-8.4    | -              | 7 x 5 x 3    | Best motor for precise movement.                               |
| 12  | JMP-BE-9524    | Mini servo                          | >=18           | -               | -                        | ~62         | 5          | 0-270°         | 5 x 4 x 3    | **Plugs into sensor ports!**                                   |
#### 2. Controllers

The **controllers** category includes various controllers to control the robot and run code. Here is the full table of their specifications.


| Name                                      | M6-RCU                                    | E6-RCU                                    | M5-RCU                             | C6-RCU                                    | H-RCU                           | E7-RCU                                  |
| ----------------------------------------- | ----------------------------------------- | ----------------------------------------- | ---------------------------------- | ----------------------------------------- | ------------------------------- | --------------------------------------- |
| Microcontroller                           | STM32F407, 32-bit                         | STM32F407, 32-bit                         | ESP32-S, 32-bit                    | STM32F407, 32-bit                         | ?                               | STM32H743                               |
| CPU                                       | Cortex-M4, 168 MHz, 196KB SRAM, 1MB FLASH | Cortex-M4, 168 MHz, 196KB SRAM, 1MB FLASH | ?                                  | Cortex-M4, 168 MHz, 196KB SRAM, 1MB FLASH | 8-core processor                | Cortex-M7, 400 MHz, 1MB SRAM, 2MB FLASH |
| Size, mm                                  | 70 x 70 x 32                              | 110 x 70 x 44                             | 70 x 70 x 29                       | 70 x 70 x 29                              | 110 x 70 x 40                   | 110 x 70 x 40                           |
| Weight, g                                 | 124                                       | 251                                       | 85                                 | 115                                       | 293                             | 242                                     |
| Supported coding software                 | ZMROBO 3.0, RoboCode, RoboEXP, Cabin      | ZMROBO 3.0, RoboCode, RoboEXP, Cabin      | ZMROBO 3.0, RoboCode, Cabin, cards | RoboCode, RoboEXP                         | ZMROBO 3.0, RoboCode            | RoboCode, RoboEXP                       |
| RAM                                       | 8 MB                                      | 16 MB                                     | ?                                  | ?                                         | 2 GB                            | ?                                       |
| Flash memory                              | 8 MB                                      | 16 MB (+16MB for MP3)                     | 8 MB                               | ?                                         | 16 GB                           | 120 MB                                  |
| USB Type-C                                | V                                         | V                                         | V                                  | V                                         | V                               | V                                       |
| Bluetooth                                 | 4.2 BLE                                   | 4.2 BLE                                   | 4.2 BR/EDR & BLE                   | 4.2 BLE                                   | 4.2 BLE                         | 5.0                                     |
| Wifi                                      | X                                         | X                                         | 802.11b/g/n/e/i                    | X                                         | 2.4 GHz / 5 GHz                 | 2.4 GHz                                 |
| Built-in sensors                          | Sound                                     | Sound                                     | X                                  | Sound                                     | Sound, gyroscope, accelerometer | Sound                                   |
| Screen type                               | Touch screen, color                       | Touch screen, color                       | Matrix, yellow                     | Color                                     | Touch screen, color             | Touch screen, color                     |
| Screen diagonal                           | 2.4"                                      | 2.4"                                      | X                                  | 1.8"                                      | 4"                              | 3.2"                                    |
| Screen resolution                         | 320 x 240                                 | 240 x 320                                 | 5 x 7                              | 160 x 128                                 | ?                               | ?                                       |
| Motor ports                               | 4                                         | 4                                         | 2                                  | 3                                         | 0                               | 8                                       |
| Sensor ports                              | 5                                         | 8                                         | 3                                  | 4                                         | 0                               | 8                                       |
| General ports (for both motors & sensors) | 0                                         | 0                                         | 0                                  | 0                                         | 12                              | 0                                       |
| UART port number(s)                       | P5                                        | P8                                        | -                                  | -                                         | ?                               | P6, P8                                  |
| Servos can be plugged into                | P3, P4, P5                                | P4, P5, P6                                | P1, P2                             | P2, P3, P4                                | -                               | ?                                       |
| Voltage, V                                | 8.4                                       | 8.4                                       | 3.7                                | 3.7                                       | 8.4                             | 8.4                                     |
| Battery capacity, mAh                     | 800                                       | 2000                                      | 800                                | 2100                                      | 2500                            | 2600                                    |
| Charging                                  | USB-C, 2A, 5V                             | USB-C, 2A, 5V                             | USB-C, 2A, 5V                      | USB-C, 2A, 5V                             | USB-C, 2A, 5V                   | USB-C, 2A, 5V                           |

All controller motor/sensor/general ports use RJ-12 interface.
#### 3. Sensors

The **sensors** category has a self-explanatory name. Here's the full list of ZMROBO sensors and their descriptions:

1. **Ultrasonic sensor** (JMP-BE-6311, JMP-BE-6306) - an ultrasonic distance sensor. Woking voltage: 5V, detection distance: 5-200 cm, accuracy: 1 cm. Has 2 built-in RGB LED lights.
2. **Intelligent eye** (JMP-BE-1531) - can receive and send numbers from 0 to 255 via built-in infrared module from/to other intelligent eyes. Also has 8 24-color LED lights.
3. **Gesture sensor** (JMP-BE-2628) - identifies the direction of motion of an object in front of it.
	 1 - up
	 2 - down
	 3 - left
	 4 - right
	 5 - toward the sensor
	 6 - back from the sensor
	 7 - clockwise
	 8 - counter-clockwise
	 Working voltage: 5V, detection distance: 3-10 cm.
4. **Touch sensor** (JMP-BE-1618) - recognizes and returns the corresponding value of False or True according to whether the touch switch is pressed to the touch position. Working voltage: 5V.
5. **Photoelectric sensor** (JMP-BE-1146A) - scans the gray value of an object and returns it (0-4096).
6. **Infrared ranging sensor** (JMP-BE-6205) - returns a number in 1-10 range depending of the distance to an object (3-20 cm detection range), working voltage: 5V. A completely inaccurate sensor, unrecommended for use.
7. **Color sensor** (JMP-BE-1141A) - scans the color of an object and returns the corresponding number:
	1 - red
	2 - green
	3 - blue
	4 - yellow
	5 - black (or no object)
	6 - white
	Or returns raw RGB data.
	Working voltage: 5V
8. **Temperature & humidity sensor** (JMP-BE-1942) - self-explanatory. Detection range: -40 - 125°C for temperature, 0-100% RH for humidity. Working voltage: 5V. When temperature/humidity changes dramatically, takes about 5 minutes to return to an accurate value.
9. **Laser ranging sensor** (JMP-BE-1245) - best for measuring distance. Returns the distance in mm. Detection range: 2-120 cm, accuracy: 1 cm, working voltage: 5V.
10. **Intelligent tracking module** (JMP-BE-1149) - the absolute best option for line tracking. Has seven independent photoeletric sensors with 7-color LED lights. Uses IIC communication. Working voltage: 5V.
11. **Color lamp** (JMP-BE-1536) - just a 7-color LED light. Working voltage: 5V.
12. **Barometric sensor** (JMP-BE-2020) - detects the ambient air pressure and returns it. Working pressure range: 30-110 kPa, accuracy: 0.2 Pa. Working voltage: 5V.
13. **Magnetic sensor** (JMP-BE-1643) - returns the magnetic field strength and direction around itself. Minimum strength: 0.9 mT. Working voltage: 5V.

#### 4. Modules.

The **modules** part category contains highly functionable devices. Here's the full list of them:

1. **AI vision module** (JMP-BE-1743) - a **black** electronic component that integrates both machine vision and voice control capabilities. Built with a 64-bit dual core K210 processor, supports Python programming and multiple neural network models, has 8 MB SRAM and 16 MB flash memory. Operating voltage: 5V, operating current: >=350 mA. Supported neural network models: YOLOv3, MobileNetV2, TinyYOLOv2. Image recognition: QVGA 60 FPS, VGA 30 FPS. Camera: 2 MP, 80° FOV. Display: 1.54" 240x240 TFT LCD. Voice commands: 59. Size: 50 x 50 x 36 mm. Not to be confused with Machine vision module (JMP-BE-1748), which is white.
2. **Bluetooth adapter** (JMP-BE-9203) - a USB Type-A bluetooth adapter. Should be plugged into a computer to communicate with a controller via bluetooth. Effective communication distance: 10 meters.
3. **Scanning camera** (JMP-BE-1744) - scans barcodes and QR-codes that encode numbers from 0-255. Working voltage: 5V, scanning distance range: 5-18 cm.
4. **16x16 blue dot matrix** (JMP-BE-1534) - can display 1 Chinese character, 2 other characters or custom patterns. Uses HT1632C chip, running speed: 256 kHz. Working voltage: 2.4-5.5V.
5. **IoT module** (JMP-BE-9261) - enables connection to Wi-Fi and interaction with IoT platforms for data exchange. It supports remote control and monitoring of various devices, such as turning lights on or off, starting devices, and executing programmed tasks.

#### 5. Plastic parts.

The last but not least, **plastic parts** category has a self-explanatory name. Here are some types of plastic ZMROBO parts.

1. **Wheels**. ZMROBO has different types of wheels, for example: mecanum wheels, 65 x 25 mm wheels with silicone tires and 56 x 26 mm wheels with rubber tires. Also there is the metal ball caster (similar to LEGO MINDSTORMS EV3), a plastic ball caster and a small red metal ball caster (JMP-BP-1276).
2. Beams, pegs, axles, gears, frames and plates are all similar to LEGO (except being 1.5x bigger).
3. **Disassembly tools** (JMC-JM-0238) are great for disassembling builds.

## RoboEXP software

### Overview

RoboEXP is one of several applications for writing code for ZMROBO robots. It is considered the most advanced of them all, because it supports a convenient graphical "G language" and the C language, while other applications use Scratch-like blocks and Python. There are 2 file types in RoboEXP: **application** and **subroutine**. Subroutines can be referenced in applications to organize code.

### Interface description

When the user opens RoboEXP, they can see its interface. It consists of different elements: Menu bar, Toolbar and the rest of the screen is gray, while no files are opened.

#### Menu bar

There are different buttons on the Menu bar which open a drop-down menu of options upon being clicked on. Here's the list of these buttons and their menus:

##### 1. File

The **file** menu features basic options: New, Open, Open, Open Example Programs, Save, Save as, Save all, Close, Close all files, Export As Code Application (saves the file as an application), Export As Flow Subroutine (saves the file as a subroutine), Print, Recent Files, Update (RoboEXP) and Exit. There's also the Convert Old Projects option, which helps you make a project created in RoboEXP 2.1 and below compatible to newer versions. The code is stored in paired files - .rcu and .c with the same name.

##### 2. Edit

The **edit** menu features classic actions: Undo, Redo, Cut, Copy, Paste, Delete and Select all.

##### 3. View

The **view** menu lets the user show and hide different interface windows: Icons Window (G language only), Code Window (G language only), Property Window (G language only), Variable Window (G language only), Template Code Window (C language only) and Output Window.

##### 4. Project

The **project** menu contains options to control the project:
1. **New Private Subroutine** (G language only) - creates a subroutine file in the same language and folder with a custom name and automatically references it in the current project.
2. **Reference Existing Subroutine** (G language only) - opens a file manager window for the user to select a .rcu subroutine file to reference. This is required to start using it in the project, if it's not referenced yet.
3. **Open Selected Subroutine** (G language only) - opens the code of the selected subroutine.
4. **Update Private Subroutine** (G language only) - refreshes the selected subroutine (required when the subroutines parameters/return type have changed).
5. **Private Subroutines Manager** (G language only) - opens the manager window, which allows the user to add/remove subroutines from the project and sort them in the icon list.
6. **Project Properties** - opens the project properties window, which allows customization of the file's caption, author and description, return type and description and parameters (in a subroutine).

##### 5. Tool

The **tool** menu has different tools:
1. **System Library** - lets the user customize the built-in library of functions.
2. **Compile** - compiles the file and shows the result in the Output Window. Also shows errors in referenced subroutines.
3. **Download** (Bluetooth and wired) - downloads the file to the RCU. Compiles the file beforehand if Compile Before Download is enabled in Options -> Global Settings.
4. **Options** - opens the Options window.

##### 6. Window

The **window** menu lets the user cycle between opened RoboEXP windows and files.

##### 7. Help

The **help** menu features 2 buttons:
1. **Help topics** - opens a `.chm` documentation file.
2. **About** - opens a window with information about your RoboEXP version, selected controller type and a link to ZMROBO's website.

#### Toolbar

The **toolbar** is a line of icons that help the user access most frequently used actions faster. At the end it shows the selected controller type, which opens the Options window when double-clicked.

#### Options

The **options** window lets the user control the software's behavior. It features 3 sections of settings:
##### 1. Software Type

The **software type** section has 2 settings: software type (controller type) and language. There are 3 languages in RoboEXP: English, Chinese (Simplified) and Chinese (Traditional). Changing these 2 settings won't do anything unless RoboEXP is restarted.

##### 2. Global Settings

The **global settings** section has several useful settings, for example:
1. **Compile file before download** - self-explanatory, enabled by default, not recommended to be disabled.
2. **Show message box after download** - decides if the "Download file completed." message should be shown after downloading a file to RCU.

##### 3. Flow View

The **flow view** section features various customization settings:
1. **Show code line** (for G language) - decides if subroutine's C syntax should be displayed in the Property Window when the subroutine is selected.
2. **Show description in tip** (for G language) - decides if a subroutine's description should be displayed in the tip when hovering its icon.
3. **Show N parameters** (for G language) - decides how many subroutine parameters should be shown above its icon.
4. **Back color** (for G language) - the background color.
5. **Max undo steps (1-20)** - self-explanatory.

### Programming in G language

#### Overview

G language is a graphic programming language, created by ZMROBO and used only in RoboEXP. The program written in this language is stored in a `.rcu` file and looks like a sequence of icons connected to each other. The icons are mostly functions, which are executed from left to right. The G code gets automatically converted to C code, which is then compiled and downloaded to the RCU, so the RCU stores C code only.

#### Window descriptions

There are 5 windows in the G language code editor:

1. **Icons** - a full list of icons divided into 9 sections, 8 of them store built-in icons and the 9th one has icons of referenced subroutines.
2. **Code** - displays the code, converted to C language.
3. **Property** - when an icon is selected, show its properties, otherwise is empty.
4. **Variables** - a full list of local and global variables.
5. **Output** - shows the result of the current file's last compilation.

#### Variables

Variables in G language can be created, edited and deleted in the Variables Window. There are 2 types of variables: **local** and **global**. **Local** variables are unique for each file. **Global** variables must be created in the main application file, and they also should be added to its subroutine files with same properties if needed to be used there. Every variable has 4 properties:
1. **Name** - the name of the variable.
2. **Type** - the variable's type (from C): int, char, long, unsigned int, unsigned char, unsigned long, double or string.
3. **Default** - the variable's default value.
4. **Hint** - a comment.

#### Icon descriptions

Every icon in the code can have up to 2 connections (except Start and If): one on the left side and one on the right side. The program starts with the Start icon, and then the user can drag icons out of the Icons Window and connect them to each other. Unconnected or incorrectly connected icons are black & white. The unconnected icons are completely ignored by the compiler. They are also ignored if they're connected to each other and not to the Start icon.

The 205 built-in icons are divided into 8 categories:
1. **Flow Control** - basic blocks like Start, If, While, For and so on. Contains 9 icons.
2. **Performer** - motor and servo control. Contains 41 icons.
3. **Light Sensor** - light, color and line-tracking sensors control. Contains 26 icons.
4. **Touch Sensor** - touch sensor control. Contains 6 icons.
5. **Other Sensor** - other sensors control. Contains 38 icons.
6. **Built In** - controller's built-in functions like delay, mic, music play etc. Contains 26 icons.
7. **Display** - controller's display control. Contains 27 icons.
8. **Wireless** - wireless communications. Contains 32 icons.

Here's the description of every single icon:
**Note**: if there aren't 205 icons listed, that's normal, because there are the ones that are useless or the ones that don't have a complete statement of their purpose, which may not be listed here.
##### 1. Flow Control

| Name       | Description                                                                                                                                                                                                                                                                                                |
| ---------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| If         | A basic `if` operator. Creates an end icon when placed.<br>Has 2 connection "ports" on the right side, the upper one is<br>for code that executes when the condition is `true`, the lower<br>one - for the `else` code. The end icon also has 2 "slots" on<br>the left side for corresponding connections. |
| While      | A basic `while` cycle. Creates an end icon when placed.                                                                                                                                                                                                                                                    |
| For        | A basic `for` cycle. Creates an end icon when placed.                                                                                                                                                                                                                                                      |
| Calculate  | Useful to assign a value to a variable, C-like syntax.<br>`;` at the end isn't needed.                                                                                                                                                                                                                     |
| Continue   | A basic `continue` operator.                                                                                                                                                                                                                                                                               |
| Break      | A basic `break` operator.                                                                                                                                                                                                                                                                                  |
| Return     | A basic `return` operator.                                                                                                                                                                                                                                                                                 |
| CodeEditor | Lets the user insert pieces of C-code inside the G-code.                                                                                                                                                                                                                                                   |
| Start      | Start of the program.                                                                                                                                                                                                                                                                                      |

##### 2. Performer


| Icon name                               | C syntax                                               | Description                                                                                                                                     | Parameter descriptions                                                                                                                                         |
| --------------------------------------- | ------------------------------------------------------ | ----------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| LED                                     | `Set3CLED(which, Color);`                              | Sets the color lamp (JMP-BE-1536) status.                                                                                                       | **which**: lamp port (\_P1\_-\_P8\_).<br>**Color**: a number in 0-7 range: 0 - OFF, 1 - RED, 2 - GREEN, 3 - BLUE, 4 - YELLOW, 5 - PURPLE, 6 - CYAN, 7 - WHITE. |
| Motor                                   | `SetMotor(which, speed);`                              | Sets a motor's speed.                                                                                                                           | **which**: motor port (\_M1\_-\_M8\_).<br>**speed**: speed value (-100 - 100).                                                                                 |
| Release motor                           | `SetMotorFree(which);`                                 | Releases a motor free.                                                                                                                          | **which**: motor port (\_M1\_-\_M8\_).                                                                                                                         |
| HighSpeedServo (gray icon)              | `SetMotorServo(which, speed, angle);`                  | Starts a motor with given speed and stops it at a given angle. Continues the program immediately after starting the motor.                      | **which**: motor port (\_M1\_-\_M8\_).<br>**speed**: speed value (-100 - 100).<br>**angle**: angle value (1-3600)                                              |
| Wait for Angle                          | `SetWaitForAngle(which, speed, angle);`                | Starts a motor with given speed and stops it at a given angle. Doesn't continue the program until the motor reaches the target angle.           | **which**: motor port (\_M1\_-\_M8\_).<br>**speed**: speed value (-100 - 100).<br>**angle**: angle value (1-3600)                                              |
| HighSpeedServo (for JMP-BE-9523)        | `SetMotorServo2048(which, speed, angle);`              | Starts a motor with given speed and stops it at a given angle. Continues the program immediately after starting the motor.                      | **which**: motor port (\_M1\_-\_M8\_).<br>**speed**: speed value (-100 - 100).<br>**angle**: angle value (1-3600)                                              |
| Wait for Angle (for JMP-BE-9523)        | `SetWaitForAngle2048(which, speed, angle);`            | Starts a motor with given speed and stops it at a given angle. Doesn't continue the program until the motor reaches the target angle.           | **which**: motor port (\_M1\_-\_M8\_).<br>**speed**: speed value (-100 - 100).<br>**angle**: angle value (1-3600)                                              |
| Encoder                                 | `GetMotorCode(which);`                                 | Returns the motor encoder value.                                                                                                                | **which**: motor port (\_M1\_-\_M8\_).                                                                                                                         |
| Reset encoder                           | `SetMotorCode(which);`                                 | Resets a motor's encoder                                                                                                                        | **which**: motor port (\_M1\_-\_M8\_).                                                                                                                         |
| Set the Magnetic Servo Degree & Time    | `SetMagneticServoDegreeTime(which, degree, time);`     | Sets a servo to a given degree in given time. Continues the program immediately after starting the servo.<br>For JMP-BE-9520.                   | **which**: servo port (\_P1\_-\_P8\_).<br>**degree**: degree to go to (0-359).<br>**time**: time in ms.                                                        |
| Set Magnetic Servo Degree & Speed       | `SetMagneticServoDegreeSpeed(which, degree, speed);`   | Sets a servo to a given degree with given speed. Continues the program immediately after starting the servo.<br>For JMP-BE-9520.                | **which**: servo port (\_P1\_-\_P8\_).<br>**degree**: degree to go to (0-359).<br>**speed**: speed value (1-100).                                              |
| Set Magnetic Servo Wait For Degree      | `SetMagneticServoWaitForDegree(which, degree, speed);` | Sets a servo to a given degree with given speed. angle. Doesn't continue the program until the motor reaches the target angle. For JMP-BE-9520. | **which**: servo port (\_P1\_-\_P8\_).<br>**degree**: degree to go to (0-359).<br>**speed**: speed value (1-100).                                              |
| Set Magnetic Servo code-motor           | `SetMagneticServoCodeMotor(which, code value, speed);` | Moves a servo by a given code value with given speed. For JMP-BE-9520.                                                                          | **which**: servo port (\_P1\_-\_P8\_).<br>**code value**: code value (4096 CPR).<br>**speed**: speed value (-100 - 100).                                       |
| Magnetic Servo Motor                    | `SetMagneticServoMotor(which, speed);`                 | Starts a servo with given speed in gear motor mode.<br>For JMP-BE-9520.                                                                         | **which**: servo port (\_P1\_-\_P8\_).<br>**speed**: speed value (-100 - 100).                                                                                 |
| Magnetic Servo Encoder                  | `SetMagneticServoEncoder(which);`                      | Resets a servo's encoder.<br>For JMP-BE-9520.<br>                                                                                               | **which**: servo port (\_P1\_-\_P8\_).                                                                                                                         |
| Get Magnetic Servo Encoder              | `GetMagneticServoEncoder(which);`                      | Returns a servo's encoder value.<br>For JMP-BE-9520.                                                                                            | **which**: servo port (\_P1\_-\_P8\_).                                                                                                                         |
| Get Magnetic Servo Degree               | `GetMagneticServoDegree(which);`                       | Returns a servo's angle value.<br>For JMP-BE-9520.                                                                                              | **which**: servo port (\_P1\_-\_P8\_).                                                                                                                         |
| Magnetic Servo torque                   | `SetMagneticServoPowerDown(which);`                    | Releases a servo (normally it tries to keep itself in an angle and resists movement).<br>For JMP-BE-9520.                                       | **which**: servo port (\_P1\_-\_P8\_).                                                                                                                         |
| Servo                                   | `SetSeeringEngine(which, angle);`                      | Sets a servo to a given angle.<br>For JMP-BE-9524.                                                                                              | **which**: servo channel (1-3).<br>**angle**: the target angle (0-270 or 360 to release servo).                                                                |
| Seering Engine speed                    | `SetSeeringEngineTime(which, angle, Time);`            | Sets a servo to a given angle in given time.<br>For JMP-BE-9524.                                                                                | **which**: servo channel (1-3).<br>**angle**: the target angle (0-270 or 360 to release servo).<br>**time**: time in ms (0-5000).                              |
| Motor speed control (wrench on icon)    | `SetMotorConstSpeedValue(which, code, P, I, D);`       | Sets PID coefficients for `SetMotorConstSpeed`.                                                                                                 | **which**: motor port (\_M1\_-\_M8\_).<br>**code**: motor's encoder CPR.<br>**P, I, D**: coefficients, type: double.                                           |
| Motor speed control (no wrench on icon) | `SetMotorConstSpeed(which, speed);`                    | Starts a motor with given speed. Uses PID regulation to compensate aging, unsmooth surface and other factors, that change speed.                | **which**: motor port (\_M1\_-\_M8\_).<br>**speed**: speed value (-100 - 100).                                                                                 |
