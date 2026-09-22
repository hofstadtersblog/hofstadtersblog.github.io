---
layout: default
title: Projects
section: projects
permalink: /projects/
---

# Projects

<p class="section-intro">{{ site.sections.projects.blurb }}</p>

<ul class="post-list">
{% assign items = site.projects | sort: 'date' | reverse %}
{% for post in items %}
  <li>
    <span class="post-date">{{ post.date | date: "%B %-d, %Y" }}</span>
    <h3><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
    {% if post.excerpt and post.excerpt != empty %}<p class="post-excerpt">{{ post.excerpt | strip_html | truncate: 160 }}</p>{% endif %}
  </li>
{% else %}
  <li class="empty-note">Nothing posted here yet — add a Markdown file to <code>_projects/</code> to get started.</li>
{% endfor %}
</ul>
