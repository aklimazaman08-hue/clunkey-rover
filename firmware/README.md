# Firmware Design

## Overview

The Clunkey Rover will use an ESP32 as its main controller. The firmware will control the four drive motors and read information from the HC-SR04 ultrasonic sensor.

The goal is to allow the rover to move independently and respond to obstacles in its path.

## Planned Robot Behavior

The firmware will allow the rover to:

1. Move forward.
2. Move backward when needed.
3. Turn left.
4. Turn right.
5. Stop the motors.
6. Read the ultrasonic sensor.
7. Detect when an obstacle is nearby.
8. Change direction when an obstacle is detected.

## Autonomous Logic

The basic autonomous behavior will follow this process:

- Start the rover.
- Move forward.
- Continuously check the ultrasonic sensor.
- If the path is clear, continue moving forward.
- If an obstacle is detected, stop.
- Choose a new direction.
- Turn and continue moving.

## Motor Control

The ESP32 will send control signals to the two TB6612FNG motor drivers.

- Motor Driver 1 controls the left-side motors.
- Motor Driver 2 controls the right-side motors.
- The left and right motor groups will be controlled together to allow the rover to move and turn.

## Sensor Control

The HC-SR04 ultrasonic sensor will provide distance information to the ESP32.

The ESP32 will use this information to determine whether the rover's path is clear or whether it needs to change direction.

## Planned Firmware Structure

The firmware will eventually contain functions for:

- Forward movement
- Reverse movement
- Left turn
- Right turn
- Stopping
- Reading distance
- Obstacle detection
- Autonomous decision-making

## Current Status

The firmware is currently in the planning stage. The control logic will be tested and refined after the physical electronics are available.
