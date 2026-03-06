<style>
.paper-card{
  display:flex;
  align-items:flex-start;
  gap:20px;
  flex-wrap:wrap;

  background:#ffffff;
  border:1px solid #e6e6e6;
  border-radius:14px;
  padding:18px;
  margin:25px 0;

  box-shadow:0 6px 18px rgba(0,0,0,0.08);
  transition:all 0.2s ease;
}

.paper-card:hover{
  transform:translateY(-3px);
  box-shadow:0 10px 26px rgba(0,0,0,0.12);
}

.paper-image{
  position:relative;
  flex:0 0 300px;
  max-width:300px;
  border-radius:10px;
  overflow:hidden;
}

.paper-image img{
  width:100%;
  display:block;
}

.paper-content{
  flex:1 1 200px;
  text-align:justify;
}

.keyword-container{
  margin-top:15px;
}

.keyword{
  display:inline-block;
  padding:4px 12px;
  margin:4px 6px 4px 0;
  font-size:14px;
  border-radius:12px;
  background:#f2f3f5;
  color:#333;
  transition:all 0.2s ease;
}

.keyword:hover{
  background:#e1e5ea;
}

/* 手机适配 */
@media (max-width:768px){
  .paper-image{
    flex:1 1 100%;
    max-width:100%;
  }
}
</style>


<div class="paper-card">

  <div class="paper-image">
    <img src="/web_resources/publication/picture/under_review.png">

    <span style="
      position:absolute;
      top:10px;
      left:10px;
      background:rgba(13,40,216,0.9);
      color:#fff;
      padding:3px 9px;
      font-size:12px;
      font-weight:bold;
      border-radius:4px;
      box-shadow:0 1px 3px rgba(0,0,0,0.3);">
      Under Review
    </span>
  </div>

  <div class="paper-content">

    <span style="color:#1772d0;display:block;margin-bottom:10px;">
      <b>Geometry-Structured Perception for Topology-Agnostic Robotic Rebar Tying (Under Review)</b>
    </span>

    <p>
      <strong>Huiguang Wang</strong>, Zekai Jin, Yi Shao<sup>*</sup><br>

      <a href="https://huiguangwang.top/tutorial/Topology-Agnostic-Robotic-Rebar-Tying/" target="_blank"><b>[Page]</b></a>
      <a href="https://huiguangwang.top/tutorial/Topology-Agnostic-Robotic-Rebar-Tying/" target="_blank"><b>[Code]</b></a>
      <a href="https://huiguangwang.top/tutorial/Topology-Agnostic-Robotic-Rebar-Tying/" target="_blank"><b>[Dataset]</b></a>
    </p>

    <div class="keyword-container">
      <span class="keyword">Rebar tying</span>
      <span class="keyword">Topology-agnostic</span>
      <span class="keyword">Collision free</span>
    </div>

  </div>

</div>