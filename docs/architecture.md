# ROS2 Medical Lab Architecture

## Overview

ROS2 Medical Lab is a medical device simulation project built with ROS2 and Python.

The project simulates communication between medical devices in an operating room or intensive care unit (ICU).

The main objective is to learn:

* ROS2 Topics
* ROS2 Services
* ROS2 Actions
* ROS2 Parameters
* ROS2 Launch System

---

## System Components

### Patient Monitor

Simulates patient vital signs:

* Heart Rate
* SpO2
* Blood Pressure

Publishes data through ROS2 Topics.

---

### Infusion Pump

Simulates an infusion pump device.

Provides:

* Service interface
* Action interface

---

### Alarm System

Monitors patient vital signs.

Triggers alarms when values exceed predefined thresholds.

---

### Central Controller

Acts as the central management system.

Responsibilities:

* Receive patient data
* Query infusion pump status
* Send infusion commands
* Log system events

---

## System Communication

Patient Monitor
↓ Topic
Central Controller

Patient Monitor
↓ Topic
Alarm System

Central Controller
↓ Service
Infusion Pump

Central Controller
↓ Action
Infusion Pump

---

## Future Extensions

* Gazebo Simulation
* MoveIt2 Integration
* Medical Robot Arm
* Closed-loop Anesthesia System
