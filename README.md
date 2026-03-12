# Modeling, shape prediction and experimental validation of a tendon-actuated continuum robot.

This project presents the modeling, shape prediction, and experimental validation of a tendon-actuated continuum robot developed during my PhD research.

## Overview

Continuum robots are promising for minimally invasive surgery and manipulation in constrained environments.  

This repository presents the modeling, shape prediction, and experimental validation of a tendon-actuated continuum robot developed during my PhD research in robotics.

The work focuses on physically-based modeling using Cosserat rod theory, reduced-order actuation modeling, and real-time shape prediction from tendon tension measurements.

## Key Contributions

- Developed a **3D nonlinear mechanical model of tendon-actuated continuum robots based on Cosserat rod theory**.
- Proposed a **shape prediction framework using actuated strain modes (ASM)** that enables direct shape reconstruction from tendon tension measurements.
- Derived an **analytical construction of an actuation-adapted strain basis** for continuum robots with arbitrary tendon routing.
- Developed an **SVD-based actuation redundancy elimination method** for tendon-driven systems.
- Designed and built a **single-segment tendon-actuated continuum robot prototype platform** for experimental validation.
- Performed **extensive experimental validation for multiple tendon routing paths (parallel, convergent, spiral)**.

## Prototype Platform

Single-segment tendon-actuated continuum robot prototype used for experiments:
![Robot](media/robot_photo.jpg)

Effector with different routing types:
![Effector](media/effector_photo.jpg)

All components of the prototype plateform were designed and built during my 1st year of my Ph.D.  

## Demo Video

Demo video of the continuum robot prototype and experiments:

[Watch the demo video](video/demo.mp4)

## Mechanical Modeling

The robot is modeled using Cosserat rod theory.  
The backbone deformation is parameterized using strain fields and reduced using modal basis functions.

The project involves:

- nonlinear Cosserat rod modeling
- establishment of reduced Lagrangian formulation based on virtual work and Lagragian mechanics
- construction of strain modal basis adapted to tendon routing
- Achievement of fast shape prediction of tendon-actuated continuum robots

## Experimental Results

Example of shape prediction results:

![result](media/result1.png)

## Applications

Potential applications include:

- Minimally invasive surgical robotics
- Flexible robotic manipulation
- Inspection in constrained industrial environments
- Exploration in aerospace

## Related Publications

Z. Zhang, M. T. Chikhaoui, V. Lebastard, F. Boyer  
Shape Reconstruction of Tendon-Actuated Continuum Robot Using Standard Proprioception  
IEEE Robotics and Automation Letters (under review)

## Contact

Zibo Zhang  
PhD in Robotics

Email: zibo.zhang@tsm-education.fr / zibo.zhang@univ-grenoble-alpes.fr / zibo.zhang@imt-atlantique.fr
