# Table of Content



# Introduction
This engineering documentation details comprehensive aspects of the car’s mobility management, power and sensor systems, obstacle detection and avoidance, construction design, integration of third-party sensors, and the improvements that were made throughout our preparation for the World Robot Olympiad (WRO) Open Championship in Manila, Philippines 2025 under the Future Engineers Category.

# Content
**schemes** This folder contains one or several schematic diagrams in the form of JPEG, PNG, or PDF of the electromechanical components illustrating all the elements (electronic components and motors) used in the vehicle and how they connect.

**src** This folder contains all the programming flowcharts and all programming used to participate in the WRO 2024 Future Engineers Category.

**pictures-team & vehicle** This folder contains photos of the team participating in the WRO, photos of the vehicle (from all sides and bottom views) and photo shown in documentation.

**video** This folder contains video.md file that demonstrates how the robot functions to solve both tasks.

**models** This folder contains the 3D design of the vehicle in .lxf and the rendered model of the vehicle.

**other** This folder contains other files which can be used to understand how to prepare the vehicle for the competition.

# X-UniTech Team, Malaysia
Proudly from Malaysia, X-UniTech is a three-member engineering team specializing in the development of autonomous vehicles. Our team is responsible for the end-to-end design, construction, and integration of the vehicle's mechanical and electronic systems to ensure optimal performance. Meet our members:

**Vun Xiu Xuan, Alvin Kong Wei Ee, and Jennissa Aing Anak Jim.**
<img width="365" height="257" alt="image" src="https://github.com/user-attachments/assets/d50b551d-1ce7-4557-a622-ba1f8753d287" />
<img width="364" height="264" alt="image" src="https://github.com/user-attachments/assets/5ba15b15-0ddf-4bdf-a3ad-2fbf60f25bc9" />


# Performance video
This video demonstrates our autonomous vehicle's design and its operational performance in both the Open Challenge and the Obstacle Challenge. Scan the QR code below to watch the video for both challenges.

Please click the link (https://drive.google.com/file/d/18GrwdV6JntD4dnHnbf9u1oeJ7yk-v8FS/view?usp=sharing)  or scan the QR code to watch the video and explore our project in action.

<img width="166" height="165" alt="image" src="https://github.com/user-attachments/assets/e35994b9-700a-440a-b06a-3705248d47ea" />


# 1.0 Mobility management
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


## 1.2  Chassis of the self-driving car
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


# 2.0	Power and sense management
This section details the vehicle's power source and sensor systems. It covers the selection rationale and implementation of each sensor, along with an analysis of the system's power consumption. A complete Build of Materials (BOM) and wiring diagram are also provided for reference.

## 2.1 Power source
The self-driving car is powered by a Soshine 1.5V AA rechargeable lithium-ion (Li-ion) battery with an energy capacity of 2600 mWh. This battery technology was selected for its stable voltage output, which ensures consistent and reliable performance for all electronic components. 

<img width="438" height="300" alt="image" src="https://github.com/user-attachments/assets/cd4c3ab6-8e85-4856-9d72-5b4642d59f65" />


## 2.2 Sensor
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


## 2.3 Build of materials

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


# 3.0 Obstacle management
In our project, we utilize the Clev3r-Python programming language to operate the robot. The programming structure is divided into two main sections which is the Open Challenge and the Obstacle Challenge. This section includes a flowchart and an overview of the code used for both challenges. 

## 3.1 Open challenge
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



## 3.2	Obstacle challenge
To complete the Obstacle Challenge, our robot utilizes four sensors which is a Pixy2 Camera, a gyro sensor, two ultrasonic sensors on both the left and right sides and a colour sensor. Since both ultrasonic sensors need to be connected to the same port, we use a multiplexer so that the robot can read data from both of the sensors.

<img width="591" height="374" alt="image" src="https://github.com/user-attachments/assets/f3bdb29f-8d7b-4ede-b0ff-0218912b86cc" />

<img width="593" height="361" alt="image" src="https://github.com/user-attachments/assets/83ffc2d7-9d8c-4bbc-b8bd-3b8c02a7c27d" />


The Pixy2 Camera is connected to port 1 and it helps to detect the presence of pillars and magenta parking lot during the round. Next, the EV3 Gyro Sensor that connected to port 2 helps to ensures that the robot does the accurate turns and keep the robot’s heading straight during the round. Thirdly, both of the EV3 Ultrasonic Sensor is connected to EV3 Brick port 3 via the multiplexer. They help to detect the presence of the inner and outer wall and prevent the robot from hitting into the wall. Lastly, we utilize the EV3 Colour Sensor to identify the coloured line on the map which is the orange and blue line. The identified colour allows the robot to know the direction accurately. For instance, if orange line is scanned first, the direction will be in clockwise direction.

Diagram below shows the flowchart for Obstacle Challenge: 

<img width="697" height="1035" alt="image" src="https://github.com/user-attachments/assets/479eef98-618f-4304-a424-0bfc770f519f" />

Appendix 3 contains the complete programming code for the Obstacle Challenge. 

Below is a brief explanation of the key parts of the code used to control the robot during the challenge.
1.	Initialization and Set Up
This part is aim to set up the Pixy2 Camera and multiplexer before running. The setLampOn and setLampOff function turns the lamp of the sensor on and off while the getSignature function allow the Pixy2Camera to read the position of the green and red pillars through their XY coordinate shown in the Pixy Mon V2 apps. The setMultiplexerMode function allows the EV3 to connect with both ultrasonic sensors in the same port while the getMultiplexerValues function allows the robot to read the distance values from the left and right ultrasonic sensors. 

<img width="657" height="467" alt="image" src="https://github.com/user-attachments/assets/d7dcc817-cb47-48ba-a820-a88ecad721c6" />


Plus, each sensor such as EV3 Gyro Sensor, EV3 Color Sensor, EV3 Ultrasonic Sensor and Pixy2 Camera must be set up to their own port before the robot starts. ReadSensor continuously updates the green (Signature 1) and red (Signature 2) pillars positions on the camera views. The magenta parking lot position (Signature 3) also updated from time to time. Moreover, the robot also reads the gyro angle and wall distance in real time so that the robot will not off from its target.

<img width="581" height="381" alt="image" src="https://github.com/user-attachments/assets/67309d3b-521b-4ffc-b8c4-5811903b5fe6" />


The GyroReset allows the robot to reset the gyro sensor so that the gyro will measuring the angles from zero again. In sense, it is like pressing the “reset” button on the EV3 Gyro Sensor so that it starts measure the heading from 0 again. This is important because it avoids cumulative errors that might affect the robot.

image

 
2.	Reset Steering
The ResetSteering helps to reset the steering motor before the robot starts running. It will turn the steering wheel all the way to one side and let the robot know that is the starting point. This is important because it will allow the robot steering always aligned in middle before it starts to move.

image


3.	PID Steering Control
The PID Steering function helps the robot to adjust the steering motor whenever it starts to drift off from the target. This function is crucial in the Obstacle Challenge because it allows the robot to maintain in the straight heading after avoiding the pillars. The P part fixes most of the error right away, the I part makes small adjustments over time and the D part make sure that the correction is done smoothly. These three adjustments are added together to get one correction value, which is sent to motor A to turn the steering. This keeps the robot moving smoothly, avoiding zig-zagging, and makes its turns more accurate.

image

 
4.	Drive
The Drive function combined four main parts which including the TrackWall, TrackPillar and PID Steering. In sum, these values help the robot constantly adjust its steering and make sure the robot move smoothly and accurately.

(i)	TrackWall
The robot checks its distances from the walls within the range of 150mm. If it’s too close to one of the sides, it will steer away. Plus, the robot will check which wall is closer by comparing the distance values from both sides. If the left wall is closer, the robot will adjust its steering to follow the left side. If the right wall is closer, it will follow the right side instead, but with a negative steering value to turn in the opposite direction.

image

If neither wall is detected within the set range, the robot will not make any wall-following adjustments. This allows it to continue moving straight without unnecessary corrections.
 
image

(ii)	TrackPillar
This part help to calculate how far each pillar from the Pixy2 Camera’s view. It uses the Pythagorean theorem to figure out the straight-line distance based on the difference in horizontal (x) and vertical (y) positions.

image

This part helps the robot to check the presence of red, green pillars and magenta parking lot. If the pillars are near to the robot, the robot will start reacting by showing the LED colours. 

image

If the green pillar is the closest, it sets @lastPillar = 1 and lights the green LED. Additionally, the y-coordinate (150) allow the robot to know the distance of the pillar from the Pixy2 Camera’s view. However, if the red pillar is the closet, it sets @lastPillar = 2 and light red LED. The steering will start to do the adjustment once the red pillars is located at the y-coordinate value (160) from the Pixy2 Camera’s view. If the magenta parking lot is near, the orange LED lights up. The robot will steer to the right if it is moving clockwise, or to the left if it is moving counter clockwise to avoid hitting the magenta parking lot.
When no pillar is nearby, the robot turns off its LED light and uses the ultrasonic sensors to follow the wall. If it is moving clockwise, it will check the left wall. Conversely, if it is moving counter clockwise, it will check the right wall. If it is too far off its intended direction (relative heading), it will not make any wall adjustments to avoid over-correcting. 
 
image

(iii)	Steering Error
The robot’s steering correction is based on a combination of pillar tracking and wall tracking. The robot then applies this correction to the PID steering motor. At the same time, it powers the drive motor which is the Motor D to move forward at runSpeed.

image

5.	Others movement block
(i)	WaitDegrees
WaitDegrees function makes the robot to move a certain distance based on the rotation of its drive motor (Motor D). The stop=1 means the robot will stops the motor and waits for a 50ms after finishing the movement.

 image

(ii)	SteeringDrive
The SteeringDrive function makes the robot move forward a certain distance while controlling the steering. Therefore, it will combine the current steering motor position with any additional steering adjustment during both of the challenge rounds. 

image

6.	Main program
When the robot starts, it first decides whether it will move in a counterclockwise or clockwise direction based on the ultrasonic sensor readings from the left and right sides.

image
 
As shown in the diagram below, if the left wall distance is greater than the right wall distance (leftWall>rightWall), the robot will know that it is counterclockwise. However, if the right wall is greater than left wall (rightWall>leftWall), the robot will know that it is in clockwise direction.

image
 
Next, the pillar X value tells the robot where the pillar should appear in the camera’s field of view. By using this value, the robot will avoid the pillar or adjust its path to stay centred when following it. 

image

After exiting the parking lot, the robot will drive forward at a speed of 45 until its colour sensor detects either a blue line or an orange line on the ground. Once one of these lines is detected, the robot will immediately play a sound to indicate that the line has been found. 

image

During the Obstacle Round, the robot adjusts its steering by correcting any error measured from three sources which include TrackPillar and TrackWall. The steering target is slightly different depending on whether the robot is moving clockwise or counterclockwise so a different adjustment value is applied for each direction. This steering correction process is repeated for 12 loops.

image

This part of the program ensures the robot does not overturn and end up facing the wrong direction while avoiding a pillar. When the robot avoids a pillar on its left side, which mean it passes a green pillar in a clockwise run or a red pillar in a counterclockwise run. It needs to turn a greater number of degrees. This extra turning ensures it does not accidentally scan the wrong-coloured line, which could cause it to head in the wrong direction.

image

After completing 12 loops, the robot will move straight for 300 for counter clockwise to ensures the robot do not hit any pillars while moving into the parking area. After moving for certain degrees, the robot will adjust its heading based on the direction. The robot will drive into the wall with a speed of 100 to make sure its heading is perfectly straight. This is important because it allows the robot to move backward in a straight way. 

 image

Next, the robot will perform a reverse action and readjust the heading target to ensure it is perfectly straight and aligned parallel to the magenta parking lot.

 image

The robot will move forward while maintaining a fixed distance from the parking lot which is 300 mm for a counter clockwise heading and 240 mm for a clockwise heading. As it moves, it continuously checks this distance. If the distance goes out of range, the robot will adjust its steering to bring it back to the correct value. Once it passes the second magenta parking lot, the robot will reverse into the parking space and ensure it is parked parallel to the parking lot.
 	 
image
 
The flow diagram below illustrates the detailed process of parking in the magenta parking lot.
 
image



# 4.0 Engineering factor
This section showcases our custom-designed and third-party open-source parts along with detailed explanations of all the components installed in the car. 

At first, our autonomous self-driving car is primarily built using the LEGO Mindstorms Education EV3 Core Set 45544. However, we faced several challenges while completing both the Open and Obstacle Challenges. For example, our design required more sensor ports than the EV3 brick could provide, the EV3 colour sensor often gave inconsistent readings due to external light interference, and we lacked of suitable camera to accurately scan the pillars and the magenta parking lot. To overcome these challenges and enhance our robot’s performance, we incorporated third-party components into the design. The diagram below illustrates the additional components we used and how they helped overcome these issues.
 
image

**(i)	EV3 Sensor Multiplexer**
We added an EV3 Sensor Multiplexer so our robot can use five sensors at once. There are two ultrasonic sensors connected to the multiplexer with different channel. With all five working together, the robot can move more accurately and handle Obstacles Challenge better.

 image

**(ii)	3D Printed Casing**
We created a 3D-printed casing for the colour sensor. This casing blocks external light so the sensor can detect colours more accurately, and it also protects the sensor from damage if the robot bumps into something.

 image

**(iii)	Pixy2 Camera**
We use the Pixy2 Camera because it can quickly and accurately detect objects while the robot is moving. In our design, the Pixy2 Camera is mainly used to scan and track the magenta parking lot, green and red pillars, which helps the robot recognize them in time and make the right navigation decisions during the Open and Obstacle Challenges.
 
image
 


# 5.0 Improvements
In this section, we explain the problems we faced while building our self-driving car and the different methods we used to solve them. By studying each problem carefully, we made changes that improved the car performances. The improvements towards the robot can be categorized into two main parts which is the construction and programming parts.

**5.1	Robot construction**
We improved the construction of robot from time to time whenever we encountered challenges. Below are some of the improvements we implemented.

**(i)	Replace the front steering wheel with a smaller size wheel**
Initially, we are using the LEGO tyre 44771 for the front wheel but then we switched to the smaller tyre from Spike Essential Set which is known as the Medium Azure Hard Rubber Tyre. The reduced size improved the car’s maneuverability, making it easier to turn and park in tight spaces. Moreover, the steering’s sensitivity is better when avoiding pillars.

 image

**(ii)	Adding a 3D-Printed Casing to the EV3 Colour Sensor**
Our EV3 colour sensor failed to detect the orange and blue lights for several times. Since this scanning process is crucial for determining the robot’s direction, we designed and 3D-printed a custom casing for the sensor. The casing’s main purpose is to block external light that could interfere with colours detection, while also protecting the sensor from impacts or collisions.

 image
 
**(iii)	Implementing a multiplexer to solve the limited EV3 ports issue**
We also encountered an issue with the limited number of EV3 ports. During the Obstacle Challenge, multiple sensors were required at the same time, which quickly used up all available ports. To overcome this, we used a multiplexer, which allowed us to expand the number of connections. Both ultrasonic sensors were connected to the multiplexer, freeing up the built-in EV3 ports for other essential sensors.

  image

**(iv)	Pixy2 Camera Position Adjustment**
Initially, we noticed a delay in the robot’s response when avoiding pillars. Hence, we adjusted the Pixy2 camera position by moving it slightly backward. This allowed the camera to detect pillars earlier, giving the steering system more time to make corrections and preventing collisions towards the pillars during Obstacle Challenge.

  image

**5.2	Robot programming
(i)	Resetting the gyro**
When we tested our EV3 robot, we noticed the gyro sensor sometimes drifted. This means that even when the robot was not turning, the angle reading slowly changed. At first, we tried fixing it by adding a software reset in our program. The reset switched the sensor into the correct mode, sent a command to set the angle back to zero, and waited until it was ready. This worked most of the time, especially when we reset it just before the robot started moving.

 image
 
However, we found that the gyro could still drift during the run, even after the software reset. Things like vibration, motor movement, and small calculation errors could still affect the reading. Hence, we decided that a hard reset might work better. A hard reset clears the sensor’s memory more deeply than a software reset, giving a cleaner and more stable reading at the start.
 
  image
  
**(ii)	Ensuring continuous operation of ultrasonic sensor**
The ultrasonic sensor has an issue where it may turn off unexpectedly during operation without any warning. To address this, we've developed a program that automatically sets the robot's motor speed to zero whenever the ultrasonic sensor detects a value of zero. This precaution effectively stops the robot's movement until the sensor resumes normal operation, reducing any risks associated with the sensor failure. Once the ultrasonic sensor begins detecting values again, the robot will return to its normal speed, ensuring smooth and uninterrupted movement.

  image

**(iii)	Adding signal light to EV3 Brick**
At first, we didn’t connect the Pixy camera with the EV3 brick’s LED light. This made it harder to know when the robot had spotted a pillar. During testing, we had to guess whether the robot was reacting at the right time.
To make this easier for competition, we set the LED to change colour when the robot sees a pillar. By looking at the LED and the robot’s position on the map, we can quickly tell if it is reacting too early or too late. We also thought about adding sound alerts, but in a crowded and noisy place, it would be hard to hear them. That’s why using lights is a better choice to overcome the problems.

  image
 
**(iv)	PID Steering**
Before this, we didn’t use PID steering in our robot’s program. From our observation, the steering corrections were not precise. The robot sometimes drifted off track or turned too much, which made it slower and less accurate.
To solve this, we added PID steering. This allows the robot to constantly adjust its steering to follow the target path more accurately. After adding PID, the robot turns smoothly and stays on track much better. This greatly improved our performance in both of the challenges. The video in the QR code clearly shows the difference when PID steering is applied.

  image


# Credits

We extend our sincere appreciation to LEGO Education for their generous support in providing high-quality LEGO EV3 and SPIKE Essential sets, and to Bambu Lab for their advanced 3D printing technology, which contributed significantly to the development of our custom components.

# Appendix 1
The Building Instruction of the Self-Driving Car

Image

# Appendix 2
Open Challenge Programming

Image

# Appendix 3
Obstacle Challenge Programming

Image
