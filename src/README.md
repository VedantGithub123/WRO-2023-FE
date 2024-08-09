## Control Software
This directory contains the code required for our robot and explains it.

## Software and Language
To program our robot, we use the LEGO MINDSTORMS App and code in Python. Compiling and running our code is straightforward, as the app provides tools to write, test, and upload our programs directly to the LEGO Robot Inventor Hub.

## Organization of Code
Our code follows Object-Oriented Programming (OOP) principles, where we use separate classes to manage each sensor and component of our robot. We utilize the libraries provided by LEGO to interact with the electronic components.

## Chassis Class
In the Chassis class, we control the drive and steering motors. This class includes methods like drive and steer, which are used to manage the speed and direction of the motors.

Drive Method: This function controls the robot's movement, taking a speed value and adjusting the motor speeds accordingly to move the robot straight or at an angle.
Steer Method: This function adjusts the steering angle of the robot. It limits the steering angle to a specific range and applies this value to the motor controlling the direction.
## Camera Class
The Camera class interfaces with the LEGO Robot Inventor's Vision Sensor, detecting objects and processing visual data. The class includes methods to identify and track colored blocks or other objects that the sensor is programmed to recognize.

Track Object Method: This method processes the visual input from the sensor to identify and follow a specific object or color.
## Open Challenge Code
For the obstacle challenge, we use ultrasonic sensors and the Vision Sensor. Our code utilizes these sensors to avoid obstacles and navigate effectively. The code is divided into two main sections: normal navigation and turning logic.

## Normal Navigation
In the normal navigation logic, we start by checking the distance to nearby obstacles using the ultrasonic sensor. Based on this data, we adjust the robot’s speed and direction to avoid collisions.

Obstacle Detection: The ultrasonic sensor measures the distance to the nearest obstacle, and if the obstacle is too close, the robot slows down or turns to avoid it.
Object Following: When the Vision Sensor detects a specific object (e.g., a colored block), the robot adjusts its path to follow the object.
## Turning Logic
When an obstacle is detected, the turning logic is activated. The robot calculates the optimal angle to turn based on sensor data, then executes the turn smoothly to navigate around the obstacle.

Turn Calculation: The code calculates the necessary turn angle based on the position of the detected obstacle.
Execute Turn: The robot performs the calculated turn, adjusting its path to continue navigating the environment.
This version is specifically adapted for the LEGO Robot Inventor kit and reflects the programming environment and components available in this kit.
