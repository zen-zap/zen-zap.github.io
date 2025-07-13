---
layout: resume
icon: "fa-solid fa-file"
order: 3
title: Resume
permalink: /resume/
---

<div class="pdf-viewer">
  <canvas id="pdf-canvas"></canvas>
</div>
<div class="pdf-controls mt-3">
  <button id="prev-page" class="btn btn-outline-secondary" style="display:none;">
    <i class="fas fa-chevron-left"></i> Previous
  </button>
  <span id="page-info" class="mx-3">Page 1 of 1</span>
  <button id="next-page" class="btn btn-outline-secondary" style="display:none;">
    Next <i class="fas fa-chevron-right"></i>
  </button>
  <a href="{{ '/assets/files/resume.pdf' | relative_url }}"
     download="Ashutosh_Panda_Resume.pdf"
     class="btn btn-download ms-3">
    <i class="fas fa-download"></i> Download
  </a>
</div>