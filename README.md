# OBSTACLE-AVODING-ARDUINO-CAR-.
Introduction

An Obstacle Avoiding Arduino Car is an autonomous robotic vehicle capable of detecting obstacles in its path and navigating safely without human intervention. The system uses an ultrasonic sensor to measure distance, a servo motor to scan surroundings, and gear motors to control movement.
This project demonstrates the basic concepts of robotics, embedded systems, and sensor-based automation, making it ideal for beginners and academic projects.

Objective of the Project

The main objectives of this project are:
To design a self-navigating robotic car
To understand distance measurement using ultrasonic sensors
To implement motor control using Arduino
To develop basic decision-making logic for obstacle avoidance
To gain hands-on experience with embedded hardware components

Components Used and Description
Arduino Uno
The Arduino Uno is the main controller of the system. It processes sensor data and controls motors accordingly.
Microcontroller: ATmega328P
Operating Voltage: 5V
Digital I/O Pins: 14
PWM Pins: 6

Ultrasonic Sensor (HC-SR04)
The ultrasonic sensor is used to detect obstacles and measure distance.
Working Principle: Echo-based distance measurement
Range: 2 cm – 400 cm
Pins: VCC, Trigger, Echo, GND

Distance Formula:
Distance = (Time × Speed of Sound) / 2

3.3 Servo Motor (SG90)
The servo motor rotates the ultrasonic sensor left and right to scan the surroundings.
Rotation: 0°–180°
Control: PWM signal from Arduino
Purpose: Directional obstacle detection

 Gear Motors
Gear motors are responsible for vehicle movement.
Provide high torque at low speed
Used for forward, backward, left, and right motion
Connected via motor driver (L298N / L293D)

Jumper Wires
Used for temporary electrical connections between Arduino, sensors, and motors.


. Working Principle (Detailed)
The ultrasonic sensor emits ultrasonic waves.
Waves hit an obstacle and reflect back to the sensor.
Arduino calculates the distance using time delay.
If the distance is greater than the threshold, the car moves forward.
If an obstacle is detected:
The car stops
Servo rotates sensor left and right
Arduino compares left and right distances
The car turns toward the direction with more free space.
The process repeats continuously.


Circuit Working Explanation
Ultrasonic sensor Trigger & Echo pins are connected to Arduino digital pins.
Servo motor control pin is connected to a PWM pin.
Gear motors are connected via a motor driver module.
Arduino sends control signals based on sensor readings.
Power is supplied using battery or USB.

Algorithm (Logic Flow)
Start

Initialize pins and servo position

Measure distance using ultrasonic sensor

If distance > safe limit → Move Forward

Else:

Stop

Scan left and right

Compare distances

Turn in safer direction

Repeat
