---
layout: default
title: Notes
---

<div class="posts">
  <h1>Research Notes</h1>
  <p>这里是我平时学习和研究的随笔记录。</p>
  
  <hr>

  <ul style="list-style: none; padding-left: 0;">
    {% for post in site.posts %}
      <li style="margin-bottom: 20px;">
        <span style="color: #999; font-family: monospace;">{{ post.date | date: "%Y-%m-%d" }}</span>
        <br>
        <a href="{{ post.url }}" style="font-size: 1.2rem; font-weight: bold; text-decoration: none;">
          {{ post.title }}
        </a>
        <p style="font-size: 0.9rem; color: #666; margin-top: 5px;">
          {{ post.excerpt | strip_html | truncatewords: 20 }}
        </p>
      </li>
    {% endfor %}
  </ul>
</div>