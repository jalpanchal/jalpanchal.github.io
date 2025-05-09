---
layout: splash
title: "Resume"
permalink: /resume/
author_profile: false
toc: true
# toc_label: "Contents"
# # toc_icon: "file-alt"
toc_sticky: true

h_min: 1
h_max: 2
---

<!-- <div class="download-button">
    <a href="/assets/files/JalPanchal_Resume_Mar2025.pdf" class="btn btn--primary btn--large"><i class="fas fa-download"></i> Download PDF Resume</a>
</div> -->


## Summary

Experienced R&D Scientist with 5+ years in physiological signal processing, clinical validation and product development. Developed a novel stress metric within 6 months, offering innovative insights into user physiological states. Transformed research prototypes into a production-ready product within 2 years. Committed to creating meaningful health solutions through scientific innovation.


## Professional Experience
<!-- Resume Page Component -->
<div class="experience-container">
  <div class="company-list">
    <ul>
      <li id="company-1" class="company-item active" onclick="showExperience(1)">
        MindMics Inc.
        <ul class="role-list">
          <li id="role-1-1" onclick="event.stopPropagation(); showRole(1, 1)">Senior R&D Scientist</li>
          <li id="role-1-2" onclick="event.stopPropagation(); showRole(1, 2)">Project Lead</li>
          <li id="role-1-3" onclick="event.stopPropagation(); showRole(1, 3)">Algorithm Developer</li>
          <li id="role-1-4" onclick="event.stopPropagation(); showRole(1, 4)">Manufacturing Engineer</li>
        </ul>
      </li>
      <li id="company-2" class="company-item" onclick="showExperience(2)">
        ModeliCon Infotech
        <ul class="role-list">
          <li id="role-2-1" onclick="event.stopPropagation(); showRole(2, 1)">Product Engineer</li>
          <li id="role-2-2" onclick="event.stopPropagation(); showRole(2, 2)">Product Master</li>
        </ul>
      </li>
      <li id="company-3" class="company-item" onclick="showExperience(3)">
        Sunlux Technologies
        <ul class="role-list">
          <li id="role-3-1" onclick="event.stopPropagation(); showRole(3, 1)">Project Engineer</li>
        </ul>
      </li>
    </ul>
  </div>

  <div class="experience-details">
    <div id="experience-1-1" class="experience-item active">
      <h2>Senior R&D Scientist @ MindMics Inc.</h2>
      <p>June 2022 - Present</p>
      <ul>
        <li>Led algorithm development for physiological metrics and biofeedback interventions.</li>
        <li>Created motion artifact algorithms for wearable acoustics.</li>
      </ul>
    </div>
    <div id="experience-1-2" class="experience-item">
      <h2>Project Lead @ MindMics Inc.</h2>
      <p>2023 - 2024</p>
      <ul>
        <li>Managed multi-disciplinary teams to deliver high-impact projects.</li>
        <li>Coordinated with hardware and software teams for integrated solutions.</li>
      </ul>
    </div>
    <div id="experience-1-3" class="experience-item">
      <h2>Algorithm Developer @ MindMics Inc.</h2>
      <p>2022 - 2023</p>
      <ul>
        <li>Developed signal processing algorithms for physiological monitoring.</li>
        <li>Worked closely with data science teams to optimize models.</li>
      </ul>
    </div>
    <div id="experience-1-4" class="experience-item">
      <h2>Manufacturing Engineer @ MindMics Inc.</h2>
      <p>2023 - 2024</p>
      <ul>
        <li>Established a manufacturing line for TWS earbuds.</li>
        <li>Implemented quality control processes to improve production efficiency.</li>
      </ul>
    </div>
    <div id="experience-2-1" class="experience-item">
      <h2>Product Engineer @ ModeliCon Infotech</h2>
      <p>2017 - 2018</p>
      <ul>
        <li>Designed and shipped the company's first product for real-time simulation and control.</li>
        <li>Integrated industrial control systems with mathematical models for closed-loop testing.</li>
      </ul>
    </div>
    <div id="experience-2-2" class="experience-item">
      <h2>Product Master @ ModeliCon Infotech</h2>
      <p>2017 - 2019</p>
      <ul>
        <li>Designed and shipped the company's first product for real-time simulation and control.</li>
        <li>Integrated industrial control systems with mathematical models for closed-loop testing.</li>
      </ul>
    </div>
    <div id="experience-3-1" class="experience-item">
      <h2>Project Engineer @ Sunlux Technologies</h2>
      <p>2015 - 2017</p>
      <ul>
        <li>Developed control algorithms that improved equipment efficiency by 15%.</li>
        <li>Modeled the internal environment of Indian Navy vessels to optimize performance.</li>
      </ul>
    </div>
  </div>
</div>


<!-- Add this script to handle switching between companies and roles -->
<script>
  function showExperience(companyId) {
    // Deactivate all companies
    document.querySelectorAll('.company-item').forEach(company => {
      company.classList.toggle('active', company.id === `company-${companyId}`);
    });

    // Hide all experience items
    document.querySelectorAll('.experience-item').forEach(item => item.classList.remove('active'));

    // Reset all role highlights
    document.querySelectorAll('.role-list li').forEach(role => role.classList.remove('active-role'));

    // Show the first role of the selected company by default
    const firstRoleButton = document.querySelector(`#company-${companyId} .role-list li:first-child`);
    if (firstRoleButton) {
      const [_, cId, rId] = firstRoleButton.id.split("-");
      const firstRoleItem = document.getElementById(`experience-${cId}-${rId}`);
      if (firstRoleItem) firstRoleItem.classList.add('active');
      firstRoleButton.classList.add('active-role');
    }
  }

  function showRole(companyId, roleId) {
    // Deactivate all experience items
    document.querySelectorAll('.experience-item').forEach(item => item.classList.remove('active'));

    // Highlight the selected role
    document.querySelectorAll('.role-list li').forEach(role => role.classList.remove('active-role'));

    // Show only the selected role
    const selectedRole = document.getElementById(`experience-${companyId}-${roleId}`);
    if (selectedRole) selectedRole.classList.add('active');

    // Highlight the selected role button
    const activeRole = document.getElementById(`role-${companyId}-${roleId}`);
    if (activeRole) activeRole.classList.add('active-role');

    // Ensure the correct company is highlighted
    document.querySelectorAll('.company-item').forEach(company => {
      company.classList.toggle('active', company.id === `company-${companyId}`);
    });
  }

  // Initialize by showing the first company and first role
  window.onload = () => {
    showExperience(1);
  };
</script>
 
<!-- Styles for the component -->
<style>
.experience-container {
  display: flex;
  gap: 20px;
}

.company-list ul {
  list-style: none;
  padding: 0;
}

.company-item {
  margin-bottom: 15px;
  cursor: pointer;
  color: #94a3b8;
  font-weight: 600;
}
.company-item.hover {
  color:rgb(80, 80, 80);
}

.company-item.active {
  color:rgb(0, 0, 0);
  border-left: 3px solid rgb(0, 0, 0);
  padding-left: 10px;
}

.role-list {
  margin-left: 15px;
  margin-top: 10px;
  list-style: none;
  padding-left: 10px;
}

.role-list li {
  color: #94a3b8;
  cursor: pointer;
  margin-bottom: 5px;
}

.role-list li.active-role {
  color:rgb(0, 0, 0);
  font-weight: bold;
}

.role-list li:hover {
  color:rgb(80, 80, 80);
}

.experience-details {
  flex-grow: 1;
}

.experience-item {
  display: none;
}

.experience-item.active {
  display: block;
}


.active-role {
  font-weight: bold;
  color: #007acc;
}
</style>
