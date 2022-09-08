---
layout: tag
title: "Tag: Data Visualization"
permalink: /t/data_visualization
---

<ul class="post-list">
    {%- for post in site.tags["data_visualization"] -%}
    <li>
        {%- assign date_format = site.minima.date_format | default: "%b %-d, %Y" -%} 
        <span class="post-meta">
            {{ post.date | date: date_format }}
        </span>
        <h3>
            <a class="post-link" href="{{ post.url | relative_url }}">
                {{ post.title | escape }}
            </a>
        </h3>
    </li>
    {%- endfor -%}
</ul>