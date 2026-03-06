---
layout: single
permalink: /pub/
title: Publications
classes: wide
author_profile: true
last_modified_at: 2025-09-21
comments: True
---


{% assign p2026 = site.pages | where_exp:"p","p.path contains 'publication/2026/'" %}
{% assign p2025 = site.pages | where_exp:"p","p.path contains 'publication/2025/'" %}
{% assign p2024 = site.pages | where_exp:"p","p.path contains 'publication/2024/'" %}
{% assign p2022 = site.pages | where_exp:"p","p.path contains 'publication/2022/'" %}

{% assign paper_total = 0 %}
{% assign paper_total = paper_total | plus: p2026.size %}
{% assign paper_total = paper_total | plus: p2025.size %}
{% assign paper_total = paper_total | plus: p2024.size %}
{% assign paper_total = paper_total | plus: p2022.size %}

<div id="categories" style="margin-bottom: 20px; display: flex; flex-wrap: wrap; gap: 20px; font-size: 16px; line-height: 24px;">
  <div style="flex: 0 0 calc(33.333% - 20px); display: flex; justify-content: space-between; border-bottom: 1px solid #ccc; padding-bottom: 10px; box-sizing: border-box;">
    <div><a href="#papers-and-patents" style="text-decoration: none; color:rgb(0, 0, 0);">Papers</a></div>
    <div><a href="#papers-and-patents" style="text-decoration: none; color:rgb(0, 0, 0);" id="paper-count">({{ paper_total }})</a></div>
  </div>
</div>


<div id="categories" style="margin-bottom: 20px; display: flex; flex-wrap: wrap; gap: 20px; font-size: 16px; line-height: 24px;">
  <div style="flex: 0 0 calc(33.333% - 20px); display: flex; justify-content: space-between; border-bottom: 1px solid #ccc; padding-bottom: 10px; box-sizing: border-box;">
    <div><a href="#papers-and-patents" style="text-decoration: none; color:rgb(0, 0, 0);">Papers</a></div>
    <div><a href="#papers-and-patents" style="text-decoration: none; color:rgb(0, 0, 0);" id="paper-count">({{ paper_total }})</a></div>
  </div>
  <div style="flex: 0 0 calc(33.333% - 20px); display: flex; justify-content: space-between; border-bottom: 1px solid #ccc; padding-bottom: 10px; box-sizing: border-box;">
    <div><a href="#thesis" style="text-decoration: none; color:rgb(0, 0, 0);">Thesis</a></div>
    <div><a href="#thesis" style="text-decoration: none; color:rgb(0, 0, 0);">(2)</a></div>
  </div>
  <div style="flex: 0 0 calc(33.333% - 20px); display: flex; justify-content: space-between; border-bottom: 1px solid #ccc; padding-bottom: 10px; box-sizing: border-box;">
    <div><a href="#design-work" style="text-decoration: none; color:rgb(0, 0, 0);">Design</a></div>
    <div><a href="#design-work" style="text-decoration: none; color:rgb(0, 0, 0);">(6)</a></div>
  </div>
  
</div>





## Papers and Patents




<div id="categories" style="margin-bottom: 20px; display: flex; flex-wrap: wrap; gap: 20px; font-size: 16px; line-height: 24px;">

  <div style="flex: 0 0 calc(33.333% - 20px); display: flex; justify-content: space-between; border-bottom: 1px solid #ccc; padding-bottom: 10px;">
    <div><a href="#2026" style="text-decoration:none;color:black;">2026</a></div>
    <div><a href="#2026" style="text-decoration:none;color:black;">({{ p2026 | size }})</a></div>
  </div>

  <div style="flex: 0 0 calc(33.333% - 20px); display: flex; justify-content: space-between; border-bottom: 1px solid #ccc; padding-bottom: 10px;">
    <div><a href="#2025" style="text-decoration:none;color:black;">2025</a></div>
    <div><a href="#2025" style="text-decoration:none;color:black;">({{ p2025 | size }})</a></div>
  </div>

  <div style="flex: 0 0 calc(33.333% - 20px); display: flex; justify-content: space-between; border-bottom: 1px solid #ccc; padding-bottom: 10px;">
    <div><a href="#2024" style="text-decoration:none;color:black;">2024</a></div>
    <div><a href="#2024" style="text-decoration:none;color:black;">({{ p2024 | size }})</a></div>
  </div>

  <div style="flex: 0 0 calc(33.333% - 20px); display: flex; justify-content: space-between; border-bottom: 1px solid #ccc; padding-bottom: 10px;">
    <div><a href="#2022" style="text-decoration:none;color:black;">2022</a></div>
    <div><a href="#2022" style="text-decoration:none;color:black;">({{ p2022 | size }})</a></div>
  </div>

</div>


<b>* means corresponding author and † means co-first author</b>


### 2026
<hr>

{% assign papers_2026 = site.pages
  | where_exp: "p", "p.path contains 'publication/2026/'"
  | sort: "name" | reverse %}

{% for p in papers_2026 %}
  {{ p.content }}
{% endfor %}



### 2025
<hr>
{% assign papers_2025 = site.pages
  | where_exp: "p", "p.path contains 'publication/2025/'"
  | sort: "name" | reverse %}

{% for p in papers_2025 %}
  {{ p.content }}
{% endfor %}



### 2024
<hr>
{% assign papers_2024 = site.pages
  | where_exp: "p", "p.path contains 'publication/2024/'"
  | sort: "name" | reverse %}

{% for p in papers_2024 %}
  {{ p.content }}
{% endfor %}



### 2022
<hr>
{% assign papers_2022 = site.pages
  | where_exp: "p", "p.path contains 'publication/2022/'"
  | sort: "name" | reverse %}

{% for p in papers_2022 %}
  {{ p.content }}
{% endfor %}



<div style="text-align: justify;">
  <p>New publications will come soon!🚀🚀🚀</p>
</div>

<script>
  window.addEventListener('DOMContentLoaded', () => {
    const paperCount = document.querySelectorAll('.paper-patent-item').length;
    const paperCountElement = document.querySelector('#paper-count');
    if (paperCountElement) {
      paperCountElement.textContent = `(${paperCount})`;
    }
  });
</script>

## Thesis

<hr>
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
