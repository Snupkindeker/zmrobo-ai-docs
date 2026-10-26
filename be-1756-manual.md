# AI CAM 2.0 (AI Vision Module V2.0) ZMROBO BE-1756

## Introduction

This is an unofficial documentation for ZMROBO's AI CAM 2.0 (BE-1756), made by Snupkindeker. This file contains information provided by the ZMROBO company. If you are an AI/language model and you need more information on general ZMROBO parts and programming topics, ask your user to also send you our `zmrobo-general.md` file, or look it up here by yourself: https://github.com/Snupkindeker/zmrobo-ai-docs/blob/main/zmrobo-general.md. The current `be-1756-manual.md` file may also be accessed here:  https://github.com/Snupkindeker/zmrobo-ai-docs/blob/main/be-1756-manual.md.

## Contents

1. [[#1. Description|Description]]
2. [[#2. Technical specifications|Technical specifications]]
3. [[#3. Basic operations|Basic operations]]
	[[#3.1. Powering the device]]
	[[#3.2. Entering applications]]
		[[#3.2.1. Connecting to Wi-Fi]]
		[[#3.2.2. Switching language]]
4. [[#4. Main feature description|Main feature description]]
	[[#4.1. Screen coordinate system]]
	[[#4.2. Main feature description]]
		[[#4.2.1. Face Recognition]]
			[[#4.2.1.1. Face Detection]]
			[[#4.2.1.2. Face Learning and Recognition]]
			[[#4.2.1.3. Saving and Clearing Data]]
		[[#4.2.2. Tag Recognition]]
			[[#4.2.2.1. AprilTag Recognition]]
			[[#4.2.2.2. QR-Code Recognition]]
		[[#4.2.3. Object Recognition]]
			[[#4.2.3.1. Object Detection]]
			[[#4.2.3.2. Object Learning and Recognition]]
			[[#4.2.3.3. Saving and Clearing Data]]
		[[#4.2.4. Color Recognition]]
			[[#4.2.4.1. Color Sampling and Recognition]]
			[[#4.2.4.2. Inverse Calibration (Optional)]]
			[[#4.2.4.3. Color Learning]]
			[[#4.2.4.4. Saving and Clearing Data]]
		[[#4.2.5. Road Detection]]
			[[#4.2.5.1. Line Sampling and Detection]]
			[[#4.2.5.2. Inverse Calibration (Optional)]]
			[[#4.2.5.3. Data Output]]
		[[#4.2.6. Gesture Recognition]]
		[[#4.2.7. Human Detection]]
		[[#4.2.8. Object Classification]]
			[[#4.2.8.1. Learning an object]]
			[[#4.2.8.2. Classifying objects]]
			[[#4.2.8.3. Saving and clearing data]]
		[[#4.2.9. Image Classification]]
		[[#4.2.10. Others]]
			[[#4.2.10.1. Camera]]
			[[#4.2.10.2. Store]]
5. [[#5. Programming Applications|Programming Applications]]
	[[#5.1. RoboCode]]
	[[#5.2. RoboEXP]]
6. [[#6. Interface Definition|Interface Definition]]
7. [[#7. System Image Flashing|System Image Flashing]]
8. [[#8. Notes|Notes]]

## 1. Description

**AI CAM** is a high-performance AI terminal designed for education and robotics enthusiasts. With powerful AI computing capability, it can directly run advanced lightweight models to perform real-time object detection and recognition. It comes with a variety of built-in pre-trained AI models, supporting color recognition, object tracking, face recognition, and tag detection. Users can switch between recognition algorithms with a single click through the graphical interface, significantly lowering the barrier to AI application development.

### Module elements description

| №   | Element name     | Description                                                                                                                                                                                                                            |
| --- | ---------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 1   | User button      | Located at the top of the module. Short-press to confirm a capture action or complete a learning operation.                                                                                                                            |
| 2   | Microphone       | Located on the back side. Captures voice input. Pointing toward the microphone improves recognition efficiency during speech recognition tasks.                                                                                        |
| 3   | Camera           | Located on the back side. Used for image acquisition and visual recognition.                                                                                                                                                           |
| 4   | Reset button     | Located at the top of the module, next to the User button. Short-press to reboot the system; its function is equivalent to powering off and on again.                                                                                  |
| 5   | Screen           | Covers the module's front side. Displays the operation interface and supports touch interaction.                                                                                                                                       |
| 6   | Mouting holes    | Located on the bottom of the module. Compatible with 10 mm modular building blocks for installation or integration into robot structures.                                                                                              |
| 7   | 6-pin port       | Located on the left side of the module. Connects to other devices (e.g., controllers) for data transmission and control.                                                                                                               |
| 8   | TF card slot     | Located on the right side of the module, above the Type-C port. Insert a TF card (SD-card) to load AI CAM system files or to expand storage.                                                                                           |
| 9   | Power indicator  | Located below the status indicator, above the Type-C port. Shows the power status of AI CAM; green indicates a normal power supply.                                                                                                    |
| 10  | Status indicator | Located above the power indicator, below the TF card slot. Indicates the operating status of the AI CAM system. A **flashing blue light** means data is being transmitted, while a **solid blue light** indicates a system data error. |
| 11  | Type-C port      | Located on the right side, below the power indicator. Used for power supply or data transfer, and can also be used to update the AI vision module firmware.                                                                            |

## 2. Technical specifications


| Item                     | Specification/Description                                                                                                                   |
| ------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------- |
| CPU, NPU, RAM            | **Core 1**: 1 GHz RISC-V C906 / ARM A53<br>**Core 2**: 700 MHz RISC-V C906<br>**NPU**: 1 TOPS INT8 (BF16 supported)<br>**RAM**: 256 MB DDR3 |
| Operating system         | Linux                                                                                                                                       |
| AI Inference Performance | YOLO11n (640x640): 23 FPS                                                                                                                   |
| Video codec              | H.264 / H.265 / MJPEG hardware decoding, supports 2K@30fps encoding/decoding                                                                |
| Camera                   | 2 MP, 90° FOV                                                                                                                               |
| Display                  | 2.4-inch capacitive multi-touch screen, 480×640 resolution                                                                                  |
| Storage expansion        | Supports TF card (32 GB included)                                                                                                           |
| Wireless connections     | Wi-Fi 6 (2.4G + 5G dual-band), Bluetooth 5.4                                                                                                |
| Wired interfaces         | **Type-C USB 2.0** (supports power supply, Device/Host mode, USB camera), **PH 1.25 mm 6-pin serial port**                                  |
| Sensors                  | 6-axis gyroscope, analog microphone, 1× user button, 1× reset button                                                                        |
| Indicators               | Power indicator, system status indicator                                                                                                    |
| Power Supply             | Operating voltage: 4.5–5 V. Operating current: ≥200 mA, recommended power supply: ≥5V 500mA.                                                |
| RTC                      | Onboard BM8653 RTC + coin-cell battery (backup timekeeping when powered off)                                                                |
| Size                     | 20mm × 70mm × 63mm                                                                                                                          |
| Supported controllers*   | E7-RCU, E6-RCU, M6-RCU                                                                                                                      |
>**Author's note**: the supported controller list is based on the author's own experience, may be inaccurate.

## 3. Basic operations

### 3.1. Powering the device

AI CAM can be powered through either the **6-Pin port** or the **Type-C port**. The required power specification is ≥5V 500mA. Once connected to a power source, the device will boot up and display the function interface. The first boot may take longer than usual; please wait patiently.

If the device fails to start, please check whether the **TF card** is inserted correctly. Since the operating system is installed on the TF card, the device cannot boot without it.

> **Note**: The **6-Pin port** uses serial communication (UART). To enable data transmission, it must be connected to the serial port of a controller (e.g., the P7 or P8 port of the E7 controller). Otherwise, it will function only as a power supply.

### 3.2. Entering applications

After powering on, the functions of AI CAM are presented in the form of applications. You can operate it just like using apps on a smartphone. Swipe on the screen to browse all available applications, and tap to open one. The following examples illustrate the basic operation methods using two common functions:

### 3.2.1. Connecting to Wi-Fi

Find and tap the **“Settings”** application on the interface. In the Settings menu, select **“Wi-Fi”**. Choose the target Wi-Fi network from the available list.

Enter the password, then tap ✅ to confirm. A prompt will appear when the connection is successful. You can also check the network status via **“Device Info”**, where the WLAN IP address will be displayed. To return to the previous page, tap the ◀ icon in the upper-left corner.

### 3.2.2. Switching language

Locate and tap the **“Settings”** application. In the Settings menu, select **“Language”**. Choose the desired language. The system currently supports **Simplified Chinese** and **English**.

## 4. Main feature description

The module supports a wide range of AI vision capabilities, including face/body/gesture recognition, object detection and classification, QR code/tag recognition, color detection, road detection, and image classification.

### 4.1. Screen coordinate system

The screen coordinate system follows standard conventions: The origin (0, 0) is located at the top-left corner of the screen. The X-axis increases horizontally to the right, and the Y-axis increases vertically downward. X-axis range: **0–639**, Y-axis range: **0–479.**

### 4.2. Main feature description

#### 4.2.1. Face Recognition

The module can detect, learn, and recognize multiple faces.

##### 4.2.1.1. Face Detection

In **Face Recognition** mode, the screen displays the camera feed in real time. When a face is detected, a **white bounding box** automatically appears around it for precise indication.

##### 4.2.1.2. Face Learning and Recognition

Point the camera toward the face to be learned and ensure the **crosshair** at the center of the screen is aligned within the white bounding box. Press the **User Button** to start the learning process. The module will automatically learn the face.

After learning is completed:
 - If a learned face is recognized, the bounding box will turn **colored** (e.g., orange, blue).
 - The **ID number** will appear at the upper-left corner of the box. (The ID corresponds to the learning order: the first learned face is **ID1**, the second is **ID2**, and so on.)
You may continue learning additional faces in the same way. The module supports up to **20 different faces.**

If multiple faces are recognized simultaneously:
 - The face located **furthest to the left** is considered Target 1.
 - The next face to the right is Target 2, and so on.

##### 4.2.1.3. Saving and Clearing Data

Tap the *function icon* at the bottom-left corner of the screen to open the menu containing **Save** and **Clear** options.
 - **Save**: Stores the learned face data. If you exit Face Recognition mode without saving, all learned data will be automatically cleared.
 - **Clear**: Deletes all learned face data.

#### 4.2.2. Tag Recognition

The AI CAM can recognize both AprilTag markers and QR codes.

##### 4.2.2.1. AprilTag Recognition

In the **"Tag Recognition"** mode, the system supports identifying AprilTag markers of the **TAG36H11** family, with a valid ID range of **0–255**.

> **AprilTag** is a visual fiducial system widely used in robot localization, drone navigation, and camera calibration. It uses special markers similar to QR codes but with a simpler structure to ensure real-time performance.
> 
> According to encoding structure and data capacity, AprilTag markers come in various families, including: **TAG16H5**, **TAG25H7**, **TAG25H9**, **TAG36H10**, **TAG36H11**, and **ARTOOLKIT**, etc.
> 
> AprilTag online generator: [https://chev.me/arucogen/](https://chev.me/arucogen/)
> *(Select the TAG36H11 family when generating tags.)*

##### 4.2.2.2. QR-Code Recognition

In the **"QR Code"** mode, the system can recognize QR codes containing numbers, letters, and Chinese characters.

#### 4.2.3. Object Recognition

The AI CAM can recognize **80 predefined object categories**, including humans, animals, vehicles, outdoor facilities, daily items, and food. To recognize any learnt object, use [[#4.2.8. Object Classification|Object Classification]].

Supported object classes are listed below (based on the COCO dataset):


| Supercategory       | Object Classes                                                                                                                          |
| ------------------- | --------------------------------------------------------------------------------------------------------------------------------------- |
| Person / Human body | person                                                                                                                                  |
| Vehicles            | bicycle, car, motorcycle, airplane, bus, train, truck, boat                                                                             |
| Outdoor facilities  | traffic light, fire hydrant, stop sign, parking meter, bench                                                                            |
| Animals             | bird, cat, dog, horse, sheep, cow, elephant, bear, zebra, giraffe                                                                       |
| Personal items      | backpack, umbrella, handbag, tie, suitcase                                                                                              |
| Sports equipment    | frisbee, skis, snowboard, sports ball, kite, baseball bat, baseball glove, skateboard, surfboard, tennis racket                         |
| Kitchenware & food  | - bottle, wine glass, cup, fork, knife, spoon, bowl<br>- banana, apple, sandwich, orange, broccoli, carrot, hot dog, pizza, donut, cake |
| Furniture           | chair, couch, potted plant, bed, dining table, toilet, TV                                                                               |
| Electronics         | laptop, mouse, remote, keyboard, cell phone                                                                                             |
| Home appliances     | microwave, oven, toaster, sink, refrigerator                                                                                            |
| Indoor items        | book, clock, vase, scissors, teddy bear, hair dryer, toothbrush                                                                         |

##### 4.2.3.1. Object Detection

In **Object Recognition** mode, when a detectable object appears in view, the module will automatically generate a white bounding box around it.

> **Note**: For optimal recognition performance, choose objects with distinctive features and clear textures, and place them against a light-colored, uncluttered background during learning and recognition.

##### 4.2.3.2. Object Learning and Recognition

Point the camera at the object you want to learn and ensure the crosshair at the center of the screen is positioned within the white bounding box. Then press the User Button, and the module will automatically learn the object.

After learning is completed, if the AI CAM recognizes the learned object, the bounding box will turn into a colored box (e.g., orange or blue), and an **ID number** will be displayed at the upper-left corner of the box. The module assigns a unique ID to each object based on the learning order, and **the same category of object cannot be learned more than once**.

From a technical perspective, object learning is essentially the process of assigning an ID number to the specified object.

##### 4.2.3.3. Saving and Clearing Data

Tap the function icon located at the bottom-left corner, and the **Save** and **Clear** icons will appear.

 - Tapping **Save** stores the learned object data.
 - If you do not save the data, it will be automatically cleared when exiting the Object Recognition mode.
 - Tapping **Clear** removes all learned object data.

#### 4.2.4. Color Recognition

The module can learn and recognize up to 20 different colors.

##### 4.2.4.1. Color Sampling and Recognition

Place the target color in the center area of the screen. Select any three different positions within the target color region and tap them in sequence. Each tapped position will be marked as a **"sampling point."** The module will automatically outline the color region based on the sampling points and generate the corresponding LAB color values.

>**LAB Color Space**
>
> - **L (Lightness)**: Indicates the brightness level, ranging from black (0) to white (100).
> - **A (Green–Red Axis)**: Negative values indicate green; positive values indicate red. Range: –127 to 127.
> - **B (Blue–Yellow Axis)**: Negative values indicate blue; positive values indicate yellow. Range: –127 to 127.
>
>LAB is a color space designed to better match human visual perception. Its key advantage is that the L component is independent from the color components (A and B). Therefore, adjusting the L value mainly affects brightness without significantly altering the color tone itself, making color calibration more intuitive and accurate.

##### 4.2.4.2. Inverse Calibration (Optional)

Tap the **"eye" icon** in the upper-right corner of the screen to enable **image inversion**. Then tap the corresponding **LAB threshold values** (L Min, L Max, A Min, A Max, B Min, B Max), and adjust the sliders on the right. Fine-tune the thresholds until the **target region appears in pure white**, ensuring optimal recognition accuracy.

##### 4.2.4.3. Color Learning

Point the camera at the target color and ensure that the **crosshair at the center** of the screen is positioned inside the white bounding box. Press the **User Button** to start learning the color.

After learning, if the system recognizes a previously learned color, the bounding box will turn colored (e.g., orange or blue), and the **ID number** will appear at the upper-left corner of the bounding box.

(The module assigns ID numbers based on the learning order. To avoid conflicts, **do not learn the same color category more than once**.)

##### 4.2.4.4. Saving and Clearing Data

Tap the function icon in the lower-left corner to open the menu containing **"Save"** and **"Clear"**.

 - **Save** – Stores all learned color data. If data is not saved, it will be **automatically cleared** upon exiting the Color Recognition mode.
 - **Clear** – Deletes all learned color data.

#### 4.2.5. Road Detection

Used for detecting a single guiding line on a solid-color background, suitable for basic line-following applications. This mode does not support multi-line paths, intersections, or other complex map layouts.

##### 4.2.5.1. Line Sampling and Detection

Point the camera at the line and keep an appropriate distance (not too far). Ensure that the guiding line is positioned near the center of the screen. Tap three different positions on the line to sample; each tap will display a sampling point. Based on the sampling points, the module will mark the detected line direction with a green segment and generate the corresponding LAB color values.

##### 4.2.5.2. Inverse Calibration (Optional)

If the detected line direction deviates significantly, tap the **“eye” icon** in the upper-right corner to invert the image. Then readjust the sampling points (you may also adjust the distance between the camera and the line) until the detected direction becomes accurate.

##### 4.2.5.3. Data Output

The module outputs the X-coordinate data of the upper endpoint (first target) and the lower endpoint (second target) of the green line segment in real time (only in this app, other apps index targets from left to right).

#### 4.2.6. Gesture Recognition

The module can recognize six predefined static gestures (supports both left and right hands).

The recognizable gestures are shown in the image below.

>**Author's note**: here's the gesture description:
>ID1. Paper from "rock, paper, scissors": all fingers are straight.
>ID2. Rock from "rock, paper, scissors": a fist, all fingers are curled.
>ID3. Scissors from "rock, paper, scissors": only the index and middle fingers are straight.
>ID4. The "OK" gesture: the index finger making a ring with the thumb.
>ID5. The "Thumbs up" or "Like" gesture.
>ID6. Index, middle and pinky fingers are curled.

When a gesture is detected, a colored bounding box will appear around the gesture, and the ID number will be displayed at the top-left corner of the box.

##### 4.2.7. Human Detection

The module can detect and label 17 keypoints of the human body and output their corresponding coordinates.

>**Human body keypoints include**:
>
> - **Head**: nose, left/right eye, left/right ear
> - **Upper limbs**: left/right shoulder, left/right elbow, left/right wrist
> - **Torso & lower limbs**: left/right hip, left/right knee, left/right ankle

When a human body is detected, the module will dynamically annotate these keypoints on the image.


| ID  | Keypoint       |
| --- | -------------- |
| 1   | Nose           |
| 2   | Left Eye       |
| 3   | Right Eye      |
| 4   | Left Ear       |
| 5   | Right Ear      |
| 6   | Left Shoulder  |
| 7   | Right shoulder |
| 8   | Left Elbow     |
| 9   | Right Elbow    |
| 10  | Left Wrist     |
| 11  | Right Wrist    |
| 12  | Left Hip       |
| 13  | Right Hip      |
| 14  | Left Knee      |
| 15  | Right Knee     |
| 16  | Left Ankle     |
| 17  | Right Ankle    |

Use `GetAICamStr(..);` and `GetAICamIDStr(..);` to read the values from this app.

#### 4.2.8. Object Classification

The module can learn up to five objects or patterns as predefined categories. During recognition, detected targets will be classified into the corresponding category.

##### 4.2.8.1. Learning an object

Select the target ID number at the bottom of the screen (options: ID1–ID5), then point the camera at the object to be learned.

Press and hold the user button, and move the camera around the object from different angles. When the screen displays *“ID (number) learned”*, the learning process is complete.

To learn another object, repeat the steps above and select a different ID.

##### 4.2.8.2. Classifying objects

When a learned object is recognized, a colored bounding box will appear on the screen, and the corresponding ID number will be shown at the top-left corner of the box.

##### 4.2.8.3. Saving and clearing data

Tap the function icon at the bottom-left corner, and two options will appear: **Save** and **Clear**.

 - **Save**: Stores the learned data for the selected ID. If data is not saved, it will be cleared automatically when exiting the Object Classification mode.
 - **Clear**: Deletes the learned data for the selected ID. After clearing, you can relearn the object.

#### 4.2.9. Image Classification

The module can recognize **11 predefined patterns** (officially provided).

> **Author's note**: here's the download link for the recognizable images: https://zmrobo.top/yuque/Electronic_Hardware/AI_CAM/Image%20Classification%20Cards.zip.

#### 4.2.10. Others

##### 4.2.10.1. Camera

You can capture real-time photos or record videos and save them to the album. Photos and videos can be transferred to a computer; this requires firmware version v4.12.5 or later, or you can scan the QR-code below to install the latest version of the camera app.

>**Author's note**: here's the QR-code image link: https://cdn.nlark.com/yuque/0/2026/png/29159856/1791428789291-63c910e0-ec1e-4de3-8af0-eb73a0cb9f6d.png
>
>Direct link: https://asset-zmrobo.oss-cn-zhangjiakou.aliyuncs.com/temp/BE1756/%E6%8B%93%E5%B1%95%E5%8A%9F%E8%83%BD/zm_camera-v1.0.0.zip
>
>Use [wlan0](http://10.168.0.120:8080/) to transfer files for wireless connections and [usb0](http://10.111.96.1:8080/)/[usb1](http://10.111.95.1:8080/) for wired connections.

##### 4.2.10.2. Store

You can uninstall or install functional applications (such as Face Recognition, Color Recognition, etc.) to update or extend available features.

###### 1) Install an App by Scanning a QR-Code
Tap “Scan to Install” to open the scanning screen, then scan the QR-code for the specified app.

After installation, the newly installed app can be found at the bottom of the app list.

###### 2) Uninstall an App

To update a feature, you need to uninstall its app first.

## 5. Programming Applications

### 5.1. RoboCode

After opening the software, **create a new work** → **Hardware mode** → select **E7-RCU** → Confirm to enter the hardware programming interface.

Click the "Add Extension" icon in the lower-left corner of the programming interface. In the More Extensions page, select and add the **AI CAM** extension.

Then, return to the programming interface, and you will see a new category named **"AI CAM"**. This category contains all programming blocks related to the AI vision module.

### 5.2. RoboEXP

| G icon name                       | C syntax                                                 | Description                                                                                                                                                                                                                                                                   | Parameters                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| --------------------------------- | -------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Set AICAM Mode (icon with wrench) | `SetAICam(_PORT_ which, uint8_t cmd);`                   | Set the AI Vision Module to a Specified Recognition Mode. Execute this block **after the AI module has fully powered on**.                                                                                                                                                    | **which**: Port (\_P5\_ for M6-RCU, \_P8\_ for E6-RCU, \_P7\_ and \_P8\_ for E7-RCU).<br>**cmd**: Mode index (1–11), corresponding to:<br>1. Camera<br>2. Face Recognition<br>3. AprilTag Recognition<br>4. QR Code Recognition<br>5. Object Detection<br>6. Color Recognition<br>7. Road Recognition<br>8. Gesture Recognition<br>9. Human Keypoint Detection<br>10. Object Classification<br>11. Image Classification                                                 |
| Set AICAM Mode (icon with "ABC")  | `SetAICamCmd(_PORT_ which, string cmd);`                 | Set the AI CAM to a specified recognition mode. Execute this module **after the AI CAM has started up**.                                                                                                                                                                      | **which**: Port (\_P5\_ for M6-RCU, \_P8\_ for E6-RCU, \_P7\_ and \_P8\_ for E7-RCU).<br>**cmd**: *(Enter an English string)* Switch function: camera, face recognition (`face`), AprilTag recognition (`apriltag`), object recognition (`detector`), color recognition (`color`), road recognition (`road`), gesture recognition (`gesture`), human recognition (`human`), object classification (`classifier`), image classification (`image`), or a custom function. |
| Wait to set AICAM Mode            | `SetWaitAICamCmd(_PORT_ which, string cmd);`             | Wait for the AI CAM to start up and switch to the specified recognition algorithm before continuing program execution. (Blocking)                                                                                                                                             | **which**: Port (\_P5\_ for M6-RCU, \_P8\_ for E6-RCU, \_P7\_ and \_P8\_ for E7-RCU).<br>**cmd**: *(Enter an English string)* Switch function: camera, face recognition (`face`), AprilTag recognition (`apriltag`), object recognition (`detector`), color recognition (`color`), road recognition (`road`), gesture recognition (`gesture`), human recognition (`human`), object classification (`classifier`), image classification (`image`), or a custom function. |
| Read AICAM data                   | `GetAICam(_PORT_ which, uint8_t target, uint8_t cmd);`   | Get the **data** of the target recognized by the AI CAM                                                                                                                                                                                                                       | **which**: Port (\_P5\_ for M6-RCU, \_P8\_ for E6-RCU, \_P7\_ and \_P8\_ for E7-RCU).<br>**target**: Target index (1–20); targets on screen are indexed **from left to right**.<br>**cmd**: Data field (1–7), representing:<br>1. ID<br>2. X coordinate<br>3. Y coordinate<br>4. Width<br>5. Height<br>6. Size<br>7. Confidence                                                                                                                                         |
| Read AICAM target name            | `GetAICamStr(_PORT_ which, uint8_t target);`             | Get the **name** of a target recognized by the AI CAM.<br><br>Some functions return the name of the recognized object. This module can be used for functions such as QR code recognition, barcode recognition*, object recognition, and human recognition.                    | **which**: Port (\_P5\_ for M6-RCU, \_P8\_ for E6-RCU, \_P7\_ and \_P8\_ for E7-RCU).<br>**target**: Target number (numbered from left to right on the screen): 1–20.                                                                                                                                                                                                                                                                                                   |
| Read AICAM recognition ID data    | `GetAICamIDData(_PORT_ which, uint8_t ID, uint8_t cmd);` | Get **data** of a specified target (**ID**) recognized by the AI CAM.                                                                                                                                                                                                         | **which**: Port (\_P5\_ for M6-RCU, \_P8\_ for E6-RCU, \_P7\_ and \_P8\_ for E7-RCU).<br>**ID**: Specified target ID: 1–20.<br>**cmd**: Data field (1–7), representing:<br>1. ID<br>2. X coordinate<br>3. Y coordinate<br>4. Width<br>5. Height<br>6. Size<br>7. Confidence<br>**Return value range**: X coordinate (0–639), Y coordinate (0–479), width (0–639), height (0–479), size (0–100), confidence (0–100).                                                     |
| Read AICAM recognition ID name    | `GetAICamIDStr(_PORT_ which, uint8_t ID);`               | Get the **name** of a specified target (**ID**) recognized by the AI CAM.<br><br>Some functions return the name of the recognized object. This module can be used for functions such as QR code recognition, barcode recognition*, object recognition, and human recognition. | **which**: Port (\_P5\_ for M6-RCU, \_P8\_ for E6-RCU, \_P7\_ and \_P8\_ for E7-RCU).<br>**ID**: Specified target ID: 1–20.                                                                                                                                                                                                                                                                                                                                             |

>\***Author's note**: barcode recognition is mentioned as an example of a custom application.

## 6. Interface Definition

The pinout definition of the module's 6-pin connector is as follows: (an [image](https://cdn.nlark.com/yuque/0/2022/png/26280360/1646017683614-8aee7128-63ff-4e14-a35f-e92859574d12.png?x-oss-process=image%2Fformat%2Cwebp) of pins numbered 1-6 from left to right).


| №   | Description   |
| --- | ------------- |
| 1   | GND           |
| 2   | 5V (Power)    |
| 3   | Not Connected |
| 4   | Not Connected |
| 5   | RX            |
| 6   | TX            |

## 7. System Image Flashing

The camera system is stored on a TF card. You can use a card reader to upgrade the system image. The two latest versions are provided below.

### 1. v4.12.4, corresponds to `aicam-2026-01-12.img.xz` file

[Download v4.12.4](https://zmrobo.top/yuque/Electronic_Hardware/AI_CAM/BE1756%20AI%20CAM-System%20image%20flashing%20v4.12.4.zip)

**Changelog**:
Increased the font size in **Settings** and added the **Auto Start on Boot, Backlight, Volume**, and **USB Settings** functions.

### 2. v4.12.5, corresponds to `aicam-2026-06-10.img.xz` file

[Download v4.12.5](https://zmrobo.top/yuque/Electronic_Hardware/AI_CAM/BE1756%20AI%20CAM-System%20image%20flashing%20v4.12.5.zip)

**Changelog**:
1. The **Settings** app can no longer be uninstalled from the **Store**.
2. **Camera** now supports photo and video export.
3. **Human Recognition** has been changed to single-person mode.
4. **Settings** → **Wi-Fi** now supports displaying the current connection status.
5. App names now support commonly used Chinese characters.
6. Added **Voice Recognition** (Chinese), **Text Recognition**, and **Expression Recognition**.

## 8. Notes

 - The module has relatively high power consumption, so it is normal for it to generate heat. Ensure adequate heat dissipation. Do not remove the TF card during use.
 - If the device gets stuck on the startup screen after powering on, the system is most likely corrupted. Re-flash the system image to the TF card.
 - If the screen remains completely black after powering on and re-flashing the system image to the TF card does not resolve the issue, the module needs to be serviced.
 - If entering any mode causes the app to immediately crash and return to the main screen, check whether the **Runtime Library** is installed under **Settings** → **Runtime Library**. If it is not installed, connect to Wi-Fi to install it.
 - If the controller cannot switch modes, check whether the program is running properly and whether the **PH-6P port** is functioning normally.

>**Author's note**: this is an unofficial, independent guide written by [Snupkindeker](https://github.com/Snupkindeker). All the information is either gathered from public sources, or based on the author's own experience. The official Yuque article can be accessed here: https://www.yuque.com/zmrobo-en/hardware/dmlxxlggllouy9fu#XMdFv.
