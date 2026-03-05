<div id="pub-list"></div>

<script>
  const items = [
    {
      imageSrc: "/web_resources/publication/picture/under_review.png",
      imageAlt: "under review",
      badgeText: "Under Review",
      badgeRGBA: "rgba(13, 40, 216, 0.9)",
      title: "Geometry-Driven Perception and Action for Topology-Agnostic Robotic Rebar Tying",
      authorsHtml: "<strong>Huiguang Wang</strong>, Zekai Jin, Yi Shao<sup>*</sup>",
      links: {
        page: "https://huiguangwang.top/tutorial/Topology-Agnostic-Robotic-Rebar-Tying/",
        code: "https://huiguangwang.top/tutorial/Topology-Agnostic-Robotic-Rebar-Tying/",
        dataset: "https://huiguangwang.top/tutorial/Topology-Agnostic-Robotic-Rebar-Tying/"
      },
      extraLinksHtml: "",
      keywords: ["Rebar tying", "Topology-agnostic", "Collision free"]
    }
  ];

  // 建议把样式放全局一次（不要每条都插入）
  const style = document.createElement("style");
  style.textContent = `
    .keyword-container{ margin:20px 0; }
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
    .keyword:hover{ background:#e1e5ea; }
  `;
  document.head.appendChild(style);

  function renderItem(it){
    const keywordsHtml = it.keywords.map(k => `<span class="keyword">${k}</span>`).join("\n");

    return `
<div class="paper-patent-item"
     style="display:flex; align-items:flex-start; margin:20px 0; gap:20px; flex-wrap:wrap;">

  <div style="position:relative; flex:1 1 100%; max-width:300px; margin:0 auto;">
    <img src="${it.imageSrc}" alt="${it.imageAlt}" style="width:100%; height:auto; display:block;">
    <span style="
      position:absolute; top:10px; left:10px;
      background:${it.badgeRGBA};
      color:#fff; padding:2px 8px;
      font-size:12px; font-weight:bold;
      border-radius:4px;
      box-shadow:0 1px 3px rgba(0,0,0,0.3);">
      ${it.badgeText}
    </span>
  </div>

  <div style="text-align:justify; flex:1 1 200px;">
    <span style="color:#1772d0; display:block; margin-bottom:10px;">
      <b>${it.title}</b>
    </span>

    <p>
      ${it.authorsHtml}<br>
      <a href="${it.links.page}" target="_blank" rel="noopener"><b>[Page]</b></a>
      <a href="${it.links.code}" target="_blank" rel="noopener"><b>[Code]</b></a>
      <a href="${it.links.dataset}" target="_blank" rel="noopener"><b>[Dataset]</b></a>
      ${it.extraLinksHtml || ""}
    </p>

    <div class="keyword-container">
      ${keywordsHtml}
    </div>
  </div>
</div>`;
  }

  document.getElementById("pub-list").innerHTML = items.map(renderItem).join("\n");
</script>