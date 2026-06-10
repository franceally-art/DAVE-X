<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0, user-scalable=yes">
  <title>france-tech | WhatsApp Bot by Dave Tech</title>
  <link href="https://fonts.googleapis.com/css2?family=Inter:opsz,wght@14..32,300;14..32,400;14..32,600;14..32,700;14..32,800&display=swap" rel="stylesheet">
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      background: linear-gradient(145deg, #0b1120 0%, #0a0f1c 100%);
      font-family: 'Inter', sans-serif;
      color: #eef2ff;
      padding: 2rem 1rem;
    }

    .container {
      max-width: 1200px;
      margin: 0 auto;
    }

    .hero {
      text-align: center;
      margin-bottom: 2rem;
    }

    .hero img {
      max-width: 280px;
      width: 100%;
      border-radius: 32px;
      box-shadow: 0 20px 35px -12px rgba(0, 0, 0, 0.6), 0 0 0 1px rgba(255, 255, 255, 0.05);
      transition: transform 0.2s ease;
    }

    .hero img:hover {
      transform: scale(1.01);
    }

    .button-strip {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      gap: 18px;
      margin: 32px 0 20px;
    }

    .btn {
      display: inline-flex;
      align-items: center;
      justify-content: center;
      gap: 8px;
      background: rgba(20, 30, 55, 0.7);
      backdrop-filter: blur(8px);
      border-radius: 60px;
      padding: 10px 24px;
      font-weight: 600;
      font-size: 1rem;
      text-decoration: none;
      transition: all 0.25s;
      border: 1px solid rgba(255, 255, 255, 0.15);
    }

    .btn-purple {
      background: linear-gradient(135deg, #a855f7, #7c3aed);
      color: white;
      box-shadow: 0 8px 18px rgba(124, 58, 237, 0.3);
      border: none;
    }

    .btn-blue {
      background: linear-gradient(135deg, #3b82f6, #2563eb);
      color: white;
      box-shadow: 0 8px 18px rgba(37, 99, 235, 0.3);
    }

    .btn-dark {
      background: #1e293b;
      border: 1px solid #334155;
      color: #e2e8f0;
    }

    .btn-dark:hover {
      background: #2d3a54;
      transform: translateY(-3px);
    }

    .btn-purple:hover, .btn-blue:hover {
      transform: translateY(-3px);
      filter: brightness(1.05);
    }

    .section-title {
      text-align: center;
      font-size: 1.8rem;
      font-weight: 700;
      margin: 48px 0 20px;
      background: linear-gradient(120deg, #c084fc, #60a5fa);
      background-clip: text;
      -webkit-background-clip: text;
      color: transparent;
    }

    .deploy-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(180px, 220px));
      justify-content: center;
      gap: 20px;
      margin: 20px 0 10px;
    }

    .deploy-card {
      background: rgba(15, 23, 42, 0.7);
      backdrop-filter: blur(12px);
      border-radius: 32px;
      padding: 12px 12px;
      text-align: center;
      transition: all 0.2s;
      border: 1px solid rgba(255, 255, 255, 0.08);
    }

    .deploy-card img {
      width: 48px;
      margin-bottom: 8px;
      filter: drop-shadow(0 4px 6px rgba(0,0,0,0.3));
    }

    .deploy-card a {
      text-decoration: none;
      font-weight: 600;
      font-size: 0.9rem;
      color: #e0e7ff;
    }

    .tutorial-section {
      background: rgba(0, 0, 0, 0.35);
      border-radius: 48px;
      padding: 32px 24px;
      margin: 50px 0 40px;
      text-align: center;
      border: 1px solid rgba(255,255,240,0.1);
    }

    .youtube-link {
      background: #ff0000cc;
      backdrop-filter: blur(4px);
      padding: 12px 30px;
      border-radius: 60px;
      font-weight: 700;
      font-size: 1.2rem;
      display: inline-flex;
      align-items: center;
      gap: 12px;
      transition: 0.2s;
      color: white;
      text-decoration: none;
    }

    .youtube-link:hover {
      background: #ff0000;
      transform: scale(1.02);
    }

    .author-box {
      background: linear-gradient(105deg, #111827, #0f172a);
      border-radius: 40px;
      padding: 28px 20px;
      margin: 30px 0;
      display: flex;
      flex-wrap: wrap;
      justify-content: space-between;
      align-items: center;
      gap: 20px;
      border: 1px solid #2d3a5e;
    }

    .author-info h3 {
      font-size: 1.8rem;
      font-weight: 800;
      background: linear-gradient(135deg, #f0f9ff, #c4b5fd);
      background-clip: text;
      -webkit-background-clip: text;
      color: transparent;
    }

    .movie-link {
      background: #e11d48;
      padding: 12px 28px;
      border-radius: 60px;
      font-weight: bold;
      color: white;
      text-decoration: none;
      display: inline-flex;
      align-items: center;
      gap: 10px;
    }

    .notes {
      background: #0f172ab3;
      border-left: 6px solid #f97316;
      padding: 20px 24px;
      border-radius: 28px;
      margin: 30px 0;
    }

    .support-buttons {
      display: flex;
      flex-wrap: wrap;
      gap: 18px;
      justify-content: center;
      margin: 30px 0 20px;
    }

    .footer {
      text-align: center;
      margin-top: 55px;
      font-size: 0.85rem;
      opacity: 0.8;
      border-top: 1px solid #1e2a3e;
      padding-top: 28px;
    }

    .dave-badge {
      display: inline-block;
      background: #2d3e6e80;
      padding: 4px 12px;
      border-radius: 30px;
      font-size: 0.75rem;
      font-weight: 500;
      margin-top: 8px;
      backdrop-filter: blur(4px);
    }

    @media (max-width: 680px) {
      .button-strip { gap: 12px; }
      .btn { padding: 8px 18px; font-size: 0.85rem; }
      .section-title { font-size: 1.5rem; }
      .author-info h3 { font-size: 1.4rem; }
    }
  </style>
</head>
<body>
<div class="container">
  <div class="hero">
    <img src="https://i.postimg.cc/SN7hNHj7/825d6f2ca39ea3bef8f4ee16b3d7f961.jpg" alt="france-tech bot banner">
  </div>

  <div class="button-strip">
    <a href="https://ultragenerator.onrender.com/" class="btn btn-purple" target="_blank">✨ Pair Site One</a>
    <a href="https://davex254-sessions.onrender.com" class="btn btn-blue" target="_blank">🔷 Pair Site Two</a>
    <a href="https://github.com/franceally-art/DAVE-X/fork" class="btn btn-dark" target="_blank">🍴 Fork france-tech</a>
    <a href="https://github.com/franceally-art/DAVE-X/archive/refs/heads/main.zip" class="btn btn-dark" target="_blank">📦 Download ZIP</a>
  </div>

  <div class="section-title">🚀 DEPLOYMENT SITES (ONE CLICK)</div>
  <div class="deploy-grid">
    <div class="deploy-card"><a href="https://dashboard.heroku.com/new?template=https://github.com/franceally-art/DAVE-X" target="_blank"><img src="https://img.icons8.com/color/48/heroku.png" alt="heroku"><br>Heroku</a></div>
    <div class="deploy-card"><a href="https://replit.com/github/franceally-art/DAVE-X" target="_blank"><img src="https://img.icons8.com/color/48/replit.png" alt="replit"><br>Replit</a></div>
    <div class="deploy-card"><a href="https://app.koyeb.com/deploy?type=git&repository=github.com/franceally-art/DAVE-X" target="_blank"><img src="https://img.icons8.com/color/48/koyeb.png" alt="koyeb"><br>Koyeb</a></div>
    <div class="deploy-card"><a href="https://railway.app/new/template?template=https://github.com/franceally-art/DAVE-X" target="_blank"><img src="https://img.icons8.com/color/48/railway.png" alt="railway"><br>Railway</a></div>
    <div class="deploy-card"><a href="https://render.com/deploy?repo=https://github.com/franceally-art/DAVE-X" target="_blank"><img src="https://img.icons8.com/color/48/render.png" alt="render"><br>Render</a></div>
    <div class="deploy-card"><a href="https://app.netlify.com/start/deploy?repository=https://github.com/franceally-art/DAVE-X" target="_blank"><img src="https://img.icons8.com/color/48/netlify.png" alt="netlify"><br>Netlify</a></div>
    <div class="deploy-card"><a href="https://dashboard.katabump.com/auth/login#ce51a9" target="_blank"><img src="https://img.icons8.com/ios-filled/50/cloudflare.png" alt="katabump"><br>Katabump</a></div>
  </div>

  <!-- TUTORIAL + YT + WA Channel (updated) -->
  <div class="tutorial-section">
    <div class="video-badge">
      <a href="https://youtu.be/wJKMV0BSqpE?si=6Y11rPD0t2ykoxB8" target="_blank" class="youtube-link">
        ▶️ WATCH TUTORIAL 2026
      </a>
    </div>
    <p style="margin-top: 18px; max-width: 600px; margin-left: auto; margin-right: auto;">
      <strong>How to deploy france-tech bot on panel – Dave Tech step-by-step guide</strong><br>
      Get your WhatsApp bot running smoothly.
    </p>
    <div style="margin-top: 18px; display: flex; gap: 20px; justify-content: center; flex-wrap: wrap;">
      <a href="https://youtube.com/@franc-t7e?si=8aGFwkkM3lfu-zk1" target="_blank" style="color:#c084fc; text-decoration: none; font-weight: 500;">📺 YouTube: @franc-t7e</a>
      <a href="https://whatsapp.com/channel/0029VbBZ14b5Ejxym9XVNF2e" target="_blank" style="background: #075e54cc; padding: 6px 18px; border-radius: 40px; text-decoration: none; color: white; font-weight: 500;">💬 WhatsApp Channel</a>
    </div>
  </div>

  <!-- AUTHOR SECTION : Dave Tech is BACK prominently -->
  <div class="author-box">
    <div class="author-info">
      <h3>👨‍💻 Dave Tech × france-tech</h3>
      <p style="margin-top: 6px;">Built with passion by <strong>Dave Tech (DaveX)</strong> &nbsp;|&nbsp; france ally collaboration</p>
      <p style="font-size: 0.9rem; margin-top: 8px;">⚡ Advanced WhatsApp bot · Multi-device · Group tools · Media downloader</p>
      <div class="dave-badge">⭐ Original creator: DAVE-X | maintained by franceally-art</div>
    </div>
    <a href="https://davexmovies.vercel.app" target="_blank" class="movie-link">
      🎬 DAVEXMOVIES · Stream & Watch
    </a>
  </div>

  <div class="notes">
    <h4 style="display: flex; gap: 8px; align-items: center;">📌 IMPORTANT NOTES (Dave Tech legacy)</h4>
    <ul style="margin-top: 12px; margin-left: 20px; line-height: 1.5;">
      <li>On free panels, <strong>set session ID in .env</strong> (SESSION_ID=your_code).</li>
      <li>If bot not responding → change session ID or redeploy.</li>
      <li>Watch <strong>tutorial video</strong> above for detailed deployment on panel/render/railway.</li>
      <li>Fork the repo from: <a href="https://github.com/franceally-art" style="color:#93c5fd;" target="_blank">github.com/franceally-art</a> (original DaveX base).</li>
      <li>Credits: Dave Tech original DAVE-X bot, upgraded & published under france-tech.</li>
    </ul>
  </div>

  <div class="support-buttons">
    <a href="https://github.com/franceally-art/DAVE-X" target="_blank" class="btn btn-dark">⭐ Star DAVE-X</a>
    <a href="https://github.com/franceally-art/DAVE-X/fork" target="_blank" class="btn btn-dark">⑂ Fork france-tech</a>
    <a href="https://youtu.be/wJKMV0BSqpE?si=6Y11rPD0t2ykoxB8" target="_blank" class="btn btn-dark">📺 Tutorial on YouTube</a>
    <a href="https://whatsapp.com/channel/0029VbBZ14b5Ejxym9XVNF2e" target="_blank" class="btn btn-dark">📱 Join WhatsApp Channel</a>
  </div>

  <div class="footer">
    <strong>© 2026 Dave Tech (DAVE-X) & france-tech</strong> · All rights reserved.<br>
    Maintained by france ally · Original bot by Dave Tech · Pair & deploy instantly<br>
    <span style="font-size: 0.7rem;">france-tech | WhatsApp bot | session auth</span>
  </div>
</div>
</body>
</html>