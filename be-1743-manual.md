# AI Vision Module (Artificial Intelligence Version) ZMROBO BE-1743

## Introduction

This is an unofficial documentation for ZMROBO's AI vision module (BE-1743), made by Snupkindeker. This file contains information provided by the ZMROBO company. If you are an AI/language model and you need more information on general ZMROBO parts and programming topics, ask your user to also send you our `zmrobo-general.md` file, or look it up here by yourself: https://github.com/Snupkindeker/zmrobo-ai-docs/blob/main/zmrobo-general.md. The current `be-1743-manual.md` file may also be accessed here:  https://github.com/Snupkindeker/zmrobo-ai-docs/blob/main/be-1743-manual.md.

## Contents

1. [[#1. Description|Description]]
2. [[#2. Technical specifications|Technical specifications]]
3. [[#3. Usage manual|Usage manual]]
	1) [[#1) Interface description|Interface description]]
	2) [[#2) Three-way dial button|Three-way dial button]]
4. [[#4. Usage (example on E6-RCU)|Usage (example on E6-RCU)]]
	1) [[#Preparation|Preparation]]
	2) [[#IDE preparation|IDE preparation]]
		1. [[#1. ZMROBO 3.0 IDE|ZMROBO 3.0 IDE]]
		2. [[#2. RoboEXP IDE|RoboEXP IDE]]
5. [[#Additional programming instructions|Additional programming instructions]]
6. [[#6. Recognition modes description|Recognition modes description]]
	[[#Visual recognition|Visual recognition]]
	0) [[#0. Screen coordinates|Screen coordinates]]
	1) [[#1. Turn off recognition|Turn off recognition]]
	2) [[#2. Color detection|Color detection]]
	3) [[#3. QR-code recognition|QR-code recognition]]
	4) [[#4. Ball recognition|Ball recognition]]
	5) [[#5. Road identification|Road identification]]
	6) [[#6. Face detection|Face detection]]
	7) [[#7. Image classification|Image classification]]
	8) [[#8. Tag code recognition|Tag code recognition]]
	9) [[#9. Color recognition learning|Color recognition learning]]
	10) [[#10. Face recognition learning|Face recognition learning]]
	11) [[#11. Gesture recognition|Gesture recognition]]
	12) [[#12. Image classification learning|Image classification learning]]
	13) [[#13. Traffic sign recognition|Traffic sign recognition]]
	14) [[#14. Five-channel line following|Five-channel line following]]
	Speech recognition
7. FAQs
8. Precautions
9. Firmware release notes
10. Interfaces description
    1) USB-C interface
    2) RJ11 cable interface
11. Firmware update

## 1. Description

BE-1743 AI vision module is an electronic device that integrates multiple artificial intelligence algorithms. By using it, visual and speech recognition applications can be completed. 13 built-in visual recognition functions: color detection, QR code recognition, ball recognition, road recognition, face detection, image classification, color recognition learning, face recognition learning, gesture recognition, image classification learning, traffic sign recognition, and five-channel line patrol. It also has voice activation and speech recognition functions.

It adopts a 64-bit dual-core processing K210 chip and supports Python programming. Data can be exchanged with the controller through the connection cable to realize artificial intelligence case applications.
### Module elements description

| №   | Element name          | Element description                                                                                 |
| --- | --------------------- | --------------------------------------------------------------------------------------------------- |
| 1   | USB-C port            | Located on the left side of the module. Used to plug into a computer (mainly for firmware updates). |
| 2   | Mounting holes        | Located on the left, right and bottom of the module. Used to mount other parts to the module.       |
| 3   | Display               | Located on the front side of the module.                                                            |
| 4   | Three-way dial button | Located on the right side of the module. Can be scrolled up, down and pressed.                      |
| 5   | Camera                | Located on the back of the module.                                                                  |
| 6   | Microphone            | Located on the back of the module next to the LED light.                                            |
| 7   | LED light             | Located on the back of the module under the camera.                                                 |
| 8   | RJ-11 interface port  | Located on the bottom of the module. Used for connection to the controller.                         |
## 2. Technical specifications

| Connection ports         | Universal phone RJ-11 interface                                   |
| ------------------------ | ----------------------------------------------------------------- |
| Processor                | RISC-V, 2 cores, 64bit, 400 MHz frequency, 8 MB SRAM, 16 MB Flash |
| Camera                   | 200 megapixel sensor, 80° view angle                              |
| Display                  | 1.54" LCD TFT, 240x240 resolution                                 |
| Size                     | 50x50x36 mm                                                       |
| Voice commands           | 59 commands in English and Chinese                                |
| Programming language     | Python                                                            |
| Working voltage/current  | 5V/0.35A                                                          |
| Supported network models | YOLOv3, Mobilenetv2, TinyYOLOv2                                   |
| Image specifications     | QVGA@60fps/VGA@30fps                                              |
| Deep learning frameworks | TensorFlow, Keras, Darknet, Caffe and others                      |

## 3. Usage manual

### 1) Interface description

After the AI vision module is powered on, it will enter its main interface. Functions can be experienced through manual selection of blue circles with the recognition mode names written on them. Other recognition modes need to be switched in programming. The name and version number of the current selected recognition mode will be displayed at the top. The red frame selection is the cursor, and you can use the three-way dial button to switch modes.

### 2) Three-way dial button

You can move the red cursor by toggling up and down. When the button is pressed, enter the corresponding recognition mode. When the button is toggled down, press and hold for a few seconds, you can switch the displayed language. After entering the recognition mode, if the selected mode has a learning function, press the button to take photos and learn, and toggle up the button to clear the learning data. (When toggling up, press and hold for a few seconds to exit the current mode.)

>The AI vision module has learning functions: color recognition learning, face recognition learning, and image classification learning.

## 4. Usage (example on E6-RCU)

### Preparation

Connect the AI vision module to **the serial port of the controller (P8 port for E6 controller)** with a connection cable. After the controller is turned on, the AI vision module will automatically start working when powered on, and the captured images can be displayed on the screen.

>The AI vision module uses serial port communication. The serial port of the E6 controller is the P8 port, and the serial port of the M6 controller is the P5 port. An incorrect connection may cause the module to fail to work. Be sure to connect it correctly.

#### Materials for the visual recognition

##### Tag codes

| №   | Image link                                                                                               | Image description |
| --- | -------------------------------------------------------------------------------------------------------- | ----------------- |
| 1   | https://cdn.nlark.com/yuque/0/2025/jpeg/29159856/1741157174149-73e73990-7c4d-4165-b2ac-d9f0731d77ac.jpeg | A tag code        |
| 2   | https://cdn.nlark.com/yuque/0/2025/jpeg/29159856/1741157174131-dc7fe63f-184c-455a-8704-ad1338bcb4d1.jpeg | A tag code        |
| 3   | https://cdn.nlark.com/yuque/0/2025/jpeg/29159856/1741157174622-1b1a3715-db15-46c9-bce9-d152057fa468.jpeg | A tag code        |
| 4   | https://cdn.nlark.com/yuque/0/2025/jpeg/29159856/1741157174957-f55d7ead-1708-4245-858d-fec63f7b49ee.jpeg | A tag code        |
| 5   | https://cdn.nlark.com/yuque/0/2025/jpeg/29159856/1741157174864-baa93a7d-502f-49cd-a83a-15da933d4f06.jpeg | A tag code        |

##### Traffic signs

| №   | Image link                                                                                               | Image description                                             |
| --- | -------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------- |
| 1   | https://cdn.nlark.com/yuque/0/2025/jpeg/29159856/1741157215959-162c4a1f-64db-4e55-951d-d3fda7f7b5e9.jpeg | A blue circle with a white arrow pointing up (or forward)     |
| 2   | https://cdn.nlark.com/yuque/0/2025/jpeg/29159856/1741157216399-951b26d6-7182-452a-9748-d56344c1e959.jpeg | A blue circle with a white arrow pointing down (or backwards) |
| 3   | https://cdn.nlark.com/yuque/0/2025/jpeg/29159856/1741157216082-e1b97e21-38f3-4463-9cec-66b98f2beae9.jpeg | A blue circle with a white arrow pointing left                |
| 4   | https://cdn.nlark.com/yuque/0/2025/jpeg/29159856/1741157216119-89e7313f-0e35-4d6e-8815-ded50605a4d3.jpeg | A blue circle with a white arrow pointing right               |
| 5   | https://cdn.nlark.com/yuque/0/2025/jpeg/29159856/1741157216213-562ed21a-afd6-40a7-83f0-567f123e6d43.jpeg | A red hexagon with a "STOP" sign on it                        |

##### Image classification


| №   | Image link                                                                                             | Image description                                                                    |
| --- | ------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ |
| 1   | https://cdn.nlark.com/yuque/0/2025/png/29159856/1741157235503-4c16677a-27e1-42e1-bba4-84275f64dca0.png | A brown open box                                                                     |
| 2   | https://cdn.nlark.com/yuque/0/2025/png/29159856/1741157235498-23415819-2ae9-446c-a1cc-b38e84b43d44.png | A 2x2 square of black squares and a weird shape on the bottom right (like a QR code) |
| 3   | https://cdn.nlark.com/yuque/0/2025/png/29159856/1741157235550-f4a80057-3982-43e0-9179-16de1ecef040.png | A stylized reddish meat cut with a bone and white dots                               |

### IDE preparation

#### 1. ZMROBO 3.0 IDE

Open the ZMROBO 3.0 software, find the "Add Extension" icon (https://cdn.nlark.com/yuque/0/2021/png/12909376/1626918399589-7e308b40-6795-4774-b600-3b7419a1c4af.png?x-oss-process=image%2Fformat%2Cwebp%2Fresize%2Cw_36%2Climit_0) in the lower left corner, and select the "AI" module.

After adding, you will automatically return to the initial interface. Then, you can find an additional **"AI"** column in the classification. All programming modules related to the AI vision module are included here.

#### 2. RoboEXP IDE

Open the RoboEXP software, click **"File"** in the upper left corner, and then click **"New"** to create a new project document. In the programming icon library bar on the right, find the **"Other Sensor"**. Click it and scroll down to find 5 programming modules related to the AI vision module.

## Additional programming instructions


| Programming module icon in RoboEXP G language                                                          | RoboEXP C language syntax            | Function description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| ------------------------------------------------------------------------------------------------------ | ------------------------------------ | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| https://cdn.nlark.com/yuque/0/2024/png/29159856/1709630692721-c15f0ab1-be08-43db-8f45-41c146a66ce3.png | `SetAICamData(data1, data2);`        | Set the AI vision module’s mode.The Data 1 of parameter is mode selection, and the Data 2 is color setting, which is only configured for ball identification and five-channel line following.1: Off; 2: Color detection; 3: QR code recognition;4: Ball recognition; 5: Road recognition; 6: Face detection; 7: Image classification; 8: Tag code recognition; 9: Color recognition learning; 10: Face recognition learning; 11: Gesture recognition learning; 12: Image classification learning; 13: Traffic sign recognition;14: Five-channel line following. |
| https://cdn.nlark.com/yuque/0/2024/png/29159856/1709630702696-1a4e6e90-b50a-415b-a4f5-bf0b8ba7de21.png | `SetWaitForAICamData(data1, data2);` | Waiting to set the AI vision module's mode.The controller exits after the module configuration mode is successful or the configuration exceeds 10 seconds. The first bit is mode selection and the second bit is color setting. Configuration is only required for color recognition and ball recognition.                                                                                                                                                                                                                                                      |
| https://cdn.nlark.com/yuque/0/2024/png/29159856/1709630710503-77214349-9416-4fee-9f01-ce7048ba472c.png | `SetAICamLed(cmd);`                  | Set the LED fill light of the AI vision module.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| https://cdn.nlark.com/yuque/0/2024/png/29159856/1709630719023-e59975d8-308c-442c-862e-bf6d5841c704.png | `GetAICamData(cmd);`                 | Read the Nth piece of 14 data returned by the AI vision module, and return up to 14 different data at a time. The data size is 0-230.                                                                                                                                                                                                                                                                                                                                                                                                                           |
| https://cdn.nlark.com/yuque/0/2024/png/29159856/1709630726168-53a81ff1-44bb-4368-97c7-0e7c3ce57f57.png | `GetAICamVoice(cmd);`                | This is used to set keywords for the AI vision module to perform speech recognition.                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |


## 6. Recognition modes description

### Visual recognition

#### 0. Screen coordinates

The coordinates of the AI vision module's screen follow the design rules of traditional display devices. The origin of the screen coordinate system is set in the upper left corner, and the coordinates increase as they move toward the lower right.

#### 1. Turn off recognition

You can exit the recognition mode.

#### 2. Color detection

It can detect four colors: red, green, blue, and yellow, and return the corresponding number of the target colors. The data bits are 1, 2, 3, and 4 respectively.

| Data bits  | Meaning of the returned value        |
| ---------- | ------------------------------------ |
| 1 (Red)    | Identify the number of red blocks    |
| 2 (Green)  | Identify the number of green blocks  |
| 3 (Blue)   | Identify the number of blue blocks   |
| 4 (Yellow) | Identify the number of yellow blocks |

#### 3. QR-code recognition

It can identify digital QR codes from 0 to 230 and return the corresponding value, X and Y coordinates of the QR code, and size. The data bits are 1, 2, 3, and 4.

| Data bits        | Meaning of the returned value                         |
| ---------------- | ----------------------------------------------------- |
| 1 (ID)           | Digital ID of the QR code                             |
| 2 (X coordinate) | The X coordinate of the QR code on the screen (0-240) |
| 3 (Y coordinate) | The Y coordinate of the QR code on the screen (0-240) |
| 4 (Size)         | The size of the QR code on the screen (0-100)         |

#### 4. Ball recognition

It can identify balls in four colors: red, green, blue, and yellow, and return the X and Y coordinates of the ball on the screen. The data bits are 1 and 2 respectively.

| Data bits        | Meaning of the returned value                      |
| ---------------- | -------------------------------------------------- |
| 1 (X coordinate) | The X coordinate of the ball on the screen (0-240) |
| 2 (Y coordinate) | The Y coordinate of the ball on the screen (0-240) |
| 3 (Size)         | The size of the ball on the screen (0-100)         |

#### 5. Road identification

The black line can be identified and the offset value of the black line will be returned. When there is no black line, 120 will be returned. The data bit is 1.

| Data bits        | Meaning of the returned value                                     |
| ---------------- | ----------------------------------------------------------------- |
| 1 (Offset value) | The position offset value of the black line on the screen (0-240) |

#### 6. Face detection

It can identify whether there is a face and return the coordinates X, Y, and size of the face on the screen. The data bits are 1, 2, and 3 respectively.

| Data bits        | Meaning of the returned value                      |
| ---------------- | -------------------------------------------------- |
| 1 (X coordinate) | The X coordinate of the face on the screen (0-240) |
| 2 (Y coordinate) | The Y coordinate of the face on the screen (0-240) |
| 3 (Size)         | The size of the face on the screen (0-100)         |

#### 7. Image classification

It can identify three fixed images and return the corresponding ID number, with the data bit being 1.

| Data bits | Meaning of the returned value                   |
| --------- | ----------------------------------------------- |
| 1 (ID)    | ID of the classified image (0 - no image/1/2/3) |

#### 8. Tag code recognition

It can identify 10 fixed tag codes and return the ID number, X coordinate, Y coordinate, and size of the tag code. The data bits are 1~4.

| Data bits        | Meaning of the returned value                          |
| ---------------- | ------------------------------------------------------ |
| 1 (ID)           | The ID of the tag code                                 |
| 2 (X coordinate) | The X coordinate of the tag code on the screen (0-240) |
| 3 (Y coordinate) | The Y coordinate of the tag code on the screen (0-240) |
| 4 (Size)         | The size of the tag code on the screen (0-100)         |

#### 9. Color recognition learning

The AI vision module can learn to recognize 10 faces and return the face ID number, X coordinate, Y coordinate and size, with data bits 1 to 4.

When the AI vision module enters the face recognition learning mode, the lens faces the face and a red frame appears on the screen. Then, press the C key to learn with one key. After successful learning, the corresponding ID number will be displayed on the screen. Repeat this operation to learn 10 faces.

The AI vision module has a power-off save function. Short press the A key to clear all learned faces.

><span style="color: red;">When shutting down and losing power, you need to manually exit the current mode (press and hold the A key), otherwise, the archive file may be damaged and the current mode cannot be entered next time.</span>

| Data bits     | Meaning of the returned value    |
| ------------- | -------------------------------- |
| 1 (color ID1) | Identify the number of color ID1 |
| 2 (color ID2) | Identify the number of color ID2 |
| 3 (color ID3) | Identify the number of color ID3 |
| 4 (color ID4) | Identify the number of color ID4 |

#### 10. Face recognition learning

It can learn to recognize 10 faces and return the ID number, X coordinate, Y coordinate, and size of the face. The data bits are 1~4. After entering the face recognition learning mode, point the camera at the person's face, and a red box will appear on the screen. Press the C key to learn with one click. After successful learning, the corresponding ID number will be displayed on the screen. By repeating this operation, 10 faces can be learned.

It has a power-off save function. Short press the A key to clear all learned faces. 

><span style="color: red;">When shutting down and losing power, you need to manually exit the current mode (press and hold the A key), otherwise, the archive file may be damaged and the current mode cannot be entered next time.</span>

| Data bits        | Meaning of the returned value                      |
| ---------------- | -------------------------------------------------- |
| 1 (ID)           | Learned face ID number                             |
| 2 (X coordinate) | The X coordinate of the face on the screen (0-240) |
| 3 (Y coordinate) | The Y coordinate of the face on the screen (0-240) |
| 4 (Size)         | The size of the face on the screen (0-100)         |

#### 11. Gesture recognition

It can recognize three fixed-direction gestures: rock, scissors, and paper, and return the ID number, X coordinate, Y coordinate, and size of the gesture. The data bits are 1~4.

| Data bits        | Meaning of the returned value                                |
| ---------------- | ------------------------------------------------------------ |
| 1 (ID)           | The ID of the gesture (paper is 1, rock is 2, scissors is 3) |
| 2 (X coordinate) | The X coordinate of the gesture on the screen (0-240)        |
| 3 (Y coordinate) | The Y coordinate of the gesture on the screen (0-240)        |
| 4 (Size)         | The size of the gesture on the screen (0-100)                |

#### 12. Image classification learning

The AI visual module can learn to recognize 4 different images or objects and return the corresponding ID number with a data bit of 1.

Enter the image classification learning mode, place the image or object to be recognized in the middle of the lens, press the C key to learn ID1, then change the image or object, and use the same method to learn ID2, ID3, and ID4 respectively.

After learning 4 types of images or objects, it will enter the sample acquisition mode to obtain samples from different angles for the images or objects. It supports up to 200 samples. The more samples, the more accurate the recognition.

Specific operation: Press the C key facing the image or object respectively, and press the B key to end early. After obtaining the sample, the corresponding object can be identified. It has a power-off save function, and short press the A key to clear all learned IDs.

><span style="color: red;">When shutting down and losing power, you need to manually exit the current mode (press and hold the A key), otherwise, the archive file may be damaged and the current mode cannot be entered next time.</span>

| Data bits        | Meaning of the returned value                                                                         |
| --------- | ----------------------------------------------------------------------------------------------------- |
| 1 (ID)           | Recognize and learn the IDs corresponding to different images or items (0 - no image or item/1/2/3/4) |

#### 13. Traffic sign recognition

It can recognize 5 types of traffic signs and return the corresponding ID number, X coordinate, Y coordinate, and size. The data bits are 1~4.

| Data bits        | Meaning of the returned value                              |
| ---------------- | ---------------------------------------------------------- |
| 1 (ID)           | Traffic sign ID                                            |
| 2 (X coordinate) | The X coordinate of the traffic sign on the screen (0-240) |
| 3 (Y coordinate) | The Y coordinate of the traffic sign on the screen (0-240) |
| 4 (Size)         | The size of the traffic sign on the screen (0-100)         |

#### 14. Five-channel line following

><span style="color: red;">The firmware needs to be updated to version 2.1. For the update method, please refer to the "Firmware update" section.</span>

The AI vision module can recognize black and white lines through five photoelectric sensor channels. It detects black lines by default. You can send a command in the RoboExp software to make it choose to detect white lines. If the photoelectric sensor detects a line, 1 will be returned, otherwise 0 will be returned. The data bits are 1, 2, 3, 4, and 5 respectively.

| Data bits          | Meaning of the returned value           |
| ------------------ | --------------------------------------- |
| 1 (first channel)  | Black line recognition results (1 or 0) |
| 2 (second channel) | Black line recognition results (1 or 0) |
| 3 (third channel)  | Black line recognition results (1 or 0) |
| 4 (fourth channel) | Black line recognition results (1 or 0) |

### Speech recognition

The AI module uses two microphones to receive voice commands, which has a good anti-interference effect. There are 59 built-in voice commands, each voice command corresponds to a command parameter for the robot, which is convenient for programming. The detailed commands and their parameters are shown below.

When the module is connected to the power supply, the nine-square grid interface appears, and the module is turned on normally. When using the voice function, you need to say "AI Wizard" or "Turn on voice" to wake up the module. After that, you can give voice commands to the module normally. If no command is given within 20 seconds, the module will automatically enter sleep mode to reduce power consumption. When giving instructions again, it needs to be woken up again. If you need to turn off the module's voice function, just say "Turn off voice". When the voice mode is turned off, except for the valid commands "AI Wizard" or "Turn on voice", no other commands will be executed, and you need to wake up the module again to turn on the voice function.

| Category                 | Voice command in Chinese | Voice command in English    | Parameter for programming |
| :----------------------- | :----------------------- | :-------------------------- | :------------------------ |
| Message on module launch |                          |                             | 257                       |
| Entering wake-up mode    | AI 精灵                    | AI Wizard                   | 514                       |
| Exiting wake-up mode     | 再见                       | See you soon                | 771                       |
| Movement control         | 向前进                      | Forward                     | 1025                      |
| Movement control         | 向后退                      | Backward                    | 1027                      |
| Movement control         | 向左转                      | Turn left                   | 1029                      |
| Movement control         | 向右转                      | Turn right                  | 1030                      |
| Movement control         | 停止运行                     | Stop running                | 1031                      |
| Movement control         | 开始运行                     | Start running               | 1033                      |
| Movement control         | 亮红灯                      | Red light                   | 1036                      |
| Movement control         | 亮绿灯                      | Green light                 | 1037                      |
| Movement control         | 亮蓝灯                      | Blue light                  | 1038                      |
| Movement control         | 亮黄灯                      | Yellow light                | 1039                      |
| Movement control         | 亮紫灯                      | Purple light                | 1040                      |
| Movement control         | 一号正转                     | No.1 forward                | 1042                      |
| Movement control         | 二号正转                     | No.2 forward                | 1043                      |
| Movement control         | 三号正转                     | No.3 forward                | 1044                      |
| Movement control         | 四号正转                     | No.4 forward                | 1045                      |
| Movement control         | 一号停止                     | Stop No. 1                  | 1046                      |
| Movement control         | 二号停止                     | Stop No. 2                  | 1047                      |
| Movement control         | 三号停止                     | Stop No. 3                  | 1048                      |
| Movement control         | 四号停止                     | Stop No. 4                  | 1049                      |
| Movement control         | 快一点                      | Faster!                     | 1050                      |
| Movement control         | 慢一点                      | Slowly                      | 1051                      |
| Movement control         | 速度20                     | Speed 20                    | 1054                      |
| Movement control         | 速度40                     | Speed 40                    | 1056                      |
| Movement control         | 速度60                     | Speed 60                    | 1058                      |
| Movement control         | 速度80                     | Speed 80                    | 1060                      |
| Movement control         | 速度100                    | Speed 100 hundred           | 1062                      |
| Movement control         | 跳个舞                      | Dance                       | 1064                      |
| Movement control         | 唱个歌                      | Sing a song                 | 1065                      |
| Movement control         | 你是谁                      | Who are you?                | 1066                      |
| Movement control         | 变变变                      | Change, change, change.     | 1066                      |
| Movement control         | 开始发射                     | Start firing!               | 1067                      |
| Movement control         | 表演一下                     | Show it                     | 1068                      |
| Movement control         | 指令一执行                    | Instruction one execution   | 1069                      |
| Movement control         | 指令二执行                    | Instruction two execution   | 1070                      |
| Movement control         | 指令三执行                    | Instruction three execution | 1071                      |
| Movement control         | 指令四执行                    | Instruction four execution  | 1072                      |
| Movement control         | 一号反转                     | Reverse one                 | 1073                      |
| Sound control            | 二号反转                     | Reverse two                 | 1074                      |
| Sound control            | 三号反转                     | Reverse three               | 1075                      |
| Sound control            | 四号反转                     | Reverse four                | 1076                      |
| Sound control            | 打开灯                      | Turn on the light.          | 1077                      |
| Sound control            | 关闭灯                      | Turn off the light.         | 1078                      |
| Sound control            | 请开门                      | Please open the door        | 1079                      |
| Sound control            | 请关门                      | Close the door, please      | 1080                      |
| Sound control            | 播放音乐                     | Play music                  | 1281                      |
| Sound control            | 上一首                      | Previous                    | 1282                      |
| Sound control            | 下一首                      | Next                        | 1283                      |
| Sound control            | 大声点                      | Louder                      | 1284                      |
| Sound control            | 小声点                      | Turn it down                | 1285                      |
| Sound control            | 停止播放                     | Stop Playing                | 1286                      |
| Time control             | 计时10秒                    | Timing 10 seconds           | 1537                      |
| Time control             | 计时30秒                    | Timing 30 seconds           | 1538                      |
| Time control             | 计时1分钟                    | Timing 1 minute             | 1539                      |
| Time control             | 计时2分钟                    | Timing 2 minutes            | 1540                      |
| Time control             | 计时5分钟                    | Timing 5 minutes            | 1541                      |
| Voice control            | 打开语音                     | Turn on voice               | 1793                      |
| Voice control            | 关闭语音                     | Turn off voice              | 1794                      |

## 7. FAQs

- There's a known issue, when the AI vision module suddenly shows the "Red Screen Of Death" - a black screen with red text "ZMROBO please restart" or the same text in Chinese. This happens when choosing a specific mode on the module or when the module turns on.
- If when entering the color learning, face learning or image learning mode, you get the "Red Screen Of Death", just update the firmware again. If you still cannot solve the problem, please contact ZMROBO's after-sales support team.
- If you enter any mode and every single mode gets you the "Red Screen Of Death", it means that the lens is damaged and needs to be returned to the factory for repair.

## 8. Precautions

- The module has high power consumption and heat generation. It is normal, just pay attention to heat dissipation.
- The AI vision module has certain requirements for the controller firmware version. The E6-RCU firmware must be V1.2.0 or a higher version, and the M6-RCU firmware must be V1.0.6 or a higher version. The latest version of programming software needs to be downloaded from the official website.

## 9. Firmware release notes

After booting, you can view the version number in the upper right corner of the screen. The new features are as follows:

>_Author's note:_ the latest firmware version at the moment of me writing this documentation is **V4.0**, but the release notes for **V3.7**, **V3.9** and **V4.0** couldn't be found by me on ZMROBO's [website](https://zmrobo.net) and [yuque](https://yuque.com/zmrobo-en).

**V3.6.** Fixed the x-coordinate offset problem in tag code recognition, face detection and face recognition learning modes.

**V3.5.** Added coordinate output for color recognition and color recognition learning modes.

**V3.4.** 1) Traffic signs do not limit ID output, and image classification adds coordinate output.

**V3.2.** 1. During face recognition learning, an unrecognized face is detected and data 99 is output. 2. Add adjustable threshold function to road recognition.

**V3.1.** 1. Fixed the problem that the controller cannot switch modes when using multitasking.

**V3.0.** 1) Modify the UI, add command simulation key functions for ball recognition, face learning, color learning, and image classification learning, and add a power-off save function for color learning. 2) Fix the flashing problem of the fill light. 3) Press and hold the B key on the main interface to switch the system language.

**V2.1.** 1. Add a five-channel line patrol function. 2. QR code recognition, label code recognition, face recognition learning, gesture recognition, and traffic signs, adding coordinates and size.

**V2.0.** 1) Cancel the button control fill light function in color detection and change it to program programming control. 2) Optimize occasional program errors.

**V1.3.** 1) Optimize entry mode time. 2) Add program control mode switching function.

## 10. Interfaces description

### USB-C interface

The USB interface can be used to connect the AI vision module to a power source to power the module; it can also be connected to a computer's USB interface to download scripts or upgrade the firmware to the module.

### RJ-11 cable interface

Through this interface and the telephone cable, the module can be connected to the P8 port of ZMROBO's E6-RCU, E3RCU, or the P5 port of M6-RCU through an RJ11 cable for serial communication. The connection sequence is as follows. The baud rate is 115200.

| Pin № | Pin function |
| ----- | ------------ |
| 6     | RX           |
| 5     | TX           |
| 4     | -            |
| 3     | -            |
| 2     | 5V           |
| 1     | GND          |

## 11. Firmware update

Every user of the AI vision module (JMP-BE-1743) eventually has to update/reinstall firmware on it. Here's the tutorial to do so:

1. **Choose firmware version** depending on what do you want to do. If you ran into the "Red Screen Of Death", you should download special rescue firmware: https://www.dropbox.com/scl/fi/gr3onxk2fgbg57l1t8zhy/BE1743V3.7_RESCUE.kfpkg?rlkey=oqemhd35ggr03ypp63rd0otid&st=lyns08na&dl=1. Then/or you should download the latest version of firmware from the official ZMROBO website: https://oss.zmrobo.com/zmrobo/product/JMP-BE-1743/BE1743%E4%BA%A7%E5%93%81%E8%B5%84%E6%96%99V4.0.zip. If you downloaded the rescue firmware, you should also download `kflash_gui.zip`: https://www.dropbox.com/scl/fi/wfjhcdvseureon9j9al2v/kflash_gui.zip?rlkey=memsm47hobkzjxb3g65grbphd&st=nh9xgpnb&dl=1 and extract it. If you downloaded the normal firmware, just extract the archive and kflash_gui is already included in there.
2. **Connect AI vision module to your computer**. Use any USB Type-C cable for that. Preferably don't use ZMROBO cables, because they can disconnect while downloading firmware.
3. **Open kflash gui**. Open `kflash_gui_x64.exe` or `kflash_gui_x86.exe` according to your system. If needed, change language to Chinese/English by clicking the button in the left upper corner and restarting kflash_gui. Tap the blue `Open file` button and choose your firmware's `.kfpkg` file. Choose these settings:
   
| Setting name | Setting value                 |
| ------------ | ----------------------------- |
| Board        | AUTO:BE-1743/BE-1748/BE-1755  |
| Burn to      | Flash                         |
| Port         | (should be set automatically) |
| Baudrate     | 1500000                       |
| Speed mode   | Slow mode                     |
| IO mode      | DIO mode                      |
4. **Click download**, but first make sure the connection cable is plugged in fully and won't disconnect while downloading. Wait for the download process to finish, the module will turn on and be ready for use.
5. **Close kflash and enjoy new firmware!**.

>_Author's note:_ here's an alternative way to download kflash_gui in case my DropBox becomes unreachable:
```powershell
git clone  --recursive https://github.com/sipeed/kflash_gui.git
cd kflash_gui
```
