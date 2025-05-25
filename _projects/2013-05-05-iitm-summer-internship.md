---
title: "Unveiling the Science of Touch"
categories:
  - Projects
tags:
  - Motion-Sensing
  - CAD
  - Nueromotor-Disability
  - LabVIEW
  - Arduino
  - Prototyping
# author_profile: false
layout: single
header:
  image: /assets/images/projects/iitm_header.JPG
  teaser : /assets/images/projects/iitm_thumbnail.JPG
toc: false
# toc_sticky: true
# featured: true
math: true
---

## Unveiling the Science of Touch: My Summer Foray into Skin Friction Measurement at IIT Madras
During my Summer Fellowship at the Neuromechanics Lab, Department of Applied Mechanics, Indian Institute of Technology Madras, I undertook a compelling project: the design and development of a novel tribometer apparatus to investigate the frictional properties between human digits and various surface materials. This endeavor constituted a comprehensive integration of mechanical design principles, precision instrumentation, electronic systems, and seamless software integration, culminating in a functional system for the quantitative analysis of skin-material friction coefficients.

### The Challenge: Quantifying the Elusive Force of Friction
The interaction of the human hand with surfaces presents a remarkably intricate biomechanical phenomenon. While classical Amonton's laws of friction provide a foundational framework for solid-solid interfaces, the inherent viscoelastic and topographical characteristics of human skin introduce complexities not fully elucidated by traditional models. Our primary objective was to engineer an instrument capable of:

- Measuring the coefficient of friction between finger digits and diverse test surfaces.
- Analyzing the variation in friction as a function of applied normal forces.
- Comparing empirical results with theoretical friction models.
- Generating reliable and repeatable measurements essential for rigorous scientific inquiry.

This necessitated a system capable of precisely quantifying both the normal force ($F_{\nu}$) exerted by the digit and the tangential frictional force ($F_f$) at the onset of slip, thereby enabling the accurate calculation of the coefficient of friction ($\mu=\frac{F_f}{F_{\nu}}$) 


### Iterative Design: From Concept to Refined Prototype
I adopted a rigorous iterative design methodology, developing two distinct prototypes – Alpha and Beta – with continuous enhancements derived from systematic testing and performance evaluation. This approach was instrumental in refining the system's accuracy, robustness, and overall operational efficacy.

### Tribometer Setup Alpha: The Initial Foray
<figure class="m-figure center">
  <a href="/assets/images/projects/iitm_friction_measurement_alpha.JPG" class="popup">
    <img src="/assets/images/projects/iitm_friction_measurement_alpha.JPG" alt="Setup Alpha" />
  </a>
  <figcaption>Setup Alpha using a timing belt and pulley</figcaption>
</figure>
My initial prototype, designated "Setup Alpha," employed a linear guide mechanism, drawing conceptual inspiration from the precision linear motion systems commonly found in printer cartridges.

- Mechanical Design & Actuation: I engineered a system utilizing a DC geared motor (12V, 45kg-cm torque, 60rpm) to actuate a timing pulley and belt system, which in turn translated a linear slide. This slide was equipped with an ATI multidimensional force sensor for the acquisition of critical force data. The structural base comprised a stable 10mm wood sheet, selected for its material properties conducive to prototyping and stability.
- Control System Integration: I developed Arduino code for motor direction and speed control, subsequently integrating this with a LabVIEW graphical user interface. This integration facilitated intuitive control and real-time data acquisition from the force sensor, thereby demonstrating my capability to interface hardware and software components effectively.

During the evaluation phase, Setup Alpha revealed two principal areas for improvement: significant parasitic friction within the linear motion system itself and challenges in maintaining consistent tension in the timing belt. These observations provided critical insights for the subsequent design iteration.

<figure class="m-figure center">
  <a href="/assets/images/projects/iitm_friction_measurement_timingbelt_setup2.JPG" class="popup">
    <img src="/assets/images/projects/iitm_friction_measurement_timingbelt_setup2.JPG" alt="Setup Alpha" />
  </a>
  <figcaption>Setup Alpha with LabVIEW Interface</figcaption>
</figure>

### Tribometer Setup Beta: Innovation through Iteration
To mitigate the limitations identified in Setup Alpha, I conceptualized and developed "Setup Beta," which ingeniously incorporated a capstan-bowstring mechanism. This represented a substantial redesign aimed at achieving smoother motion and superior tension control.
<figure class="m-figure center">
  <a href="/assets/images/projects/iitm_friction_measurement_capstan_setup.JPG" class="popup">
    <img src="/assets/images/projects/iitm_friction_measurement_capstan_setup.JPG" alt="Setup Alpha" />
  </a>
  <figcaption>Setup Beta using a custom capstan and bowstring</figcaption>
</figure>

- Refined Mechanical Design: In Beta, a custom-designed capstan featuring a V-thread groove (20mm diameter, 1.5mm pitch) was affixed to the motor shaft. This capstan wound and unwound a 1.2mm diameter stainless steel rope, functioning as the "bowstring." This rope was securely attached to a movable base, ensuring precise linear displacement of the slide block and the integrated force sensor.
- Tension Control & Stability: A strategically positioned spring mechanism maintained consistent cable tension, resulting in a significant reduction in mechanical resistance compared to the timing belt system. This demonstrated my ability to diagnose and implement sophisticated mechanical solutions.
- Achieved Performance: This refined apparatus achieved a linear speed of approximately 6 cm/s, enabling reliable slip measurement under controlled conditions.

### Software Integration: The Brain of the System
The control and data acquisition architecture of the tribometer seamlessly combined Arduino for low-level motor control with LabVIEW for a robust user interface and comprehensive data processing.
- Arduino Development: I authored several iterations of Arduino code, encompassing functionalities from basic ON/OFF control to sophisticated speed and direction modulation, ultimately integrating these for seamless communication with LabVIEW. This work underscored my proficiency in microcontroller programming.
- LabVIEW Interface: The LabVIEW Virtual Instruments (VIs) I developed provided:
  - Real-time force data visualization.
  - Precise motor speed and direction control.
  - Robust data recording and export capabilities.
  - An integrated experimental workflow, thereby streamlining the entire measurement process.This demonstrates my competency in graphical programming and the creation of intuitive human-machine interfaces.

### Results and Analysis: Quantifying the Unseen
With the fully functional tribometer, we were able to conduct rigorous quantitative analysis, yielding valuable insights:
- Determination of the static coefficient of friction between human finger digits and various material surfaces.
- Analysis of the relationship between friction coefficients and varying normal forces.
- Differentiation between static and kinetic friction coefficients.
- Crucially, empirical verification of Amonton's laws for skin-surface interfaces, notwithstanding the unique properties of human skin.

By plotting the horizontal friction force ($F_h$) against the vertical normal force ($F_{\nu}$)at the moment of slip, the coefficient of friction was precisely ascertained as the slope of the resultant curve.

## Looking Ahead
This IIT Madras summer research project represents an invaluable cornerstone in my engineering trajectory. It not only deepened my comprehension of tribology and biomechanics but also solidified my practical engineering skills within a real-world research context. The comprehensive experience gained in designing, constructing, troubleshooting, and validating these systems will be instrumental in future endeavors spanning robotics, biomechanics, and mechatronics. I am particularly enthusiastic about the potential of such systems to contribute to a more profound understanding of human-machine interaction and to inform the design of more intuitive and effective robotic interfaces.

---
## Skills Overview
This project constituted an immersive experience that facilitated the application and significant development of a robust set of technical competencies:
- **Mechatronics System Design & Prototyping:** From conceptualization to physical realization, I designed and constructed complex electromechanical systems employing diverse materials and mechanisms (e.g., timing belts, capstan-bowstring).
- **CAD Modeling:** I utilized CAD software for the design of custom components for the experimental setup, ensuring precision and manufacturability.
- **Robotics & Control Systems:** My work encompassed programming microcontrollers (Arduino Uno) and integrating them with graphical programming environments (LabVIEW) for precise motor control and system automation.
- **Sensor Integration & Data Acquisition:** I acquired practical experience working with ATI multidirectional force sensors for accurate force measurement and establishing reliable data logging protocols.
- **Problem Solving & Iterative Development:** I systematically identified design deficiencies in initial prototypes and implemented effective corrective solutions, thereby demonstrating a strong iterative development mindset.
- **Electronics & Circuit Design:** I was responsible for the design of motor driver circuits and the overall integration of sensors within the electrical system.
- **Data Analysis & Scientific Rigor:** I processed raw force sensor data to compute friction coefficients, ensuring the scientific validity and integrity of the measurements.
- **Research Application:** I successfully translated abstract theoretical concepts of friction into a tangible, functional measurement system.

## Research Lab and Principal Investigator
- **Lab Name:** Neuromechanics Lab (the BRAIN Lab Now)
- **Department:** Department of Applied Mechanics
- **Principal Investigator:** Dr. Varadhan S.K.M.
- **Institution:** Indian Institute of Technology, Madras