---
permalink: /about/
title: "About"
layout: single
toc: false
popup: false
---
## Short Summary

Hi! I’m Jal, a passionate researcher and engineer specializing in biomedical systems and digital health. I love creating tech that directly improves people’s lives.

---

<div class="gallery-container">
  <div class="gallery-item w-1">
    <a href="/assets/images/iitm_friction_measurement_capston_setup.JPG" class="glightbox" data-gallery="gallery">
      <img src="/assets/images/iitm_friction_measurement_capston_setup.JPG" alt="Gallery Image 1">
    </a>
  </div>
  <div class="gallery-item w-1">
    <a href="/assets/images/sim_cad.png" class="glightbox" data-gallery="gallery">
      <img src="/assets/images/sim_cad.png" alt="Gallery Image 2">
    </a>
  </div>
  <div class="gallery-item w-1">
    <a href="/assets/images/jal_ecg_mm.jpg" class="glightbox" data-gallery="gallery">
      <img src="/assets/images/jal_ecg_mm.jpg" alt="Gallery Image 3">
    </a>
  </div>
  <div class="gallery-item w-2">
    <a href="/assets/videos/sim_openpose.mp4" class="glightbox" data-gallery="gallery" data-type="video">
      <img src="/assets/images/thumb_sim_openpose.jpg" alt="Video Thumbnail">
    </a>
  </div>
  <div class="gallery-item w-1">
    <a href="/assets/images/iitm_friction_measurement_timingbelt_setup1.JPG" class="glightbox" data-gallery="gallery">
      <img src="/assets/images/iitm_friction_measurement_timingbelt_setup1.JPG" alt="Gallery Image 4">
    </a>
  </div>
  <div class="gallery-item w-1">
    <a href="/assets/images/iitm_friction_measurement_timingbelt_setup2.JPG" class="glightbox" data-gallery="gallery">
      <img src="/assets/images/iitm_friction_measurement_timingbelt_setup2.JPG" alt="Gallery Image 5">
    </a>
  </div>
  <div class="gallery-item r-2">
    <a href="/assets/images/jal_soldering.jpg" class="glightbox" data-gallery="gallery">
      <img src="/assets/images/jal_soldering.jpg" alt="Gallery Image 6">
    </a>
  </div>
  <div class="gallery-item w-2">
    <a href="/assets/videos/ppg_cleaning.mp4" class="glightbox" data-gallery="gallery" data-type="video">
      <img src="/assets/images/thumb_ppg_cleaning.jpg" alt="Video Thumbnail">
    </a>
  </div>
  <div class="gallery-item r-2">
    <a href="/assets/videos/ces2025_pose.mp4" class="glightbox" data-gallery="gallery" data-type="video">
      <img src="/assets/images/thumb_ces2025_pose.jpg" alt="Video Thumbnail">
    </a>
  </div>
  <div class="gallery-item w-1">
    <a href="/assets/images/iitm_friction_measurement_timingbelt_setup1.JPG" class="glightbox" data-gallery="gallery">
      <img src="/assets/images/iitm_friction_measurement_timingbelt_setup1.JPG" alt="Gallery Image 7">
    </a>
  </div>
  <div class="gallery-item r-2">
    <a href="/assets/images/jal_qualcomm_shenzhen.jpeg" class="glightbox" data-gallery="gallery">
      <img src="/assets/images/jal_qualcomm_shenzhen.jpeg" alt="Gallery Image 8">
    </a>
  </div>
  <div class="gallery-item w-1">
    <a href="/assets/images/jal_campfire.jpg" class="glightbox" data-gallery="gallery">
      <img src="/assets/images/jal_campfire.jpg" alt="Gallery Image 9">
    </a>
  </div>
  <div class="gallery-item w-1">
    <a href="/assets/images/jal_cycle_nahant.jpeg" class="glightbox" data-gallery="gallery">
      <img src="/assets/images/jal_cycle_nahant.jpeg" alt="Gallery Image 10">
    </a>
  </div>
  <div class="gallery-item w-1">
    <a href="/assets/images/jal_mocktrial02_jan6.jpeg" class="glightbox" data-gallery="gallery">
      <img src="/assets/images/jal_mocktrial02_jan6.jpeg" alt="Gallery Image 11">
    </a>
  </div>
  <div class="gallery-item w-1">
    <a href="/assets/images/iitm_friction_measurement_capston_setup.JPG" class="glightbox" data-gallery="gallery">
      <img src="/assets/images/iitm_friction_measurement_capston_setup.JPG" alt="Gallery Image 12">
    </a>
  </div>
  <div class="gallery-item w-1">
    <a href="/assets/images/jal_ces2025_booth.jpg" class="glightbox" data-gallery="gallery">
      <img src="/assets/images/jal_ces2025_booth.jpg" alt="Gallery Image 13">
    </a>
  </div>
  <div class="gallery-item w-1">
    <a href="/assets/images/jal_cycle_repair_kitchen.jpeg" class="glightbox" data-gallery="gallery">
      <img src="/assets/images/jal_cycle_repair_kitchen.jpeg" alt="Gallery Image 14">
    </a>
  </div>
</div>


## Time line

<div class="container py-5">
  <h2 class="mb-5">My Journey</h2>
  <div class="row">
    <div class="col-md-6">
      <div class="timeline-item mb-5">
        <h5 class="fw-bold">2025</h5>
        <p class="text-muted">Started working on non-invasive BP monitoring with PPG sensors.</p>
      </div>
      <div class="timeline-item mb-5">
        <h5 class="fw-bold">2023</h5>
        <p class="text-muted">Published paper on motion artifact removal using adaptive filtering.</p>
      </div>
      <div class="timeline-item mb-5">
        <h5 class="fw-bold">2021</h5>
        <p class="text-muted">Completed Master’s in Robotics from UPenn.</p>
      </div>
    </div>
  </div>
</div>

##
<script>
  const lightbox = GLightbox({
    selector: '.glightbox',
    touchNavigation: true,
    loop: true,
    autoplayVideos: true
  });
</script>

<style>
  .mfp-hide {
  display: none !important;
}
  
.gallery-container {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 0.5rem;
  max-width: 100%;
}
.gallery-item {
  position: relative;
  overflow: visible;
}

.gallery-item img, .gallery-item video {
  width: 100%;
  border-radius: 5px;
  box-shadow: 0 4px 20px rgba(0,0,0,0.2);
  display: block;
  pointer-events: auto; /* ensure image/video accepts pointer events */
}

.gallery-item img,
.gallery-item video {
  transition: transform 0.3s ease, opacity 0.3s ease;
}

.gallery-item:hover img{
  cursor: zoom-in;
  aspect-ratio: auto  !important;
  position: absolute  !important;
  width: auto  !important;
  height: auto  !important;
  max-width: 50vw   !important;
  max-height: none  !important;
  object-fit: contain  !important;
  transform: scale(1.5);
  z-index: 100;
  background: white;
  box-shadow: 0 8px 30px rgba(0, 0, 0, 0.3);

}
.gallery-item:hover video {
  ursor: zoom-in;
  aspect-ratio: auto  !important;
  position: absolute  !important;
  width: auto  !important;
  height: auto  !important;
  max-width: 50vw  !important;
  max-height: none  !important;
  object-fit: contain  !important;
  transform: scale(1.5);
  z-index: 100;
  background: white;
  box-shadow: 0 8px 30px rgba(0, 0, 0, 0.3);
}

.gallery-item.w-1 {
  grid-column: span 1;
}

.gallery-item.w-1 img {
    aspect-ratio: 4 / 3;
  object-fit: cover;
}

.gallery-item.w-2 img,
.gallery-item.w-2 video{
    aspect-ratio: 8/2.95;
  object-fit: cover;
}


.gallery-item.r-2 img,
.gallery-item.r-2 video{
    aspect-ratio: 2/3.1;
  object-fit: cover;
}

.gallery-item.w-2 {
  grid-column: span 2;
}

.gallery-item.w-3 {
  grid-column: span 3;
}

.gallery-item.r-2 {
  grid-row: span 2;
}
.gallery-item.rw-2 {
  grid-row: span 2;
  grid-column: span 2;
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
.timeline-item {
  border-left: 3px solid #007bff;
  padding-left: 1rem;
  position: relative;
}

.timeline-item::before {
  content: '';
  position: absolute;
  left: -9px;
  top: 0.25rem;
  width: 16px;
  height: 16px;
  background-color: #007bff;
  border-radius: 50%;
}

</style>
