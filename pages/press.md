---
layout: page
title: Press
permalink: /press/
---

<div class="tabs">
    <input id="tab2" type="radio" name="tabs">
    <label for="tab2"><span>≣ List</span></label>
    <input id="tab1" type="radio" name="tabs" checked>
    <label for="tab1"><span>⊞ Grid </span></label>
  <section id="content1" class="tab-content grid">
  <div class="grid">
      {%- if site.categories.press.size > 0 -%}
      <ul class="post-list">
        {%- for post in site.categories.press -%}
        <li>
          {%- assign date_format = site.minima.date_format | default: "%Y" -%}
          <a href="{{ post.url }}" ><img class="thumbnail" src="{{ post.thumbnail }}" /></a>
          {%- if site.show_excerpts -%}
            {{ post.excerpt }}
          {%- endif -%}
        </li>
        {%- endfor -%}
      </ul>
    {%- endif -%}
  </div>
  </section>
  <section id="content2" class="tab-content">
  <div class="list">
    {%- if site.categories.artwork.size > 0 -%}
      <ul>
        {%- for post in site.categories.press -%}
        <li>
          <a href="{{ post.url }}" ><img class="thumbnail" src="{{ post.thumbnail }}" /></a>
          <h3>
            <a href="{{ post.url | relative_url }}">
              {{ post.title | escape }}
              {%- assign date_format = site.minima.date_format | default: "%Y" -%}
          <span class="post-meta">| {{ post.date | date: date_format }}</span>
            </a>
          </h3>
          {%- if site.show_excerpts -%}
            {{ post.excerpt }}
          {%- endif -%}
        </li>
        {%- endfor -%}
      </ul>
    {%- endif -%}
  </div>
  </section>
</div> <!-- end .tabs -->
