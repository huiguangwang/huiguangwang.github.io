---
layout: single
permalink: /publication/
title: Publications
classes: wide
author_profile: true
last_modified_at: 2025-01-18
---

<style>
/* 顶部分类栏 */
#categories {
  margin-bottom: 20px;
  display: flex;
  justify-content: space-between;
  font-size: 16px;
  line-height: 24px;
}
#categories > div {
  flex: 1;
  display: flex;
  justify-content: space-between;
  margin-right: 20px;
  border-bottom: 1px solid #ccc;
  padding-bottom: 10px;
}
#categories > div:last-child {
  margin-right: 0;
}
#categories a {
  text-decoration: none;
  color: rgb(0, 0, 0);
}

/* 每个 item 的排版 */
.pub-item {
  display: flex;
  align-items: flex-start;
  margin-top: 20px;
  margin-bottom: 20px;
  gap: 20px; /* 图文间距 */
}

.pub-img {
  position: relative;
  flex-shrink: 0;
  width: 100%;
  max-width: 300px; /* PC 端最大宽度 */
}

.pub-img img {
  width: 100%;
  height: auto;
  display: block;
}

.pub-img span {
  position: absolute;
  top: 10px;
  left: 10px;
  background: rgba(13, 40, 216, 0.9);
  color: #fff;
  padding: 2px 8px;
  font-size: 12px;
  font-weight: bold;
  border-radius: 4px;
  box-shadow: 0 1px 3px rgba(0,0,0,0.3);
}

.pub-text {
  text-align: justify;
}

/* 手机端适配 */
@media (max-width: 768px) {
  .pub-item {
    flex-direction: column; /* 上下结构 */
    align-items: center;
  }
  .pub-img {
    max-width: 90%; /* 手机端缩小 */
    margin-bottom: 10px;
  }
  .pub-text {
    width: 100%;
  }
}
</style>

<div id="categories">
  <div>
    <div><a href="#papers-and-patents">Papers and Patents</a></div>
    <div><a href="#papers-and-patents" id="paper-count">(0)</a></div>
  </div>
  <div>
    <div><a href="#thesis">Thesis</a></div>
    <div><a href="#thesis">(2)</a></div>
  </div>
  <div>
    <div><a href="#design-work">Design Work</a></div>
    <div><a href="#design-work">(6)</a></div>
  </div>
</div>

---

## Papers and Patents
<b>* means corresponding author</b>

<div class="pub-item">
  <div class="pub-img">
    <img src="/web_resources/post/unsupervised_segmentation/preview.png">
    <span>Under Review</span>
  </div>
  <div class="pub-text">
    <span style="color:#1772d0; display: block; margin-bottom: 10px;">
      <b>Rebar Tying and Welding Unified Framework Based on an Unsupervised Rebar Segmentation Algorithm (Under Review)</b>
    </span>
    <p>
      <strong>Huiguang Wang</strong>, Jiayao Zou, Shuo Wang, Yu Dai, Shaopeng Xu, Lu Deng<sup>*</sup><br>
      <a href="https://huiguangwang.top/tutorial/Unsupervised-learning-segmentation/"><b>[Code]</b></a>
    </p>
  </div>
</div>

---

