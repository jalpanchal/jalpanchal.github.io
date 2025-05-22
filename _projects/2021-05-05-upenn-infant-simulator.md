---
title: "Robotics for Early Neuromotor Assessment"
categories:
  - Projects
tags:
  - Robotics
  - Computer Vision
  - Keras
  - Python
# author_profile: false
# layout: archive
header:
  image: /assets/images/iitm_friction_measurement_timingbelt_setup2.JPG
  teaser: /assets/images/projects/upenn_infantsim_thumbnail.png
toc: false
# toc_sticky: true
featured : true
expet: "Exploring the development of a robotic infant simulator for quantitative assessment of neuromotor development, integrating mechanical design, kinematics, and computer vision."
---

## Building a Robotic Infant: Advancing Early Neuromotor Assessment
During my independent study at the University of Pennsylvania, I had the incredible opportunity to design and build a robotic infant simulator. This project was a crucial step towards creating accessible and quantitative tools for the early diagnosis of developmental disorders like Cerebral Palsy (CP), blending my expertise in robotics, computer vision, and biomechanics.

## The Clinical Need: Quantitative Assessment for Developmental Delays
Developmental disorders are a major cause of childhood disability. Early diagnosis and intervention are key to improving patient quality of life. Current neuromotor assessment often relies on subjective expert evaluations, which can be limited in accessibility and consistency. Our goal was to develop a system that could accurately measure infant movements and their corresponding Center of Pressure (COP) changes – a vital biomarker for postural control and potential neuromotor delays. The challenge? Obtaining consistent, repeatable movements from human infants for systematic research is exceptionally difficult.

## My Solution: A 4-DOF Robotic Infant Simulator
To overcome this, I engineered a novel 4-Degree of Freedom (DOF) pediatric robot simulator. This robot is capable of mimicking simple arm and leg movements of an infant lying supine, providing a controlled and repeatable platform to investigate how variations in body size, weight, and limb movements affect COP. This simulator seamlessly integrates with the existing PANDA (Play And Neuro-Development Assessment) Gym system at the Rehabilitation Robotics Lab at UPenn.

## Technical Deep Dive: My Capabilities in Action
This project was a comprehensive exercise in robotic system development, demonstrating several key technical proficiencies:

## Mechanical Design & Fabrication
- Realistic Foundation: I selected a 559 mm (22-inch) silicone infant simulator as the base, prioritizing its realistic size and appearance for meaningful simulation.
- Precision Actuation: Each limb was actuated with 1-DOF using Dynamixel XC430-W240-T servo motors. Their 1.9 Nm stall torque, metal gears, and precise control were critical for accurately simulating infant limb accelerations.
- Custom Structure: I designed and 3D-printed a custom PLA plastic torso to house the electronics, provide a stable motor mount, and ensure limbs moved along defined planes. Hip angles were fixed at 60° for leg movements, and arm movements were parallel to the sagittal plane.
- Biomechanical Fidelity: To represent infants of different ages (0-6 months), the simulator's total weight could be adjusted from 1.9 kg to 8 kg by filling the hollow limbs with sand and adding mass to the head and torso. This meticulous attention to detail was vital for replicating infant biomechanics.

## Kinematics and Modeling
- Forward Kinematics (FK) Model: I developed a robust FK model for each limb using the Denavit-Hartenberg (DH) convention. This allowed for precise calculation of joint locations and accurate prediction of the Center of Mass (COM) for various limb angles, providing essential ground truth data for simulator movements.
- Coordinate Transformations: Complex transformations were implemented to seamlessly shift joint references from individual limb frames to the simulator's frame, and subsequently to the PANDA Gym's mat frame, ensuring accurate spatial mapping and integration.

## Sensor Integration and Data Acquisition
- PANDA Gym Integration: The simulator was integrated with the PANDA Gym, which features a 610x610 mm pressure-sensitive mat equipped with four load cells for 60 Hz COP measurement.
Visual Data Capture: A GoPro Hero 4 Session camera captured video at 1080p, 30 fps, providing crucial visual data for subsequent computer vision analysis.
- Synchronized Data Streams: Data from motor joint positions (12.5 Hz), camera video, and pressure mat COP were carefully synchronized and recorded, enabling comprehensive, multi-modal analysis.

## Computer Vision and Data Analysis
- Pose Estimation with OpenPose: The system leveraged OpenPose for camera-based pose detection. This was a critical component for predicting COP changes directly from visual data, demonstrating the potential for non-invasive assessment.
- Multi-Modal Comparison: My study involved a rigorous 3-way comparison between the simulator's ground truth position, pressure mat COP data, and computer-vision pose detection. This allowed for a deep understanding of the factors influencing limb joint positions and their correlation with COP.
- Validation of Computer Vision: The results were highly promising, demonstrating a high correlation (r=0.79) between camera-predicted joint positions and COP location for movements along the caudal-cephalic axis. This strongly supports the feasibility of predicting COP from a computer-vision system.

## Impact and Future Directions
This project represents a significant contribution to the development of quantitative and low-cost tools for early neuromotor assessment. The robotic infant simulator now serves as a robust and repeatable platform for future controlled experiments, allowing researchers to further refine the intricate relationship between infant movement and critical biomechanical indicators of neurodevelopmental health.

## Research Lab and Principal Investigator

- **Lab Name:** <a href="https://www.med.upenn.edu/rehabilitation-robotics-lab/">Rehabilitation Robotics Lab</a>
- **Principal Investigator:** Dr. Michelle Johnson
- **Institution:** University of Pennsylvania

## Learn More: Publication

<b>Panchal J</b>, Sowande OF , Prosser L, Johnson MJ. <b>Design of pediatric robot to simulate infant biomechanics for neuro-developmental assessment in a sensorized gym.</b> Proc IEEE RAS EMBS Int Conf Biomed Robot Biomechatron. 2022 Aug;2022:10.1109/biorob52689.2022.9925371 <a href="https://pubmed.ncbi.nlm.nih.gov/37041966/">Link</a>