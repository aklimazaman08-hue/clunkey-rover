# Clunkey Rover Electronics

## Overview

Clunkey Rover will use an ESP32 as the main controller. The ESP32 will control four geared DC motors through two TB6612FNG motor drivers and use an HC-SR04 ultrasonic sensor to detect obstacles.

## Main Electronics

- ESP32 development board
- 2 × TB6612FNG motor drivers
- 4 × TT geared DC motors
- HC-SR04 ultrasonic sensor
- 4×AA battery holder and batteries
- Jumper wires and connectors

## System Connections

### ESP32 → Motor Drivers

The ESP32 will send control signals to the two TB6612FNG motor drivers.

- Motor Driver 1 controls the left-side motors.
- Motor Driver 2 controls the right-side motors.
- Each driver can control two motors.

### Motor Drivers → Motors

The four motors will provide the rover's movement.

- Driver 1 → Front-left motor
- Driver 1 → Rear-left motor
- Driver 2 → Front-right motor
- Driver 2 → Rear-right motor

The rover will use the motors to move forward, backward, and turn.

### ESP32 → Ultrasonic Sensor

The HC-SR04 ultrasonic sensor will be used to detect objects in front of the rover.

The ESP32 will read the sensor and use the distance information to decide when the rover should change direction.

The sensor's signal voltage will be checked for ESP32 compatibility before the physical build.

### Power

The planned power source is a 4×AA battery holder.

The electronics will be designed so that the power connections are appropriate for the ESP32, motor drivers, and motors.

## Basic System Diagram

Battery
↓
Motor Drivers
↓
4 Drive Motors

ESP32
├──→ Motor Driver 1
├──→ Motor Driver 2
└──→ Ultrasonic Sensor

## Design Goal

The electronics system will allow Clunkey Rover to drive using four motors while detecting obstacles with the ultrasonic sensor. The ESP32 will act as the main controller for the autonomous behavior.
