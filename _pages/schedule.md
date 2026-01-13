---
layout: page
permalink: /schedule/
title: Schedule
description: Workshop program and schedule
nav: true
nav_order: 3
---

<style>
.schedule-note {
  font-size: 0.95rem;
  color: #9ca3af;
  font-style: italic;
  margin-bottom: 2rem;
}

.section {
  margin-bottom: 2.5rem;
}

.section h2 {
  font-size: 1.15rem;
  font-weight: 600;
  color: #1e293b;
  margin-bottom: 0.75rem;
  padding-bottom: 0.5rem;
  border-bottom: 2px solid #e5e7eb;
}

/* Schedule Table */
.schedule-table {
  width: 100%;
  border-collapse: collapse;
}

.schedule-table th {
  text-align: left;
  padding: 0.75rem 0;
  border-bottom: 2px solid #e5e7eb;
  font-size: 0.85rem;
  font-weight: 600;
  color: #6b7280;
  text-transform: uppercase;
  letter-spacing: 0.3px;
}

.schedule-table td {
  padding: 0.65rem 0;
  border-bottom: 1px solid #f3f4f6;
  font-size: 0.95rem;
}

.schedule-table tr:last-child td {
  border-bottom: none;
}

.time {
  color: #6366f1;
  font-weight: 500;
  font-family: 'SF Mono', 'Roboto Mono', monospace;
  font-size: 0.9rem;
  width: 130px;
}

.event {
  color: #374151;
}

.event-break {
  color: #9ca3af;
  font-style: italic;
}

/* Speakers Grid */
.speakers-grid {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 1.25rem;
}

@media (max-width: 768px) {
  .speakers-grid { grid-template-columns: repeat(2, 1fr); }
}

.speaker {
  text-align: center;
  padding: 20px 12px;
  background: #f9fafb;
  border-radius: 12px;
  transition: all 0.2s;
}

.speaker:hover {
  background: #f3f4f6;
}

.speaker-avatar {
  width: 72px;
  height: 72px;
  border-radius: 50%;
  margin: 0 auto 12px;
  overflow: hidden;
  border: 2px solid #e5e7eb;
}

.speaker-avatar img {
  width: 100%;
  height: 100%;
  object-fit: cover;
}

.speaker-name {
  font-weight: 600;
  color: #1e293b;
  font-size: 0.95rem;
  margin-bottom: 4px;
  line-height: 1.3;
}

.speaker-affiliation {
  font-size: 0.8rem;
  color: #6b7280;
  line-height: 1.4;
}

/* Placeholder */
.placeholder {
  color: #9ca3af;
  font-style: italic;
  font-size: 0.95rem;
}
</style>

<p class="schedule-note">The detailed schedule will be announced closer to the workshop date.</p>

<div class="section">
<h2>Tentative Program</h2>
<table class="schedule-table">
  <thead>
    <tr>
      <th>Time</th>
      <th>Event</th>
    </tr>
  </thead>
<tbody>
  <tr><td class="time">09:00 – 09:10</td><td class="event">Introduction and Opening Remarks</td></tr>
  <tr><td class="time">09:10 – 09:40</td><td class="event">Invited Talk 1</td></tr>
  <tr><td class="time">09:40 – 10:00</td><td class="event">Poster Spotlights</td></tr>

  <tr><td class="time">10:00 – 10:30</td><td class="event event-break">Coffee Break</td></tr>

  <tr><td class="time">10:30 – 11:30</td><td class="event">Poster Session 1</td></tr>
  <tr><td class="time">11:30 – 12:00</td><td class="event">Invited Talk 2</td></tr>

  <tr><td class="time">12:00 – 13:30</td><td class="event event-break">Lunch Break</td></tr>

  <tr><td class="time">13:30 – 14:30</td><td class="event">Invited Talks 3–4</td></tr>
  <tr><td class="time">14:30 – 15:30</td><td class="event">Poster Session 2</td></tr>

  <tr><td class="time">15:30 – 16:00</td><td class="event event-break">Coffee Break</td></tr>

  <tr><td class="time">16:00 – 16:30</td><td class="event">Invited Talk 5</td></tr>
  <tr><td class="time">16:30 – 17:00</td><td class="event">Contributed Talks</td></tr>
  <tr><td class="time">17:00 – 18:00</td><td class="event">Panel Discussion</td></tr>
  <tr><td class="time">18:00</td><td class="event">End</td></tr>
</tbody>
</table>
</div>

<div class="section">
<h2>Invited Speakers</h2>
<div class="speakers-grid">
{% for speaker in site.data.speakers %}
  <div class="speaker">
    <div class="speaker-avatar"><img src="{{ speaker.image | relative_url }}" alt="{{ speaker.name }}"></div>
    <div class="speaker-name">{{ speaker.name }}</div>
    <div class="speaker-affiliation">{{ speaker.affiliation }}</div>
  </div>
{% endfor %}
</div>
</div>

<div class="section">
<h2>Accepted Papers</h2>
<p class="placeholder">To be announced after the review process</p>
</div>
