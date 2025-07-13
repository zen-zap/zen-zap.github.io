---
layout: page
icon: "fa-solid fa-file"
order: 3
title: Resume
permalink: /resume/
---

![Resume]({{ 'resume.png' | relative_url }}){: .resume-image }

<div class="resume-actions">
  <a href="{{ '/assets/files/resume.pdf' | relative_url }}" 
     download="Ashutosh_Panda_Resume.pdf" 
     class="btn btn-download">
    <i class="fas fa-download"></i> Download
  </a>
</div>

<style>
.resume-image {
  max-width: 100%;
  height: auto;
  border-radius: 8px;
  box-shadow: 0 4px 12px rgba(0,0,0,0.1);
  margin: 2rem auto;
  display: block;
}

.resume-actions {
  text-align: center;
  margin: 2rem 0;
}

.btn-download {
  background-color: #a259f7;
  border: none;
  color: white;
  padding: 0.75rem 1.5rem;
  border-radius: 6px;
  text-decoration: none;
  font-weight: 500;
  transition: all 0.2s ease;
}

.btn-download:hover {
  background-color: #7c3aed;
  color: white;
  transform: translateY(-1px);
  box-shadow: 0 4px 12px rgba(162, 89, 247, 0.3);
}
</style>