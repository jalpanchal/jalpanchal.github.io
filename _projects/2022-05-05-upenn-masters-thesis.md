---
title: "Unlocking Brain and Body Signals"
date: 2022-05-21 # Or the date you'd like to publish this post
categories:
  - Projects
tags:
  - Wearables
  - ECG
  - EEG
  - Apple Watch
  - Fitbit
  - Neuroscience
excerpt: "A deep dive into my Master's thesis work on understanding and monitoring behavioral states in seizure patients using network neuroscience and wearable devices."
header:
  image: "/assets/images/projects/upenn_thesis_part1_methods2.png"
  teaser: /assets/images/projects/upenn_thesis_thumbnail.png # Optional: Add a relevant image path here
  # You might want to create an image for your thesis post, e.g., a brain network or a wearable device graphic.
toc: false
featured: true
---
## My Master's Journey into Seizure Monitoring

As part of my Master's thesis in Robotics at the University of Pennsylvania, I embarked on a fascinating journey to explore how we can better understand and monitor behavioral states in seizure patients. This work combined cutting-edge network neuroscience with practical insights from everyday wearable devices like the Apple Watch. The ultimate goal is to move towards providing real-time behavioral feedback for individuals living with epilepsy.

<p style="color: red; text-align: center;">Test: This should be red and centered</p>

## Part 1: Decoding Brain Activity with Network Neuroscience
<figure class="m-figure center">
  <img src="/assets/images/projects/upenn_thesis_part1_methods.png" alt="calculation of temporal changes in HRV and network properties" />
  <figcaption>Steps in calculation of temporal changes in HRV and network properties.</figcaption>
</figure>


Epilepsy is a complex neurological disorder characterized by unpredictable seizures. Understanding the underlying changes in the brain and body that precede a seizure is crucial for improving management and potentially forecasting these events. My first objective was to investigate the intricate relationship between the brain's functional network activity and the autonomic nervous system (ANS), measured through heart rate (HR) and heart rate variability (HRV) parameters, in the period leading up to a seizure.

**Why Network Neuroscience?**
The brain is a vast and interconnected network. Seizures are known to activate the sympathetic nervous system, and parasympathetic activation can also be prominent during partial seizures. However, establishing a clear connection between ANS changes and seizure activity is challenging due to the complexity of seizures and individual variability. Network theory offers a powerful lens to understand these complex relationships, allowing us to analyze how different brain regions interact over time.

**Our Approach**
We used intracranial EEG (brain activity) and ECG (heart activity) data from 12 patients with drug-resistant temporal lobe epilepsy. We focused on a 60-minute window before a seizure onset.


1.  **Building Brain Networks:** For each one-minute window, we constructed functional connectivity networks where brain electrodes were "nodes" and the strength of their connections (based on Pearson correlation) were "edge weights".
2.  **Community Detection:** We used the Louvain algorithm to identify communities within these networks – groups of brain regions that show strong internal connections.
3.  **Measuring Flexibility:** A key concept was "flexibility," which quantifies how often a brain region switches its community assignment over time. We clustered nodes into three groups based on their flexibility: low, moderate, and high.
4.  **Heart Rate Variability (HRV) Analysis:** Simultaneously, we analyzed ECG signals to derive various HRV parameters, including Heart Rate (HR), Root Mean Square of Successive Differences (RMSSD), Low Frequency (LF) to High Frequency (HF) ratio (LF/HF), and SD1/SD2. These parameters provide insights into the balance of sympathetic and parasympathetic activity in the ANS.

<figure class="m-figure center">
  <img src="/assets/images/projects/upenn_thesis_part1_methods2.png" alt="calculation of temporal changes in HRV and network properties" />
  <figcaption>Node clustering using flexibility</figcaption>
</figure>

**Key Findings**
Our analysis revealed a significant association between HRV parameters and changes in brain network properties, particularly for a specific subset of brain regions. We found that brain regions with *low flexibility* (Cluster 1) showed the strongest correlations with HRV parameters. Among the HRV parameters, Heart Rate (HR) consistently showed the strongest correlation with changes in network strength and global efficiency. This suggests that specific, less-changing brain regions might be more tightly linked to autonomic nervous system activity before a seizure. This is a crucial step towards understanding the complex interplay between brain activity and ANS changes, which can eventually inform behavioral feedback strategies for epilepsy management.

<figure class="m-figure center">
  <img src="/assets/images/projects/upenn_thesis_part1_summary.png" alt="Summary" />
  <figcaption>Summary of correlation between HRV parameters and network parameters across all subjects</figcaption>
</figure>
---
## Part 2: Wearable Devices for Behavioral State Detection

In the second part of my thesis, I focused on the practical application of commercially available wearable devices for continuous monitoring of physiological signals and their potential to detect behavioral state changes in epilepsy patients. This involved evaluating the Fitbit Sense and Apple Watch Series 7.

**Study Design and Data Collection**
We conducted a clinical trial where patients admitted to the Epilepsy Monitoring Unit (EMU) wore either a Fitbit Sense or an Apple Watch Series 7. Alongside the wearable data, we simultaneously collected gold-standard intracranial/scalp EEG and Lead II ECG signals from the hospital, along to clinical annotations. This allowed for a direct comparison between wearable data and high-resolution clinical data.

The selected devices offered various features for continuous monitoring:

* **Fitbit Sense:** Regularly logs heart rate (up to 1Hz during activity) and sleep tracking. It also provides intermittent data on skin temperature, respiration rate, oxygen saturation, electrodermal activity, and 30-second ECG recordings when triggered. It boasted a multi-day battery life, which was beneficial for data collection ease.
* **Apple Watch Series 7:** Regularly logs heart rate (up to 1Hz during activity) and sleep tracking. It also captures accelerometer data at 50 Hz (using a third-party app like SensorLog) and respiration rate, and offers 30-second ECG recordings.

**Evaluating Wearable Accuracy**
We compared the heart rate and HRV measurements from the wearables against the ECG gold standard.

<figure class="m-figure center">
  <img src="/assets/images/projects/upenn_thesis_ecg_processing1.png" alt="ECG signal processing" />
  <figcaption>ECG signal processing</figcaption>
</figure>

* **Heart Rate (HR):** We observed a good agreement in heart rate values between the wearable devices and ECG, with an overall Pearson correlation of r=0.87. Specifically, Apple Watch measurements showed higher accuracy and better agreement with ECG-based HR compared to Fitbit.
* **Heart Rate Variability (HRV):** For HRV parameters like RMSSD and HF power, the agreement was notably lower, with overall correlations of r=0.14 for RMSSD and r=0.1 for HF power. This could be attributed to the sparse sampling rate of HR data by the wearables, which might not capture the subtle variations needed for accurate HRV calculations.

<figure class="m-figure center">
  <img src="/assets/images/projects/upenn_thesis_ecg_processing2.png" alt="ECG signal processing and HRV computation" />
  <figcaption>ECG signal processing and HRV computation</figcaption>
</figure>

**Identifying Behavioral States Around Seizures**
Despite the limitations in HRV accuracy, we explored a method to identify behavioral states around a seizure using hourly average values of RMSSD and HF values from non-seizure days as a baseline. From an initial analysis of 9 seizures across 3 subjects, we observed a promising trend: the RMSSD state decreased from a higher state to a lower state before a seizure started. This observation aligns with similar findings in athletes, where a drop in RMSSD can indicate fatigue. This suggests a potential for identifying stress or fatigue as a precursor to seizures, offering valuable insights for patients.

<figure class="m-figure center">
  <img src="/assets/images/projects/upenn_thesis_part2_hrv_level_001_sz1.png" alt="HRV states around seizure" />
  <figcaption>HRV states around seizure</figcaption>
</figure>

**Looking Ahead**
This thesis represents a crucial first step in understanding the complex interplay between brain activity, autonomic nervous system changes, and behavioral states in epilepsy. While wearable devices show great promise for continuous, long-term monitoring, further research with larger datasets is needed to validate these initial observations and overcome the limitations in HRV measurement accuracy from consumer-grade devices. Ultimately, this work contributes to paving the way for personalized behavioral feedback systems that could significantly improve the lives of people with epilepsy.

---
## Research Lab and Principal Investigator

- **Lab Name:** <a href="https://littlab.seas.upenn.edu">Litt Lab</a>, <a href="https://cnt.upenn.edu/">Center for Neuroengineering and Therapeutics (CNT)</a>
- **Principal Investigator:** Dr. Brian Litt
- **Institution:** University of Pennsylvania


**Learn More:**

<div class="download-button download-button--left"><a href="/assets/files/JalPanchal_MastersThesis.pdf" class="tag">Download Master's Thesis PDF</a></div>

Watch my presentation on YouTube

 <div style="position: relative; padding-bottom: 56.25%; height: 0; overflow: hidden; max-width: 100%;">
  <iframe
    src="https://www.youtube.com/embed/yAQRYOV1Jx0?si=3D1k1p1ZrPA6EA9D"
    frameborder="0"
    allowfullscreen
    style="position: absolute; top:0; left: 0; width: 100%; height: 100%;">
  </iframe>
</div>


Thanks for reading! If you're interested in wearable-based health monitoring, epilepsy research, or signal processing — feel free to reach out or browse my other projects.