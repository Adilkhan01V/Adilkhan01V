<style>
  @import url('https://fonts.googleapis.com/css2?family=Fira+Code:wght@400;500;700&family=Outfit:wght@300;400;600;700&display=swap');
  
  * {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
  }
  
  :root {
    --primary: #00ff00;
    --secondary: #00ffff;
    --accent: #ff006e;
    --dark-bg: #0a0e27;
    --card-bg: #1a1f3a;
    --text-primary: #ffffff;
    --text-secondary: #a0aec0;
  }
  
  @keyframes glow {
    0%, 100% {
      text-shadow: 0 0 10px var(--primary), 0 0 20px var(--primary);
    }
    50% {
      text-shadow: 0 0 20px var(--primary), 0 0 40px var(--secondary);
    }
  }
  
  @keyframes slideInDown {
    from {
      opacity: 0;
      transform: translateY(-30px);
    }
    to {
      opacity: 1;
      transform: translateY(0);
    }
  }
  
  @keyframes slideInUp {
    from {
      opacity: 0;
      transform: translateY(30px);
    }
    to {
      opacity: 1;
      transform: translateY(0);
    }
  }
  
  @keyframes float {
    0%, 100% {
      transform: translateY(0px);
    }
    50% {
      transform: translateY(-20px);
    }
  }
  
  @keyframes rotate3d {
    0% {
      transform: rotateX(0deg) rotateY(0deg);
    }
    100% {
      transform: rotateX(5deg) rotateY(5deg);
    }
  }
  
  @keyframes shimmer {
    0% {
      background-position: -1000px 0;
    }
    100% {
      background-position: 1000px 0;
    }
  }
  
  @keyframes pulse-glow {
    0%, 100% {
      box-shadow: 0 0 0 0 rgba(0, 255, 0, 0.7);
    }
    50% {
      box-shadow: 0 0 0 10px rgba(0, 255, 0, 0);
    }
  }
  
  .header-container {
    animation: slideInDown 0.8s ease-out;
  }
  
  .title {
    font-family: 'Outfit', sans-serif;
    font-size: 3.5em;
    font-weight: 700;
    animation: glow 3s ease-in-out infinite;
    margin: 20px 0;
  }
  
  .subtitle {
    font-family: 'Fira Code', monospace;
    font-size: 1.1em;
    color: var(--secondary);
    animation: slideInUp 1s ease-out 0.3s both;
  }
  
  .card {
    background: linear-gradient(135deg, rgba(0, 255, 0, 0.1) 0%, rgba(0, 255, 255, 0.1) 100%);
    border: 2px solid var(--primary);
    border-radius: 12px;
    padding: 20px;
    margin: 15px auto;
    backdrop-filter: blur(10px);
    animation: slideInUp 0.8s ease-out;
    transition: all 0.3s ease;
    max-width: 600px;
  }
  
  .card:hover {
    transform: translateY(-5px);
    box-shadow: 0 0 20px rgba(0, 255, 0, 0.5), inset 0 0 20px rgba(0, 255, 255, 0.1);
    animation: pulse-glow 2s infinite;
  }
  
  .tech-stack {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    gap: 10px;
    margin: 20px 0;
  }
  
  .tech-badge {
    font-family: 'Fira Code', monospace;
    background: linear-gradient(135deg, var(--primary), var(--secondary));
    color: #000;
    padding: 8px 16px;
    border-radius: 50px;
    font-weight: 600;
    font-size: 0.9em;
    animation: float 3s ease-in-out infinite;
    border: 2px solid var(--primary);
    transition: all 0.3s ease;
  }
  
  .tech-badge:hover {
    transform: scale(1.1) rotate(2deg);
    box-shadow: 0 0 20px var(--primary);
  }
  
  .section-title {
    font-family: 'Outfit', sans-serif;
    font-size: 2em;
    color: var(--primary);
    margin: 40px 0 20px;
    text-align: center;
    position: relative;
    animation: slideInDown 0.6s ease-out;
  }
  
  .section-title::before {
    content: '';
    position: absolute;
    bottom: -10px;
    left: 50%;
    transform: translateX(-50%);
    width: 100px;
    height: 3px;
    background: linear-gradient(90deg, transparent, var(--primary), var(--secondary), transparent);
    animation: shimmer 2s infinite;
  }
  
  .stats-container {
    display: flex;
    justify-content: center;
    gap: 20px;
    flex-wrap: wrap;
    margin: 30px 0;
  }
  
  .stat-box {
    text-align: center;
    padding: 20px;
    background: rgba(0, 255, 0, 0.05);
    border: 2px solid var(--secondary);
    border-radius: 10px;
    min-width: 150px;
    animation: slideInUp 0.8s ease-out;
    transition: all 0.3s ease;
  }
  
  .stat-box:hover {
    transform: rotateX(10deg) translateY(-5px);
    box-shadow: 0 10px 30px rgba(0, 255, 255, 0.3);
    background: rgba(0, 255, 255, 0.1);
  }
  
  .stat-number {
    font-size: 2em;
    color: var(--primary);
    font-weight: 700;
    animation: glow 3s ease-in-out infinite;
  }
  
  .stat-label {
    color: var(--text-secondary);
    font-size: 0.9em;
    margin-top: 5px;
  }
  
  .divider {
    height: 2px;
    background: linear-gradient(90deg, transparent, var(--primary), var(--secondary), transparent);
    margin: 30px 0;
    animation: shimmer 3s infinite;
  }
  
  .cta-button {
    display: inline-block;
    padding: 12px 24px;
    background: linear-gradient(135deg, var(--primary), var(--secondary));
    color: #000;
    text-decoration: none;
    border-radius: 50px;
    font-weight: 600;
    font-family: 'Outfit', sans-serif;
    margin: 10px;
    border: 2px solid var(--primary);
    transition: all 0.3s ease;
    animation: slideInUp 1s ease-out;
  }
  
  .cta-button:hover {
    transform: translateY(-3px);
    box-shadow: 0 10px 25px rgba(0, 255, 0, 0.4);
  }
  
  .code-block {
    background: rgba(10, 14, 39, 0.9);
    border: 2px solid var(--secondary);
    border-radius: 10px;
    padding: 15px;
    font-family: 'Fira Code', monospace;
    color: var(--primary);
    overflow-x: auto;
    animation: slideInUp 0.8s ease-out;
    text-align: center;
  }
  
  .footer {
    text-align: center;
    margin-top: 50px;
    animation: slideInUp 1.2s ease-out;
    color: var(--text-secondary);
  }
</style>

<div align="center">

<div class="header-container">

# <span class="title">ADIL KHAN</span>

<div class="subtitle">
  ✨ Full-Stack Developer | Tech Enthusiast | Problem Solver ✨
</div>

</div>

---

<div class="card">
  <p style="font-size: 1.2em; color: var(--secondary); margin: 10px 0;">
    🚀 Building next-generation solutions with cutting-edge technology
  </p>
  <p style="color: var(--text-secondary); margin: 10px 0;">
    📚 College student passionate about coding | 🤝 Mentoring beginners | 💡 Always learning & growing
  </p>
</div>

---

<h2 class="section-title">⚙️ Tech Stack</h2>

<div style="margin: 30px 0;">

<div style="margin: 20px 0;">
  <p style="color: var(--secondary); font-weight: 600; margin-bottom: 10px;">Languages</p>
  <div class="tech-stack">
    <span class="tech-badge">C</span>
    <span class="tech-badge">C++</span>
    <span class="tech-badge">JavaScript</span>
    <span class="tech-badge">Python</span>
    <span class="tech-badge">HTML5</span>
  </div>
</div>

<div style="margin: 20px 0;">
  <p style="color: var(--secondary); font-weight: 600; margin-bottom: 10px;">Frontend & Tools</p>
  <div class="tech-stack">
    <span class="tech-badge">Netlify</span>
    <span class="tech-badge">Figma</span>
    <span class="tech-badge">Git</span>
    <span class="tech-badge">GitHub</span>
  </div>
</div>

<div style="margin: 20px 0;">
  <p style="color: var(--secondary); font-weight: 600; margin-bottom: 10px;">Databases & Backend</p>
  <div class="tech-stack">
    <span class="tech-badge">MySQL</span>
    <span class="tech-badge">Firebase</span>
    <span class="tech-badge">Oracle</span>
  </div>
</div>

</div>

<div class="divider"></div>

<h2 class="section-title">📊 GitHub Analytics</h2>

<div class="stats-container">
  <div class="stat-box">
    <div class="stat-number">💻</div>
    <div class="stat-label">Open Source</div>
  </div>
  <div class="stat-box">
    <div class="stat-number">🔥</div>
    <div class="stat-label">Consistent Coder</div>
  </div>
  <div class="stat-box">
    <div class="stat-number">📈</div>
    <div class="stat-label">Always Growing</div>
  </div>
</div>

<div style="margin: 30px 0;">
  <a href="https://github.com/Adilkhan01V" target="_blank">
    <img src="https://github-readme-stats.vercel.app/api?username=Adilkhan01V&theme=tokyonight&hide_border=true&include_all_commits=true&count_private=true&bg_color=0d1117&text_color=30b433&title_color=58a6ff&icon_color=1f6feb" alt="GitHub Stats" style="border-radius: 10px; max-width: 100%; margin: 10px 0;">
  </a>
</div>

<div style="margin: 30px 0;">
  <a href="https://github.com/Adilkhan01V" target="_blank">
    <img src="https://nirzak-streak-stats.vercel.app/?user=Adilkhan01V&theme=tokyonight&hide_border=true&background=0d1117&ring=58a6ff&fire=ff7a15&currStreakNum=30b433" alt="Streak Stats" style="border-radius: 10px; max-width: 100%; margin: 10px 0;">
  </a>
</div>

<div style="margin: 30px 0;">
  <a href="https://github.com/Adilkhan01V" target="_blank">
    <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=Adilkhan01V&theme=tokyonight&hide_border=true&layout=compact&bg_color=0d1117&text_color=30b433&title_color=58a6ff" alt="Top Languages" style="border-radius: 10px; max-width: 100%; margin: 10px 0;">
  </a>
</div>

<div style="margin: 30px 0;">
  <a href="https://github.com/Adilkhan01V" target="_blank">
    <img src="https://github-profile-trophy.vercel.app/?username=Adilkhan01V&theme=tokyonight&no-frame=false&no-bg=true&margin-w=4&row=2" alt="GitHub Trophies" style="max-width: 100%; margin: 10px 0;">
  </a>
</div>

<div class="divider"></div>

<h2 class="section-title">💡 Featured Highlights</h2>

<div class="card">
  <div style="font-size: 1.5em; margin-bottom: 10px;">🎯 Current Focus</div>
  <p style="color: var(--text-secondary);">
    Mastering full-stack development | Contributing to open source | Building portfolio projects
  </p>
</div>

<div class="card">
  <div style="font-size: 1.5em; margin-bottom: 10px;">🤝 Let's Collaborate</div>
  <p style="color: var(--text-secondary);">
    I love mentoring beginners and working on exciting projects together. Let's build something amazing!
  </p>
</div>

<div class="divider"></div>

<h2 class="section-title">🔗 Connect & Explore</h2>

<div style="margin: 30px 0;">
  <a href="mailto:adilkhan52762@gmail.com" class="cta-button">📧 Email Me</a>
  <a href="https://github.com/Adilkhan01V" class="cta-button">💻 Visit GitHub</a>
</div>

<div class="code-block">
  while (true) {<br/>
  &nbsp;&nbsp;learn();<br/>
  &nbsp;&nbsp;build();<br/>
  &nbsp;&nbsp;contribute();<br/>
  &nbsp;&nbsp;repeat();<br/>
  }
</div>

<div class="footer">
  <p style="margin: 30px 0; font-size: 0.9em;">
    <img src="https://visitcount.itsvg.in/api?id=Adilkhan01V&icon=6&color=12" alt="Profile Views">
  </p>
  <p style="margin: 20px 0; color: var(--primary);">
    ⭐ If you find my work interesting, don't forget to star my repositories!
  </p>
  <p style="margin-top: 30px; font-size: 0.85em;">
    Made with 💚 | Designed with passion | Built for the future
  </p>
</div>

</div>
