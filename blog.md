---
layout: page
title: 医聊圈
permalink: /blog/
---

<style>
.blog-page {
  background: linear-gradient(135deg, #0f172a, #1e293b);
  min-height: 100vh;
  padding: 2rem 1rem;
  font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif;
}
.container {
  max-width: 1000px;
  margin: 0 auto;
  background: rgba(255,255,255,0.96);
  padding: 2.5rem;
  border-radius: 16px;
  box-shadow: 0 8px 32px rgba(0,80,150,0.15);
  border-top: 5px solid #007bff;
}
h1 {
  color: #1e293b;
  margin-bottom: 0.5rem;
}
.subtitle {
  color: #64748b;
  margin-bottom: 2rem;
}
.grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(180px, 1fr));
  gap: 1rem;
  margin-bottom: 2rem;
}
.card {
  background: #f8fafc;
  padding: 1.5rem;
  border-radius: 12px;
  text-align: center;
  border-left: 4px solid #007bff;
  transition: 0.3s;
  text-decoration: none;
  color: #1e293b;
  font-weight: 500;
  cursor: pointer;
}
.card:hover {
  transform: translateY(-4px);
  box-shadow: 0 4px 14px rgba(0,100,180,0.15);
}
.section {
  display: none;
  margin-top: 2rem;
}
.section.active {
  display: block;
}
.back-btn {
  background: #007bff;
  color: white;
  border: none;
  padding: 8px 14px;
  border-radius: 8px;
  margin-bottom: 1rem;
  cursor: pointer;
}
.new-topic {
  background: #f1f5f9;
  padding: 1rem;
  border-radius: 8px;
  margin-bottom: 1rem;
}
.new-topic input, .new-topic textarea {
  width: 100%;
  padding: 10px;
  margin-bottom: 8px;
  border: 1px solid #ddd;
  border-radius: 6px;
}
.post-btn {
  background: #007bff;
  color: white;
  border: none;
  padding: 8px 16px;
  border-radius: 8px;
  cursor: pointer;
}
.article {
  background: white;
  padding: 1.2rem;
  border-radius: 10px;
  margin-bottom: 1rem;
  box-shadow: 0 2px 8px rgba(0,0,0,0.05);
}
.article h4 {
  margin: 0 0 0.5rem;
  color: #1e293b;
}
.article p {
  color: #475569;
  margin-bottom: 0.8rem;
}
.comment-box {
  margin-top: 0.8rem;
  padding-top: 0.8rem;
  border-top: 1px solid #eee;
}
.comment-input {
  width: 100%;
  padding: 6px;
  margin-top: 6px;
  border-radius: 6px;
  border: 1px solid #ddd;
}
.comment-item {
  background: #f8f9fa;
  padding: 6px 10px;
  border-radius: 6px;
  margin-top: 6px;
  font-size: 14px;
}
</style>

<div class="blog-page">
  <div class="container">
    <h1>医聊圈</h1>
    <p class="subtitle">临床/麻醉 · 神经科学 · 教学 · 科研 · 自由交流</p>

    <!-- 板块入口 -->
    <div id="sections" class="grid">
      <div class="card" onclick="go('clinical')">📕 临床</div>
      <div class="card" onclick="go('teach')">🎓 教学</div>
      <div class="card" onclick="go('research')">🔬 科研心得</div>
      <div class="card" onclick="go('academic')">📝 学术分享</div>
      <div class="card" onclick="go('chat')">💬 闲聊灌水</div>
    </div>

    <!-- 临床 -->
    <div id="clinical" class="section">
      <button class="back-btn" onclick="back()">← 返回</button>
      <h3>📕 临床</h3>
      <div class="new-topic">
        <input placeholder="文章标题" id="t-clinical">
        <textarea rows="3" placeholder="写点内容…" id="c-clinical"></textarea>
        <button class="post-btn" onclick="post('clinical')">发布文章</button>
      </div>
      <div id="list-clinical"></div>
    </div>

    <!-- 教学 -->
    <div id="teach" class="section">
      <button class="back-btn" onclick="back()">← 返回</button>
      <h3>🎓 教学</h3>
      <div class="new-topic">
        <input placeholder="文章标题" id="t-teach">
        <textarea rows="3" placeholder="写点内容…" id="c-teach"></textarea>
        <button class="post-btn" onclick="post('teach')">发布文章</button>
      </div>
      <div id="list-teach"></div>
    </div>

    <!-- 科研 -->
    <div id="research" class="section">
      <button class="back-btn" onclick="back()">← 返回</button>
      <h3>🔬 科研心得</h3>
      <div class="new-topic">
        <input placeholder="文章标题" id="t-research">
        <textarea rows="3" placeholder="写点内容…" id="c-research"></textarea>
        <button class="post-btn" onclick="post('research')">发布文章</button>
      </div>
      <div id="list-research"></div>
    </div>

    <!-- 学术 -->
    <div id="academic" class="section">
      <button class="back-btn" onclick="back()">← 返回</button>
      <h3>📝 学术分享</h3>
      <div class="new-topic">
        <input placeholder="文章标题" id="t-academic">
        <textarea rows="3" placeholder="写点内容…" id="c-academic"></textarea>
        <button class="post-btn" onclick="post('academic')">发布文章</button>
      </div>
      <div id="list-academic"></div>
    </div>

    <!-- 闲聊 -->
    <div id="chat" class="section">
      <button class="back-btn" onclick="back()">← 返回</button>
      <h3>💬 闲聊灌水</h3>
      <div class="new-topic">
        <input placeholder="文章标题" id="t-chat">
        <textarea rows="3" placeholder="畅所欲言…" id="c-chat"></textarea>
        <button class="post-btn" onclick="post('chat')">发布文章</button>
      </div>
      <div id="list-chat"></div>
    </div>

  </div>
</div>

<script>
let current = "";

function go(sec) {
  current = sec;
  document.getElementById("sections").style.display = "none";
  document.querySelectorAll(".section").forEach(s => s.classList.remove("active"));
  document.getElementById(sec).classList.add("active");
  loadPosts(sec);
}

function back() {
  current = "";
  document.getElementById("sections").style.display = "grid";
  document.querySelectorAll(".section").forEach(s => s.classList.remove("active"));
}

function post(sec) {
  let title = document.getElementById("t-"+sec).value.trim();
  let content = document.getElementById("c-"+sec).value.trim();
  if (!title || !content) return;
  let posts = JSON.parse(localStorage.getItem("posts_"+sec)) || [];
  posts.push({ id: Date.now(), title, content, comments: [] });
  localStorage.setItem("posts_"+sec, JSON.stringify(posts));
  document.getElementById("t-"+sec).value = "";
  document.getElementById("c-"+sec).value = "";
  loadPosts(sec);
}

function loadPosts(sec) {
  let container = document.getElementById("list-"+sec);
  let posts = JSON.parse(localStorage.getItem("posts_"+sec)) || [];
  container.innerHTML = "";
  posts.forEach((post, idx) => {
    let div = document.createElement("div");
    div.className = "article";
    div.innerHTML = `
      <h4>${post.title}</h4>
      <p>${post.content}</p>
      <div class="comment-box">
        <small>评论区</small>
        <input class="comment-input" placeholder="写下评论…" onkeydown="if(event.key==='Enter')addComment(${idx}, this.value, '${sec}')">
        <div id="cmt_${sec}_${idx}"></div>
      </div>
    `;
    container.appendChild(div);
    loadComments(idx, sec);
  });
}

function addComment(pid, text, sec) {
  if (!text.trim()) return;
  let posts = JSON.parse(localStorage.getItem("posts_"+sec)) || [];
  posts[pid].comments.push(text.trim());
  localStorage.setItem("posts_"+sec, JSON.stringify(posts));
  loadComments(pid, sec);
  event.target.value = "";
}

function loadComments(pid, sec) {
  let posts = JSON.parse(localStorage.getItem("posts_"+sec)) || [];
  let box = document.getElementById(`cmt_${sec}_${pid}`);
  box.innerHTML = "";
  posts[pid].comments.forEach(c => {
    let item = document.createElement("div");
    item.className = "comment-item";
    item.innerText = c;
    box.appendChild(item);
  });
}
</script>
