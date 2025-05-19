---
permalink: /about/
title: "About"
layout: single
toc: false
---
## Short Summary

Hi! I’m Jal, a passionate researcher and engineer specializing in biomedical systems and digital health. I love creating tech that directly improves people’s lives.

---

<div class="gallery-container">
  <div class="gallery-item w-1">
      <img src="/assets/images/iitm_friction_measurement_capston_setup.JPG" alt="Gallery Image 1">
  </div>
  <div class="gallery-item w-1">
    <img src="/assets/images/jal.png" alt="Gallery Image 2">
  </div>
  <div class="gallery-item w-1">
    <img src="/assets/images/jal.png" alt="Gallery Image 3">
  </div>
  <div class="gallery-item w-1">
    <img src="/assets/images/iitm_friction_measurement_timingbelt_setup1.JPG" alt="Gallery Image 4">
  </div>
  <div class="gallery-item w-2">
    <video controls autoplay loop mute>
      <source src="/assets/videos/ppg_cleaning.mp4" type="video/mp4">
      Your browser does not support the video tag.
    </video>
  </div>
  <div class="gallery-item w-1">
    <img src="/assets/images/jal.png" alt="Gallery Image 5">
  </div>
  <div class="gallery-item w-1">
    <img src="/assets/images/iitm_friction_measurement_timingbelt_setup1.JPG" alt="Gallery Image 5">
  </div>
  <div class="gallery-item w-1">
    <img src="/assets/images/jal.png" alt="Gallery Image 5">
  </div>
  <div class="gallery-item w-1">
    <img src="/assets/images/jal.png" alt="Gallery Image 5">
  </div>
  <div class="gallery-item w-1">
    <img src="/assets/images/jal.png" alt="Gallery Image 5">
  </div>
  <div class="gallery-item w-3">
    <video controls autoplay loop mute autoplay loop mute>
      <source src="/assets/videos/ppg_cleaning.mp4" type="video/mp4">
      Your browser does not support the video tag.
    </video>
  </div>
  <div class="gallery-item w-1">
    <img src="/assets/images/iitm_friction_measurement_capston_setup.JPG" alt="Gallery Image 5">
  </div>
  <div class="gallery-item w-1">
    <img src="/assets/images/jal.png" alt="Gallery Image 5">
  </div>
  <div class="gallery-item w-1">
    <img src="/assets/images/jal.png" alt="Gallery Image 5">
  </div>
</div>

<style>
.gallery-container {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 0.5rem;
  max-width: 100%;
}

.gallery-item img, .gallery-item video {
  width: 100%;
  border-radius: 5px;
  box-shadow: 0 4px 20px rgba(0,0,0,0.2);
  display: block;
  pointer-events: auto; /* ensure image/video accepts pointer events */
}
.gallery-item img{
  aspect-ratio: 4 / 3;
  object-fit: cover;

}
.gallery-item img,
.gallery-item video {
  transition: transform 0.3s ease;
}

.gallery-item:hover img{
  transform: scale(2.5);
  z-index: 10;
  position: relative;
}
.gallery-item:hover video {
  transform: scale(1.5);
  z-index: 10;
  position: relative;
}

.gallery-item.w-1 {
  grid-column: span 1;
}

.gallery-item.w-2 {
  grid-column: span 2;
}

.gallery-item.w-3 {
  grid-column: span 3;
}

@media (max-width: 768px) {
  .gallery-container {
    grid-template-columns: repeat(2, 1fr);
  }

  .gallery-item.w-1 {
    grid-column: span 1;
  }

  .gallery-item.w-2 {
    grid-column: span 2;
  }

  .gallery-item.w-3 {
    grid-column: span 2;
  }
}

@media (max-width: 480px) {
  .gallery-container {
    grid-template-columns: 1fr 1fr;
  }

  .gallery-item.w-1 {
    grid-column: span 1;
  }

  .gallery-item.w-2 {
    grid-column: span 2;
  }

  .gallery-item.w-3 {
    grid-column: span 2;
  }
}

</style>
