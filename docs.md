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
