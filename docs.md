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


| Name            | M6-RCU                                    | E6-RCU                                    | M5-RCU          | C6-RCU                                    | H-RCU            | E7-RCU                                  |
| --------------- | ----------------------------------------- | ----------------------------------------- | --------------- | ----------------------------------------- | ---------------- | --------------------------------------- |
| Microcontroller | STM32F407, 32-bit                         | STM32F407, 32-bit                         | ESP32-S, 32-bit | STM32F407, 32-bit                         | ?                | STM32H743                               |
| CPU             | Cortex-M4, 168 MHz, 196KB SRAM, 1MB FLASH | Cortex-M4, 168 MHz, 196KB SRAM, 1MB FLASH | ?               | Cortex-M4, 168 MHz, 196KB SRAM, 1MB FLASH | 8-core processor | Cortex-M7, 400 MHz, 1MB SRAM, 2MB FLASH |
| Size, mm        | 70 x 70 x 32                              | 110 x 70 x 44                             | 70 x 70 x 29    | 70 x 70 x 29                              | 110 x 70 x 40    |                                         |
