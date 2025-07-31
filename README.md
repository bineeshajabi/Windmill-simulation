# Wind Turbine Yaw Control System – Simulink Project

This repository contains a MATLAB Simulink implementation of a **yaw control system for a wind turbine**, developed as part of the ESC700P/U – Electronic Sensing module at Queen Mary University of London.

## Project Objective

To model a closed-loop control system where a wind turbine adjusts its **yaw orientation** using feedback from a **gyroscope sensor**. The goal is to rotate the turbine toward a **desired angle** using a **DC motor**, while accounting for sensor noise, filtering, and feedback control dynamics.

---

## System Overview

The control system consists of two main parts:

### 1. **Control/Actuation Subsystem**
- **Step input**: Desired yaw angle 
- **PID controller**: Controls the yaw error
- **PWM and H-bridge**: Drives the motor with appropriate signals
- **DC motor (Maxon 353294)**: Rotates the turbine

### 2. **Sensing/Processing Subsystem**
- **Gyroscope**: Measures angular velocity (with noise and bias)
- **Band-pass filter**: Removes noise and drift
- **Bias compensator**: Eliminates constant sensor offset
- **Integrator**: Converts angular velocity into yaw angle
- **Feedback**: Feeds measured yaw angle back into the PID controller

<img width="940" height="718" alt="windmill#" src="https://github.com/user-attachments/assets/41fbaa8f-ae97-4bbe-83a5-f3406d19e0a4" />
