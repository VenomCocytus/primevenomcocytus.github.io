---
layout: page
menu: data visualization
title: Data Visualisation with D3.js
permalink: /datavisualization/
---

<ul class="post-list">
    {%- for post in site.categories['data_visualization'] -%}
    <li>
        {%- assign date_format = site.minima.date_format | default: "%b %-d, %Y" -%}
        <span class="post-meta">
            {{ post.date | date: date_format }}
        </span>
        <span class="post-meta" style="padding-left: 20px;">
          {%- for tag in post.tags -%}
            <a href="/t/{{ tag | downcase | replace: ' ', '-' }}">
              #{{ tag }}
            </a>&nbsp;
          {%- endfor -%}
        </span>
        <h3>
            <a class="post-link" href="{{ post.url | relative_url }}">
                {{ post.title | escape }}
            </a>
        </h3>
        {%- if site.show_excerpts -%}
            {{ post.excerpt }}
        {%- endif -%}
    </li>
    {%- endfor -%}
</ul>