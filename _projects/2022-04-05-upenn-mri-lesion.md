---
title: "Computer Vision for MS Lesion Detection in Portable MRI"
date: 2021-12-15 # Or the date you'd like to publish this post (e.g., end of project)
categories:
  - Projects
tags:
  - Machine-Learning
  - Computer-Vision
  - Medical-Imaging
  - MRI
  - Multiple-Sclerosis
  - Image-Segmentation
excerpt: "Developing an algorithm to detect Multiple Sclerosis lesions in FLAIR MRI scans from portable, low-power machines."
header:
  image: /assets/images/projects/upenn_cis581_header.jpg
  teaser: /assets/images/projects/upenn_cis581_thumbnail.jpg
toc: false
featured: true
---

## Revolutionizing MRI: Detecting MS Lesions with Portable Scanners

As part of a Computer Vision course project (CIS 581) at the University of Pennsylvania, our team embarked on a critical challenge: developing an algorithm to detect Multiple Sclerosis (MS) lesions in Fluid-Attenuated Inversion Recovery (FLAIR) MRI scans acquired from a portable, low-power MRI machine. This project addresses a significant limitation of traditional 3T MRI machines – their high cost and lack of portability – by leveraging newer, accessible portable MRI technologies like Hyperfine's 64mT system.

 <figure class="m-figure center">
      <img src="/assets/images/work_in_progress.jpg" alt="Work In Progress" />
</figure>


<!-- ## The Challenge of Multiple Sclerosis and Portable MRI

Multiple Sclerosis is a complex inflammatory and degenerative disease of the central nervous system, characterized by demyelinating lesions that are typically identified using MRI scans. While 3T MRI machines are the gold standard in hospitals, their immobility and expense limit their reach, especially in remote areas or emergency settings. The advent of portable, low-power MRI machines opens up new possibilities for accessible neuroimaging. Our goal was to develop a computer vision algorithm capable of detecting these crucial MS lesions from such portable scans.

## Our Approach: A Pipeline for Lesion Detection
<figure class="m-figure center">
<a href="/assets/images/projects/lesion_detection_overview.png" class="popup">
  <img src="/assets/images/projects/lesion_detection_overview.png" alt="Overview of lesion detection methodology" />
</a>
  <figcaption>Our four-step methodology for MS lesion detection.</figcaption>
</figure>

Our methodology involved a four-step pipeline to process FLAIR MRI scans from both 3T and 64mT portable machines:

1.  **Data Acquisition:** We utilized FLAIR MRI axial slices from 5 subjects, with 5 slices selected from each, obtained from both 3T and 64mT portable MRI scans.
2.  **Brain Extraction and Registration:** The first crucial pre-processing step involved removing non-brain tissue (skull, skin, etc.) using FSL's Brain Extraction Tool (BET). Subsequently, we registered the 64mT portable MRI scans to their corresponding 3T scans using ITK-SNAP to align the images for consistent analysis.
    <figure class="m-figure center">
    <a href="/assets/images/projects/lesion_detection_brain_extraction.png" class="popup">
      <img src="/assets/images/projects/lesion_detection_brain_extraction.png" alt="Brain extraction process" />
    </a>
      <figcaption>Brain extraction and registration of 3T and 64mT scans.</figcaption>
    </figure>
3.  **Unsupervised Segmentation with Gaussian Mixture Models (GMM) and Flood Fill:**
    * **Gaussian Mixture Model (GMM):** After pre-processing, we applied an unsupervised Gaussian Mixture Model (GMM) to segment the brain into different intensity clusters. This allowed us to identify regions corresponding to white matter, gray matter, cerebrospinal fluid (CSF), and importantly, potential lesion clusters based on their pixel intensities. The lesion cluster was identified as the segment with the highest mean intensity, often representing the brightest regions in FLAIR images.
    <figure class="m-figure center">
    <a href="/assets/images/projects/lesion_detection_gmm_output.png" class="popup">
      <img src="/assets/images/projects/lesion_detection_gmm_output.png" alt="GMM output showing lesion cluster" />
    </a>
      <figcaption>GMM output highlighting the identified lesion cluster.</figcaption>
    </figure>
    * **Flood Fill Algorithm:** To refine the lesion detection, we then used a flood fill algorithm. This algorithm was applied to the lesion cluster identified by the GMM to accurately delineate the boundaries of the lesions, providing a precise segmentation mask.
    <figure class="m-figure center">
    <a href="/assets/images/projects/lesion_detection_flood_fill.png" class="popup">
      <img src="/assets/images/projects/lesion_detection_flood_fill.png" alt="Flood fill segmentation example" />
    </a>
      <figcaption>Segmentation results using flood fill on 3T and 64mT scans.</figcaption>
    </figure>

4.  **Comparison and Evaluation (Dice Coefficient):** To assess the accuracy of our algorithm, we compared our automatically generated lesion masks against manually annotated masks (ground truth). The primary metric used for evaluation was the **Dice Coefficient**, which measures the similarity between two segmentation masks. A higher Dice Coefficient indicates better agreement.
    <figure class="m-figure center">
    <a href="/assets/images/projects/lesion_detection_dice_boxplot.png" class="popup">
      <img src="/assets/images/projects/lesion_detection_dice_boxplot.png" alt="Dice Coefficient boxplots" />
    </a>
      <figcaption>Dice Coefficient Boxplots for evaluated subjects (P41 and P46).</figcaption>
    </figure>
    We achieved an overall Dice Coefficient of approximately 0.406. While this indicates a foundational level of agreement, the variability seen in the boxplots suggests challenges related to the small dataset and the inherent differences between 3T and 64mT image qualities.

## Key Findings & Future Directions

Our project successfully demonstrated a pipeline for unsupervised MS lesion detection using portable MRI scans. The use of GMM for intensity clustering and flood fill for precise segmentation proved to be a viable approach. The Dice Coefficient provides a quantitative measure of performance, highlighting areas for improvement.

This project was a crucial first step, and several avenues exist for future research:
* **Larger Dataset:** Expanding the dataset to include more subjects and a wider range of lesion characteristics would significantly improve model robustness and generalization.
* **Supervised Learning:** Exploring supervised GMM approaches or deep learning models like Convolutional Neural Networks (CNNs) could yield higher accuracy by leveraging annotated data more effectively.
* **Advanced Pre-processing:** Investigating more sophisticated pre-processing techniques, such as contrast filters, could enhance lesion visibility.
* **3D Lesion Detection:** Extending the algorithm to perform 3D lesion detection for volumetric analysis would provide a more comprehensive assessment.

This work contributes to the growing field of accessible medical imaging, paving the way for more widespread and timely diagnosis and monitoring of neurological conditions like Multiple Sclerosis.

---
## Skills Overview

This project provided a unique opportunity to apply and develop a diverse set of skills, including:

* **Computer Vision & Image Processing:** Expertise in techniques like brain extraction, image registration, intensity-based segmentation, and flood fill algorithms.
* **Machine Learning (Unsupervised Learning):** Practical application of Gaussian Mixture Models for clustering and anomaly detection in medical images.
* **Medical Image Analysis:** Experience in working with FLAIR MRI scans and understanding the characteristics of MS lesions.
* **Data Analysis & Evaluation:** Proficient in using metrics like the Dice Coefficient for quantitative assessment of segmentation performance.
* **Scientific Programming:** Strong capabilities in Python for data manipulation, analysis, and visualization of medical images.
* **Technical Writing & Presentation:** Ability to clearly articulate complex methodologies and findings in both written reports and oral presentations.
* **Team Collaboration:** Experience working effectively within a project team to achieve a common goal.

## Project Team and Course

-   **Team Members:** Aishwarya Wesanekar, Anamil Mehta, Jal Mahendra Panchal, Parimal Mehta
-   **Course:** CIS 581: Computer Vision and Computational Photography, Fall 2021
-   **Institution:** University of Pennsylvania

## Learn More:

<div class="download-button download-button--left"><a href="/assets/files/UPenn_HyperfineLesion_FinalReport.pdf" class="tag">Download Project Report PDF</a></div> 

Thanks for reading! If you're interested in medical imaging, computer vision, or machine learning for healthcare, feel free to reach out or browse my other projects. -->