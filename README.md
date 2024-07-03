WRO Future Engineers Team TSBV Engineering Documentation
====

This repository contains engineering materials of a self-driven vehicle model participating in the WRO Future Engineers competition in the 2024 season. More information on each subcomponent of the robot is placed in the README.md files in each folder.

## Content
* `build` contains documentation about our chassis and material choice
* `photos` contains two folders where one contains the team photos and the other contains the robot photos
* `src` contains the code of control software for all components that were programmed to participate in the competition
* `strategy` contains documentation and diagrams explaining our approach to the problem
* `video` contains the video.md file with the link to a video where the driving demonstration exists


### Who We Are
Team TSBV is a group of high school students who aspire to be leaders in the future of autonomous vehicles. By taking the initiative to participate in the WRO Future Engineers challenge, we hope to gain experience in this field of engineering and problem solving. We have been exposed to many robotic and logic challenges, the objectives for this season are as follows:
- Gain knowledge in the field of autonomous vehicles.
- Expose us to the nuances of software organization (i.e. Github).
- Acquire competency in skills related to electronic components.
- Learn how to coordinate and work as a team to solve the problem with innovation and creativity.

### Our Robot & Iterations
The robot has different components, such as sensors and motors. We must understand that in order to use the sensors and motors that will be mentioned later, we need something with which we can control or connect to get the data or control the robot, for the same is used an intelogente brick which would be the LEGO MINDSTORMS EV3, which will control all the actions of the robot and will indicate the realization of others in accordance with the purpose we want to achieve, in addition, is the main component with which I will be collecting information that will be used during programming, apart from the above mentioned, there are other components and sensors that help me to collect important data, on the other hand, we have the engines, which 1 will help me to form the traction of the robot, which simply will make it move forward and backward, this goes hand in hand with another engine direction which will allow me to control the trajectory of the robot and change it. Other components of the robot are the sensors, which were selected with different objectives, starting with the ultrasonic sensor that will allow us to measure the distance of the robot with reference to an object, to use this data to prevent it from colliding with it, in addition to the color sensor that will support us in helping the robot to select which direction to move according to the condition. 
It should be noted that everything, both sensors and motors, are connected to the Smart Brick, which will control everything.
Related to the programming of what the robot must do, we have worked and practiced the rounds in different ways, given the case that the direction of rotation and position is drawn at the time, the robot is ready to face the situation wherever it starts and how it starts.
To summarize the execution of what the robot has to do, we can divide it into rounds:
- In a first round the robot, depending on the position, will usually align its direction and center itself in the middle of the track, to turn its tires at an angle that will allow it to move without going off or colliding with the track, in addition to activating the motor for a certain time that will allow it to give the same 3 laps.
- In the second round, the robot will keep in a constant cycle evaluating different factors by means of the sensors, such as the distance of the objects, as well as their color, in addition that within this cycle the robot will have conditions that will tell it when to do an action, such as turning when it is at a certain distance and knowing the direction to turn depending on the color.
