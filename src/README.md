Control software
====

This directory contains the code required for our robot and explains it

## Software and Language
To program our robot, we use the Arduino IDE and code an Arduino Sketch based on C++. Compiling and uploading our code is a simple process, as there are two buttons to help verify and upload our code. The click of this button will automatically compile and upload our code to the Arduino Nano microcontroller.

## Organization of Code
Our code follows Object Oriented Programming conventions, where we use one program type for each and every sensor and component of our robot. The library we use to interact with our electronic components are: Lego Mindstorms
### Chassis Class
In the chassis class, (ignition) blocks are used to control the drive and steering motors. These are "speed, timing", which is used to control the drive motor as the steering motor we are using.
The first method in our class is the motion function, which takes a whole speed accompanied by a turning angle of 10° to 20°. 
The second method in our class is the steering function, which steers our car at the correct angle. This method limits an angle variable to a specific range and then writes that range to the motor input pin.

### Camera Class
The Camera class interfaces with the PixyCam 2.1 through SPI (Serial Peripheral Interface) and gets the detected blocks. The member variable in this function is the "pixy" variable, an instance of the Pixy2 class provided by the "Pixy2.h" library. 


## Open Challenge Code
For the obstacle challenge, we use ultrasonic sensors and camera. Our code uses these sensors to avoid obstacles and turn effectively. This code is divided into two main parts: the first part is normal navigation and the other part is turning logic.
Normal Navigation
In the normal navigation logic, we start by checking the time a full turn takes and then we get the closest power based on that. Then, we set the speed with its time, and its rotation degrees at the current block if the block is close enough to the robot.
Then, we have the same direction detection logic as the open challenge. After that, we have the block that follows, which we do if we see a block, not a line or nothing, which is done in the following code.
