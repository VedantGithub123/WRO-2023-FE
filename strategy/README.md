## Strategyyyyyyyyyyyyyy

This directory consists of an explanation and diagrams of our strategy for both the open and obstacle rounds.

## Open Challenge Strategy

🥸 In the open challenge, our approach focuses on simplicity and precision. Since the primary variable is the size of the interior walls, our strategy is to have the robot follow a square path while maintaining consistent alignment and timing for turns. We have calibrated the robot to turn at precise angles and distances to navigate the square track efficiently. Our method involves continuous movement along the edges of the square, with the robot adjusting its path at each corner using pre-programmed degrees of rotation.

To ensure success, we've tested the robot extensively, fine-tuning the timing and motor power for each segment of the path. By consistently repeating this process, the robot can complete the required laps without colliding with the walls or deviating from the track. The strategy is straightforward but effective, relying on accurate calibration and consistent performance. Diagrams and flowcharts demonstrating the process are included below.

## Obstacle Challenge Strategy

For the obstacle challenge, we have developed a two-pronged strategy to tackle the varying obstacle arrangements. We are using both approaches simultaneously to determine which is more effective during the competition. The color sensor will play a crucial role in detecting and reacting to obstacles, while the distance sensor will help the robot navigate safely.

### Strategy 1

💡💡 The first strategy involves a reactive approach where the robot responds to each obstacle as it is detected. The robot will use its color sensor to identify the color of the obstacle and execute a corresponding turn—left for green and right for red. The robot will then realign itself and continue on the path. This method allows for real-time decision-making, ensuring that the robot can adapt to different obstacle configurations quickly. We are using a straightforward control loop to adjust the steering based on the detected obstacle, ensuring smooth and efficient movement around the obstacles. (Lol)

### Strategy 2

Our second strategy is a pre-planned path approach where the robot is programmed to follow a specific path that avoids obstacles. Using the distance sensor to detect obstacles in advance, the robot will adjust its trajectory before reaching the obstacle. This involves mapping out a series of waypoints on the mat, which the robot will follow while making calculated adjustments to avoid obstacles. By using this method, the robot can navigate the course with minimal interruption, maintaining a steady pace and reducing the need for sudden, sharp turns. This strategy is ideal for a more controlled environment where obstacles are relatively static and predictable.

Both strategies will be tested extensively, and the best-performing method will be refined for the final competition. 
