---
layout: page
title: Artwork
permalink: /artwork/
---

<div class="list-label">
 ⊞ Grid | ≣ List
</div>

<div class="grid">
    {%- if site.categories.artwork.size > 0 -%}
    <ul class="post-list">
      {%- for post in site.categories.artwork -%}
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
<div class="list">
  {%- if site.categories.artwork.size > 0 -%}
    <ul>
      {%- for post in site.categories.artwork -%}
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

