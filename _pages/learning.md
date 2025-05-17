---
permalink: /about/
title: "About"
layout: splash
toc: false
---
<div class="full-width-section">
  <div class="container flex-container">
    <div class="photo-wrapper">
      <img src="{{ '/assets/images/jal.png' | relative_url }}" alt="Your Name" />
    </div>
    <div class="welcome-text">
      <p>
        <strong style="color: white; font-size: 1.2em;">
          Welcome! I'm Jal, a passionate engineer with expertise in biomedical systems, signal processing, and data analytics.
        </strong>
      </p>
    </div>
  </div>
</div>

<style>
.full-width-section {
  width: 100vw;
  position: relative;
  left: 50%;
  right: 50%;
  margin-left: -50vw;
  margin-right: -50vw;
  background-color: #000000;
  padding: 0 0;
}

.flex-container {
  display: flex;
  align-items: center;
  gap: 2rem;
}
.photo-wrapper {
  margin: 0; /* Remove any default margin */
  padding: 0; /* Remove any default padding */
}
.photo-wrapper img {
  max-width: 500px;
  width: 100%;
  height: auto;
  border-radius: 10px;
}

.welcome-text {
  flex: 1;
  color: white;
}

/* Responsive: stack photo on top on narrow screens */
@media (max-width: 600px) {
  .flex-container {
    flex-direction: column;
    text-align: center;
  }
  
  .photo-wrapper img {
    max-width: 200px;
    margin-bottom: 1rem;
    margin-left: auto;
    margin-right: auto;
  }
}
</style>
