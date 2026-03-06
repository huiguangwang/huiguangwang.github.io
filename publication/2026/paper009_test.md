<style>
/* ====== Paper Card (Apple-ish / Scholar-ish) ====== */
.paper-card{
  position: relative;
  display:flex;
  gap:18px;
  flex-wrap:wrap;
  align-items:flex-start;

  background: rgba(255,255,255,0.92);
  border: 1px solid rgba(0,0,0,0.08);
  border-radius: 16px;
  padding: 18px;
  margin: 22px 0;

  box-shadow: 0 10px 26px rgba(0,0,0,0.08);
  transition: transform .18s ease, box-shadow .18s ease, border-color .18s ease;
}

/* 整张卡片 hover */
.paper-card:hover{
  transform: translateY(-3px);
  box-shadow: 0 16px 36px rgba(0,0,0,0.12);
  border-color: rgba(0,0,0,0.14);
}

/* 让整张卡片可点击：用绝对定位的 a 覆盖整个卡片 */
.paper-card .card-link{
  position:absolute;
  inset:0;
  border-radius:16px;
  z-index:1;
  text-decoration:none;
}

/* 交互可访问性：键盘聚焦时高亮 */
.paper-card .card-link:focus{
  outline: none;
}
.paper-card .card-link:focus-visible{
  box-shadow: 0 0 0 3px rgba(23,114,208,0.35);
}

/* 内容需要在 card-link 上面 */
.paper-card .paper-inner{
  position:relative;
  z-index:2;
  width:100%;
  display:flex;
  gap:18px;
  flex-wrap:wrap;
  align-items:flex-start;
}

/* 左侧封面 */
.paper-cover{
  position:relative;
  flex: 0 0 300px;
  max-width:300px;
  border-radius:14px;
  overflow:hidden;
  border: 1px solid rgba(0,0,0,0.06);
  background:#fff;
}
.paper-cover img{
  width:100%;
  height:auto;
  display:block;
}

/* 左上角状态标签（在封面上） */
.cover-badge{
  position:absolute;
  top:10px;
  left:10px;
  padding:3px 10px;
  border-radius:999px;
  font-size:12px;
  font-weight:700;
  color:#fff;
  background: rgba(13, 40, 216, 0.92);
  box-shadow: 0 6px 16px rgba(0,0,0,0.18);
}

/* 右侧内容 */
.paper-content{
  flex: 1 1 240px;
  min-width:240px;
  text-align: left;
}

/* 标题 */
.paper-title{
  font-size: 18px;
  line-height: 1.35;
  margin: 2px 0 10px 0;
  color:#0b2540;
  font-weight: 800;
}

/* 作者行 */
.paper-authors{
  margin: 0 0 12px 0;
  color: rgba(0,0,0,0.72);
  font-size: 14px;
}
.paper-authors strong{
  color: rgba(0,0,0,0.86);
}

/* 顶部 tag 行：会议/期刊/状态 */
.tag-row{
  display:flex;
  gap:8px;
  flex-wrap:wrap;
  margin-bottom:10px;
}
.tag{
  display:inline-flex;
  align-items:center;
  gap:6px;
  padding:4px 10px;
  border-radius:999px;
  font-size:12px;
  font-weight:700;
  border:1px solid rgba(0,0,0,0.08);
  background: rgba(0,0,0,0.03);
  color: rgba(0,0,0,0.72);
}

/* 彩色会议 tag（你想加新的直接照着写） */
.tag.icra{ background: rgba(255, 59, 48, 0.10); color: rgba(255, 59, 48, 0.95); border-color: rgba(255, 59, 48, 0.22); }
.tag.iros{ background: rgba(255, 149, 0, 0.12); color: rgba(255, 149, 0, 0.98); border-color: rgba(255, 149, 0, 0.24); }
.tag.rss { background: rgba(52, 199, 89, 0.12); color: rgba(52, 199, 89, 0.98); border-color: rgba(52, 199, 89, 0.24); }
.tag.underreview{ background: rgba(0, 122, 255, 0.12); color: rgba(0, 122, 255, 0.98); border-color: rgba(0, 122, 255, 0.24); }

/* 按钮组 */
.btn-row{
  display:flex;
  gap:10px;
  flex-wrap:wrap;
  margin: 10px 0 6px 0;
}

/* 链接按钮（图标用纯文字符号，不依赖外部库，MD里最稳） */
.paper-btn{
  display:inline-flex;
  align-items:center;
  gap:8px;
  padding:8px 12px;
  border-radius:12px;
  font-size:13px;
  font-weight:700;

  border:1px solid rgba(0,0,0,0.10);
  background: rgba(255,255,255,0.9);
  color: rgba(11,37,64,0.92);
  text-decoration:none;

  box-shadow: 0 6px 16px rgba(0,0,0,0.06);
  transition: transform .15s ease, box-shadow .15s ease, border-color .15s ease;
}

/* 关键：按钮要能点到，必须比 card-link 更高层级 */
.paper-btn{
  position:relative;
  z-index:3;
}

.paper-btn:hover{
  transform: translateY(-1px);
  box-shadow: 0 10px 22px rgba(0,0,0,0.10);
  border-color: rgba(0,0,0,0.16);
}

/* keyword 标签 */
.keyword-row{
  margin-top: 12px;
  display:flex;
  flex-wrap:wrap;
  gap:8px;
}
.keyword{
  display:inline-block;
  padding:6px 10px;
  border-radius:999px;
  font-size:13px;
  background: rgba(0,0,0,0.045);
  border: 1px solid rgba(0,0,0,0.08);
  color: rgba(0,0,0,0.72);
  transition: background .15s ease;
}
.keyword:hover{
  background: rgba(0,0,0,0.07);
}

/* 手机：封面全宽 */
@media (max-width: 780px){
  .paper-cover{
    flex: 1 1 100%;
    max-width: 100%;
  }
}
</style>


<!-- ====== Card 1 ====== -->
<div class="paper-card">

  <!-- 整张卡片点击跳转：把 href 换成你的论文主页 -->
  <a class="card-link" href="https://huiguangwang.top/tutorial/Topology-Agnostic-Robotic-Rebar-Tying/" target="_blank" aria-label="Open paper page"></a>

  <div class="paper-inner">

    <div class="paper-cover">
      <img src="/web_resources/publication/picture/under_review.png" alt="paper cover">
      <span class="cover-badge">Under Review</span>
    </div>

    <div class="paper-content">

      <div class="tag-row">
        <!-- 彩色会议/状态 tag：按需删改 -->
        <span class="tag underreview">Under Review</span>
        <!-- 例如你想标 ICRA / IROS / RSS，就取消注释并选一个 -->
        <!-- <span class="tag icra">ICRA</span> -->
        <!-- <span class="tag iros">IROS</span> -->
        <!-- <span class="tag rss">RSS</span> -->
      </div>

      <div class="paper-title">
        Geometry-Structured Perception for Topology-Agnostic Robotic Rebar Tying
      </div>

      <p class="paper-authors">
        <strong>Huiguang Wang</strong>, Zekai Jin, Yi Shao<sup>*</sup>
      </p>

      <div class="btn-row">
        <!-- 按钮链接：href 换成你真实地址 -->
        <a class="paper-btn" href="https://huiguangwang.top/tutorial/Topology-Agnostic-Robotic-Rebar-Tying/" target="_blank">📄 Page</a>
        <a class="paper-btn" href="https://huiguangwang.top/tutorial/Topology-Agnostic-Robotic-Rebar-Tying/" target="_blank">💻 Code</a>
        <a class="paper-btn" href="https://huiguangwang.top/tutorial/Topology-Agnostic-Robotic-Rebar-Tying/" target="_blank">🧩 Dataset</a>
      </div>

      <div class="keyword-row">
        <span class="keyword">Rebar tying</span>
        <span class="keyword">Topology-agnostic</span>
        <span class="keyword">Collision free</span>
      </div>

    </div>
  </div>
</div>