<style>

/* ===== Paper Card ===== */

.paper-card{
  position: relative;
  display:flex;
  gap:18px;
  flex-wrap:wrap;
  align-items:flex-start;

  background: rgba(255,255,255,0.95);
  border: 1px solid rgba(0,0,0,0.08);
  border-radius:16px;
  padding:18px;
  margin:24px 0;

  box-shadow:0 10px 26px rgba(0,0,0,0.08);
  transition: all .18s ease;
}

.paper-card:hover{
  transform: translateY(-3px);
  box-shadow:0 16px 36px rgba(0,0,0,0.12);
}

/* 整卡点击 */

.paper-card .card-link{
  position:absolute;
  inset:0;
  border-radius:16px;
  z-index:1;
}

/* 内容层级 */

.paper-inner{
  position:relative;
  z-index:2;
  display:flex;
  gap:18px;
  flex-wrap:wrap;
  width:100%;
}

/* ===== 封面 4:3 比例 ===== */

.paper-cover{
  position:relative;
  flex:0 0 300px;
  max-width:300px;

  aspect-ratio: 4 / 3;

  display:flex;
  align-items:center;
  justify-content:center;

  border-radius:14px;
  overflow:hidden;
  border:1px solid rgba(0,0,0,0.06);
  background:#ffffff
}

.paper-cover img{
  max-width:100%;
  max-height:100%;
  object-fit:contain;
}

/* ===== Under Review badge ===== */

.cover-badge{
  position:absolute;
  top:10px;
  left:10px;

  padding:4px 12px;
  border-radius:999px;

  font-size:12px;
  font-weight:700;
  color:white;

  background: linear-gradient(
    135deg,
    rgba(13,40,216,0.95),
    rgba(84,120,255,0.85)
  );

  box-shadow:0 6px 16px rgba(0,0,0,0.25);
}

/* ===== 右侧内容 ===== */

.paper-content{
  flex:1 1 240px;
  min-width:240px;
}

.paper-title{
  font-size:18px;
  font-weight:800;
  line-height:1.35;
  margin-bottom:8px;
  color:#0b2540;
}

.paper-authors{
  font-size:14px;
  margin-bottom:6px;
  color:rgba(0,0,0,0.75);
}

/* ===== 新增期刊行 ===== */

.paper-venue{
  font-size:14px;
  margin-bottom:12px;
  color:#1772d0;
  font-weight:600;
}

/* ===== 按钮 ===== */

.btn-row{
  display:flex;
  gap:10px;
  flex-wrap:wrap;
  margin-bottom:12px;
}

.paper-btn{
  position:relative;
  z-index:3;

  display:inline-flex;
  align-items:center;
  gap:6px;

  padding:8px 12px;
  border-radius:12px;

  font-size:13px;
  font-weight:700;

  border:1px solid rgba(0,0,0,0.1);
  background:white;

  text-decoration:none;
  color:#0b2540;

  box-shadow:0 6px 16px rgba(0,0,0,0.06);
  transition: all .15s ease;
}

.paper-btn:hover{
  transform:translateY(-1px);
  box-shadow:0 10px 22px rgba(0,0,0,0.12);
}

/* ===== keywords ===== */

.keyword-row{
  display:flex;
  flex-wrap:wrap;
  gap:8px;
}

.keyword{
  padding:6px 10px;
  border-radius:999px;

  font-size:13px;

  background:rgba(0,0,0,0.05);
  border:1px solid rgba(0,0,0,0.08);

  color:rgba(0,0,0,0.7);
}

/* ===== 手机适配 ===== */

@media (max-width:780px){

  .paper-cover{
    flex:1 1 100%;
    max-width:100%;
  }

}

</style>


<div class="paper-card">

<a class="card-link"
href="#"
target="_blank"></a>

<div class="paper-inner">

<div class="paper-cover">

<img src="/web_resources/publication/picture/under_review.png">

<span class="cover-badge">
Under Review
</span>

</div>


<div class="paper-content">

<div class="paper-title">
Harnessing Human Expertise for High-Precision Robotic Assembly in Industrialized Construction: A Sample-Efficient Installer-in-the-Loop Interactive Reinforcement Learning Framework
</div>

<p class="paper-authors">
Zekai Jin, <strong>Huiguang Wang</strong>, Xiaoning Sun, Yi Shao<sup>*</sup>
</p>

<div class="paper-venue">
<!-- Under Review -->
</div>


<div class="btn-row">

<!-- 如果之后有 page / pdf / code 可以加在这里 -->
<!-- 示例 -->

<a class="paper-btn"
href=""
target="_blank">
📑 PDF
</a>

<a class="paper-btn"
href=""
target="_blank">
💻 Code
</a>


</div>


<div class="keyword-row">

<span class="keyword">Windows installation</span>
<span class="keyword">Reinforcement learning</span>
<span class="keyword">Installer-in-the-Loop</span>

</div>

</div>
</div>
</div>