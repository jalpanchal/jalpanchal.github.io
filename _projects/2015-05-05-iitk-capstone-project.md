---
title: "Innovating Robot tracking"
date: 2015-05-21 # Or the date you'd like to publish this post
categories:
  - Projects
tags:
  - Acoustics
  - Robots
  - CAD
  - Wireless-Communication
excerpt: "A deep dive into my Bachelor's thesis work on designing and developing communication and tracking modules for a Pipeline Health Monitoring Robot (PHMR) using Helmholtz resonators and ZigBee protocol."
header:
  image: /assets/images/projects/iitk_header.jpg
  teaser: /assets/images/projects/iitk_thumbnail.jpg # Optional: Add a relevant image path here
toc: false
featured: true
---

## My Bachelor's Journey into Pipeline Health Monitoring
As part of my Bachelor of Technology degree in Mechatronics Engineering at Manipal Institute of Technology, I embarked on a project to design and develop a sophisticated communication and tracking module for a Pipeline Health Monitoring Robot (PHMR). This initiative was a response to a project from Gas Authority of India Ltd. (GAIL) given to Indian Institute of Technology, Kanpur, aimed at developing a system to inspect natural gas pipelines for defects using a conduit crawler robot. My role involved creating innovative solutions for accurately locating and communicating with the robot as it navigated through pipelines.

This thesis explored two distinct yet complementary systems for tracking the PHMR's motion inside pipelines: an acoustic tracking system utilizing a Helmholtz resonator and a wireless location monitoring system leveraging ZigBee communication protocol. The goal was to provide efficient and reliable methods for monitoring the robot's live movement during operation.

## Part 1: Acoustic Tracking with Helmholtz Resonators
The first part of my project focused on developing an acoustic tracking system. Given that the PHMR would operate within natural gas pipelines, an energy-efficient solution was paramount. We decided to design a system that could generate a sound signal using the flow of the gas itself, eliminating the need for external electronic sound generation.

### The Helmholtz Resonator Concept
A Helmholtz resonator, essentially a container of gas with an open hole, vibrates due to the 'springiness' of the air inside when excited by an air jet. This principle is similar to blowing across the top of an empty bottle to produce a sound. The oscillating air in the neck acts like a mass on a spring, and the internal air volume provides the 'springiness'.

<figure class="m-figure center">
  <a href="/assets/images/projects/iitk_helmholtzresonator_process.jpg" class="popup">
    <img src="/assets/images/projects/iitk_helmholtzresonator_process.jpg" alt="Helmholtz Resonator build" />
  </a>
  <figcaption>Design and Fabrication of a Helmholtz Resonator</figcaption>
</figure>

We designed a Helmholtz resonator with a target resonant frequency of 200 Hz. This low frequency was chosen because acoustic analyses indicate that lower frequency sound signals experience less attenuation and have higher transmission across multiple media, which is crucial for signals traveling from the gas medium to the pipe wall. The resonator was intended to be embedded within the PHMR's body, generating the sound signal as the robot moved with the fuel flow.

### Experimental Insights
<figure class="m-figure center">
  <video controls autoplay muted style="max-width: 100%; height: auto; display: block; margin: 0 auto;">
    <source src="/assets/videos/iitk_phmr_hraudio.mp4" type="video/mp4">
    Your browser does not support the video tag.
  </video>
  <figcaption>Helmholtz Resonator audio test [Unmute Video]</figcaption>
</figure>

<figure class="m-figure center">
  <a href="/assets/images/projects/iitk_helmholtzresonator_fft.jpg" class="popup">
    <img src="/assets/images/projects/iitk_helmholtzresonator_fft.jpg" alt="Helmholtz Resonator FFT" />
  </a>
  <figcaption>Testing Resonance Frequency of Helmholtz Resonator</figcaption>
</figure>
Extensive experiments were conducted to understand sound propagation through pipe walls. Initial tests using a speaker as a sound source and microphones/accelerometers as receivers revealed that sound primarily propagated through the air medium, with poor transmission through the carbon steel pipe wall. High attenuation was observed when sound signals attempted to cross from air to the pipe material.

<figure class="m-figure center">
  <a href="/assets/images/projects/iitk_helmholtzresonator_jalexp.jpg" class="popup">
    <img src="/assets/images/projects/iitk_helmholtzresonator_jalexp.jpg" alt="Helmholtz Resonator testing" />
  </a>
  <figcaption>Testing of of different air flow patterns</figcaption>
</figure>
Further experiments involved using an impact hammer to generate sound directly on the pipe wall. While this confirmed sound generation within the wall, its transmission along the pipe was very poor and highly attenuated, largely due to the pipe's coating absorbing the signals. These findings underscored the necessity of a low-frequency, directly excited acoustic source like the Helmholtz resonator and led to the consideration of highly sensitive receivers (e.g., sensitive microphones placed flush with the inner pipe wall or piezoelectric strips) to capture the vibrations.



## Part 2: Wireless Location Monitoring with Odometer and Xbee
The second crucial component of the PHMR tracking system was a wireless location monitoring system. The objective was to provide live tracking of the robot's movement using wireless communication. This system integrated an odometer for distance measurement and Xbee modules for reliable wireless data transmission using the ZigBee communication protocol.
<figure class="m-figure center">
  <a href="/assets/images/projects/iitk_phmr_zigbeesetup.jpg" class="popup">
    <img src="/assets/images/projects/iitk_phmr_zigbeesetup.jpg" alt="ZigBee Odometer" />
  </a>
  <figcaption>Overview of ZigBee based location monitoring system</figcaption>
</figure>

### The Odometer and Xbee Integration
The wireless system comprised a transmitter module within the PHMR and a receiver at a base station.

- Odometer Assembly: The odometer was assembled with a wheel containing an LED on one side and a Light Dependent Resistor (LDR) on the other, designed to measure the distance traveled by the robot. This assembly was integrated into the transmission module inside the PHMR.
- Xbee Communication: Xbee Pro S1 PCB antenna modules were used for wireless communication. The transmitter part utilized an Arduino Uno R3 board with an Xbee module, while the receiver at the base station used an Intel Galileo Gen 2 board also equipped with an Xbee module. This setup allowed for continuous communication and transmission of the PHMR's location data.
<figure class="m-figure center">
  <a href="/assets/images/projects/iitk_phmr_odometersetup.jpg" class="popup">
    <img src="/assets/images/projects/iitk_phmr_odometersetup.jpg" alt="ZigBee Odometer" />
  </a>
  <figcaption>Overview of ZigBee based location monitoring system</figcaption>
</figure>
- Live Motion Tracking: The system was designed to show the live movement of the PHMR at the base station, which was critical for operational monitoring. The block diagrams illustrated how the odometer's data would be processed and transmitted wirelessly, enabling real-time tracking of the robot's position.
- This wireless module provided a robust and energy-efficient solution for tracking the PHMR, complementing the acoustic system by offering a direct method for live position updates within the pipeline.

<figure class="m-figure center">
  <video controls autoplay loop muted style="max-width: 100%; height: auto; display: block; margin: 0 auto;">
    <source src="/assets/videos/iitk_phmr_labview.mp4" type="video/mp4">
    Your browser does not support the video tag.
  </video>
  <figcaption>LabView Live motion tracking Interface</figcaption>
</figure>

## Conclusion
My undergraduate thesis successfully designed and developed two distinct yet interconnected systems for pipeline health monitoring robots: an innovative acoustic tracking system using Helmholtz resonators and a wireless location monitoring system integrating an odometer with Xbee/ZigBee communication. This work contributed to advancing non-intrusive pipeline inspection technologies, addressing the challenges of communication and tracking within complex and harsh environments like natural gas pipelines. The insights gained from the Helmholtz resonator experiments, particularly regarding sound propagation in pipes, and the successful implementation of the wireless tracking module lay a strong foundation for future developments in this field.

---
## Skills Overview
This project provided a comprehensive learning experience, allowing me to apply and enhance a range of technical and engineering skills:
- **Core Engineering Principles:** Applied knowledge of Acoustics, Fluid Dynamics, and Mechatronics for system design and analysis.
- **Design & Simulation:** Utilized CATIA V5 for CAD modeling and COMSOL Multiphysics for Finite Element Analysis (FEA) and acoustic simulations.
- **Experimental & Data Analysis:** Designed and executed experiments, performing data acquisition and signal processing (FFT analysis) using LabVIEW.
- **Embedded Systems & IoT:** Programmed microcontrollers (Arduino, Intel Galileo) and integrated hardware for real-time operation and wireless communication via ZigBee protocol.
- **System Integration & Problem Solving:** Successfully combined diverse components into a functional system, demonstrating strong troubleshooting and debugging capabilities.
- **Project Management & Documentation:** Managed project phases from concept to completion and produced comprehensive technical reports.
- **GUI Development:** Created user-friendly graphical interfaces for system monitoring.

## Research Lab and Principal Investigator
- **Institution:** Manipal Institute of Technology, Manipal University (for Bachelor of Technology) 
- **Internship Host:** Smart Material Structures and Systems (SMSS) Laboratory, Department of Mechanical Engineering, Indian Institute of Technology Kanpur 
- **Project Guide (Manipal University):** Ms. Sherine Jesna V. A. 
- **Project Guide (IIT Kanpur):** Dr. Bishakh Bhattacharya 

## Learn More:

<div class="download-button download-button--left"><a href="/assets/files/JalPanchal_UndergradThesis.pdf" class="tag">Download Undergrad Thesis PDF</a></div>

Thanks for reading! If you're interested in pipeline robotics, acoustic sensing, wireless communication, or mechatronics — feel free to reach out or browse my other projects.