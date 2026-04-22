
<style>
  @import url('https://fonts.googleapis.com/css2?family=Press+Start+2P&display=swap');
  * { box-sizing: border-box; margin: 0; padding: 0; image-rendering: pixelated; }
  body { background: transparent; }
  .mc { font-family: 'Press Start 2P', monospace; }

  .wrapper {
    background: #1a1a2e;
    border: 4px solid #5BFF6E;
    box-shadow: inset 0 0 0 4px #1a1a2e, 0 0 0 8px #2d5a2e;
    padding: 24px;
    color: #fff;
  }

  /* Header */
  .header {
    text-align: center;
    margin-bottom: 24px;
    border-bottom: 4px solid #5BFF6E;
    padding-bottom: 20px;
  }
  .header-ascii {
    font-family: 'Press Start 2P', monospace;
    font-size: 13px;
    color: #5BFF6E;
    letter-spacing: 2px;
    line-height: 1.8;
    text-shadow: 2px 2px #003300;
  }
  .typing-row {
    margin-top: 14px;
    font-family: 'Press Start 2P', monospace;
    font-size: 10px;
    color: #5BFF6E;
  }

  /* Section */
  .section {
    margin-bottom: 20px;
    background: #0d1117;
    border: 3px solid #2d4a2e;
    padding: 16px;
  }
  .section-title {
    font-family: 'Press Start 2P', monospace;
    font-size: 10px;
    color: #5BFF6E;
    margin-bottom: 14px;
    border-bottom: 2px solid #2d4a2e;
    padding-bottom: 8px;
  }
  .yaml-block {
    font-family: monospace;
    font-size: 12px;
    color: #ccc;
    line-height: 2;
  }
  .yaml-key { color: #FF6B35; }
  .yaml-val { color: #5BFF6E; }

  .quote {
    font-family: monospace;
    font-size: 12px;
    color: #aaa;
    border-left: 3px solid #FF6B35;
    padding-left: 10px;
    margin-top: 12px;
    font-style: italic;
  }

  /* Skill bars */
  .skill-row { margin-bottom: 10px; }
  .skill-label {
    font-family: 'Press Start 2P', monospace;
    font-size: 8px;
    color: #aaa;
    margin-bottom: 4px;
  }
  .skill-bar-bg {
    height: 14px;
    background: #1a1a2e;
    border: 2px solid #2d4a2e;
    width: 100%;
  }
  .skill-bar-fill {
    height: 100%;
    background: repeating-linear-gradient(
      90deg,
      #5BFF6E 0px, #5BFF6E 10px,
      #3dcc55 10px, #3dcc55 12px
    );
  }

  .tools-grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 8px;
    margin-top: 10px;
  }
  .tool-badge {
    font-family: 'Press Start 2P', monospace;
    font-size: 7px;
    background: #1a3a1e;
    border: 2px solid #5BFF6E;
    color: #5BFF6E;
    padding: 6px 4px;
    text-align: center;
  }

  /* Quest board */
  .quest-item {
    font-family: 'Press Start 2P', monospace;
    font-size: 8px;
    color: #ccc;
    padding: 8px 0;
    border-bottom: 1px solid #2d4a2e;
    display: flex;
    align-items: center;
    gap: 8px;
  }
  .quest-tag {
    font-size: 7px;
    background: #1a3a1e;
    color: #5BFF6E;
    border: 2px solid #5BFF6E;
    padding: 3px 5px;
    white-space: nowrap;
  }
  .quest-tag.upcoming { background: #3a2a00; color: #FF6B35; border-color: #FF6B35; }

  /* Achievements */
  .achievement {
    display: flex;
    align-items: center;
    gap: 10px;
    margin-bottom: 10px;
    background: #0d1117;
    border: 2px solid #2d4a2e;
    padding: 8px 10px;
    transition: border-color 0.1s;
  }
  .achievement:hover { border-color: #5BFF6E; }
  .ach-icon {
    width: 36px;
    height: 36px;
    background: #1a3a1e;
    border: 3px solid #5BFF6E;
    display: flex; align-items: center; justify-content: center;
    font-size: 16px;
    flex-shrink: 0;
  }
  .ach-text { flex: 1; }
  .ach-name {
    font-family: 'Press Start 2P', monospace;
    font-size: 8px;
    color: #FFD700;
    margin-bottom: 3px;
  }
  .ach-desc {
    font-family: monospace;
    font-size: 11px;
    color: #aaa;
  }

  /* Stats scoreboard */
  .stats-grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 10px;
  }
  .stat-card {
    background: #1a1a2e;
    border: 2px solid #2d4a2e;
    padding: 12px 8px;
    text-align: center;
  }
  .stat-num {
    font-family: 'Press Start 2P', monospace;
    font-size: 14px;
    color: #5BFF6E;
  }
  .stat-label {
    font-family: 'Press Start 2P', monospace;
    font-size: 6px;
    color: #888;
    margin-top: 6px;
  }

  /* Connect */
  .connect-row {
    display: flex;
    gap: 10px;
    justify-content: center;
    flex-wrap: wrap;
  }
  .connect-btn {
    font-family: 'Press Start 2P', monospace;
    font-size: 8px;
    background: #1a1a2e;
    border: 2px solid #5BFF6E;
    color: #5BFF6E;
    padding: 10px 14px;
    cursor: pointer;
    text-decoration: none;
    display: inline-block;
  }
  .connect-btn:hover { background: #5BFF6E; color: #0d1117; }

  /* Footer */
  .footer {
    text-align: center;
    margin-top: 20px;
    border-top: 4px solid #2d4a2e;
    padding-top: 16px;
  }
  .footer-warning {
    font-family: 'Press Start 2P', monospace;
    font-size: 7px;
    color: #FF6B35;
    line-height: 2;
  }
  .footer-sub {
    font-family: monospace;
    font-size: 11px;
    color: #555;
    margin-top: 10px;
  }
  .visitor-badge {
    font-family: 'Press Start 2P', monospace;
    font-size: 8px;
    background: #1a3a1e;
    border: 2px solid #5BFF6E;
    color: #5BFF6E;
    padding: 6px 12px;
    display: inline-block;
    margin-top: 10px;
  }

  /* Typing animation */
  @keyframes blink { 0%,100%{opacity:1} 50%{opacity:0} }
  .cursor { display: inline-block; animation: blink 1s infinite; }
  @keyframes typeSwap {
    0%,22%  { content: "Hey there, I'm Steve0123 ⛏️"; }
    25%,47% { content: "Software Developer 💻"; }
    50%,72% { content: "Minecraft Addict 🎮"; }
    75%,97% { content: "Building Cool Stuff 🔨"; }
    100%    { content: "Hey there, I'm Steve0123 ⛏️"; }
  }
</style>

<div class="wrapper">

  <!-- HEADER -->
  <div class="header">
    <div class="header-ascii">
      ░██████╗████████╗███████╗██╗░░░██╗███████╗<br>
      ██╔════╝╚══██╔══╝██╔════╝██║░░░██║██╔════╝<br>
      ╚█████╗░░░░██║░░░█████╗░░╚██╗░██╔╝█████╗░░<br>
      ░╚═══██╗░░░██║░░░██╔══╝░░░╚████╔╝░██╔══╝░░<br>
      ██████╔╝░░░██║░░░███████╗░░╚██╔╝░░███████╗<br>
      ╚═════╝░░░░╚═╝░░░╚══════╝░░░╚═╝░░░╚══════╝
    </div>
    <div class="typing-row" id="typer">Hey there, I'm Steve0123 ⛏️<span class="cursor">_</span></div>
  </div>

  <!-- ABOUT ME -->
  <div class="section">
    <div class="section-title">🪓 STEVE'S LOG — ABOUT ME</div>
    <div class="yaml-block">
      <div><span class="yaml-key">Name:&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</span><span class="yaml-val">Steve Byron (stevebyron0123)</span></div>
      <div><span class="yaml-key">Role:&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</span><span class="yaml-val">Software Developer Intern @ XShark</span></div>
      <div><span class="yaml-key">Location:&nbsp;</span><span class="yaml-val">USA 🇺🇸</span></div>
      <div><span class="yaml-key">Status:&nbsp;&nbsp;&nbsp;</span><span class="yaml-val">Mining through bugs & building solutions</span></div>
      <div><span class="yaml-key">Hobbies:&nbsp;&nbsp;</span><span class="yaml-val">Coding, Crafting, Surviving Creepers</span></div>
    </div>
    <div class="quote">"Just a guy who treats every bug like a Creeper — face it head on or it'll blow up in your face." 💥</div>
  </div>

  <!-- SKILL INVENTORY -->
  <div class="section">
    <div class="section-title">⚔️ SKILL INVENTORY</div>

    <div style="font-family:'Press Start 2P',monospace;font-size:8px;color:#FF6B35;margin-bottom:10px;">WEAPONS (Languages)</div>
    <div class="skill-row"><div class="skill-label">JavaScript</div><div class="skill-bar-bg"><div class="skill-bar-fill" style="width:85%"></div></div></div>
    <div class="skill-row"><div class="skill-label">Python</div><div class="skill-bar-bg"><div class="skill-bar-fill" style="width:75%"></div></div></div>
    <div class="skill-row"><div class="skill-label">TypeScript</div><div class="skill-bar-bg"><div class="skill-bar-fill" style="width:65%"></div></div></div>
    <div class="skill-row"><div class="skill-label">HTML / CSS</div><div class="skill-bar-bg"><div class="skill-bar-fill" style="width:50%"></div></div></div>

    <div style="font-family:'Press Start 2P',monospace;font-size:8px;color:#FF6B35;margin:14px 0 10px;">🛡️ ARMOR (Frameworks & Tools)</div>
    <div class="tools-grid">
      <div class="tool-badge">⚙️ React</div>
      <div class="tool-badge">🔥 Node.js</div>
      <div class="tool-badge">🛠️ Git</div>
      <div class="tool-badge">🗄️ SQL</div>
      <div class="tool-badge">🐳 Docker</div>
      <div class="tool-badge">☁️ Cloud</div>
    </div>

    <div style="font-family:'Press Start 2P',monospace;font-size:8px;color:#FF6B35;margin:14px 0 10px;">🧱 BUILDING BLOCKS (Learning)</div>
    <div class="tools-grid">
      <div class="tool-badge" style="border-color:#aaa;color:#aaa;">🌱 Architecture</div>
      <div class="tool-badge" style="border-color:#aaa;color:#aaa;">🌱 Sys Design</div>
      <div class="tool-badge" style="border-color:#aaa;color:#aaa;">🌱 DevOps</div>
    </div>
  </div>

  <!-- QUEST BOARD -->
  <div class="section">
    <div class="section-title">🏰 QUEST BOARD — ACTIVE MISSIONS</div>
    <div class="quest-item"><span class="quest-tag">IN PROGRESS</span> 🔨 Building scalable web solutions @ XShark</div>
    <div class="quest-item"><span class="quest-tag">IN PROGRESS</span> 🐛 Fixing bugs one commit at a time</div>
    <div class="quest-item"><span class="quest-tag">IN PROGRESS</span> 📚 Leveling up developer skills</div>
    <div class="quest-item" style="border:none"><span class="quest-tag upcoming">UPCOMING</span> 🌐 Launching personal projects into the wild</div>
  </div>

  <!-- STATS -->
  <div class="section">
    <div class="section-title">📊 THE SCOREBOARD</div>
    <div class="stats-grid">
      <div class="stat-card"><div class="stat-num">0</div><div class="stat-label">Repos</div></div>
      <div class="stat-card"><div class="stat-num">0</div><div class="stat-label">Stars</div></div>
      <div class="stat-card"><div class="stat-num">1</div><div class="stat-label">Day Streak</div></div>
    </div>
    <div style="font-family:'Press Start 2P',monospace;font-size:7px;color:#555;text-align:center;margin-top:12px;">[ Just joined — watch this space grow ] 🌱</div>
  </div>

  <!-- ACHIEVEMENTS -->
  <div class="section">
    <div class="section-title">🏆 ACHIEVEMENTS UNLOCKED</div>
    <div class="achievement"><div class="ach-icon">⛏️</div><div class="ach-text"><div class="ach-name">Taking Inventory</div><div class="ach-desc">Started my GitHub journey</div></div></div>
    <div class="achievement"><div class="ach-icon">💻</div><div class="ach-text"><div class="ach-name">Getting Wood</div><div class="ach-desc">Wrote my first lines of code</div></div></div>
    <div class="achievement"><div class="ach-icon">🔥</div><div class="ach-text"><div class="ach-name">Hot Topic</div><div class="ach-desc">Built & deployed a real app</div></div></div>
    <div class="achievement"><div class="ach-icon">🌐</div><div class="ach-text"><div class="ach-name">Into the Nether</div><div class="ach-desc">Survived my first internship</div></div></div>
    <div class="achievement"><div class="ach-icon">🐛</div><div class="ach-text"><div class="ach-name">Monster Hunter</div><div class="ach-desc">Squashed 100+ bugs</div></div></div>
    <div class="achievement"><div class="ach-icon">🤝</div><div class="ach-text"><div class="ach-name">Getting an Upgrade</div><div class="ach-desc">Collaborated on a team project</div></div></div>
    <div class="achievement" style="opacity:0.5"><div class="ach-icon" style="border-color:#555;background:#111">⭐</div><div class="ach-text"><div class="ach-name" style="color:#555">The End?</div><div class="ach-desc">??? Still crafting...</div></div></div>
  </div>

  <!-- CONNECT -->
  <div class="section">
    <div class="section-title">📡 SEND A SIGNAL</div>
    <div class="connect-row">
      <a class="connect-btn" href="https://x.com/byronsmith0123">✖ @byronsmith0123</a>
      <a class="connect-btn" href="https://github.com/stevebyron0123">◈ stevebyron0123</a>
    </div>
  </div>

  <!-- FOOTER -->
  <div class="footer">
    <div class="footer-warning">
      ⚠ WARNING: This developer may start mining at 3AM.<br>
      Creepers have been known to destroy his code.<br>
      He always punches trees first. 🌲
    </div>
    <div class="footer-sub">Made with ❤️ and way too many Minecraft references</div>
    <div class="visitor-badge">👁 Visitors: <span id="vc">0</span></div>
  </div>

</div>

<script>
  const lines = [
    "Hey there, I'm Steve0123 ⛏️",
    "Software Developer 💻",
    "Minecraft Addict 🎮",
    "Building Cool Stuff 🔨"
  ];
  let li = 0, ci = 0, deleting = false;
  const el = document.getElementById('typer');
  function type() {
    const cur = lines[li];
    if (!deleting) {
      ci++;
      el.innerHTML = cur.slice(0, ci) + '<span class="cursor">_</span>';
      if (ci === cur.length) { deleting = true; setTimeout(type, 1500); return; }
    } else {
      ci--;
      el.innerHTML = cur.slice(0, ci) + '<span class="cursor">_</span>';
      if (ci === 0) { deleting = false; li = (li + 1) % lines.length; }
    }
    setTimeout(type, deleting ? 40 : 80);
  }
  type();

  let v = 0;
  const vc = document.getElementById('vc');
  const iv = setInterval(() => { v++; vc.textContent = v; if(v>=42) clearInterval(iv); }, 50);
</script>
