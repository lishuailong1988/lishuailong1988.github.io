---
layout: page
title: 医聊圈
permalink: /blog/
---

<style>
/* 科技医疗风格背景 */
.blog-page {
  background: linear-gradient(135deg, #0f172a, #1e293b);
  min-height: 100vh;
  padding: 2rem 1rem;
  font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif;
}
.blog-container {
  max-width: 920px;
  margin: 0 auto;
  background: rgba(255,255,255,0.96);
  padding: 2.5rem;
  border-radius: 16px;
  box-shadow: 0 8px 32px rgba(0,80,150,0.15);
  border-top: 5px solid #007bff;
}
.blog-title {
  font-size: 2rem;
  color: #0f172a;
  margin-bottom: 0.5rem;
}
.blog-sub {
  color: #64748b;
  margin-bottom: 2rem;
}

/* 五大板块卡片 */
.grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(180px, 1fr));
  gap: 1rem;
  margin-bottom: 2.5rem;
}
.card {
  background: #f8fafc;
  padding: 1.4rem;
  border-radius: 12px;
  text-align: center;
  border-left: 4px solid #007bff;
  transition: 0.3s;
  text-decoration: none;
  color: #1e293b;
  font-weight: 500;
}
.card:hover {
  transform: translateY(-4px);
  box-shadow: 0 4px 14px rgba(0,100,180,0.15);
}

/* 文章板块 */
.article {
  background: #ffffff;
  padding: 2rem;
  border-radius: 12px;
  margin-bottom: 2rem;
  box-shadow: 0 2px 10px rgba(0,0,0,0.05);
}
.article h3 {
  font-size: 1.4rem;
  color: #1e293b;
  margin-top: 0;
  margin-bottom: 1rem;
}

/* 可保存评论区 */
.comment-section {
  margin-top: 1.5rem;
  padding-top: 1rem;
  border-top: 1px solid #eee;
}
.comment-input {
  width: 100%;
  padding: 10px;
  border: 1px solid #ddd;
  border-radius: 8px;
  margin-bottom: 10px;
  font-size: 14px;
}
.comment-btn {
  background: #007bff;
  color: white;
  border: none;
  padding: 8px 16px;
  border-radius: 8px;
  cursor: pointer;
}
.comment-btn:hover {
  background: #005cbf;
}
.comment-list {
  margin-top: 1rem;
  max-height: 300px;
  overflow-y: auto;
}
.comment-item {
  background: #f8f9fa;
  padding: 10px 14px;
  border-radius: 8px;
  margin-bottom: 8px;
  font-size: 14px;
}

.back-home {
  color: #007bff;
  font-weight: bold;
  text-decoration: none;
  margin-top: 2rem;
  display: inline-block;
}
</style>

<div class="blog-page">
<div class="blog-container">

  <h1 class="blog-title">学术博客 & 交流区</h1>
  <p class="blog-sub">麻醉学 · 神经科学 · 教学科研 · 自由交流</p>

  <!-- 五大板块 -->
  <div class="grid">
    <a href="#clinical" class="card">📕 临床</a>
    <a href="#teach" class="card">🎓 教学</a>
    <a href="#research" class="card">🔬 科研心得</a>
    <a href="#academic" class="card">📝 学术分享</a>
    <a href="#chat" class="card">💬 闲聊灌水</a>
  </div>

  <!-- 1 临床 -->
  <div id="clinical" class="article">
    <h3>📕 临床经验</h3>
    <p>在这里记录麻醉管理、危重症、临床技术、病例思考。</p>
    <div class="comment-section">
      <input type="text" class="comment-input" placeholder="写下你的评论…">
      <button class="comment-btn" onclick="addComment('clinical')">发表评论</button>
      <div class="comment-list" id="comments-clinical"></div>
    </div>
  </div>

  <!-- 2 教学 -->
  <div id="teach" class="article">
    <h3>🎓 教学心得</h3>
    <p>在这里记录授课内容、教学经验、学生培养、知识科普。</p>
    <div class="comment-section">
      <input type="text" class="comment-input" placeholder="写下你的评论…">
      <button class="comment-btn" onclick="addComment('teach')">发表评论</button>
      <div class="comment-list" id="comments-teach"></div>
    </div>
  </div>

  <!-- 3 科研心得 -->
  <div id="research" class="article">
    <h3>🔬 科研心得</h3>
    <p>在这里记录课题思路、实验进展、文献阅读、数据分析。</p>
    <div class="comment-section">
      <input type="text" class="comment-input" placeholder="写下你的评论…">
      <button class="comment-btn" onclick="addComment('research')">发表评论</button>
      <div class="comment-list" id="comments-research"></div>
    </div>
  </div>

  <!-- 4 学术分享 -->
  <div id="academic" class="article">
    <h3>📝 学术分享</h3>
    <p>在这里记录学术会议、论文写作、成果分享、行业动态。</p>
    <div class="comment-section">
      <input type="text" class="comment-input" placeholder="写下你的评论…">
      <button class="comment-btn" onclick="addComment('academic')">发表评论</button>
      <div class="comment-list" id="comments-academic"></div>
    </div>
  </div>

  <!-- 5 闲聊灌水 -->
  <div id="chat" class="article">
    <h3>💬 闲聊灌水 · 自由交流</h3>
    <p>生活、心情、行业闲聊、轻松交流，不限主题。</p>
    <div class="comment-section">
      <input type="text" class="comment-input" placeholder="畅所欲言…">
      <button class="comment-btn" onclick="addComment('chat')">发表评论</button>
      <div class="comment-list" id="comments-chat"></div>
    </div>
  </div>

  <a href="/" class="back-home">← 返回首页</a>

</div>
</div>

<script>
// 加载评论
function loadComments(type) {
  let list = document.getElementById("comments-"+type);
  let comments = JSON.parse(localStorage.getItem("comments_"+type)) || [];
  list.innerHTML = "";
  comments.forEach(c => {
    let item = document.createElement("div");
    item.className = "comment-item";
    item.innerText = c;
    list.appendChild(item);
  });
}

// 添加评论
function addComment(type) {
  let input = document.querySelector("#"+type+" .comment-input");
  let val = input.value.trim();
  if (!val) return;
  let comments = JSON.parse(localStorage.getItem("comments_"+type)) || [];
  comments.push(val);
  localStorage.setItem("comments_"+type, JSON.stringify(comments));
  input.value = "";
  loadComments(type);
}

// 初始化所有板块评论
window.onload = () => {
  loadComments("clinical");
  loadComments("teach");
  loadComments("research");
  loadComments("academic");
  loadComments("chat");
};
</script>
