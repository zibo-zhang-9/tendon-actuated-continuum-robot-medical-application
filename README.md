# Modeling and Shape Prediction of Tendon-Actuated Continuum Robots with Experimental Validation

![PhD Research](https://img.shields.io/badge/PhD-Research_Project-blue)
![Field](https://img.shields.io/badge/Field-Continuum_Robotics-green)
![Model](https://img.shields.io/badge/Model-Cosserat_Rod-orange)

![Robot](media/IMG_20240518_163047.jpg)

This project presents the modeling, shape prediction, and experimental validation of a tendon-actuated continuum robot developed during my PhD research.

# Overview

Continuum robots are promising for minimally invasive surgery and manipulation in constrained environments.  

In such environments, continuous and accurate knowledge of the nonlinear TACR shape is essential to ensure safe guidance.Although this problem has been extensively investigated and several models have been proposed, there remains strong interest in developing
a compact model enabling fast shape prediction.

This repository presents part of my PhD research on tendon-actuated continuum robots, focusing on physically-based modeling using Cosserat rod theory, reduced-order actuation modeling, real-time shape prediction from tendon tension measurements, and experimental validation.

# Key Contributions

- Developed a **3D nonlinear mechanical model of tendon-actuated continuum robots based on Cosserat rod theory**.
- Proposed a **shape prediction framework using actuated strain modes (ASM)** that enables direct shape reconstruction from tendon tension measurements.
- Derived an **analytical construction of an actuation-adapted strain basis** for continuum robots with arbitrary tendon routing.
- Developed an **SVD-based method for eliminating actuation redundancy** for tendon-actuated continuum robots.
- Designed and built a **single-segment tendon-actuated continuum robot prototype platform** for experimental validation.
- Performed **extensive experimental validation for multiple tendon routing paths (parallel, convergent, spiral)**.

# Mechanical Modeling

The robot is modeled using Cosserat rod theory.  
The backbone deformation is parameterized using strain fields and reduced using modal basis functions.

The mechanical modeling involves:

- nonlinear Cosserat rod modeling
- establishment of reduced Lagrangian formulation based on virtual work and Lagrangian mechanics
- construction of strain modal basis adapted to tendon routing
- fast shape prediction from tendon tension measurements by avoiding iterative shooting or Newton-Raphson solvers commonly used in Cosserat-rod models.

Under the proposed actuated strain basis, the strain field can be directly expressed as:

$$
\epsilon(X) = \Phi_a(X)T
$$

The robot configuration is then obtained by integrating the Cosserat kinematics:

$$
g' = g(\xi_0 + B\epsilon)^\wedge
$$

which is referred to as our shape prediction model. 

$g(X) \in SE(3)$: pose (orientation + position) of the robot cross-section at arc-length $X$

# Prototype Platform

## System Architecture

The experimental platform integrates actuation, sensing, control, and perception modules:

- Actuation: DC motors driven by a Galil motion controller
- Proprioceptive sensing: tendon tension measurement via load cells and motor encoders
- Exteroceptive sensing: electromagnetic pose tracking using the NDI Aurora system (6-DoF sensors + reference sensor)
- Vision-based measurement: stereo camera for external shape validation and features extraction
- Real-time control and data processing implemented in MATLAB

The overall hardware architecture is illustrated below:

![Hardware Architecture](media/Hardware_architecture_prototype_2.png)

## Control Framework

A multi-loop control architecture is implemented:

- Outer loop: shape / position control
- Inner loop: tendon tension regulation
- Motor-level PID control via Galil controller

This enables stable and accurate control of the continuum robot.

![Control_loop](media/control_loop_hardware_setup_2.png)

## Sensor Setup

The robot end-effector pose are measured using: NDI Aurora electromagnetic tracking system (6-DoF), combining miniature sensors and a reference sensor to provide real-time pose estimation (position + orientation) of the robot end-effector

An example of the NDI Aurora system setup:

![NDI_sensors](media/Aurora_plug_setup_2.png)

This connection involves the use of multiplexer and amplifier for multiple sensors, and real-time data acquisition via USB interface

Technical specifications of the sensors can be found in the datasheets provided in the `/docs` folder.

## Fabrication and assembly

Example of CAD of the Effector:
![Effector](media/Untitled3.png)

Effector with different routing paths (parallel, convergent, and spiral):
![Effector](media/Effector.jpg)

This prototype was fully designed, implemented, and experimentally validated during my PhD research, covering mechanical design, embedded control, multi-sensor integration, and software development.

Single-segment tendon-actuated continuum robot prototype used for experiments:
![Robot](media/robot_photo_1.jpg)

## Human-Machine Interface

![Human-machine Interface](media/Human_Machine_Interface_GUI.png)

A custom MATLAB-based graphical user interface (GUI) was developed to enable full system operation and experimental workflow:

- System connection and status monitoring (motors, Aurora sensors, cameras, tension sensors)
- Real-time control of tendon actuation (displacement and force control modes)
- Online visualization of the robot 3D shape and simulation results
- Real-time acquisition and display of multi-sensor data (Aurora pose, tendon tension, encoder feedback)
- Integration with stereo vision system for external measurement and validation
- Interactive simulation module based on Cosserat Rod based model and using physical parameters (e.g., Young's modulus E and shear modulus G)

This interface provides a unified platform for control, sensing, simulation, and experimental validation.

# Experimental Demonstration

Dynamic demonstration (.gif): 

Continuum robot prototype using parallel routing path:

![demo](media/Deformation_Routage_Parallel.gif)

Continuum robot prototype using spiral routing path:

![demo](media/Deformation_Routage_Helicoidal.gif)

For the full experimental demonstration video, click the following link: https://youtu.be/ANYyFetR3QI

# Experimental Results

The proposed modeling and shape prediction method was experimentally validated on a continuum robot prototype with multiple tendon routing paths.

Example of shape prediction results:

![result](media/Cam_A_B_Para_Conv_Spiral_5_Configs.png)

# Applications

Potential applications include:

- Minimally invasive surgical robotics
- Inspection in constrained environments
- Flexible robotic manipulation
- Aerospace inspection robots

# Technologies Used

**MATLAB**

**Python (OpenCV)**

**Computer vision**: stereo camera calibration, image segmentation

**Mechanical Design**: CAD design (SolidWorks)

**Prototyping and Fabrication**: 3D printing (IdeaMaker), mechanical assembly, and prototype integration

**Experimental Validation**: tendon tension sensing (load cells), electromagnetic pose tracking (NDI Aurora System), cameras

# Related Publications

Z. Zhang, M. T. Chikhaoui, V. Lebastard, F. Boyer  
**Shape Prediction of Tendon-Actuated Continuum Robot Using Standard Proprioception** 
IEEE Robotics and Automation Letters (under review)

Z. Zhang  
**Modeling, Shape Prediction, and Actuation Redundancy Elimination of Tendon-Actuated Continuum Robots**  
PhD Thesis, IMT Atlantique (2026)

# Contact

Zibo Zhang  
PhD in Robotics (IMT Atlantique / Université Grenoble Alpes)

Email: zibo.zhang@imt-atlantique.fr / zibo.zhang@univ-grenoble-alpes.fr / zibo.zhang@tsm-education.fr 
