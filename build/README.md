Build
====

To build our robot, we used the Lego Mindstorms EV3 kit and some additional elements. The list of materials is detailed below:
Lego Mindstorms EV3 Kit:
Programable Block EV3 Engine EV3 Large Sensors (not used in this project)
Standard Wheels Lego
Structural parts of Lego
Axis and connectors Lego
Rechargeable battery EV3 Connection CablesAdditional Items:
Additional Lego parts for structural reinforcement (if necessary)
Basic construction tools (optional, to facilitate assembly)

## Chassis Type & Explanation

Our robot is a four-wheeled vehicle which has a rear-wheel drive with steering in the front. We decided to implement a simple chassis since that would reduce the amount of complexity, and therefore chances of failure. In order to keep the drivetrain simple and efficient, we made sure not to have the steering mechanism on the same set of wheels as the driving wheels. This solves the problem of spacing, as the steering motor and the drive motors do not have to be on the same set of wheels. Our decision to do this meant that we could only have two options for driving which were front-wheel drive with steering in the back or a rear-wheel drive with steering in the front. We ultimately chose a drivetrain that had real-wheel drive with front-wheel steering as that made the robot more familiar to use, given our experience using other rear-wheel driven LEGO robots.


## Steering

Management System

Principle of Differential Direction

We use the principle of differential direction to control the movement of the robot. This system does not require a separate steering mechanism, but adjusts the speed of each engine to rotate.

Operation
Straight motion: To move the robot in a straight line, both engines rotate at the same speed.
Left rotation: To rotate to the left, the right motor rotates faster than the left motor.
Right rotation: To rotate to the right, the left engine rotates faster than the right engine


## Movement
Movement Calculation

Without the use of sensors, we rely on accurate calculations to control the movement of the robot. We use the rotation degrees of the engines to determine the distance traveled and the time required for each movement.

Distance formula
Distance=Wheel Circumference×Engine Revolutions


## Materials
Construction Steps

Installation of the EV3 Block: We place the programable EV3 block in the center of the structure to maintain a proper balance.

Engine Installation: We use two large EV3 engines, one for each rear wheel. This provides us with the power needed to move the robot and the ability to control each wheel separately for direction.

Wheel Fixation: We place standard Lego wheels on the axles connected to the engines. We fasten the front wheels to provide stability.

Chassis Structure: We use Lego structural parts to create a robust chassis that supports the weight of the EV3 block and the engines. We ensure that the chassis has enough space for the installation of the battery and the necessary wiring.

Cable and Connections: We connect the engines to the EV3 block using the cables provided in the kit. We make sure the cables are properly subjected and organized to avoid clutches.
