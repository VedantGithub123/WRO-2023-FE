Aquí tienes la documentación en inglés:

---

# Documentation for WRO Future Engineers Category - LEGO Robot Inventor

## Introduction

This document details the configuration and programming of a robot based on the LEGO Robot Inventor (51515) for the "Future Engineers" category of the World Robot Olympiad (WRO). The challenge consists of two rounds: the first requires the robot to move along a square track, while the second round involves the robot detecting and avoiding obstacles of different colors, adjusting its path based on the detected color.

## Project Objective

The objective of this project is to design, build, and program a robot capable of navigating a square track and, in a second round, detecting and avoiding obstacles based on color. This involves using sensors and implementing programming logic that enables the robot to make autonomous decisions during its course.

## Challenge Description

In the "Future Engineers" category of the WRO, participants must develop a robot capable of performing specific tasks in a controlled environment. The challenge is divided into two rounds:

1. **Round 1: Square Track Navigation**  
   The robot must follow a square track, maintaining correct alignment and turning at the corners of the track.

2. **Round 2: Color-Based Obstacle Avoidance**  
   The robot must be able to detect green and red obstacles. Depending on the obstacle color, the robot should veer left (if the color is green) or right (if the color is red) before realigning and continuing its path.

## Components and Hardware Configuration

- **Main Controller**: MSHub (51515)
- **Traction Motors**: Connected to ports C and D of the MSHub, responsible for forward and backward movement.
- **Steering Motor**: Connected to port A, responsible for controlling the robot's direction.
- **Distance Sensor**: Connected to port B, used to detect the proximity of obstacles.
- **Color Sensor**: Connected to port F, used to identify the color of obstacles.

## Mechanical Design

The robot was designed using the LEGO Robot Inventor kit. The structure has been optimized to ensure stability and maneuverability on the competition track. The design includes a robust base to support the motors and sensors, focusing on keeping the center of gravity low to avoid tipping during turns.
## Programming

### Round 1: Square Track Navigation
from mindstorms import MSHub, Motor, MotorPair, ColorSensor, DistanceSensor, App
from mindstorms.control import wait_for_seconds, wait_until, Timer
from mindstorms.operator import greater_than, greater_than_or_equal_to, less_than, less_than_or_equal_to, equal_to, not_equal_to
import math

# Crear objetos
hub = MSHub()
motor_traction = Motor('C')
motor_direction = Motor('B')
sensor_ultrasonic = DistanceSensor('D')

while True:
    distance = sensor_ultrasonic.get_distance_cm()

    if distance is not None and distance <= 30:
        # Detener motor de tracción
        motor_traction.stop()
        wait_for_seconds(0.5)

        # Girar motor de dirección a la izquierda (90 grados)
        motor_direction.run_for_seconds(1, 100)
        wait_for_seconds(0.5)
        motor_direction.stop()

        # Retroceder motor de tracción por 2 segundos
        motor_traction.run_for_seconds(1.5, -35)
        wait_for_seconds(0.5)
        motor_traction.stop()

        # Ajuste fino para realinear el robot hacia la izquierda
        motor_direction.run_for_seconds(0.8, -80)# Este ajuste lo hará girar un poco hacia la derecha
        wait_for_seconds(0.5)
        motor_direction.stop()

        # Avanzar motor de tracción por 2 segundos
        motor_traction.run_for_seconds(1.7, 50)
        wait_for_seconds(0.5)
        motor_traction.stop()

        # Realinear dirección completamente a la izquierda
        motor_direction.run_for_seconds(0.5, 38)# Ajuste para alinearlo a la izquierda
        wait_for_seconds(0.5)
        motor_direction.stop()
    else:
        # Continuar avanzando si no hay objeto cercano
        motor_traction.start_at_power(100)

    # Espera un corto tiempo antes de verificar de nuevo
    wait_for_seconds(0.1)

### Round 2: Color-Based Obstacle Avoidance

```python
from mindstorms import MSHub, Motor, DistanceSensor, ColorSensor
from mindstorms.control import wait_for_seconds

# Create objects
hub = MSHub()
motor_traction = Motor('C')
motor_direction = Motor('A')
sensor_distance = DistanceSensor('B')
sensor_color = ColorSensor('F')

# Program to avoid obstacles based on detected color
while True:
    distance = sensor_distance.get_distance_cm()

    if distance is not None and distance <= 30:
        # Stop the traction motor
        motor_traction.stop()
        wait_for_seconds(0.5)

        # Detect the color of the obstacle
        color = sensor_color.get_color()

        if color == 'green':
            # Turn steering motor to the left
            motor_direction.run_for_degrees(-90, 100)
            wait_for_seconds(0.5)
        elif color == 'red':
            # Turn steering motor to the right
            motor_direction.run_for_degrees(90, 100)
            wait_for_seconds(0.5)

        # Reverse traction motor to avoid the obstacle
        motor_traction.run_for_seconds(1.5, -35)
        wait_for_seconds(0.5)
        motor_traction.stop()

        # Realign direction forward
        motor_direction.run_to_position(0, 'shortest path')
        wait_for_seconds(0.5)

        # Move traction motor forward to continue the path
        motor_traction.start_at_power(50)
        wait_for_seconds(2)
        motor_traction.stop()
    else:
        # Continue moving if no object is nearby
        motor_traction.start_at_power(75)

    # Wait a short time before checking again
    wait_for_seconds(0.1)
```



## Testing and Adjustments

### Sensor Calibration

- **Distance Sensor**: Tests were conducted to adjust the detection distance. The sensor was calibrated to detect obstacles at 30 cm, allowing the robot to react in time.
- **Color Sensor**: Tests were performed under different lighting conditions to ensure accurate detection of green and red colors.

### Movement Adjustments

Tests were carried out to calibrate the power and duration of turns as well as traction movements. Timing was adjusted according to the specific dimensions of the competition track.

### Track Testing

Multiple tests were conducted on the competition track to fine-tune the timing and sensor-based decisions. These tests allowed for optimizing the robot's performance, ensuring it successfully completed both rounds of the challenge.

## Justification of Technical Decisions

- **Sensor Selection**: The distance and color sensors were chosen due to their ability to provide critical information needed for navigation and obstacle avoidance.
- **Navigation Algorithm**: A timing-based approach was chosen for square track navigation due to its simplicity and effectiveness in a controlled environment.
- **Power Adjustments**: The traction and steering motors were carefully calibrated to ensure a balance between speed and precision.

## Performance and Results

During testing, the robot demonstrated the ability to successfully complete square track navigation and avoid obstacles based on color detection. Minor adjustments were made to the timing of turns and traction speed to improve alignment and precision in obstacle avoidance.

## Project Planning and Management

The project was divided into several phases, including mechanical design, programming, testing, and adjustments. Each phase had specific milestones and was managed with a detailed timeline to ensure all tasks were completed within the allocated time. Team collaboration was key to the project's success, with each member responsible for a specific part of the development.
