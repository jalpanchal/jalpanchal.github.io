---
permalink: /about/
title: "About"
layout: splash
---

<div class="full-width-container">
  <div class="image-scroller">
    <img src="/assets/images/jal.png" alt="Image 1" />
    <img src="/assets/images/jal.png" alt="Image 2" />
    <img src="/assets/images/jal.png" alt="Image 3" />
    <img src="/assets/images/jal.png" alt="Image 4" />
    <img src="/assets/images/jal.png" alt="Image 5" />
    <img src="/assets/images/jal.png" alt="Image 6" />
    <img src="/assets/images/jal.png" alt="Image 1" />
    <img src="/assets/images/jal.png" alt="Image 2" />
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
}

@keyframes scroll {
  0% { transform: translateX(0); }
  100% { transform: translateX(-50%); }
}
</style>