# Content (GitHub)
**schemes** This folder contains one or several schematic diagrams in the form of JPEG, PNG, or PDF of the electromechanical components illustrating all the elements (electronic components and motors) used in the vehicle and how they connect.

**src** This folder contains all the programming flowcharts and all programming used to participate in the WRO 2024 Future Engineers Category.

**pictures-team & vehicle** This folder contains photos of the team participating in the WRO, photos of the vehicle (from all sides and bottom views) and photo shown in documentation.

**video** This folder contains video.md file that demonstrates how the robot functions to solve both tasks.

**models** This folder contains the 3D design of the vehicle in .lxf and the rendered model of the vehicle.

**other** This folder contains other files which can be used to understand how to prepare the vehicle for the competition.

# Table of Contents (Essay)
- [Introduction](#introduction)
- [X-UniTech Team, Malaysia](#x-unitech-team-malaysia)
- [Performance video](#performance-video)

- [1.0 Mobility Management](#10-mobility-management)
  - [1.1 Design of the self-driving car](#11-design-of-the-self-driving-car)
  - [1.2 Chassis of the self-driving car](#12-chassis-of-the-self-driving-car)
  - [1.3 Building of the self-driving car](#13-building-of-the-self-driving-car)

- [2.0 Power and Sense Management](#20-power-and-sense-management)
  - [2.1 Power source](#21-power-source)
  - [2.2 Sensors](#22-sensors)
  - [2.3 Build Of Materials (BOM)](#23-build-of-materials-bom)
  - [2.4 Wiring diagram](#24-wiring-diagram)

- [3.0 Obstacle Management](#30-obstacle-management)
  - [3.1 Open Challenge](#31-open-challenge)
  - [3.2 Obstacle Challenge](#32-obstacle-challenge)

- [4.0 Engineering Factors](#40-engineering-factors)
  
- [5.0 Improvement and Enhancement](#50-improvement-and-enhancement)
  - [5.1 Robot Construction](#51-robot-construction)
  - [5.2 Robot Programming](#52-robot-programming)

- [Credits](#credits)

- [Appendix 1. The Building Instruction of the Self-Driving Car](#appendix-1-the-building-instruction-of-the-self-driving-car)
- [Appendix 2. Open Challenge Programming](#appendix-2-open-challenge-programming)
- [Appendix 3. Obstacle Challenge Programming](#appendix-3-obstacle-challenge-programming)


---


# Introduction
This engineering documentation details comprehensive aspects of the car’s mobility management, power and sensor systems, obstacle detection and avoidance, construction design, integration of third-party sensors, and the improvements that were made throughout our preparation for the World Robot Olympiad (WRO) Open Championship in Manila, Philippines 2025 under the Future Engineers Category.


# X-UniTech Team, Malaysia
Proudly from Malaysia, X-UniTech is a three-member engineering team specializing in the development of autonomous vehicles. Our team is responsible for the end-to-end design, construction, and integration of the vehicle's mechanical and electronic systems to ensure optimal performance. Meet our members:

**Vun Xiu Xuan, Alvin Kong Wei Ee, and Jennissa Aing Anak Jim.**

<img width="365" height="257" alt="image" src="https://github.com/user-attachments/assets/d50b551d-1ce7-4557-a622-ba1f8753d287" />
<img width="364" height="264" alt="image" src="https://github.com/user-attachments/assets/5ba15b15-0ddf-4bdf-a3ad-2fbf60f25bc9" />


# Performance video
This video demonstrates our autonomous vehicle's design and its operational performance in both the Open Challenge and the Obstacle Challenge. Scan the QR code below to watch the video for both challenges.

Please click the link (https://drive.google.com/file/d/18GrwdV6JntD4dnHnbf9u1oeJ7yk-v8FS/view?usp=sharing)  or scan the QR code to watch the video and explore our project in action.

<img width="166" height="165" alt="image" src="https://github.com/user-attachments/assets/e35994b9-700a-440a-b06a-3705248d47ea" />


# 1.0 Mobility Management
This section details the mechanical design and propulsion system of our autonomous vehicle. It covers the chassis construction, component layout, and the integration of the motors. Additionally, it introduces the fundamental engineering principles of speed, torque, and power that govern the vehicle's performance.


## 1.1 Design of the self-driving car
The autonomous self-driving car chassis and mechanical structure are built using the Lego 45544 Mindstorms EV3 Education Set. 

<img width="516" height="368" alt="image" src="https://github.com/user-attachments/assets/42c9c357-71c3-41f2-b8d0-a25270740402" />

The figures below show the autonomous vehicle we designed and constructed.


Top view	

<img width="349" height="466" alt="image" src="https://github.com/user-attachments/assets/c5b04894-63ce-49a5-b92e-650f30c32ddf" />

Bottom view 

<img width="357" height="466" alt="image" src="https://github.com/user-attachments/assets/341b6b49-c57a-47b6-85e0-897d9bb2ec4d" />

Front view	

<img width="350" height="494" alt="image" src="https://github.com/user-attachments/assets/ef90c8b7-56d2-49cb-a10c-21f6dfb32ab6" />

Back view 

<img width="362" height="498" alt="image" src="https://github.com/user-attachments/assets/d891b837-2c75-49ce-a9d3-0316de5097e2" />

Left side view	

<img width="346" height="411" alt="image" src="https://github.com/user-attachments/assets/003be512-0aa2-4583-9ef6-77ec77f60eda" />

Right side view 

<img width="359" height="411" alt="image" src="https://github.com/user-attachments/assets/37c9c7bb-44b1-421f-b975-38e14548afab" />


## 1.2 Chassis of the self-driving car
The self-driving car chassis is designed to provide structural support and maintain stability, especially during high-speed maneuvers like sharp turns and rapid acceleration.


**(i) Selection of tyre**

For the front steering axle, we selected the Medium Azure Hard Tyre from the Spike Essential set because of its hard rubber compound that minimizes bouncing, allowing the vehicle to track in a straight line more reliably compared to softer tyres. The tyre's smaller diameter enables smoother and more precise steering corrections.

<img width="479" height="315" alt="image" src="https://github.com/user-attachments/assets/85e48324-48cb-4a60-baed-4a827232a1ad" />


The rear axle is fitted with LEGO MINDSTORMS EV3 tyres (62.4 x 20 mm) on 43.2 mm rims. These tyres were selected for the excellent traction their tread pattern provides on typical competition surfaces, such as floors and mats. This high-grip design prevents wheel slippage during rapid acceleration and high-speed cornering. 

<img width="539" height="367" alt="image" src="https://github.com/user-attachments/assets/edb8e92f-330f-4b38-9d19-06d03510cad0" />


**(ii) Implementation of motor and its engineering principle**

Our self-driving car propulsion system consists of two EV3 Medium Motors mounted in a compact, orthogonal arrangement (one horizontal, one vertical). This design offers several key advantages: it optimizes internal space, simplifies the gear train assembly, and contributes to a low center of gravity. A low center of gravity is crucial for maintaining stability during the high-speed maneuvers required in the Open Challenge.

<img width="619" height="329" alt="image" src="https://github.com/user-attachments/assets/14a16d66-a2fd-4a9f-bcc1-8c902d057c4a" />


The diagram below illustrates the specifications and features of the EV3 Medium Motor.

<img width="568" height="351" alt="image" src="https://github.com/user-attachments/assets/58403f33-14d7-4864-ae48-f65e4ec923cd" />


The vehicle's steering mechanism is controlled by an EV3 Medium Motor, selected for its high responsiveness and precision. With a running torque of 8 Ncm and a stall torque of 15 Ncm, the motor provides ample force for steering control. Furthermore, its rotational speed of 260 rpm allows quick rotations, making it well-suited for fine adjustments when avoiding traffic signs. 

 **(iii) Implementation of differential gear**
 
A differential gear is integrated into the drive axle, allowing the left and right wheels to rotate at different speeds. This mechanism is essential for executing smooth, controlled turns, as it prevents wheel binding and improves stability. This is particularly critical when navigating the tight corners found in the Open Challenge.

<img width="500" height="351" alt="image" src="https://github.com/user-attachments/assets/7e993a1f-a001-44ea-8b42-293082d8e966" />


**(iv) Engineering principle of steering**

The steering system is designed using Ackermann steering geometry. 

<img width="494" height="389" alt="image" src="https://github.com/user-attachments/assets/2c09c625-a411-4dd0-97ab-f537d002b1dc" />


This principle turns the inner front wheel at a sharper angle than the outer wheel, allowing both to follow ideal concentric turning circles. By minimizing lateral tire scrub, this geometry significantly reduces friction and wear. The primary benefits include enhanced cornering stability, improved traction, and the ability to execute sharp turns with greater precision.

<img width="421" height="311" alt="image" src="https://github.com/user-attachments/assets/80bffd62-5b4f-4463-b031-e2dc80a40fb5" />



## 1.3 Building of the self-driving car
The building instruction for the self-driving car and the video of showcasing the 3D printing process of its parts can be accessed via the QR Code below. 

Building Instruction of Self-Driving Car (PDF format)

<img width="199" height="206" alt="image" src="https://github.com/user-attachments/assets/f25afabb-8c35-4adc-92a0-4cec379ad04f" />

3D Printing Process Video

<img width="221" height="204" alt="image" src="https://github.com/user-attachments/assets/8233f609-a69f-4fa5-9d3e-60af5a02538b" />


# 2.0 Power and Sense Management
This section details the vehicle's power source and sensor systems. It covers the selection rationale and implementation of each sensor, along with an analysis of the system's power consumption. A complete Build of Materials (BOM) and wiring diagram are also provided for reference.

## 2.1 Power source
The self-driving car is powered by a Soshine 1.5V AA rechargeable lithium-ion (Li-ion) battery with an energy capacity of 2600 mWh. This battery technology was selected for its stable voltage output, which ensures consistent and reliable performance for all electronic components. 

<img width="438" height="300" alt="image" src="https://github.com/user-attachments/assets/cd4c3ab6-8e85-4856-9d72-5b4642d59f65" />


## 2.2 Sensors
The self-driving car is designed to handle the diverse requirements of the Open and Obstacle Challenges. It includes a color sensor, two ultrasonic sensors, a gyro sensor, and a Pixy2 camera. The diagram below illustrates the placement and integration of these components.

<img width="529" height="290" alt="image" src="https://github.com/user-attachments/assets/73058897-d56b-4850-9406-d10a5b7c9c1b" />


**(i) Pixy2 camera** 

The Pixy2 camera serves as the primary vision system for the vehicle during the Obstacle Challenge. Its main function is real-time object detection, allowing it to simultaneously identify and track the red and green pillars while the vehicle is in motion. It also helps to scan the magenta-colored parking zone to ensure the vehicle avoids this restricted area while navigating the course. The Pixy2 camera is mounted at a 75° angle to provide optimal visibility when tracking traffic signs.

<img width="246" height="284" alt="image" src="https://github.com/user-attachments/assets/1d2ac638-e6fd-4db8-88cf-8361be14d60c" />

<img width="284" height="283" alt="image" src="https://github.com/user-attachments/assets/d6b8ae31-ecd3-4bfa-bab4-097ae858860d" />



**(ii) Gyro sensor**

One gyro sensor is used to support our self-driving car. During both Open and Obstacle Challenge, it helps to measure angles and maintain the correct heading while driving. The gyro sensor also helps the robot to turn at accurate angle after passing the edge of the inner wall. While the gyro sensor can sometimes display errors at startup due to calibration issues, we resolved this by performing a hard reset before each run.

<img width="513" height="334" alt="image" src="https://github.com/user-attachments/assets/2bdfbba5-7d41-4714-8c05-e6997b841830" />


**(iii) Ultrasonic sensor**

Our self-driving car is equipped with two EV3 ultrasonic sensors. These sensors measure the distance between the robot and wall to avoid collision towards the walls. The sensors operate by emitting sound waves and calculating the time it takes for them to bounce back after hitting a wall. This data enables the self-driving car to navigate efficiently, make accurate turns, and aim to complete the Open Challenge in the shortest time possible. 

<img width="315" height="305" alt="image" src="https://github.com/user-attachments/assets/0809df99-9d8f-4d7b-b28f-1d5195a526bc" />


**(iv) Color sensor**

The colour sensor is only used in the Obstacle Challenge to determine when the self-driving car should turn. In a clockwise direction, the car turns right whenever it detects an orange line, while in a counterclockwise direction, it turns left upon detecting a blue line. The sensor functions by measuring the intensity of light entering it, allowing the car to identify colour lines and determine whether it is moving clockwise or counterclockwise. 

<img width="349" height="320" alt="image" src="https://github.com/user-attachments/assets/46926e19-91de-4883-96db-04ca36fd4193" />


## 2.3 Build Of Materials (BOM)

The table below shows the Build of Materials (BOM) used to build the self-driving car, making sure each part matches the car’s needs and functions.

<img width="662" height="878" alt="image" src="https://github.com/user-attachments/assets/bedbd3f5-f6c8-4b61-a982-93de403b9265" />

<img width="662" height="907" alt="image" src="https://github.com/user-attachments/assets/c15c042b-48e6-444d-80d6-ddc465878195" />

<img width="662" height="909" alt="image" src="https://github.com/user-attachments/assets/4c074d79-2e91-441d-868f-33b3e589be14" />

<img width="662" height="911" alt="image" src="https://github.com/user-attachments/assets/f1060e62-c8aa-410f-b674-557e34d851ec" />

<img width="662" height="911" alt="image" src="https://github.com/user-attachments/assets/30ff390c-36b4-4b36-8f76-fe508580a51d" />

<img width="662" height="539" alt="image" src="https://github.com/user-attachments/assets/66f3e2ff-81b4-441c-a2d6-975878f0d7a4" />


## 2.4 Wiring diagram
The wiring diagram below illustrates the sensors’ power consumption and shows how the motors and sensors are connected within our self-driving car to support the setups for both the Open Challenge and the Obstacle Challenge. 

**(i) Open challenge wiring diagram**

<img width="655" height="809" alt="image" src="https://github.com/user-attachments/assets/e0aa7e0c-77e4-455e-8e8a-7da702f94cbf" />


**(ii) Obstacle challenge wiring diagram**

<img width="631" height="963" alt="image" src="https://github.com/user-attachments/assets/32a0784a-7d09-4f24-be46-6c2d7bc2f1d3" />


# 3.0 Obstacle Management
In our project, we utilize the Clev3r-Python programming language to operate the robot. The programming structure is divided into two main sections which is the Open Challenge and the Obstacle Challenge. This section includes a flowchart and an overview of the code used for both challenges. 

## 3.1 Open Challenge
To complete the open challenge, our robot uses two main sensors which is an EV3 Gyro Sensor and two EV3 Ultrasonic Sensors on both the left and right sides. Since both EV3 Ultrasonic Sensors share the same port, we use a multiplexer to allow the robot to read data from each one separately. The left ultrasonic sensor is connected to Channel 1 of the multiplexer, while the right ultrasonic sensor is connected to Channel 3.

<img width="689" height="422" alt="image" src="https://github.com/user-attachments/assets/3fcfba2a-4495-4989-8a29-32aec5166e51" />


The EV3 Ultrasonic Sensors helps the car to measure the distance between the robot and the walls. By comparing readings from the left and right sensors, the robot can determine whether it should move clockwise or counter clockwise. These readings also help the robot adjust its steering to avoid collisions and stay at a safe distance from inner and the outer walls. Additionally, the EV3 Gyro Sensors monitor the robot’s heading, ensuring it maintains a straight path and performs accurate turns at the correct angle when turning.

<img width="647" height="378" alt="image" src="https://github.com/user-attachments/assets/3df20184-dd6b-4d99-965e-1ab41acfaa40" />


Diagram below shows the flowchart for Open Challenge: 

<img width="596" height="978" alt="image" src="https://github.com/user-attachments/assets/fd3e983a-b079-4a7a-87bd-36ca5dd3cfd6" />


Appendix 2 contains the complete programming code for the Open Challenge.

Below is a brief explanation of the key parts of the code used to control the robot during the challenge.
1.	Initialization and Setup
This part is aim to set up the sensors and multiplexer before running. The setMultiplexerMode function allows the EV3 to connect with both ultrasonic sensors in the same port while the getMultiplexerValues function allows the robot to read the distance values from the left and right ultrasonic sensors. Additionally, the ReadSensor continuously updates the robot’s heading and wall distances in real time.

<img width="603" height="427" alt="image" src="https://github.com/user-attachments/assets/7b830802-533e-4529-9f94-ff1041fb096f" />


2.	Reset Steering
Reset Steering make sure the steering motor starts at a fixed desired position before driving. The robot turns the steering motor all the way to the left for 300 milliseconds by using the medium motor in the port A. Hence, it waits until the motor completely stops moving, which means it has hit the limit. A short pause is added to let the medium motor. After that, the motor’s rotation counter is reset to zero. This step is important because it tells the robot exactly where the “straight ahead” position is.

<img width="397" height="222" alt="image" src="https://github.com/user-attachments/assets/cba77815-5420-4b5b-a06f-f2e01a617227" />


3.	PID Steering Control
The PID Steering function helps the robot to adjust the steering motor whenever it starts to drift off from the target. The P part fixes most of the error right away, the I part makes small adjustments over time and the D part make sure that the correction is done smoothly. These three adjustments are added together to get one correction value, which is sent to motor A to turn the steering. This keeps the robot moving smoothly, avoiding zig-zagging, and makes its turns more accurate.

<img width="641" height="316" alt="image" src="https://github.com/user-attachments/assets/63c8691d-fe5d-4f1f-91b2-e9cd30a4f4d4" />


4.	Drive
The Drive function moves the robot forward and keeps it aligned when following a wall. If no wall is detected on either side, the drive motor stops; otherwise, it runs at the set speed. When wall-following mode is on, the robot adjusts its steering based on the distance to the wall. It then combines this adjustment with its current heading to get a target steering angle, which is sent to the PID Steering function for smooth and accurate control.

<img width="558" height="484" alt="image" src="https://github.com/user-attachments/assets/3cb43713-634a-4a8d-9f56-3ee1d3a7217d" />


The DriveDegrees function moves the robot forward in rotation degrees. He robot will keep driving at the given speed until the target degrees are reached, and stops the motor if stop is set to 1.

<img width="570" height="152" alt="image" src="https://github.com/user-attachments/assets/4d4a8650-6a18-4910-9b34-cc59a36c8efc" />


5.	Main program
This program resets timers and steering, then drives forward until it detects a wall on either side. It determines whether to follow the right or left wall based on sensor readings.

<img width="362" height="274" alt="image" src="https://github.com/user-attachments/assets/bd077349-e435-4c7a-9b6d-c099fcd3c8b6" />

The robot will move in clockwise direction.

<img width="374" height="186" alt="image" src="https://github.com/user-attachments/assets/d137e19e-fa6a-4819-bb71-b1af397bb7b4" />

The robot will move in counter clockwise direction.

<img width="409" height="186" alt="image" src="https://github.com/user-attachments/assets/4c8dc399-8ae5-48fa-9699-383959d3dffc" />


Then, it loops for 11 times, turning 90° in the chosen direction in every loops. At the end, it makes one final 90° turn, drives forward, and displays the elapsed time on the LCD.

<img width="229" height="314" alt="image" src="https://github.com/user-attachments/assets/87a33a86-8fc1-4555-90f7-3f1018f75e71" />



## 3.2 Obstacle Challenge
To complete the Obstacle Challenge, our robot utilizes four sensors which is a Pixy2 Camera, a gyro sensor, two ultrasonic sensors on both the left and right sides and a colour sensor. Since both ultrasonic sensors need to be connected to the same port, we use a multiplexer so that the robot can read data from both of the sensors.

<img width="591" height="374" alt="image" src="https://github.com/user-attachments/assets/f3bdb29f-8d7b-4ede-b0ff-0218912b86cc" />

<img width="593" height="361" alt="image" src="https://github.com/user-attachments/assets/83ffc2d7-9d8c-4bbc-b8bd-3b8c02a7c27d" />


The Pixy2 Camera is connected to port 1 and it helps to detect the presence of pillars and magenta parking lot during the round. Next, the EV3 Gyro Sensor that connected to port 2 helps to ensures that the robot does the accurate turns and keep the robot’s heading straight during the round. Thirdly, both of the EV3 Ultrasonic Sensor is connected to EV3 Brick port 3 via the multiplexer. They help to detect the presence of the inner and outer wall and prevent the robot from hitting into the wall. Lastly, we utilize the EV3 Colour Sensor to identify the coloured line on the map which is the orange and blue line. The identified colour allows the robot to know the direction accurately. For instance, if orange line is scanned first, the direction will be in clockwise direction.

Diagram below shows the flowchart for Obstacle Challenge: 

<img width="697" height="1035" alt="image" src="https://github.com/user-attachments/assets/479eef98-618f-4304-a424-0bfc770f519f" />

Appendix 3 contains the complete programming code for the Obstacle Challenge. 

Below is a brief explanation of the key parts of the code used to control the robot during the challenge.

1. Initialization and Set Up

This part is aim to set up the Pixy2 Camera and multiplexer before running. The setLampOn and setLampOff function turns the lamp of the sensor on and off while the getSignature function allow the Pixy2Camera to read the position of the green and red pillars through their XY coordinate shown in the Pixy Mon V2 apps. The setMultiplexerMode function allows the EV3 to connect with both ultrasonic sensors in the same port while the getMultiplexerValues function allows the robot to read the distance values from the left and right ultrasonic sensors. 

<img width="657" height="467" alt="image" src="https://github.com/user-attachments/assets/d7dcc817-cb47-48ba-a820-a88ecad721c6" />


Plus, each sensor such as EV3 Gyro Sensor, EV3 Color Sensor, EV3 Ultrasonic Sensor and Pixy2 Camera must be set up to their own port before the robot starts. ReadSensor continuously updates the green (Signature 1) and red (Signature 2) pillars positions on the camera views. The magenta parking lot position (Signature 3) also updated from time to time. Moreover, the robot also reads the gyro angle and wall distance in real time so that the robot will not off from its target.

<img width="581" height="381" alt="image" src="https://github.com/user-attachments/assets/67309d3b-521b-4ffc-b8c4-5811903b5fe6" />


The GyroReset allows the robot to reset the gyro sensor so that the gyro will measuring the angles from zero again. In sense, it is like pressing the “reset” button on the EV3 Gyro Sensor so that it starts measure the heading from 0 again. This is important because it avoids cumulative errors that might affect the robot.

<img width="617" height="255" alt="image" src="https://github.com/user-attachments/assets/5e3baeef-3fc2-486a-ae19-d60312b50cd0" />


2.	Reset Steering

The ResetSteering helps to reset the steering motor before the robot starts running. It will turn the steering wheel all the way to one side and let the robot know that is the starting point. This is important because it will allow the robot steering always aligned in middle before it starts to move.

<img width="470" height="277" alt="image" src="https://github.com/user-attachments/assets/f4c2d2b9-0588-440a-be39-a0ced003cbac" />


3.	PID Steering Control

The PID Steering function helps the robot to adjust the steering motor whenever it starts to drift off from the target. This function is crucial in the Obstacle Challenge because it allows the robot to maintain in the straight heading after avoiding the pillars. The P part fixes most of the error right away, the I part makes small adjustments over time and the D part make sure that the correction is done smoothly. These three adjustments are added together to get one correction value, which is sent to motor A to turn the steering. This keeps the robot moving smoothly, avoiding zig-zagging, and makes its turns more accurate.

<img width="385" height="262" alt="image" src="https://github.com/user-attachments/assets/d171f3bd-e7cc-43a2-9ec2-3b576d3ca5fb" />


4.	Drive

The Drive function combined four main parts which including the TrackWall, TrackPillar and PID Steering. In sum, these values help the robot constantly adjust its steering and make sure the robot move smoothly and accurately.

(i)	TrackWall
The robot checks its distances from the walls within the range of 150mm. If it’s too close to one of the sides, it will steer away. Plus, the robot will check which wall is closer by comparing the distance values from both sides. If the left wall is closer, the robot will adjust its steering to follow the left side. If the right wall is closer, it will follow the right side instead, but with a negative steering value to turn in the opposite direction.

<img width="584" height="178" alt="image" src="https://github.com/user-attachments/assets/f8e58afc-3a22-44ea-8904-75c210ce57fc" />


If neither wall is detected within the set range, the robot will not make any wall-following adjustments. This allows it to continue moving straight without unnecessary corrections.
 
<img width="592" height="162" alt="image" src="https://github.com/user-attachments/assets/c06e7332-61b5-406e-be34-c99656acd609" />


(ii)	TrackPillar
This part help to calculate how far each pillar from the Pixy2 Camera’s view. It uses the Pythagorean theorem to figure out the straight-line distance based on the difference in horizontal (x) and vertical (y) positions.

<img width="703" height="90" alt="image" src="https://github.com/user-attachments/assets/fda0a321-517e-4aa5-9ce0-6e94fee56760" />


This part helps the robot to check the presence of red, green pillars and magenta parking lot. If the pillars are near to the robot, the robot will start reacting by showing the LED colours. 

<img width="663" height="495" alt="image" src="https://github.com/user-attachments/assets/1c748687-acba-4a06-a19c-496923e5e364" />


If the green pillar is the closest, it sets @lastPillar = 1 and lights the green LED. Additionally, the y-coordinate (150) allow the robot to know the distance of the pillar from the Pixy2 Camera’s view. However, if the red pillar is the closet, it sets @lastPillar = 2 and light red LED. The steering will start to do the adjustment once the red pillars is located at the y-coordinate value (160) from the Pixy2 Camera’s view. If the magenta parking lot is near, the orange LED lights up. The robot will steer to the right if it is moving clockwise, or to the left if it is moving counter clockwise to avoid hitting the magenta parking lot.
When no pillar is nearby, the robot turns off its LED light and uses the ultrasonic sensors to follow the wall. If it is moving clockwise, it will check the left wall. Conversely, if it is moving counter clockwise, it will check the right wall. If it is too far off its intended direction (relative heading), it will not make any wall adjustments to avoid over-correcting. 
 
<img width="682" height="159" alt="image" src="https://github.com/user-attachments/assets/d1087230-e24d-4094-8405-9154a71ea1c8" />


(iii)	Steering Error
The robot’s steering correction is based on a combination of pillar tracking and wall tracking. The robot then applies this correction to the PID steering motor. At the same time, it powers the drive motor which is the Motor D to move forward at runSpeed.

<img width="454" height="174" alt="image" src="https://github.com/user-attachments/assets/4541138c-3db7-442a-9633-ddce41c11418" />


5.	Others movement block

(i)	WaitDegrees
WaitDegrees function makes the robot to move a certain distance based on the rotation of its drive motor (Motor D). The stop=1 means the robot will stops the motor and waits for a 50ms after finishing the movement.

 <img width="619" height="183" alt="image" src="https://github.com/user-attachments/assets/29aa7530-1e78-427e-b758-18da4510f063" />


(ii)	SteeringDrive
The SteeringDrive function makes the robot move forward a certain distance while controlling the steering. Therefore, it will combine the current steering motor position with any additional steering adjustment during both of the challenge rounds. 

 <img width="653" height="257" alt="image" src="https://github.com/user-attachments/assets/de204873-25f9-4150-b020-8e5a967def56" />


6.	Main program

When the robot starts, it first decides whether it will move in a counterclockwise or clockwise direction based on the ultrasonic sensor readings from the left and right sides.

<img width="664" height="132" alt="image" src="https://github.com/user-attachments/assets/5058f2c5-9be5-4653-995d-1fdb90084314" />

 
As shown in the diagram below, if the left wall distance is greater than the right wall distance (leftWall>rightWall), the robot will know that it is counterclockwise. However, if the right wall is greater than left wall (rightWall>leftWall), the robot will know that it is in clockwise direction.

<img width="636" height="394" alt="image" src="https://github.com/user-attachments/assets/d665f89f-ba99-44de-a1cf-42b2b6ea9fe4" />

 
Next, the pillar X value tells the robot where the pillar should appear in the camera’s field of view. By using this value, the robot will avoid the pillar or adjust its path to stay centred when following it. 

<img width="388" height="344" alt="image" src="https://github.com/user-attachments/assets/417c271d-44b8-45e7-8bd5-c19ca724f93d" />

<img width="548" height="298" alt="image" src="https://github.com/user-attachments/assets/2bc0e100-67f2-43ef-8779-b594530c4480" />

<img width="538" height="287" alt="image" src="https://github.com/user-attachments/assets/d0aef603-0465-4733-a7cd-0b257d352a00" />


After exiting the parking lot, the robot will drive forward at a speed of 45 until its colour sensor detects either a blue line or an orange line on the ground. Once one of these lines is detected, the robot will immediately play a sound to indicate that the line has been found. 

<img width="560" height="260" alt="image" src="https://github.com/user-attachments/assets/d549e4c1-496d-428d-a516-129af419c766" />


During the Obstacle Round, the robot adjusts its steering by correcting any error measured from three sources which include TrackPillar and TrackWall. The steering target is slightly different depending on whether the robot is moving clockwise or counterclockwise so a different adjustment value is applied for each direction. This steering correction process is repeated for 12 loops.

<img width="406" height="336" alt="image" src="https://github.com/user-attachments/assets/cd9f08cd-c16a-46a0-b5b3-09cf8ea3f9b9" />


This part of the program ensures the robot does not overturn and end up facing the wrong direction while avoiding a pillar. When the robot avoids a pillar on its left side, which mean it passes a green pillar in a clockwise run or a red pillar in a counterclockwise run. It needs to turn a greater number of degrees. This extra turning ensures it does not accidentally scan the wrong-coloured line, which could cause it to head in the wrong direction.

<img width="463" height="349" alt="image" src="https://github.com/user-attachments/assets/3c4f5bdc-9b73-4a27-b774-c73a795b8d48" />


After completing 12 loops, the robot will move straight for 300 for counter clockwise to ensures the robot do not hit any pillars while moving into the parking area. After moving for certain degrees, the robot will adjust its heading based on the direction. The robot will drive into the wall with a speed of 100 to make sure its heading is perfectly straight. This is important because it allows the robot to move backward in a straight way. 

<img width="442" height="242" alt="image" src="https://github.com/user-attachments/assets/78bc6e1e-413e-40fb-b526-cafc8c0b15b7" />

<img width="431" height="295" alt="image" src="https://github.com/user-attachments/assets/8396c303-9e27-4828-a323-f71944aa778b" />


Next, the robot will perform a reverse action and readjust the heading target to ensure it is perfectly straight and aligned parallel to the magenta parking lot.

<img width="350" height="176" alt="image" src="https://github.com/user-attachments/assets/1abbb27e-1e78-4d5c-8531-b34939afe111" />


The robot will move forward while maintaining a fixed distance from the parking lot which is 300 mm for a counter clockwise heading and 240 mm for a clockwise heading. As it moves, it continuously checks this distance. If the distance goes out of range, the robot will adjust its steering to bring it back to the correct value. Once it passes the second magenta parking lot, the robot will reverse into the parking space and ensure it is parked parallel to the parking lot.
 	 
<img width="362" height="280" alt="image" src="https://github.com/user-attachments/assets/afdd36dd-1dc0-4813-aa74-c1f6e07b7697" />

<img width="352" height="280" alt="image" src="https://github.com/user-attachments/assets/40fd216f-3cd0-4cb6-b457-0fd2c8ccf0a5" />

 
The flow diagram below illustrates the detailed process of parking in the magenta parking lot.
 
<img width="745" height="764" alt="image" src="https://github.com/user-attachments/assets/1024e432-def9-4971-be31-bb51a1d401be" />



# 4.0 Engineering Factors
This section showcases our custom-designed and third-party open-source parts along with detailed explanations of all the components installed in the car. 

At first, our autonomous self-driving car is primarily built using the LEGO Mindstorms Education EV3 Core Set 45544. However, we faced several challenges while completing both the Open and Obstacle Challenges. For example, our design required more sensor ports than the EV3 brick could provide, the EV3 colour sensor often gave inconsistent readings due to external light interference, and we lacked of suitable camera to accurately scan the pillars and the magenta parking lot. To overcome these challenges and enhance our robot’s performance, we incorporated third-party components into the design. The diagram below illustrates the additional components we used and how they helped overcome these issues.
 
<img width="664" height="412" alt="image" src="https://github.com/user-attachments/assets/fc39f24b-9a7d-4055-a132-93bc9c63060b" />


**(i)	EV3 Sensor Multiplexer**

We added an EV3 Sensor Multiplexer so our robot can use five sensors at once. There are two ultrasonic sensors connected to the multiplexer with different channel. With all five working together, the robot can move more accurately and handle Obstacles Challenge better.

 <img width="452" height="399" alt="image" src="https://github.com/user-attachments/assets/25a36773-e2e2-49db-8721-d477429ee0c6" />


**(ii)	3D Printed Casing**

We created a 3D-printed casing for the colour sensor. This casing blocks external light so the sensor can detect colours more accurately, and it also protects the sensor from damage if the robot bumps into something.

 <img width="432" height="376" alt="image" src="https://github.com/user-attachments/assets/17622bb3-134b-4bc3-bfbe-68c1cf888b0e" />


**(iii)	Pixy2 Camera**

We use the Pixy2 Camera because it can quickly and accurately detect objects while the robot is moving. In our design, the Pixy2 Camera is mainly used to scan and track the magenta parking lot, green and red pillars, which helps the robot recognize them in time and make the right navigation decisions during the Open and Obstacle Challenges.
 
 <img width="726" height="269" alt="image" src="https://github.com/user-attachments/assets/a3d5ce84-2d24-4226-84c9-ef4a4b7145a9" />

 

# 5.0 Improvement and Enhancement
In this section, we explain the problems we faced while building our self-driving car and the different methods we used to solve them. By studying each problem carefully, we made changes that improved the car performances. The improvements towards the robot can be categorized into two main parts which is the construction and programming parts.

## 5.1 Robot Construction

We improved the construction of robot from time to time whenever we encountered challenges. Below are some of the improvements we implemented.

**(i)	Replace the front steering wheel with a smaller size wheel**

Initially, we are using the LEGO tyre 44771 for the front wheel but then we switched to the smaller tyre from Spike Essential Set which is known as the Medium Azure Hard Rubber Tyre. The reduced size improved the car’s maneuverability, making it easier to turn and park in tight spaces. Moreover, the steering’s sensitivity is better when avoiding pillars.

 <img width="655" height="304" alt="image" src="https://github.com/user-attachments/assets/de505ec5-620f-438d-b50e-4d97254ae388" />


**(ii)	Adding a 3D-Printed Casing to the EV3 Colour Sensor**

Our EV3 colour sensor failed to detect the orange and blue lights for several times. Since this scanning process is crucial for determining the robot’s direction, we designed and 3D-printed a custom casing for the sensor. The casing’s main purpose is to block external light that could interfere with colours detection, while also protecting the sensor from impacts or collisions.

 <img width="606" height="330" alt="image" src="https://github.com/user-attachments/assets/d71c9c71-768d-4a91-8ff2-f8a0b89fe26b" />

 
**(iii)	Implementing a multiplexer to solve the limited EV3 ports issue**

We also encountered an issue with the limited number of EV3 ports. During the Obstacle Challenge, multiple sensors were required at the same time, which quickly used up all available ports. To overcome this, we used a multiplexer, which allowed us to expand the number of connections. Both ultrasonic sensors were connected to the multiplexer, freeing up the built-in EV3 ports for other essential sensors.

  <img width="566" height="326" alt="image" src="https://github.com/user-attachments/assets/1924f1de-b4d6-4460-a012-11216d9fdad0" />


**(iv)	Pixy2 Camera Position Adjustment**

Initially, we noticed a delay in the robot’s response when avoiding pillars. Hence, we adjusted the Pixy2 camera position by moving it slightly backward. This allowed the camera to detect pillars earlier, giving the steering system more time to make corrections and preventing collisions towards the pillars during Obstacle Challenge.

  <img width="537" height="330" alt="image" src="https://github.com/user-attachments/assets/801dd19f-72ae-482c-9b1c-c17f65e88ca8" />


## 5.2 Robot Programming

(i)	Resetting the gyro**

When we tested our EV3 robot, we noticed the gyro sensor sometimes drifted. This means that even when the robot was not turning, the angle reading slowly changed. At first, we tried fixing it by adding a software reset in our program. The reset switched the sensor into the correct mode, sent a command to set the angle back to zero, and waited until it was ready. This worked most of the time, especially when we reset it just before the robot started moving.

 <img width="514" height="189" alt="image" src="https://github.com/user-attachments/assets/235d36bd-3539-4e3b-931a-b0b878f1845d" />

 
However, we found that the gyro could still drift during the run, even after the software reset. Things like vibration, motor movement, and small calculation errors could still affect the reading. Hence, we decided that a hard reset might work better. A hard reset clears the sensor’s memory more deeply than a software reset, giving a cleaner and more stable reading at the start.
 
  <img width="483" height="401" alt="image" src="https://github.com/user-attachments/assets/a4c5c592-69cd-48e4-aae1-4de5caaff037" />

  
**(ii)	Ensuring continuous operation of ultrasonic sensor**

The ultrasonic sensor has an issue where it may turn off unexpectedly during operation without any warning. To address this, we've developed a program that automatically sets the robot's motor speed to zero whenever the ultrasonic sensor detects a value of zero. This precaution effectively stops the robot's movement until the sensor resumes normal operation, reducing any risks associated with the sensor failure. Once the ultrasonic sensor begins detecting values again, the robot will return to its normal speed, ensuring smooth and uninterrupted movement.

  <img width="620" height="107" alt="image" src="https://github.com/user-attachments/assets/0ca2b448-e0a5-49a1-86ef-04b96e014df0" />


**(iii)	Adding signal light to EV3 Brick**

At first, we didn’t connect the Pixy camera with the EV3 brick’s LED light. This made it harder to know when the robot had spotted a pillar. During testing, we had to guess whether the robot was reacting at the right time.
To make this easier for competition, we set the LED to change colour when the robot sees a pillar. By looking at the LED and the robot’s position on the map, we can quickly tell if it is reacting too early or too late. We also thought about adding sound alerts, but in a crowded and noisy place, it would be hard to hear them. That’s why using lights is a better choice to overcome the problems.

  <img width="363" height="337" alt="image" src="https://github.com/user-attachments/assets/2f800df1-ad0b-4762-b0d1-d7ce408523db" />

  <img width="448" height="255" alt="image" src="https://github.com/user-attachments/assets/2532ed9f-257f-4791-bbe4-fe3119eb2307" />

 
**(iv)	PID Steering**

Before this, we didn’t use PID steering in our robot’s program. From our observation, the steering corrections were not precise. The robot sometimes drifted off track or turned too much, which made it slower and less accurate.
To solve this, we added PID steering. This allows the robot to constantly adjust its steering to follow the target path more accurately. After adding PID, the robot turns smoothly and stays on track much better. This greatly improved our performance in both of the challenges. The video in the QR code clearly shows the difference when PID steering is applied.

  Programming of the PID steering system
  
  <img width="344" height="218" alt="image" src="https://github.com/user-attachments/assets/e1303454-3f4f-4ea2-b379-d42f0c0bddc2" />

  PID Steering System Demo

  <img width="225" height="220" alt="image" src="https://github.com/user-attachments/assets/080be134-d43d-40c7-8223-faab95baf4d1" />



# Credits

We extend our sincere appreciation to LEGO Education for their generous support in providing high-quality LEGO EV3 and SPIKE Essential sets, and to Bambu Lab for their advanced 3D printing technology, which contributed significantly to the development of our custom components.

# Appendix 1. The Building Instruction of the Self-Driving Car
The Building Instruction of the Self-Driving Car

<img width="752" height="1063" alt="image" src="https://github.com/user-attachments/assets/a6396a9b-8600-4aa5-8666-029c77aa1713" />

<img width="752" height="1063" alt="image" src="https://github.com/user-attachments/assets/5c4e8127-b3f7-461f-9467-25664f49015d" />

<img width="752" height="1063" alt="image" src="https://github.com/user-attachments/assets/79b0454b-d3dc-4f8e-adc7-275427cc4cf7" />

<img width="752" height="1063" alt="image" src="https://github.com/user-attachments/assets/5a8b2ffd-88ef-4f36-bc59-daeff01ddfcc" />

<img width="752" height="1063" alt="image" src="https://github.com/user-attachments/assets/3df2acca-ac3c-4465-9488-3b1b76c4f242" />

<img width="752" height="1063" alt="image" src="https://github.com/user-attachments/assets/d5a02b18-5b7d-443c-b61e-d6dc7f8d2abb" />

<img width="752" height="1063" alt="image" src="https://github.com/user-attachments/assets/85a2579a-2dda-4004-b952-ac522e09af81" />

<img width="752" height="1063" alt="image" src="https://github.com/user-attachments/assets/7f563077-17d2-4656-b027-2dfb3e681a01" />

<img width="752" height="1063" alt="image" src="https://github.com/user-attachments/assets/169b5747-b810-4e45-8da1-a1ad06e3396d" />

<img width="752" height="1063" alt="image" src="https://github.com/user-attachments/assets/817d23b2-7c4f-485e-9d3a-5d5674ce1433" />

<img width="752" height="1063" alt="image" src="https://github.com/user-attachments/assets/bfe24264-76fe-4e58-999e-f6617cb4d228" />

<img width="752" height="1063" alt="image" src="https://github.com/user-attachments/assets/0990ac0b-8524-4027-923c-fe9b9b569f9e" />

<img width="752" height="1063" alt="image" src="https://github.com/user-attachments/assets/28c83efb-c45f-4c71-8710-0e3411dfdaba" />

<img width="752" height="1063" alt="image" src="https://github.com/user-attachments/assets/4bc7c5e0-f4dd-4c5d-b8e3-bb3488f19ff9" />

<img width="752" height="1063" alt="image" src="https://github.com/user-attachments/assets/4f486c5e-349a-4dba-bf98-45b857b37572" />

<img width="752" height="1063" alt="image" src="https://github.com/user-attachments/assets/227c41ff-287a-485d-af06-6bc8f410c377" />

<img width="752" height="1063" alt="image" src="https://github.com/user-attachments/assets/7c160b96-c7b1-4a9a-88d7-3edfd2f08cf5" />

<img width="752" height="1063" alt="image" src="https://github.com/user-attachments/assets/f01f8c34-e25f-40ba-a106-e45ae2b0196d" />

<img width="752" height="1063" alt="image" src="https://github.com/user-attachments/assets/0ba08125-d565-428f-882c-48cf404114ab" />

<img width="752" height="1063" alt="image" src="https://github.com/user-attachments/assets/1fed3c97-c7ce-46be-8dc0-29dfc2cb51e5" />

<img width="752" height="1063" alt="image" src="https://github.com/user-attachments/assets/83d2b5e6-f191-43a7-9a52-47937427779a" />

<img width="752" height="1063" alt="image" src="https://github.com/user-attachments/assets/68ab601d-9a3b-41f1-984b-9b484022226b" />

<img width="752" height="1063" alt="image" src="https://github.com/user-attachments/assets/2a7133a8-4e0f-4067-9836-694b8e8c07fa" />

<img width="752" height="1063" alt="image" src="https://github.com/user-attachments/assets/a9e6a418-8d01-4b8a-ab82-c018674052ba" />

<img width="752" height="1063" alt="image" src="https://github.com/user-attachments/assets/60d5a73d-da02-437c-bcd3-40d12696483f" />

<img width="752" height="1063" alt="image" src="https://github.com/user-attachments/assets/3a6fd252-b11f-48d6-99df-cfcd4651a389" />

<img width="752" height="1063" alt="image" src="https://github.com/user-attachments/assets/abaa1335-8849-47c8-ab74-6116c1dc8bfa" />

<img width="752" height="1063" alt="image" src="https://github.com/user-attachments/assets/e8f72490-c75b-4917-b836-96575abf4af0" />

<img width="752" height="1063" alt="image" src="https://github.com/user-attachments/assets/cc858b59-293b-4e06-a9b7-57a9055fe49f" />

<img width="752" height="1063" alt="image" src="https://github.com/user-attachments/assets/b744e712-e72e-4148-bac5-9aa97014bed7" />

<img width="752" height="1063" alt="image" src="https://github.com/user-attachments/assets/d5b5e8d8-55d7-4a39-b82a-6c55167915be" />

<img width="752" height="1063" alt="image" src="https://github.com/user-attachments/assets/c7daa6e0-73ad-4e35-b85c-14268f837f98" />

<img width="752" height="1063" alt="image" src="https://github.com/user-attachments/assets/2b1b4aaf-a140-472b-af7d-5e66d3e84d39" />

<img width="752" height="1063" alt="image" src="https://github.com/user-attachments/assets/92576833-dd11-4794-a964-10cb68bdec2e" />

<img width="752" height="1063" alt="image" src="https://github.com/user-attachments/assets/7a7d7518-7e91-44e6-841c-9c4dd6f83613" />

<img width="752" height="1063" alt="image" src="https://github.com/user-attachments/assets/ba899080-bb26-4c4a-b572-92621fad4c8c" />

<img width="752" height="1063" alt="image" src="https://github.com/user-attachments/assets/98db857d-33c6-4c9a-a6b5-c83645990f4e" />

<img width="752" height="1063" alt="image" src="https://github.com/user-attachments/assets/1a3445ee-a2b0-4535-986e-2edc7aeef305" />

<img width="752" height="1063" alt="image" src="https://github.com/user-attachments/assets/00a993dc-7ab0-4af6-a183-4f15a7b13650" />

<img width="752" height="1063" alt="image" src="https://github.com/user-attachments/assets/624caab6-865f-4225-8756-e9066a205947" />

<img width="752" height="1063" alt="image" src="https://github.com/user-attachments/assets/1e7bb21c-96c0-49a4-aef5-bb8580494492" />

<img width="752" height="1063" alt="image" src="https://github.com/user-attachments/assets/5ddb285c-6ebe-4e21-a3e6-f584e2a0f6ee" />

<img width="752" height="1063" alt="image" src="https://github.com/user-attachments/assets/6ca76a5d-126f-4563-9196-d8a9e31f1608" />

<img width="752" height="1063" alt="image" src="https://github.com/user-attachments/assets/3aa36cc6-48f8-41a9-8fe0-75bb5e2a5b4e" />

<img width="752" height="1063" alt="image" src="https://github.com/user-attachments/assets/c60f74d8-98b7-461a-b1c6-05c583ea7d67" />

<img width="752" height="1063" alt="image" src="https://github.com/user-attachments/assets/528ca9f0-7f11-47d3-bcd3-8a5fb9653552" />

<img width="752" height="1063" alt="image" src="https://github.com/user-attachments/assets/7c0ae2ed-a01a-4f2c-94c1-ef7f4409688d" />

<img width="752" height="1063" alt="image" src="https://github.com/user-attachments/assets/84e32600-07a9-495d-9425-c97eb4efa909" />

<img width="752" height="1063" alt="image" src="https://github.com/user-attachments/assets/693658f1-20d8-494d-a305-6ae4810738e9" />

<img width="752" height="1063" alt="image" src="https://github.com/user-attachments/assets/9f949fe4-e0f0-43a8-8dcb-5dcbdb828371" />

<img width="752" height="1063" alt="image" src="https://github.com/user-attachments/assets/12de4258-4a66-4b31-a0a5-eb64cf20fa9a" />

<img width="752" height="1063" alt="image" src="https://github.com/user-attachments/assets/eeef0de1-c960-4cd3-95dd-20247d7c894b" />

<img width="752" height="1063" alt="image" src="https://github.com/user-attachments/assets/cbbdd798-a772-462b-8434-d7c0552e98ee" />

<img width="752" height="1063" alt="image" src="https://github.com/user-attachments/assets/08a54732-954e-4c55-bcd0-1d9c4621f3f3" />

<img width="752" height="1063" alt="image" src="https://github.com/user-attachments/assets/cbafe0fd-c740-4566-b2e2-6d8dc741ab94" />

<img width="752" height="1063" alt="image" src="https://github.com/user-attachments/assets/2429042d-0e35-408e-87ee-9f69345c2573" />

<img width="752" height="1063" alt="image" src="https://github.com/user-attachments/assets/d6045d6b-280d-43f8-9926-131814363460" />

<img width="752" height="1063" alt="image" src="https://github.com/user-attachments/assets/a0641a2d-94a0-4a5f-97f6-7a197add58cc" />

<img width="752" height="1063" alt="image" src="https://github.com/user-attachments/assets/a2354e5d-e840-40b2-99ea-f5feca1b2e30" />

<img width="752" height="1063" alt="image" src="https://github.com/user-attachments/assets/a094f5ef-69bc-4f1d-a080-9e3f758d73fc" />

<img width="752" height="1063" alt="image" src="https://github.com/user-attachments/assets/87bddb91-8e27-44b5-8d68-2472995c5e18" />

<img width="752" height="1063" alt="image" src="https://github.com/user-attachments/assets/260df67f-2423-43e2-8041-ae6c0f66de97" />

<img width="752" height="1063" alt="image" src="https://github.com/user-attachments/assets/b25b400c-4879-49b2-8a4a-ec39f5e4eff2" />

<img width="752" height="1063" alt="image" src="https://github.com/user-attachments/assets/10d07250-54b7-402e-927d-5580e2045ea5" />

<img width="752" height="1063" alt="image" src="https://github.com/user-attachments/assets/b25d5bd0-fa0f-4662-899d-45b7c870772d" />

<img width="752" height="1063" alt="image" src="https://github.com/user-attachments/assets/72e4adf0-3ee4-46fe-9fa3-478c50330e66" />

<img width="752" height="1063" alt="image" src="https://github.com/user-attachments/assets/77638b8e-fc03-4315-b620-d03be2177c76" />

<img width="752" height="1063" alt="image" src="https://github.com/user-attachments/assets/6ae0817e-fd50-4e44-83bd-744fb7103a59" />

<img width="752" height="1063" alt="image" src="https://github.com/user-attachments/assets/98c61358-2013-4650-8069-7b13200b28fb" />

<img width="752" height="1063" alt="image" src="https://github.com/user-attachments/assets/d1e7c747-02d6-4104-b97e-f942f25086d5" />

<img width="752" height="1063" alt="image" src="https://github.com/user-attachments/assets/3964f09b-18b0-44a0-9ee0-0fe91b753fc1" />

<img width="752" height="1063" alt="image" src="https://github.com/user-attachments/assets/72e4a7cc-920a-4e87-8618-6aba97539a35" />

<img width="752" height="1063" alt="image" src="https://github.com/user-attachments/assets/3205bf3d-af25-44f7-8535-3a624424b90f" />

<img width="752" height="1063" alt="image" src="https://github.com/user-attachments/assets/29ecdd5a-77e6-41b2-8d46-4a5c2ea21b5a" />

<img width="752" height="1063" alt="image" src="https://github.com/user-attachments/assets/3e8c6f1d-eeaa-49cb-a845-e65c2ffabf1d" />

<img width="752" height="1063" alt="image" src="https://github.com/user-attachments/assets/819156f1-eb08-4edd-aef3-793b29d9bb2e" />

<img width="752" height="1063" alt="image" src="https://github.com/user-attachments/assets/8bb7c179-7844-4b52-9298-3eef7fa6b14c" />

<img width="752" height="1063" alt="image" src="https://github.com/user-attachments/assets/9718a9c7-4491-4557-a7d7-0378ef12cd5a" />

<img width="752" height="1063" alt="image" src="https://github.com/user-attachments/assets/35012ff8-8f6b-4e1f-a732-01caef9bcd32" />

<img width="752" height="1063" alt="image" src="https://github.com/user-attachments/assets/c857a1b5-53b7-4420-83e2-cb4426a025d5" />

<img width="752" height="1063" alt="image" src="https://github.com/user-attachments/assets/44801896-3bbb-4bcf-87c5-543b4c104c4d" />

<img width="752" height="1063" alt="image" src="https://github.com/user-attachments/assets/77970299-0f3e-4799-8b70-8d6736b02943" />



# Appendix 2. Open Challenge Programming
Open Challenge Programming

<img width="753" height="488" alt="image" src="https://github.com/user-attachments/assets/a101351d-6ca8-42b6-acdd-1b3bbe942da8" />

<img width="759" height="377" alt="image" src="https://github.com/user-attachments/assets/6255e87d-ca90-4d06-a858-a4f43d727112" />

<img width="720" height="599" alt="image" src="https://github.com/user-attachments/assets/c770a6eb-e295-4d2b-9420-1b4fbb38b3ae" />

<img width="708" height="528" alt="image" src="https://github.com/user-attachments/assets/f90ea498-2ca8-435f-975a-57e31c006a66" />

<img width="728" height="367" alt="image" src="https://github.com/user-attachments/assets/3f358333-66a4-4f2e-ad92-5525498eec9c" />



# Appendix 3. Obstacle Challenge Programming
Obstacle Challenge Programming

<img width="747" height="441" alt="image" src="https://github.com/user-attachments/assets/67cc5c95-db0f-4359-ad2b-f4883f46e9ac" />

<img width="753" height="477" alt="image" src="https://github.com/user-attachments/assets/58f6987d-6729-4c19-b4e9-c7c85e836ada" />

<img width="742" height="337" alt="image" src="https://github.com/user-attachments/assets/b30cc7f7-60c3-4313-865a-2f9a691ac0cf" />

<img width="747" height="443" alt="image" src="https://github.com/user-attachments/assets/bf656fb8-dc5f-4d75-87b7-1acce635942c" />

<img width="749" height="459" alt="image" src="https://github.com/user-attachments/assets/e2b068a5-abe2-422f-a377-6cdf42cc8937" />

<img width="746" height="437" alt="image" src="https://github.com/user-attachments/assets/b805d1f5-d880-43e7-9f33-d94aab666621" />

<img width="748" height="192" alt="image" src="https://github.com/user-attachments/assets/714d5639-3be6-431f-832c-9a493f7a1af3" />

<img width="745" height="402" alt="image" src="https://github.com/user-attachments/assets/c8221133-a7bb-45c3-9af7-c079e5cab48f" />

<img width="747" height="255" alt="image" src="https://github.com/user-attachments/assets/04168816-7513-47a6-91f9-3f3062583257" />

<img width="749" height="460" alt="image" src="https://github.com/user-attachments/assets/d2353a6a-4529-43ac-9d0b-76d72b5d64ff" />

<img width="746" height="353" alt="image" src="https://github.com/user-attachments/assets/5c363638-5a6d-45c6-91a3-5970c188210b" />

<img width="748" height="437" alt="image" src="https://github.com/user-attachments/assets/fc095139-23ef-4601-ae3c-a602d878ea6d" />

<img width="743" height="216" alt="image" src="https://github.com/user-attachments/assets/f43945cf-b51f-4d90-a9c6-71778977355e" />

<img width="748" height="429" alt="image" src="https://github.com/user-attachments/assets/2707efff-3714-4feb-b724-7e3d97cb101b" />

<img width="753" height="254" alt="image" src="https://github.com/user-attachments/assets/879b1257-f985-4af2-8401-c08baca815cb" />

<img width="753" height="399" alt="image" src="https://github.com/user-attachments/assets/77d6d16e-16da-4d46-98f7-24e46f4a5cb1" />

<img width="753" height="332" alt="image" src="https://github.com/user-attachments/assets/76fecc8d-3873-4d50-a32d-46317b9680fa" />

<img width="753" height="456" alt="image" src="https://github.com/user-attachments/assets/d7cbaca8-a060-4462-a411-7ab154f7d79f" />

