---
layout: default
title: About
section: home
---

# Douglas Hofstadter

<p class="tagline" id="tagline"><span id="tagline-text"></span><span class="cursor">&nbsp;</span></p>

Hello! My name is Douglas Hofstadter. This is not my real name, of course, but my internet pseudonym is Douglas Hofstadter. If you know me in person, you will probably recognize me from my picture or my description.

I am an undergraduate student living in Portland, Oregon! I am majoring in Physics (theoretical concentration) and Mathematics, and minoring in Classics. I am also interested in educational theory, though I am with-holding that until my Masters.

<div class="section-grid">
  {% for s in site.sections %}
  <a class="section-card" style="--card-accent: {{ s[1].accent }}"
     href="{% if s[0] == 'mathphysics' %}{{ '/math-physics/' | relative_url }}{% else %}{{ '/' | append: s[0] | append: '/' | relative_url }}{% endif %}">
    <h3>{{ s[1].label }}</h3>
    <p>{{ s[1].blurb }}</p>
  </a>
  {% endfor %}
</div>

If you want to know what I'm up to lately, the [rambling](/rambling/) section
is unfortunately the most honest answer.

<script src="{{ '/assets/js/typing.js' | relative_url }}" defer></script>
