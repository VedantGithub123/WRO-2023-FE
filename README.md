WRO Future Engineers Team TSBV Engineering Documentation
====

This repository contains engineering materials of a self-driven vehicle model participating in the WRO Future Engineers competition in the 2024 season. More information on each subcomponent of the robot is placed in the README.md files in each folder.

This repository contains engineering materials for a self-driven vehicle model participating in the WRO Future Engineers competition in the 2024 season. The build folder contains documentation about our chassis and material choices. The photos folder has two subfolders: one with team photos and another with robot photos. The src folder contains the control software code for all components programmed for the competition. The strategy folder includes documentation and diagrams explaining our approach to the problem. Lastly, the video folder includes the video.md file with the link to a driving demonstration video.
## Content
* `build` contains documentation about our chassis and material choice
* `photos` contains two folders where one contains the team photos and the other contains the robot photos
* `src` contains the code of control software for all components that were programmed to participate in the competition
* `strategy` contains documentation and diagrams explaining our approach to the problem
* `video` contains the video.md file with the link to a video where the driving demonstration exists


### Who We Are
Team TSBV is a group of high school students aspiring to be future leaders in autonomous vehicle technology. By participating in the WRO Future Engineers challenge, we aim to gain valuable experience in engineering and problem-solving. Our objectives for this season include gaining knowledge in the field of autonomous vehicles, becoming familiar with software organization (e.g., GitHub), developing skills related to electronic components, and learning to coordinate and work as a team to solve problems with innovation and creativity.:
- Gain knowledge in the field of autonomous vehicles.
- Expose us to the nuances of software organization (i.e. Github).
- Acquire competency in skills related to electronic components.
- Learn how to coordinate and work as a team to solve the problem with innovation and creativity.

### Our Robot & Iterations
The robot comprises various components, including sensors and motors. The EV3 Intelligent Brick serves as the main controller, managing the motors and sensors and executing the programmed code. It connects via USB, Bluetooth, and Wi-Fi (with an additional adapter) and has four motor ports and four sensor ports. The motors include a traction motor for forward and backward movement and a steering motor to control the robot's trajectory. Among the sensors, the ultrasonic sensor measures the distance between the robot and objects, helping to avoid collisions, while the color sensor detects colors and aids the robot in making directional decisions based on environmental conditions.
The robot has different components, such as sensors and motors. We must understand that in order to use the sensors and motors that will be mentioned later, we need something with which we can control or connect to get the data or control the robot, for the same is used an intelogente brick which would be the LEGO MINDSTORMS EV3, which will control all the actions of the robot and will indicate the realization of others in accordance with the purpose we want to achieve, in addition, is the main component with which I will be collecting information that will be used during programming, apart from the above mentioned, there are other components and sensors that help me to collect important data, on the other hand, we have the engines, which 1 will help me to form the traction of the robot, which simply will make it move forward and backward, this goes hand in hand with another engine direction which will allow me to control the trajectory of the robot and change it. Other components of the robot are the sensors, which were selected with different objectives, starting with the ultrasonic sensor that will allow us to measure the distance of the robot with reference to an object, to use this data to prevent it from colliding with it, in addition to the color sensor that will support us in helping the robot to select which direction to move according to the condition. 
It should be noted that everything, both sensors and motors, are connected to the Smart Brick, which will control everything.
Related to the programming of what the robot must do, we have worked and practiced the rounds in different ways, given the case that the direction of rotation and position is drawn at the time, the robot is ready to face the situation wherever it starts and how it starts.
To summarize the execution of what the robot has to do, we can divide it into rounds:
- In a first round the robot, depending on the position, will usually align its direction and center itself in the middle of the track, to turn its tires at an angle that will allow it to move without going off or colliding with the track, in addition to activating the motor for a certain time that will allow it to give the same 3 laps.
- In the second round, the robot will keep in a constant cycle evaluating different factors by means of the sensors, such as the distance of the objects, as well as their color, in addition that within this cycle the robot will have conditions that will tell it when to do an action, such as turning when it is at a certain distance and knowing the direction to turn depending on the color.
- 
### Execution Strategy
The robot's operation can be divided into different rounds. In the first round, the robot aligns itself in the center of the track and adjusts its tires at an angle that allows it to move without veering off or colliding with the track, activating the motor for a set time to complete three laps. In the second round, the robot enters a constant cycle, evaluating factors such as object distance and color. Based on this data, the robot performs specific actions, such as turning at a certain distance and determining the direction of the turn based on the detected color.

### Conclusion
The design and programming of our robot focus on precision and adaptability. By using sensors and motors controlled by the EV3 Intelligent Brick, our robot is prepared to handle various situations and meet the challenges of the WRO Future Engineers with efficiency and creativity.

### Demonstration Video
To see the robot in action, check the video.md file in the video folder for the link to our driving demonstration.

### Additional Features and Improvements
To enhance our robot's performance and functionality, we have incorporated several additional features:

Advanced Algorithms: We have developed sophisticated algorithms to improve the robot's decision-making capabilities. These include obstacle avoidance, path planning, and real-time adjustments based on sensor feedback.

Modular Design: The robot is built with a modular design, allowing easy upgrades and replacements of components. This flexibility ensures that we can quickly adapt to new challenges or integrate better technologies as they become available.

Battery Management: Efficient battery management systems have been implemented to ensure that the robot maintains optimal power levels throughout its operation. This includes monitoring battery health and implementing energy-saving protocols.

Data Logging and Analysis: The robot is equipped with a data logging system that records sensor data and performance metrics. This data is analyzed to refine our strategies and improve the robot's efficiency in subsequent runs.

User Interface and Remote Control: We have developed a user-friendly interface and remote control capabilities, allowing us to monitor and control the robot's operations from a distance. This feature is particularly useful during testing and fine-tuning phases.


### Future Goals
As we continue to develop our skills and knowledge, we have set several future goals:

Enhanced Autonomy: Improve the robot's autonomous capabilities to handle more complex environments and tasks without human intervention.

Integration with AI: Explore the integration of artificial intelligence to enhance the robot's learning and adaptive behaviors.

Collaboration and Knowledge Sharing: Collaborate with other teams and share our findings to contribute to the broader community of autonomous vehicle enthusiasts and researchers.

By continuously pushing the boundaries of what our robot can achieve, we aim to stay at the forefront of autonomous vehicle technology and inspire others to pursue innovation in this exciting field.
