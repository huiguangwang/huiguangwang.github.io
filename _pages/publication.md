---
layout: single
permalink: /pub/
title: Publications
classes: wide
author_profile: true
last_modified_at: 2026-04-19
---

{% comment %} 
  一次性初始化所有变量，确保在 HTML 渲染前完成所有逻辑计算
{% endcomment %}
{% assign all_docs = site.pages %}
{% assign p2026 = "" | split: "" %}
{% assign p2025 = "" | split: "" %}
{% assign p2024 = "" | split: "" %}
{% assign p2022 = "" | split: "" %}
{% assign thesis = "" | split: "" %}
{% assign design = "" | split: "" %}

{% for p in all_docs %}
  {% if p.path contains 'publication/2026/' %}{% assign p2026 = p2026 | push: p %}
  {% elsif p.path contains 'publication/2025/' %}{% assign p2025 = p2025 | push: p %}
  {% elsif p.path contains 'publication/2024/' %}{% assign p2024 = p2024 | push: p %}
  {% elsif p.path contains 'publication/2022/' %}{% assign p2022 = p2022 | push: p %}
  {% elsif p.path contains 'publication/thesis/' %}{% assign thesis = thesis | push: p %}
  {% elsif p.path contains 'publication/design/' %}{% assign design = design | push: p %}
  {% endif %}
{% endfor %}

{% assign paper_total = p2026.size | plus: p2025.size | plus: p2024.size | plus: p2022.size %}

{% comment %} --- 导航栏渲染 --- {% endcomment %}
<div id="categories" style="margin-bottom: 20px; display: flex; flex-wrap: wrap; gap: 20px; font-size: 16px; line-height: 24px;">
  <div style="flex: 0 0 calc(33.333% - 20px); display: flex; justify-content: space-between; border-bottom: 1px solid #ccc; padding-bottom: 10px;">
    <div><a href="#papers-and-patents" style="text-decoration:none;color:black;">Papers</a></div>
    <div><strong>({{ paper_total }})</strong></div>
  </div>
  <div style="flex: 0 0 calc(33.333% - 20px); display: flex; justify-content: space-between; border-bottom: 1px solid #ccc; padding-bottom: 10px;">
    <div><a href="#thesis" style="text-decoration:none;color:black;">Thesis</a></div>
    <div>({{ thesis.size }})</div>
  </div>
  <div style="flex: 0 0 calc(33.333% - 20px); display: flex; justify-content: space-between; border-bottom: 1px solid #ccc; padding-bottom: 10px;">
    <div><a href="#design-work" style="text-decoration:none;color:black;">Design</a></div>
    <div>({{ design.size }})</div>
  </div>
</div>

<h2 id="papers-and-patents">Papers and Patents</h2>

{% comment %} --- 年份快速跳转 --- {% endcomment %}
<div style="display: flex; gap: 15px; margin-bottom: 20px;">
  <a href="#2026">2026 ({{ p2026.size }})</a> | 
  <a href="#2025">2025 ({{ p2025.size }})</a> | 
  <a href="#2024">2024 ({{ p2024.size }})</a> | 
  <a href="#2022">2022 ({{ p2022.size }})</a>
</div>

<b>* means corresponding author and † means co-first author</b>

<h3 id="2026">2026</h3><hr>
{% assign sorted_2026 = p2026 | sort: "name" | reverse %}
{% for p in sorted_2026 %}{{ p.content }}{% endfor %}

<h3 id="2025">2025</h3><hr>
{% assign sorted_2025 = p2025 | sort: "name" | reverse %}
{% for p in sorted_2025 %}{{ p.content }}{% endfor %}

<h3 id="2024">2024</h3><hr>
{% assign sorted_2024 = p2024 | sort: "name" | reverse %}
{% for p in sorted_2024 %}{{ p.content }}{% endfor %}

<h3 id="2022">2022</h3><hr>
{% assign sorted_2022 = p2022 | sort: "name" | reverse %}
{% for p in sorted_2022 %}{{ p.content }}{% endfor %}

<h2 id="thesis">Thesis</h2>
{% for p in thesis %}{{ p.content }}{% endfor %}

<h2 id="design-work">Design Work</h2>
{% for p in design %}{{ p.content }}{% endfor %}



<div style="text-align: justify;">
  <p>New publications will come soon!🚀🚀🚀</p>
</div>



## Thesis


{% assign thesis = site.pages
  | where_exp: "p", "p.path contains 'publication/thesis/'"
  | sort: "name" | reverse %}

{% for p in thesis %}
  {{ p.content }}
{% endfor %}


## Design Work

{% assign design = site.pages
  | where_exp: "p", "p.path contains 'publication/design/'"
  | sort: "name" | reverse %}

{% for p in design %}
  {{ p.content }}
{% endfor %}



<!-- Back to Top Button -->
<div style="position: fixed; right: 20px; top: 500px;">
  <a href="#" style="text-decoration: none; background-color: #007bff; color: white; padding: 10px 20px; border-radius: 4px; font-size: 14px; box-shadow: 0 1px 3px rgba(0,0,0,0.3);">
    Back to Top
  </a>
</div>
