---
permalink: /about/
title: "About"
layout: single
toc: false
---

<div class="full-width-container">
  <div class="image-scroller">
    <img src="/assets/images/jal.png" alt="Image 1" />
    <img src="/assets/images/jal.png" alt="Image 2" />
    <img src="/assets/images/iitm_friction_measurement_timingbelt_setup1.JPG" alt="Image 3" />
    <img src="/assets/images/jal.png" alt="Image 4" />
    <img src="/assets/images/jal.png" alt="Image 5" />
    <img src="/assets/images/jal.png" alt="Image 6" />
    <img src="/assets/images/jal.png" alt="Image 1" />
    <img src="/assets/images/iitm_friction_measurement_timingbelt_setup1.JPG" alt="Image 2" />
    <img src="/assets/images/jal.png" alt="Image 3" />
    <img src="/assets/images/jal.png" alt="Image 4" />
    <img src="/assets/images/jal.png" alt="Image 5" />
    <img src="/assets/images/jal.png" alt="Image 6" />
  </div>
</div>

<style>
body {
  margin: 0;
  padding: 0;
}
.full-width-container {
  width: 100vw;
  /* overflow: hidden; */
  white-space: nowrap;
  position: relative;
  margin: 0;
  padding: 0;
}

.image-scroller {
  display: inline-flex;
  gap: 20px;
  animation: scroll 30s linear infinite;
  padding: 0;
  margin: 0;
}

.image-scroller img {
  width: 20vw;
  max-width: 200px;
  height: auto;
  border-radius: 15px;
  transition: transform 0.4s, box-shadow 0.4s;
}

.image-scroller img:hover {
  transform: scale(3) translateY(50%);
  /* position: relative; */
  z-index: 999;
  box-shadow: 0 10px 30px rgba(0, 0, 0, 0.2);
}

.image-scroller:hover {
  animation-play-state: paused;

}

@keyframes scroll {
  0% { transform: translateX(0); }
  100% { transform: translateX(-50%); }
}
</style>