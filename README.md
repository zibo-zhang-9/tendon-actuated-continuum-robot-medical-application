# Modeling, shape prediction and experimental validation of a tendon-actuated continuum robot.

![PhD Research](https://img.shields.io/badge/PhD-Research_Project-blue)
![Field](https://img.shields.io/badge/Field-Continuum_Robotics-green)
![Model](https://img.shields.io/badge/Model-Cosserat_Rod-orange)

![Robot](media/robot_photo.jpg)

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

All components of the prototype platform were designed and built during the first year of my PhD.

## Demo Video

Demo video of the continuum robot prototype and experiments:

[Watch the demo video](video/demo.mp4)

## Mechanical Modeling

The robot is modeled using Cosserat rod theory.  
The backbone deformation is parameterized using strain fields and reduced using modal basis functions.

The project involves:

- nonlinear Cosserat rod modeling
- establishment of reduced Lagrangian formulation based on virtual work and Lagrangian mechanics
- construction of strain modal basis adapted to tendon routing
- fast shape prediction from tendon tension measurements by avoiding iterative Newton-Raphson solvers

Under the proposed actuated strain basis, the strain field can be directly expressed as:

$$
\epsilon(X) = \Phi_a(X)T
$$

The robot configuration is then obtained by integrating the Cosserat kinematics:

$$
g' = g(\xi_0 + B\epsilon)^\wedge
$$

## Experimental Results

The proposed modeling and shape prediction method was experimentally validated on a continuum robot prototype with multiple tendon routing configurations.

Example of shape prediction results:

![result](media/result1.png)

## Applications

Potential applications include:

- Minimally invasive surgical robotics
- Inspection in constrained environments
- Flexible robotic manipulation
- Aerospace inspection robots

## Repository Structure

/model        → Cosserat rod modeling implementation  
/experiments  → experimental data processing  
/media        → images and figures used in README  
/video        → demonstration videos  

## Technologies Used

**MATLAB**

**Python**

**Computer vision** (stereo camera calibration, image segmentation)

**Mechanical Design** [CAD design (SolidWorks)]

**Prototyping and Fabrication** [3D printing (IdeaMaker), mechanical assembly, and prototype integration]

**Experimental Validation** – sensor integration (tension sensor, electromagnetic pose sensor, cameras), tendon actuation systems, and experimental 

## Related Publications

Z. Zhang, M. T. Chikhaoui, V. Lebastard, F. Boyer  
**Shape Prediction of Tendon-Actuated Continuum Robot Using Standard Proprioception** 
IEEE Robotics and Automation Letters (under review)

Z. Zhang  
**Modeling, Shape Prediction, and Actuation Redundancy Elimination of Tendon-Actuated Continuum Robots**  
PhD Thesis, IMT Atlantique (2026)

## Contact

Zibo Zhang  
PhD in Robotics (Université Grenoble Alpes / IMT Atlantique)

Email: zibo.zhang@tsm-education.fr / zibo.zhang@univ-grenoble-alpes.fr / zibo.zhang@imt-atlantique.fr
