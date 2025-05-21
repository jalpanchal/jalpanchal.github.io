---
title: "UPenn - Master's Thesis"
categories:
  - Projects
tags:
  - EEG
  - Wearables
  - Seizure
  - Python
# author_profile: false
# layout: archive
header:
  image: /assets/images/iitm_friction_measurement_timingbelt_setup2.JPG
  teaser: /assets/images/iitm_friction_measurement_timingbelt_setup2.JPG
toc: false
# toc_sticky: true
---

<h1>Heart, Brain, and Behavior: What Wearables and Network Neuroscience Reveal About Seizures</h1>
Insights from my master's thesis on network neuroscience and wearable data to study seizure prediction and behavioral state monitoring.
## 🧠 Part I: Using Network Neuroscience to Uncover the Link Between Heart and Brain Before a Seizure

Seizures are often unpredictable and can be triggered by subtle physiological and psychological changes. In my master’s thesis, I explored how **heart rate variability (HRV)** — a marker of autonomic nervous system (ANS) activity — might correlate with changes in **brain network connectivity** before a seizure.

### 📊 What I Did

- Used **intracranial EEG and ECG** from 12 epilepsy patients.
- Built **functional brain networks** from EEG using 1-minute windows.
- Grouped electrodes (nodes) based on their **community flexibility** over time.
- Calculated HRV metrics from ECG: **RMSSD**, **LF/HF ratio**, **SD1/SD2**.
- Measured correlation between HRV patterns and network properties like **node strength** and **global efficiency**.

### 🔍 What I Found

- A subset of **low-flexibility nodes** in the brain showed **stronger correlation** with HRV than the full network.
- **Heart rate (HR)** had the highest correlation, followed by LF/HF and SD1/SD2.
- These findings hint at a **stable sub-network** in the brain that reflects behavioral state changes — and may be important for seizure prediction.

### 🧠 Why This Matters

By combining **temporal network analysis** and HRV, we can start to uncover patterns that may serve as **biomarkers for stress, fatigue, or pre-seizure states**. This could eventually enable real-time feedback for patients using wearable devices or implants.

---

## ⌚ Part II: Evaluating Wearables for Behavioral State Monitoring in Epilepsy

As part of my thesis, I also ran a **clinical trial** to test how well consumer wearables like the **Apple Watch Series 7** and **Fitbit Sense** could monitor heart rate and behavioral states around seizures.

### 📋 Study Setup

- Recruited **7 patients** in the Epilepsy Monitoring Unit (EMU).
- Devices used: **Fitbit Sense** and **Apple Watch Series 7**.
- Collected:
  - ECG, EEG, and seizure annotations
  - HR, sleep, and motion data from wearables
  - Patient-reported mood via surveys

### 🔍 Findings

#### ✅ Accuracy

- **Apple Watch HR** closely matched ECG (r = 0.87).
- **Fitbit** had higher sampling rates but less agreement with ECG.
- **HRV metrics** (RMSSD, HF power) showed **poor agreement** — likely due to low sampling rate.

#### ⚡ Practical Challenges

- Apple Watch needed **2x/day charging**; Fitbit lasted longer.
- Accelerometry required 3rd-party apps (e.g., SensorLog).
- We proposed using **hot-swapping two Apple Watches** to avoid data loss during charging.

### 🚦 Behavioral States Around Seizures

- Calculated **z-scores** of RMSSD and HF power around seizures.
- Found that **RMSSD often dropped before a seizure**, possibly reflecting fatigue or stress.
- Recovery patterns were visible in the **post-seizure rise** in HRV.

---

## 🧭 Looking Ahead

This work was a **first step** in integrating wearable sensing and network neuroscience for seizure monitoring. Future directions include:

- Larger datasets to validate patterns
- Long-term at-home monitoring
- Real-time feedback systems for patients

---

## 🎓 Learn More

- 📘 [Full thesis PDF](/assets/pdfs/jalp_thesis_submission.pdf)
- 🎥 [Watch my presentation on YouTube](https://youtu.be/yAQRYOV1Jx0?si=3D1k1p1ZrPA6EA9D)

Thanks for reading! If you're interested in wearable-based health monitoring, epilepsy research, or signal processing — feel free to reach out or browse my other posts.

