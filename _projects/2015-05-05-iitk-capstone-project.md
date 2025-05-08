---
title: "IITK - Capstone Project"
categories:
  - Projects
tags:
  - Prototyping
  - CAD
  - Robot
  - LabVIEW
  - Arduino
# author_profile: false
# layout: archive
header:
  image: /assets/images/iitm_friction_measurement_timingbelt_setup2.JPG
# toc: true
# toc_sticky: true
---

## Project Overview

During my Summer Fellowship at the Neuromechanics Lab, Department of Applied Mechanics, IIT Madras, I designed and developed a tribometer setup to study the frictional properties between human fingers and various surface materials. This project combined mechanical design, instrumentation, electronics, and software integration to create a functional system for analyzing skin-material friction coefficients.

## The Challenge

The human hand is remarkably complex in its interactions with surfaces. While Amonton's laws of friction provide a general framework for understanding friction between solid surfaces, the unique properties of human skin create interesting variations that aren't fully explained by classical friction models. 

Our objective was to create an instrument that could:
- Measure the coefficient of friction between finger digits and various test surfaces
- Analyze variations in friction with different applied forces
- Compare experimental results with theoretical friction models
- Generate reliable, repeatable measurements for scientific study

## Technical Background

Before diving into the design, I studied the fundamentals of friction mechanics and previous research in the field:

### Friction Fundamentals
- **Dry friction** resistance between two solid surfaces in contact
- **Static friction** (μs) between non-moving surfaces
- **Kinetic friction** (μk) between moving surfaces in relative motion

The classical Amonton's laws state:
- Friction force is directly proportional to applied load
- Friction force is independent of apparent contact area
- Kinetic friction is independent of sliding velocity

The mathematical model for friction follows Coulomb's equation:
```
Ff = μ × Fn
```
Where:
- Ff is the friction force
- μ is the coefficient of friction 
- Fn is the normal force

## Design Methodology

I followed an iterative design process, developing two prototypes (Alpha and Beta) with improvements based on testing and performance evaluation:

### Design Requirements
1. Measure vertical force (Fv) and horizontal force (Fh) at the finger-surface interface
2. Create controlled slip between finger and test surface
3. Record force data for friction coefficient calculation
4. Allow testing of multiple surface materials
5. Provide consistent, repeatable measurements

## Tribometer Setup Alpha

The first prototype used a linear guide mechanism inspired by printer cartridge movement:

![Tribometer Setup Alpha](/assets/images/iitm_friction_measurement_timingbelt_setup1.JPG)

### Key Components
- **Base**: 10mm wood sheet for stability and workability
- **Linear Motion System**: Precision linear guide rail with ball bearing slide block
- **Actuation**: DC geared motor (12V, 45kg-cm torque) 
- **Motion Transfer**: Timing pulley and belt system (2mm pitch)
- **Sensing**: ATI multi-dimensional force sensor
- **Control**: Arduino Uno microcontroller with LabVIEW integration
- **Power**: 12V DC power supply

### Working Principle
The test surface attached to the force sensor moves horizontally while the subject places their finger on the surface with controlled vertical force. As the motor rotates, the timing belt drives the linear slide, creating relative motion between the finger and test surface. The force sensor continuously measures both vertical force (Fv) and horizontal friction force (Fh), allowing calculation of the coefficient of friction (μ = Fh/Fv).

### Technical Challenges
During testing of Setup Alpha, I identified two main issues:
1. High friction in the linear motion system
2. Difficulty maintaining consistent tension in the timing belt

## Tribometer Setup Beta

To address these challenges, I designed Setup Beta using a capstan-bowstring mechanism:

![Tribometer Setup Beta](/assets/images/iitm_friction_measurement_capston_setup.JPG)

### Design Improvements
- **Capstan Drive**: Replaced timing belt with a stainless steel cable (1.2mm diameter) wrapped around a custom-designed capstan
- **Tension Control**: Added spring mechanism to maintain consistent cable tension
- **Movable Base**: Redesigned component to connect the cable to the slide block
- **Reduced Friction**: Modified system reduced mechanical resistance in the linear motion

### Technical Details
- **Motor**: Same 60rpm, 45kg-cm torque DC geared motor
- **Capstan**: Custom designed with 20mm diameter, V-thread groove (1.5mm pitch)
- **Linear Speed**: Approximately 6 cm/s
- **Spring Constant**: ~2 kg/cm for maintaining cable tension
- **Control System**: Same Arduino + LabVIEW integration for precise motor control and data acquisition

## Software Integration

The control and data acquisition system combined Arduino for low-level motor control with LabVIEW for the user interface and data processing:

### Arduino Development
I wrote several iterations of Arduino code to control motor direction and speed, including:
- Basic ON/OFF control
- Direction control with switch input
- Speed control using potentiometer input
- Integrated control through LabVIEW communication

### LabVIEW Interface
The LabVIEW virtual instruments (VIs) provided:
- Real-time force data visualization
- Motor speed and direction control
- Data recording and export capabilities
- Integrated experimental workflow



## Results and Analysis

With the tribometer setup, we could analyze:

1. Static coefficient of friction between finger digits and various materials
2. Changes in friction with varying normal force
3. Differences between static and kinetic friction coefficients
4. Verification of Amonton's laws for skin-surface interfaces

By plotting Fh against Fv at the moment of slip, we could determine the coefficient of friction as the slope of the resulting curve.

## Skills Applied

This project allowed me to apply and develop several technical skills:

- **Mechanical Design**: Creating custom mechanisms and selecting appropriate components
- **CAD Modeling**: Designing custom parts for the experimental setup
- **Electronics**: Motor driver circuit design and sensor integration
- **Programming**: Arduino coding and LabVIEW development
- **Data Analysis**: Processing force sensor data to calculate friction coefficients
- **Problem Solving**: Identifying issues in the first prototype and developing improvements
- **Research Application**: Implementing theoretical concepts in a practical measurement system

## Future Improvements

Based on my experience with both prototypes, I identified several potential improvements:

1. Using a motor with optical feedback for more precise position control
2. Implementing a dedicated battery power supply for portability
3. Testing different cable materials and diameters for the bowstring mechanism
4. Redesigning the movable base for better ergonomics and reduced interference
5. Adding automatic test sequencing for improved experimental reproducibility

## Conclusion

This tribometer project successfully combined principles of mechanical design, electronics, and software integration to create a functional scientific instrument. The iterative design process allowed me to identify and solve technical challenges, resulting in a system capable of measuring and analyzing the complex frictional properties between human skin and various materials.

The experience gained in this project has strengthened my skills in mechatronics system design, instrumentation, and experimental methodology—all valuable capabilities for future engineering challenges.
