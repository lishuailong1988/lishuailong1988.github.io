---
layout: page
title: 医聊圈| Blog
permalink: /blog/
---

<style>
/* 科技医疗风格 */
.blog-page {
  background: linear-gradient(135deg, #0f172a, #1e293b);
  min-height: 100vh;
  padding: 2rem 1rem;
  font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif;
}
.blog-container {
  max-width: 900px;
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
/* 四大板块卡片 */
.grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
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
}
.card:hover {
  transform: translateY(-4px);
  box-shadow: 0 4px 14px rgba(0,100,180,0.15);
}
.card h3 {
  margin: 0.5rem 0;
  font-size: 1.1rem;
}
/* 文章区域 */
.article {
  background: white;
  padding: 1.5rem;
  border-radius: 12px;
  margin-bottom: 1.5rem;
  box-shadow: 0 2px 8px rgba(0,0,0,0.05);
}
.article h3 {
  color: #1e293b;
  margin-top: 0;
}
/* 评论区 */
.comment-box {
  background: #f8f9fa;
  padding: 1rem;
  border-radius: 8px;
  margin-top: 1rem;
}
.comment-input {
  width: 100%;
  padding: 0.6rem;
  border: 1px solid #ddd;
  border-radius: 6px;
  margin-top: 0.5rem;
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
    <h1 class="blog-title">医聊圈 · Academic Blog</h1>
    <p class="blog-sub">临床麻醉学 · 神经科学 · 专业分享</p>

    <!-- 四大板块 -->
    <div class="grid">
      <a href="#clinical" class="card">
        <h3>临床</h3>
        <p>Clinical</p>
      </a>
      <a href="#teach" class="card">
        <h3>教学</h3>
        <p>Teaching</p>
      </a>
      <a href="#research" class="card">
        <h3>科研心得</h3>
        <p>Research</p>
      </a>
      <a href="#academic" class="card">
        <h3>学术分享</h3>
        <p>Academic</p>
      </a>
      </a>
      <a href="#chat" class="card">
        <h3>闲聊灌水</h3>
        <p>Chat/p>
      </a>
    </div>

    <!-- 内容区 -->
    <div id="clinical" class="article">
      <h3>📚 临床 | Clinical</h3>
      <p>在这里记录临床经验、麻醉管理、病例思考……</p>
      <div class="comment-box">
        <strong>评论区</strong>
        <input type="text" class="comment-input" placeholder="写下你的评论…">
      </div>
    </div>

    <div id="teach" class="article">
      <h3>🎓 教学 | Teaching</h3>
      <p>在这里记录教学心得、授课内容、学生指导……</p>
      <div class="comment-box">
        <strong>评论区</strong>
        <input type="text" class="comment-input" placeholder="写下你的评论…">
      </div>
    </div>

    <div id="research" class="article">
      <h3>🔬 科研心得 | Research</h3>
      <p>在这里记录实验进展、文献阅读、课题思路……</p>
      <div class="comment-box">
        <strong>评论区</strong>
        <input type="text" class="comment-input" placeholder="写下你的评论…">
      </div>
    </div>

    <div id="academic" class="article">
      <h3>📝 学术分享 | Academic</h3>
      <p>在这里记录学术会议、论文写作、成果分享……</p>
      <div class="comment-box">
        <strong>评论区</strong>
        <input type="text" class="comment-input" placeholder="写下你的评论…">
      </div>
    </div>   
  
   <div id="academic" class="article">
      <h3>📝 闲聊灌水 | Chat</h3>
      <p>在这里随性发言……</p>
      <div class="comment-box">
        <strong>评论区</strong>
        <input type="text" class="comment-input" placeholder="写下你的评论…">
      </div>
    
    </div>

    <a href="/" class="back-home">← 返回首页</a>
  </div>
</div>
