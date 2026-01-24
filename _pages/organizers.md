---
layout: page
permalink: /organizers/
title: Organizers
description: Meet the organizing committee
nav: true
nav_order: 4
---

<style>
.section {
  margin-bottom: 2.5rem;
}

.section h2 {
  font-size: 1.15rem;
  font-weight: 600;
  color: #1e293b;
  margin-bottom: 1rem;
  padding-bottom: 0.5rem;
  border-bottom: 2px solid #e5e7eb;
}

.organizers-grid {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 1.25rem;
}

@media (max-width: 768px) {
  .organizers-grid { grid-template-columns: repeat(2, 1fr); }
}

.organizer {
  text-align: center;
  padding: 20px 12px;
  background: #f9fafb;
  border-radius: 12px;
  transition: all 0.2s;
}

.organizer:hover {
  background: #f3f4f6;
}

.organizer-avatar {
  width: 72px;
  height: 72px;
  border-radius: 50%;
  margin: 0 auto 12px;
  overflow: hidden;
  border: 2px solid #e5e7eb;
}

.organizer-avatar img {
  width: 100%;
  height: 100%;
  object-fit: cover;
}

.organizer-name {
  font-weight: 600;
  color: #1e293b;
  font-size: 0.95rem;
  margin-bottom: 4px;
  line-height: 1.3;
}

.organizer-affiliation {
  font-size: 0.8rem;
  color: #6b7280;
  line-height: 1.4;
}

.contact-link {
  color: #6366f1;
  text-decoration: none;
}

.contact-link:hover {
  text-decoration: underline;
}

/* ===== Dark Mode ===== */
html[data-theme='dark'] .section h2 {
  color: #f3f4f6;
  border-color: #374151;
}

html[data-theme='dark'] .organizer {
  background: #1f2937;
}

html[data-theme='dark'] .organizer:hover {
  background: #374151;
}

html[data-theme='dark'] .organizer-avatar {
  border-color: #4b5563;
}

html[data-theme='dark'] .organizer-name {
  color: #f3f4f6;
}

html[data-theme='dark'] .organizer-affiliation {
  color: #9ca3af;
}

html[data-theme='dark'] .contact-link {
  color: #a5b4fc;
}

html[data-theme='dark'] p {
  color: #d1d5db;
}
</style>

<div class="section">
<h2>Organizing Committee</h2>
<div class="organizers-grid">
{% for organizer in site.data.organizers %}
  <div class="organizer">
    <div class="organizer-avatar"><img src="{{ organizer.image | relative_url }}" alt="{{ organizer.name }}"></div>
    <div class="organizer-name">{{ organizer.name }}</div>
    <div class="organizer-affiliation">{{ organizer.affiliation }}</div>
  </div>
{% endfor %}
</div>
</div>

<div class="section">
<h2>Contact</h2>
<p>For any inquiries, please reach out at <a class="contact-link" href="mailto:zijing.shi-1@uts.edu.au">zijing.shi-1[at]uts.edu.au</a></p>
</div>
