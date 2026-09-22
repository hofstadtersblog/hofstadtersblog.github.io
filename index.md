---
layout: default
title: About
section: home
---

# Douglas Hofstadter

<p class="tagline" id="tagline"><span id="tagline-text"></span><span class="cursor">&nbsp;</span></p>

I'm a mostly-retired academic with an office full of unread books and a
whiteboard that hasn't been fully erased since 2019. This is where I keep
the things I'd otherwise say to an empty room: what I'm reading, problems
I can't stop poking at, pictures Mathematica made when I asked it nicely,
a few software things I built for no defensible reason, some music, and
whatever else doesn't fit anywhere.

Nothing here is peer-reviewed. Read accordingly.

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
