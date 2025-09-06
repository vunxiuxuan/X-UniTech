# Introduction
This engineering documentation covers the car’s mobility management, power and sensor systems, obstacle detection and avoidance, construction design, integration of third-party sensors, and the improvements made throughout our preparation for the World Robot Olympiad Open Championship Philippines (WRO) 2025 Future Engineers Category Competition.

# Content
**schemes** This folder contains one or several schematic diagrams in the form of JPEG, PNG, or PDF of the electromechanical components illustrating all the elements (electronic components and motors) used in the vehicle and how they connect.

**src** This folder contains all the programming flowcharts and all programming used to participate in the WRO 2024 Future Engineers Category.

**pictures-team & vehicle** This folder contains photos of the team participating in the WRO, photos of the vehicle (from all sides and bottom views) and photo shown in documentation.

**video** This folder contains video.md file that demonstrates how the robot functions to solve both tasks.

**models** This folder contains the 3D design of the vehicle in .lxf and the rendered model of the vehicle.

**other** This folder contains other files which can be used to understand how to prepare the vehicle for the competition.

# X-UniTech Team, Malaysia
X-UniTech from Malaysia is a team of three members who work together to build and program a self-driving robot car. We design, build, and manage all the electronic and mechanical parts to ensure our self-driving car runs smoothly. Here are our team members:

**Vun Xiu Xuan, Alvin Kong Wei Ee, and Jennissa Aing Anak Jim.**

image

# Performance video
This video provides an overview of our self-driving car’s design, demonstrates its performance in both the Open Challenge and the Obstacle Challenge, and explains how it operates in each scenario. Scan the QR code below to watch the video for both challenges.

Please click the link https://youtu.be/7t6WDGnzcJU or scan the QR code to watch the video and explore our project in action.
https://youtu.be/rjCbvZdWhEg 

image


# 1.0 Mobility management
This section explains how our self-driving car is designed, how the motors are used to control its movement, and how they are connected to the vehicle. It also describes the chassis and where different parts are placed. Lastly, it introduces basic engineering ideas like speed, torque, and power that affect how the car works.


## 1.1 Design of the self-driving car
The autonomous self-driving car is constructed using the Lego 45544 Mindstorms EV3 Education Set. 

The figure below displays the images of the self-driving car that we have designed and constructed.

image

## 1.2  Chassis of the self-driving car
The chassis design of the self-driving car is essential for providing structural support, ensuring stability during high-speed movements such as sharp turns and rapid accelerations.

image

**(i) Selection of tyre**

We had selected the Medium Azure Hard Tyre from Spike Essential for our front wheel steering. This is due to the hard rubber compound molding that can help the robot to move in a straight line more reliably compared to softer, bouncy tyres. Its smaller size also makes the steering correction more smoothly.

image

**(ii) Implementation of motor and its engineering principle**

Our self-driving car uses two EV3 Medium Motors to drive it forward and backward, with one placed horizontally and the other vertically. This setup saves space inside the car, makes it easier to fit the gears, and maintains a low centre of gravity, which improves stability during high-speed movements in the Open Challenge. 

image


The diagram below shows the details of the EV3 Medium Motor. 

image


The EV3 Medium Motor is implemented for its fast response and precise movements. As shown in the diagram above, a running torque of 8 Ncm and a stalled torque of 15 Ncm enable the self-driving car to manage the moderate force required for steering, where small adjustments are essential. Additionally, with a speed of 260 rpm, the motor is capable for quick rotations, making it well-suited for fine adjustments when avoiding traffic signs. 

 **(iii) Implementation of differential gear**
 
he differential gear transfers power between the two axles, enabling them to rotate at different speeds. This mechanism allows the self-driving car to execute smooth turns, especially when navigating around inner walls corners during Open Challenge.

image

**(iv) Engineering principle of steering**

We use Ackermann steering geometry, which turns the front wheels at slightly different angles. This lets the inner and outer wheels follow their own paths during a turn, reducing slipping and friction. With this design, the car stays more stable, the tyres last longer, and it can make sharp turns without sliding or tipping over.

image


## 1.3 Building of the self-driving car

The building instruction for the self-driving car and the video of showcasing the 3D printing process of its parts can be accessed via the QR Code below. 

image


# 2.0	Power and sense management

This section explains the power source of the self-driving car and the sensors uses to navigate different challenges. It describes the reason of each chosen sensor, how they are used on the car, and the details of power consumption. It also includes the Build of Materials (BOM) and the wiring diagram.

## 2.1 Power source

Our self-driving car is powered by the Soshine Rechargeable AA Lithium-ion Battery, delivering 1.5V and 2600mWh to ensure smooth and consistent operation. This battery serves as the primary energy source for our robot. 

image

## 2.2 Sensor

The self-driving car is equipped with a color sensor, two ultrasonic sensors, a gyro sensor and a Pixy2 camera. This combination equips the vehicle to effectively encounter both the Open and Obstacle Challenges. The diagram below provides a summary of the sensors integrated into our self-driving car. 

image

**(i) Pixy2 camera** 

A Pixy2 camera is used to assist our self-driving car. The Pixy2 camera supports our self-driving car by detecting red and green pillars simultaneously while moving during the Obstacle Challenge. It also helps to scan magenta parking lot and avoid hitting on it during avoiding the pillars. 

image

**(ii) Gyro sensor**

One gyro sensor is used to support our self-driving car. During both Open and Obstacle Challenge, it helps to measure angles and maintain the correct heading while driving. The gyro sensor also helps the robot to turn at accurate angle after passing the edge of the inner wall. While the gyro sensor can sometimes display errors at startup due to calibration issues, we resolved this by performing a hard reset before each run.

iamge

**(iii) Ultrasonic sensor**

Our self-driving car is equipped with two EV3 ultrasonic sensors. These sensors measure the distance between the robot and wall to avoid collision towards the walls. The sensors operate by emitting sound waves and calculating the time it takes for them to bounce back after hitting a wall. This data enables the self-driving car to navigate efficiently, make accurate turns, and aim to complete the Open Challenge in the shortest time possible. 

image

**(iv) Color sensor**

The colour sensor is only used in the Obstacle Challenge to determine when the self-driving car should turn. In a clockwise direction, the car turns right whenever it detects an orange line, while in a counterclockwise direction, it turns left upon detecting a blue line. The sensor functions by measuring the intensity of light entering it, allowing the car to identify colour lines and determine whether it is moving clockwise or counterclockwise. 

image

## 2.3 Build of materials

The table below shows the Build of Materials (BOM) used to build the self-driving car, making sure each part matches the car’s needs and functions.

image


## 2.4 Wiring diagram

The wiring diagram below illustrates the sensors’ power consumption and shows how the motors and sensors are connected within our self-driving car to support the setups for both the Open Challenge and the Obstacle Challenge. 

**(i) Open challenge wiring diagram**

image

**(ii) Obstacle challenge wiring diagram**

image

# 3.0 Obstacle management

In our project, we utilize the Clev3r-Python programming language to operate the robot. The programming structure is divided into two main sections which is the Open Challenge and the Obstacle Challenge. This section includes a flowchart and an overview of the code used for both challenges. 

## 3.1 Open challenge

To complete the open challenge, our robot uses two main sensors which is an EV3 Gyro Sensor and two EV3 Ultrasonic Sensors on both the left and right sides. Since both EV3 Ultrasonic Sensors share the same port, we use a multiplexer to allow the robot to read data from each one separately. The left ultrasonic sensor is connected to Channel 1 of the multiplexer, while the right ultrasonic sensor is connected to Channel 3.

image

Diagram below shows the flowchart for Open Challenge: 

image


Below is a brief explanation of the key parts of the code used to control the robot during the challenge.

1.	Initialization and Setup
This part is aim to set up the sensors and multiplexer before running. The setMultiplexerMode function allows the EV3 to connect with both ultrasonic sensors in the same port while the getMultiplexerValues function allows the robot to read the distance values from the left and right ultrasonic sensors. Plus, the ReadSensor continuously updates the robot’s heading and wall distances in real time.

image


2.	Reset Steering
Reset Steering make sure the steering motor starts at a fixed desired position before driving. The robot turns the steering motor all the way to the left for 300 milliseconds by using the medium motor in the port A. Hence, it waits until the motor completely stops moving, which means it has hit the limit. A short pause is added to let the medium motor. After that, the motor’s rotation counter is reset to zero. This step is important because it tells the robot exactly where the “straight ahead” position is.

image

3.	PID Steering Control
The PID Steering function helps the robot to adjust the steering motor whenever it starts to drift off from the target. The P part fixes most of the error right away, the I part makes small adjustments over time and the D part make sure that the correction is done smoothly. These three adjustments are added together to get one correction value, which is sent to motor A to turn the steering. This keeps the robot moving smoothly, avoiding zig-zagging, and makes its turns more accurate.

image

4.	Drive
The Drive function moves the robot forward and keeps it aligned when following a wall. If no wall is detected on either side, the drive motor stops; otherwise, it runs at the set speed. When wall-following mode is on, the robot adjusts its steering based on the distance to the wall. It then combines this adjustment with its current heading to get a target steering angle, which is sent to the PID Steering function for smooth and accurate control.


image


The DriveDegrees function moves the robot forward in rotation degrees. He robot will keep driving at the given speed until the target degrees are reached, and stops the motor if stop is set to 1.

image

5.	Main program
This program resets timers and steering, then drives forward until it detects a wall on either side. It determines whether to follow the right or left wall based on sensor readings.

image

Then, it loops for 11 times, turning 90° in the chosen direction in every loops. At the end, it makes one final 90° turn, drives forward, and displays the elapsed time on the LCD.

image


## 3.2	Obstacle challenge

To complete the Obstacle Challenge, our robot utilizes four sensors which is a Pixy2 Camera, a gyro sensor, two ultrasonic sensors on both the left and right sides and a colour sensor. Since both ultrasonic sensors need to be connected to the same port, we use a multiplexer so that the robot can read data from both of the sensors.

image

The Pixy2 Camera is connected to port 1 and it helps to detect the presence of pillars and magenta parking lot during the round. Next, the EV3 Gyro Sensor that connected to port 2 helps to ensures that the robot does the accurate turns and keep the robot’s heading straight during the round. Thirdly, both of the EV3 Ultrasonic Sensor is connected to EV3 Brick port 3 via the multiplexer. They help to detect the presence of the inner and outer wall and prevent the robot from hitting into the wall. Lastly, we utilize the EV3 Colour Sensor to identify the coloured line on the map which is the orange and blue line. The identified colour allows the robot to know the direction accurately. For instance, if orange line is scanned first, the direction will be in clockwise direction.

Diagram below shows the flowchart for Obstacle Challenge: 

image

Below is a brief explanation of the key parts of the code used to control the robot during the challenge.
1.	Initialization and Set Up
This part is aim to set up the Pixy2 Camera and multiplexer before running. The setLampOn and setLampOff function turns the lamp of the sensor on and off while the getSignature function allow the Pixy2Camera to read the position of the green and red pillars through their XY coordinate shown in the Pixy Mon V2 apps. The setMultiplexerMode function allows the EV3 to connect with both ultrasonic sensors in the same port while the getMultiplexerValues function allows the robot to read the distance values from the left and right ultrasonic sensors. 

image

Plus, each sensor such as EV3 Gyro Sensor, EV3 Color Sensor, EV3 Ultrasonic Sensor and Pixy2 Camera must be set up to their own port before the robot starts. ReadSensor continuously updates the green (Signature 1) and red (Signature 2) pillars positions on the camera views. The magenta parking lot position (Signature 3) also updated from time to time. Moreover, the robot also reads the gyro angle and wall distance in real time so that the robot will not off from its target.

image

 
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
We use the Pixy2 Camera because it can quickly and accurately detect objects while the robot is moving. In our design, the Pixy2 Camera is mainly used to scan and track the magenta parking lot, green and red pillars, which helps the robot recognize them in time and make the right navigation decisions during the Open and Obstacle Challenges.	. 
 
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
To make this easier for competition, we set the LED to change colour when the robot sees a pillar. By looking at the LED and the robot’s position on the map, we can quickly tell if it is reacting too early or too late. We also thought about adding sound alerts, but in a crowded and noisy place, it would be hard to hear them. That’s why using lights is a better choice for most situations.

  image
 
**(iv)	PID Steering**
Before this, we didn’t use PID steering in our robot’s program. From our observation, the steering corrections were not precise. The robot sometimes drifted off track or turned too much, which made it slower and less accurate.
To solve this, we added PID steering. This allows the robot to constantly adjust its steering to follow the target path more accurately. After adding PID, the robot turns smoothly and stays on track much better. This greatly improved our performance in both of the challenges. The video in the QR code clearly shows the difference when PID steering is applied.

 	  image


# Credits

We extend our sincere appreciation to LEGO Education for their generous support in providing high-quality LEGO EV3 and SPIKE Essential sets, and to Bambu Lab for their advanced 3D printing technology, which contributed significantly to the development of our custom components.
