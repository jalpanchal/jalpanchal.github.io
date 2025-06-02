---
layout: splash
title: Home
permalink: /
---


<div class="full-width-section">
  <div class="container flex-container">
    <div class="photo-wrapper">
      <img src="{{ '/assets/images/jal.png' | relative_url }}" alt="Jal Panchal" />
    </div>
    <div class="welcome-text">
      <p>
        <strong style="color: white; font-size: 1.2em;">
          Hi! I'm Jal, a passionate researcher and engineer with a deep interest in digital health, biomedical systems, and human-centered technology. Dive in to explore my projects, thoughts, and experiments.
        </strong>
      </p>
    </div>
  </div>
</div>


<!-- PPG Video Section -->
<div class="full-width-section white-section">
  <div class="container minimal-transition">
    <h2>Explore Biosignal Filtering</h2>
    <p class="subtitle">
      Biosignals — like most real-world signals — are often messy and full of noise.<br>
      A key skill in biomedical signal processing is learning how to clean and interpret them.
    </p>
    <p class="subtitle">
      <b>Watch how raw signals are transformed — then try it yourself in the interactive game.</b>
    </p>
  </div>
</div>

<div class="full-width-section white-section">
  <div class="container">
    <video class="ppg-video" autoplay muted loop controls>
      <source src="/assets/videos/ppg_cleaning.mp4" type="video/mp4">
      Your browser does not support the video tag.
    </video>
  <div class="instructions-container">
    <h3>PPG filtering game </h3>
    <p>Your goal is to clean the noisy PPG signal and match it as closely as possible to the clean reference signal. Aim for an <strong>RMSE (Root Mean Squared Error) below 0.12</strong> to win!</p>

    <div class="interactive-container">
      <iframe src="/assets/code/ppg_filter_interactive.html" class="interactive-frame" frameborder="0"></iframe>
    </div>
    <ul>
      <li><strong>Highpass Filter:</strong> Removes low-frequency noise (e.g., baseline drift).</li>
      <li><strong>Lowpass Filter:</strong> Removes high-frequency noise (e.g., motion artifacts).</li>
      <li><strong>Rolling Mean Filter:</strong> Smooths short-term fluctuations.</li>
    </ul>
    <h3>How to Play:</h3>
    <ol>
      <li>Start with the noisy signal (gray) and observe how it differs from the clean signal (black).</li>
      <li>Apply the filters one by one using the checkboxes.</li>
      <li>Adjust the sliders to find the optimal cutoff frequencies and window size.</li>
      <li>Watch the RMSE in the plot title - aim to reduce it below 0.12 to turn the filtered signal (blue) green.</li>
      <li>Experiment and have fun! There are multiple ways to reach the target RMSE.</li>
    </ol>
    <p class="tips">💡 <strong>Tip:</strong> Small adjustments can make a big difference. Fine-tune your settings to achieve the best possible match.</p>
    <p>Need help with biosignal processing? <a href="/about">Let's connect</a>!</p>
    <p>If you manage to get the RMSE below 0.12, take a screenshot of your filtered plot and <a href="mailto:jalpanchal1+ppg@gmail.com?subject=PPG Filtering Game Screenshot">send it to me!</a> I'd love to see your results.</p>
  </div>
  </div>
</div>


<!-- Projects Section -->
<div class="full-width-section off-white-section">
  <div class="container">
    <p>
    <strong style="color: rgb(0, 0, 0); font-size: 1.2em;">
    Here are some of my other fun projects:
    </strong>
    </p>
    <div class="card-grid-container">
    {% assign featured_projects = site.projects | where: "featured", true %}
    <div class="card-grid">
    {% for project in featured_projects limit:3 %}
        {% include post-card-image.html post=project %}

    {% endfor %}
  </div>
  </div>
  <p>
  <strong style="color: rgb(0, 0, 0); font-size: 1.2em;">
    Interested in learning more about my work?
  </strong>
  </p>
    <div class="page-tags">
      <a href="/projects/" class="tag">Projects</a>
      <a href="/resume/" class="tag">Resume</a>
      <a href="/about/" class="tag">About Me</a>
    </div>
  </div>
</div>



<style>
.flex-container {
  display: flex;
  align-items: center;
  gap: 2rem;
}
.photo-wrapper img {
  max-width: 500px;
  width: 100%;
  height: auto;
  border-radius: 10px;
  margin-bottom: 0; /* Remove padding below photo */
}
.welcome-text {
  flex: 1;
  color: white;
  /* max-width: 700px; */
  padding: 0 40px;
  text-align: left;
}
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
.full-width-section {
  width: 100vw;
  position: relative;
  left: 50%;
  right: 50%;
  margin-left: -50vw;
  margin-right: -50vw;
  padding: 0rem 0;
  padding-top: 2rem;
  background-color: #000000;
  margin-bottom: 20px;
}
.white-section {
  background-color: #ffffff;
  text-align: center;
  padding: 1rem 2rem;
}

.off-white-section {
  background-color: #f8f8f8;
  text-align: center;
  padding: 1rem 2rem;
}
.ppg-video {
  width: 100%;
  max-width: 900px;
  border-radius: 15px;
  border: 2px solid #060606;
  box-shadow: 0 4px 20px rgba(0, 0, 0, 0.5);
}

.instructions-container {
  background-color: #fbfbfb;
  border: 2px solid #ddd;
  border-radius: 12px;
  padding: 20px 30px;
  margin-bottom: 20px;
  box-shadow: 0 4px 15px rgba(0, 0, 0, 0.1);
  animation: fadeIn 0.8s ease-in-out;
  text-align: left;
}

.instructions-container h2 {
  font-size: 1.0em;
  color: #333;
  margin-bottom: 10px;
}

.instructions-container ul, .instructions-container ol {
  margin-left: 20px;
  color: #555;
  text-align: left;
}

.instructions-container li {
  margin-bottom: 10px;
}

.instructions-container .tips {
  font-style: italic;
  color: #777;
  margin-top: 15px;
}

.instructions-container a {
  color: #4CAF50;
  text-decoration: none;
  font-weight: bold;
}

.instructions-container a:hover {
  text-decoration: underline;
}

.interactive-container {
  display: flex;
  justify-content: center;
  max-width: 1200px;
  margin: 0 auto;
}

.interactive-frame {
  width: 100%;
  max-width: 1200px;
  height: 400px;
  border-radius: 12px;
  border: 2px solid #ddd;
}

.card-grid-container {
  display: flex;
  justify-content: center;
  width: 100%;
}

.card-grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
  grid-gap: 4em;
  margin-bottom: 2em;
  max-width: 1200px; /* Optional: limit the maximum width */
  width: 100%;
}

.contact-form {
  display: flex;
  flex-direction: column;
  gap: 1rem;
  max-width: 600px;
  margin: 0 auto;
  padding: 1rem;
  background-color: #ffffff;
  border-radius: 10px;
  box-shadow: 0 4px 15px rgba(0, 0, 0, 0.1);
}
.contact-form label {
  font-size: 1em;
  margin-bottom: 0.5rem;
}
.contact-form input, .contact-form textarea {
  width: 100%;
  padding: 0.8rem;
  border: 1px solid #ddd;
  border-radius: 5px;
  font-size: 1em;
}
.contact-form button {
  padding: 0.8rem;
  background-color: #4CAF50;
  color: white;
  border: none;
  border-radius: 5px;
  cursor: pointer;
  transition: background-color 0.3s ease;
}
.contact-form button:hover {
  background-color: #45a049;
}

.contact-links {
  display: flex;
  justify-content: space-between;
  flex-wrap: wrap;
}
.contact-left {
  flex: 1 1 60%;
  margin-right: 20px;
}
.links-right {
  flex: 1 1 30%;
  align-self: flex-start;
}
.links-right ul {
  list-style: none;
  padding: 0;
}
.links-right ul li {
  margin-bottom: 1rem;
}
.links-right ul li a {
  color: #333;
  text-decoration: none;
  font-weight: bold;
}
.links-right ul li a:hover {
  color: #4CAF50;
  text-decoration: underline;
}

.page-tags {
  display: flex;
  flex-wrap: wrap;
  gap: 5px;
  justify-content: center;
  z-index: 2;
  opacity: 1;
  
  .tag {
    background-color: #ffffff;
    color: #333333;
    padding: 0.2em 0.8em;
    border-radius: 7px;
    font-size: 1em;
    font-weight: 600;
    text-transform: capitalize;
    cursor: pointer;
    border: 1px solid #d2dbe1;
    transition: background-color 0.3s, color 0.3s, border-color 0.3s;
    text-decoration: none;

    &:hover {
      background-color: #6a6b6d;
      border-color: #bbc4cb;
      color : #ffffff;
      text-decoration: none;
    }

    &.active {
      background-color: #444;
      color: #ffffff;
      border-color: #444;
      box-shadow: 0 2px 8px rgba(0, 0, 0, 0.15);
    }
  }
}


.minimal-transition {
  /* width: 100vw; */
  text-align: center;
  /* padding: 3rem 1rem 1rem; */
  background-color: #ffffff;
  /* color: #111; */
  /* font-family: -apple-system, BlinkMacSystemFont, "San Francisco", "Helvetica Neue", sans-serif; */
}

.minimal-transition h2 {
  font-size: 2rem;
  font-weight: 600;
  margin-bottom: 0.5rem;
}

.minimal-transition p {
  font-size: 1.1rem;
  color: #555;
  max-width: 1000px;
  margin: 0 auto;
}

@keyframes fadeIn {
  from { opacity: 0; transform: translateY(10px); }
  to { opacity: 1; transform: translateY(0); }
}


@media (max-width: 768px) {
  .card-grid {
    grid-template-columns: repeat(auto-fill, minmax(150px, 1fr));
  }
}

@media (max-width: 480px) {
  .card-grid {
    grid-template-columns: 1fr;
  }
</style>





