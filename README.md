
<style>
  @import url('https://fonts.googleapis.com/css2?family=Space+Mono:wght@400;700&family=Sora:wght@300;400;500;600&display=swap');

  :root {
    --accent: #0E75B6;
    --accent2: #00d4ff;
    --bg: #0d1117;
    --surface: #161b22;
    --surface2: #21262d;
    --border: #30363d;
    --text: #e6edf3;
    --muted: #7d8590;
    --green: #3fb950;
  }

  * { box-sizing: border-box; margin: 0; padding: 0; }

  body { background: transparent; font-family: 'Sora', sans-serif; color: var(--text); }

  .readme-wrap {
    background: var(--bg);
    border-radius: 12px;
    border: 1px solid var(--border);
    overflow: hidden;
    max-width: 800px;
    margin: 0 auto;
  }

  .hero {
    background: linear-gradient(135deg, #0d1117 0%, #161b22 60%, #0e2030 100%);
    padding: 40px 36px 32px;
    border-bottom: 1px solid var(--border);
    position: relative;
    overflow: hidden;
  }

  .hero::before {
    content: '';
    position: absolute;
    top: -60px; right: -60px;
    width: 220px; height: 220px;
    border-radius: 50%;
    background: radial-gradient(circle, rgba(14,117,182,0.18) 0%, transparent 70%);
  }

  .hero-top {
    display: flex;
    align-items: center;
    gap: 20px;
    margin-bottom: 20px;
  }

  .avatar {
    width: 72px; height: 72px;
    border-radius: 50%;
    background: linear-gradient(135deg, #0E75B6, #00d4ff);
    display: flex; align-items: center; justify-content: center;
    font-family: 'Space Mono', monospace;
    font-size: 22px; font-weight: 700;
    color: #fff;
    border: 2px solid rgba(14,117,182,0.5);
    flex-shrink: 0;
  }

  .hero-title h1 {
    font-size: 22px; font-weight: 600;
    color: var(--text);
    line-height: 1.3;
    margin-bottom: 4px;
  }

  .hero-title p {
    font-size: 13px;
    color: var(--muted);
    font-family: 'Space Mono', monospace;
    display: flex; align-items: center; gap: 6px;
  }

  .dot { color: var(--green); font-size: 10px; }

  .tag-row {
    display: flex; flex-wrap: wrap; gap: 8px;
    margin-bottom: 20px;
  }

  .tag {
    font-size: 12px;
    font-family: 'Space Mono', monospace;
    padding: 4px 12px;
    border-radius: 20px;
    border: 1px solid;
  }

  .tag-blue { background: rgba(14,117,182,0.1); border-color: rgba(14,117,182,0.4); color: #58a6ff; }
  .tag-cyan { background: rgba(0,212,255,0.08); border-color: rgba(0,212,255,0.3); color: #00d4ff; }
  .tag-green { background: rgba(63,185,80,0.08); border-color: rgba(63,185,80,0.3); color: #3fb950; }
  .tag-purple { background: rgba(163,113,247,0.08); border-color: rgba(163,113,247,0.3); color: #a371f7; }

  .bio-items {
    display: flex; flex-direction: column; gap: 8px;
  }

  .bio-item {
    display: flex; align-items: flex-start; gap: 10px;
    font-size: 13px; color: #c9d1d9; line-height: 1.5;
  }

  .bio-icon {
    font-size: 15px; flex-shrink: 0; margin-top: 1px;
  }

  .section {
    padding: 24px 36px;
    border-bottom: 1px solid var(--border);
  }

  .section:last-child { border-bottom: none; }

  .section-header {
    display: flex; align-items: center; gap: 10px;
    margin-bottom: 18px;
  }

  .section-header span {
    font-size: 13px; font-weight: 600;
    text-transform: uppercase; letter-spacing: 0.08em;
    color: var(--muted);
    font-family: 'Space Mono', monospace;
  }

  .section-header::after {
    content: '';
    flex: 1; height: 1px;
    background: var(--border);
  }

  .tech-grid {
    display: flex; flex-wrap: wrap; gap: 8px;
  }

  .tech-badge {
    display: flex; align-items: center; gap: 6px;
    padding: 6px 12px;
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: 6px;
    font-size: 12px;
    color: #c9d1d9;
    font-family: 'Space Mono', monospace;
    transition: border-color 0.2s, background 0.2s;
  }

  .tech-badge:hover {
    border-color: var(--accent);
    background: rgba(14,117,182,0.08);
  }

  .tech-dot {
    width: 8px; height: 8px; border-radius: 50%; flex-shrink: 0;
  }

  .stats-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 12px;
  }

  .stat-card {
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: 8px;
    padding: 16px;
    position: relative;
    overflow: hidden;
  }

  .stat-card::before {
    content: '';
    position: absolute;
    top: 0; left: 0; right: 0;
    height: 2px;
    background: linear-gradient(90deg, var(--accent), var(--accent2));
  }

  .stat-label {
    font-size: 11px;
    color: var(--muted);
    font-family: 'Space Mono', monospace;
    text-transform: uppercase;
    letter-spacing: 0.06em;
    margin-bottom: 10px;
  }

  .stat-img { width: 100%; border-radius: 4px; }

  .connect-grid {
    display: flex; gap: 10px; flex-wrap: wrap;
  }

  .connect-btn {
    display: flex; align-items: center; gap: 8px;
    padding: 9px 16px;
    border-radius: 8px;
    font-size: 13px;
    font-family: 'Space Mono', monospace;
    text-decoration: none;
    border: 1px solid var(--border);
    color: #c9d1d9;
    background: var(--surface);
    cursor: pointer;
    transition: all 0.2s;
  }

  .connect-btn:hover { border-color: var(--accent); color: #58a6ff; background: rgba(14,117,182,0.08); }

  .connect-icon { font-size: 15px; }

  .quote-bar {
    background: var(--surface);
    padding: 20px 36px;
    border-top: 1px solid var(--border);
    display: flex;
    align-items: center;
    gap: 12px;
  }

  .quote-line {
    width: 3px; height: 36px;
    background: linear-gradient(180deg, var(--accent), var(--accent2));
    border-radius: 2px;
    flex-shrink: 0;
  }

  .quote-text {
    font-size: 13px;
    color: var(--muted);
    font-style: italic;
    line-height: 1.5;
  }

  .profile-counter {
    font-family: 'Space Mono', monospace;
    font-size: 11px;
    color: var(--muted);
    padding: 10px 36px 6px;
    display: flex;
    align-items: center;
    gap: 6px;
  }

  .counter-dot { width: 6px; height: 6px; border-radius: 50%; background: var(--green); animation: blink 2s infinite; }

  @keyframes blink { 0%,100%{opacity:1;} 50%{opacity:0.3;} }

  .profile-counter span { color: var(--green); font-weight: 700; }
</style>

<div class="readme-wrap">

  <div class="hero">
    <div class="hero-top">
      <div class="avatar">
        <img src="https://raw.githubusercontent.com/7oSkaaa/7oSkaaa/main/Images/about_me.gif" width="125">
      </div>
      <div class="hero-title">
        <h1>Chamath N Dissanayake</h1>
        <p><span class="dot">●</span> Full Stack Developer &amp; Cybersecurity Enthusiast · 🇱🇰 Sri Lanka</p>
      </div>
    </div>

    <div class="tag-row">
      <span class="tag tag-blue">Frontend Developer</span>
      <span class="tag tag-cyan">Cybersecurity Learner</span>
      <span class="tag tag-green">Full-stack Learner</span>
      <span class="tag tag-purple">Open to Collaborate</span>
    </div>

    <div class="bio-items">
      <div class="bio-item"><span class="bio-icon">🛡️</span><span>Exploring <strong>Networking</strong>, <strong>Ethical Hacking</strong> with Kali Linux, and system vulnerabilities</span></div>
      <div class="bio-item"><span class="bio-icon">🐍</span><span>Mastering <strong>Python</strong> for automation and security tooling</span></div>
      <div class="bio-item"><span class="bio-icon">🚀</span><span>Levelling up in <strong>Full Stack</strong> development — building robust end-to-end apps</span></div>
      <div class="bio-item"><span class="bio-icon">⚙️</span><span>Actively learning <strong>CI/CD</strong> pipelines and cloud infrastructure — looking for collaborators!</span></div>
    </div>
  </div>

  <div class="section">
    <div class="section-header"><span>🛠 Languages &amp; Tools</span></div>
    <div class="tech-grid">
      <div class="tech-badge"><span class="tech-dot" style="background:#DD0031"></span>Angular</div>
      <div class="tech-badge"><span class="tech-dot" style="background:#61DAFB"></span>React</div>
      <div class="tech-badge"><span class="tech-dot" style="background:#fff"></span>Next.js</div>
      <div class="tech-badge"><span class="tech-dot" style="background:#F7DF1E"></span>JavaScript</div>
      <div class="tech-badge"><span class="tech-dot" style="background:#007ACC"></span>TypeScript</div>
      <div class="tech-badge"><span class="tech-dot" style="background:#339933"></span>Node.js</div>
      <div class="tech-badge"><span class="tech-dot" style="background:#888"></span>Express</div>
      <div class="tech-badge"><span class="tech-dot" style="background:#777BB4"></span>PHP</div>
      <div class="tech-badge"><span class="tech-dot" style="background:#239120"></span>C#</div>
      <div class="tech-badge"><span class="tech-dot" style="background:#47A248"></span>MongoDB</div>
      <div class="tech-badge"><span class="tech-dot" style="background:#4479A1"></span>MySQL</div>
      <div class="tech-badge"><span class="tech-dot" style="background:#3776AB"></span>Python</div>
      <div class="tech-badge"><span class="tech-dot" style="background:#557C94"></span>Kali Linux</div>
      <div class="tech-badge"><span class="tech-dot" style="background:#fff"></span>Unity</div>
      <div class="tech-badge"><span class="tech-dot" style="background:#F24E1E"></span>Figma</div>
    </div>
  </div>

  <div class="section">
    <div class="section-header"><span>📊 GitHub Stats</span></div>
    <div class="stats-grid">
      <div class="stat-card">
        <div class="stat-label">Top languages</div>
        <img class="stat-img" src="https://github-readme-stats.vercel.app/api/top-langs?username=chamath123-cmyk&show_icons=true&locale=en&layout=compact&theme=tokyonight" alt="Top languages" />
      </div>
      <div class="stat-card">
        <div class="stat-label">Activity</div>
        <img class="stat-img" src="https://github-readme-stats.vercel.app/api?username=chamath123-cmyk&show_icons=true&locale=en&theme=tokyonight" alt="GitHub stats" />
      </div>
      <div class="stat-card" style="grid-column: 1/-1;">
        <div class="stat-label">Streak</div>
        <img class="stat-img" src="https://github-readme-streak-stats.herokuapp.com/?user=chamath123-cmyk&theme=tokyonight" alt="Streak stats" />
      </div>
    </div>
  </div>

  <div class="section">
    <div class="section-header"><span>🏆 Trophies</span></div>
    <img style="width:100%; border-radius:6px;" src="https://github-profile-trophy.vercel.app/?username=chamath123-cmyk&theme=tokyonight&no-frame=true&column=6" alt="GitHub trophies" />
  </div>

  <div class="section">
    <div class="section-header"><span>🤝 Connect with me</span></div>
    <div class="connect-grid">
      <a class="connect-btn" href="mailto:chamathneranjana854@mail.com">
        <span class="connect-icon">✉</span> Email
      </a>
      <a class="connect-btn" href="https://www.facebook.com/Chamathndissanayake" target="_blank">
        <span class="connect-icon">📘</span> Facebook
      </a>
      <a class="connect-btn" href="https://github.com/Chamath123-cmyk" target="_blank">
        <span class="connect-icon">🐙</span> GitHub
      </a>
    </div>
  </div>

  <div class="profile-counter">
    <span class="counter-dot"></span> Profile views: <img src="https://profile-counter.glitch.me/chamath123-cmyk/count.svg" alt="views" style="height:16px; vertical-align:middle; margin-left:4px;" />
  </div>

  <div class="quote-bar">
    <div class="quote-line"></div>
    <div class="quote-text">"Code is like humor. When you have to explain it, it's bad."</div>
  </div>

</div>
