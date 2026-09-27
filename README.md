# Universal ATV with Multi-purpose Detachable Modules

<p align="center">
  <img src="Poster.png" alt="Universal ATV Project Poster" width="900">
</p>

## Overview

This project presents a four-tracked, remotely operated ATV with independent spring-integrated suspension and a standardized modular payload interface.

The same base vehicle can be reconfigured for different applications, such as agricultural spraying, soil sensing, surveillance, reconnaissance, and robotic manipulation, without modifying the primary drivetrain or electronics.

The mechanical system was developed in SolidWorks, with structural validation performed using ANSYS Structural. The electronics architecture uses a Raspberry Pi 4 and ESP32, while the complete system is simulated using ROS 2 and Gazebo.

## Key Features

- Four-track remotely operated ATV
- Independent spring-integrated suspension
- Modular payload interface
- Skid-steering mechanism
- Custom-designed chassis
- Laser-cut wooden structural components
- FDM 3D-printed PLA brackets and mounting components
- ANSYS Structural FEA validation
- Raspberry Pi 4 + ESP32 control architecture
- Four-motor drive system using BTS7960 motor drivers
- ROS 2 and Gazebo simulation

## Mechanical Design

The chassis was designed around off-the-shelf track modules while keeping the remaining mechanical components custom-designed.

The main chassis structure was manufactured using laser-cut wood, while precision brackets and mounting fixtures were produced using FDM 3D printing with PLA.

The chassis incorporates dedicated suspension spring holders and a modular top interface for future payload configurations.

## Structural Analysis

Static Finite Element Analysis was performed using ANSYS Structural to evaluate the structural integrity of the main load-bearing components.

A distributed payload of 19.6 N was applied to the wooden upper body, while approximately 4.9 N was applied to the PLA track connectors.

Maximum deformation obtained from the analysis:

| Component | Maximum Deformation |
|---|---:|
| Wooden upper body | 1.6693 × 10⁻⁵ m |
| PLA track connectors | 1.277 × 10⁻⁷ m |

## Electronics & Control

The control architecture is divided into two layers:

### Raspberry Pi 4

- High-level control
- Wi-Fi communication
- Live camera streaming
- UART communication with ESP32

### ESP32

- Real-time motor control
- PWM generation
- Four-motor control
- BTS7960 motor-driver interface

## Gazebo & ROS 2 Simulation

The ATV was modeled and simulated in Gazebo using ROS 2.

The current implementation uses the Gazebo TrackedVehicle System Plugin to represent tracked motion. The commanded linear and angular velocities are converted into differential velocities for the left and right tracks.

Alternative approaches considered include:

- Discrete Link Method
- TrackedVehicle System Plugin
- Pseudo-Track Method

## Repository Contents

```text
CAD/
├── SolidWorks Parts & Assemblies
├── STEP Files
├── IGES Files
└── STL Files

Chassis_Images/
└── Design and fabrication images

Poster.png
└── Project poster