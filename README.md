<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <title>Dhruvitkumar Parmar | Portfolio</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <!-- Google Font -->
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&display=swap" rel="stylesheet" />
  <style>
    :root {
      --bg-gradient: radial-gradient(circle at top, #1f2933, #020617);
      --card-bg: rgba(15, 23, 42, 0.92);
      --accent: #38bdf8;
      --accent-soft: rgba(56, 189, 248, 0.12);
      --accent-2: #a855f7;
      --text-main: #e5e7eb;
      --text-soft: #9ca3af;
      --border-soft: rgba(148, 163, 184, 0.35);
      --chip-bg: rgba(15, 23, 42, 0.8);
      --shadow-soft: 0 18px 45px rgba(0, 0, 0, 0.45);
      --radius-xl: 24px;
      --radius-lg: 16px;
      --radius-pill: 999px;
      --transition-fast: 0.2s ease-out;
    }

    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
    }

    body {
      font-family: "Poppins", system-ui, -apple-system, BlinkMacSystemFont, sans-serif;
      background: var(--bg-gradient);
      color: var(--text-main);
      min-height: 100vh;
      display: flex;
      justify-content: center;
      align-items: flex-start;
      padding: 32px 16px;
    }

    .page {
      width: 100%;
      max-width: 1120px;
      margin: 0 auto;
    }

    .glass-card {
      background: var(--card-bg);
      border-radius: var(--radius-xl);
      box-shadow: var(--shadow-soft);
      border: 1px solid var(--border-soft);
      backdrop-filter: blur(16px);
      padding: 28px 24px 32px;
    }

    @media (min-width: 900px) {
      .glass-card {
        padding: 32px 32px 36px;
      }
    }

    /* Hero */
    .hero {
      display: grid;
      grid-template-columns: minmax(0, 3fr) minmax(0, 2.2fr);
      gap: 28px;
      align-items: center;
      margin-bottom: 28px;
    }

    @media (max-width: 800px) {
      .hero {
        grid-template-columns: minmax(0, 1fr);
      }
    }

    .badge-row {
      display: flex;
      flex-wrap: wrap;
      gap: 10px;
      margin-bottom: 10px;
      align-items: center;
    }

    .pill {
      display: inline-flex;
      align-items: center;
      gap: 8px;
      background: var(--accent-soft);
      border-radius: var(--radius-pill);
      padding: 4px 12px;
      font-size: 11px;
      letter-spacing: 0.06em;
      text-transform: uppercase;
      color: var(--accent);
      border: 1px solid rgba(56, 189, 248, 0.4);
    }

    .pill span {
      font-size: 14px;
    }

    .hero-title {
      font-size: 26px;
      font-weight: 600;
      line-height: 1.3;
      margin-bottom: 6px;
    }

    .hero-title span {
      background: linear-gradient(90deg, #38bdf8, #a855f7);
      -webkit-background-clip: text;
      color: transparent;
    }

    .hero-subtitle {
      font-size: 14px;
      color: var(--text-soft);
      margin-bottom: 14px;
    }

    .hero-subtitle span.flag {
      font-size: 18px;
      margin-left: 4px;
    }

    .meta {
      display: flex;
      flex-wrap: wrap;
      gap: 8px 16px;
      font-size: 12px;
      color: var(--text-soft);
      margin-bottom: 14px;
    }

    .meta strong {
      color: var(--text-main);
      font-weight: 500;
    }

    .hero-actions {
      display: flex;
      flex-wrap: wrap;
      gap: 10px;
      margin-bottom: 10px;
    }

    .btn {
      display: inline-flex;
      align-items: center;
      justify-content: center;
      gap: 6px;
      border-radius: var(--radius-pill);
      padding: 8px 16px;
      font-size: 13px;
      font-weight: 500;
      border: 1px solid transparent;
      cursor: pointer;
      text-decoration: none;
      transition: transform var(--transition-fast), box-shadow var(--transition-fast),
        background var(--transition-fast), border var(--transition-fast);
      white-space: nowrap;
    }

    .btn-primary {
      background: linear-gradient(135deg, #38bdf8, #0ea5e9);
      color: #0b1220;
      box-shadow: 0 10px 25px rgba(56, 189, 248, 0.35);
    }

    .btn-primary:hover {
      transform: translateY(-1px);
      box-shadow: 0 14px 30px rgba(56, 189, 248, 0.45);
    }

    .btn-ghost {
      background: rgba(15, 23, 42, 0.7);
      color: var(--text-main);
      border-color: rgba(148, 163, 184, 0.6);
    }

    .btn-ghost:hover {
      background: rgba(15, 23, 42, 0.95);
      transform: translateY(-1px);
    }

    .hero-mini {
      font-size: 12px;
      color: var(--text-soft);
      margin-top: 4px;
    }

    .hero-right {
      display: flex;
      justify-content: center;
      align-items: center;
    }

    .hero-card {
      position: relative;
      overflow: hidden;
      border-radius: 22px;
      padding: 18px;
      background: radial-gradient(circle at top left, rgba(56, 189, 248, 0.16), transparent),
                  radial-gradient(circle at bottom right, rgba(168, 85, 247, 0.18), transparent),
                  #020617;
      border: 1px solid rgba(148, 163, 184, 0.35);
    }

    .hero-card-inner {
      background: rgba(15, 23, 42, 0.9);
      border-radius: 16px;
      padding: 14px 14px 16px;
      display: flex;
      flex-direction: column;
      align-items: center;
      gap: 10px;
    }

    .hero-avatar {
      width: 120px;
      height: 120px;
      border-radius: 26px;
      overflow: hidden;
      border: 1px solid rgba(148, 163, 184, 0.7);
      box-shadow: 0 12px 30px rgba(0, 0, 0, 0.7);
    }

    .hero-avatar img {
      width: 100%;
      height: 100%;
      object-fit: cover;
    }

    .hero-name {
      font-size: 16px;
      font-weight: 600;
    }

    .hero-tag {
      font-size: 11px;
      color: var(--text-soft);
      text-transform: uppercase;
      letter-spacing: 0.1em;
    }

    .hero-username {
      font-size: 12px;
      color: var(--accent);
      background: rgba(56, 189, 248, 0.1);
      padding: 4px 10px;
      border-radius: var(--radius-pill);
      border: 1px solid rgba(56, 189, 248, 0.4);
    }

    .hero-stats {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      gap: 10px;
      margin-top: 8px;
    }

    .tiny-stat {
      font-size: 11px;
      padding: 6px 10px;
      background: rgba(15, 23, 42, 0.95);
      border-radius: 999px;
      border: 1px solid rgba(55, 65, 81, 0.9);
      color: var(--text-soft);
    }

    .tiny-stat span {
      color: var(--accent);
      font-weight: 500;
    }

    /* Sections */
    .sections-grid {
      display: grid;
      grid-template-columns: minmax(0, 2.4fr) minmax(0, 2.1fr);
      gap: 24px;
      margin-top: 10px;
    }

    @media (max-width: 900px) {
      .sections-grid {
        grid-template-columns: minmax(0, 1fr);
      }
    }

    .section-card {
      background: rgba(15, 23, 42, 0.85);
      border-radius: var(--radius-lg);
      border: 1px solid rgba(51, 65, 85, 0.9);
      padding: 16px 16px 18px;
    }

    .section-heading {
      font-size: 14px;
      font-weight: 600;
      margin-bottom: 10px;
      display: flex;
      align-items: center;
      gap: 8px;
    }

    .section-heading span.accent-dot {
      display: inline-block;
      width: 7px;
      height: 7px;
      border-radius: 999px;
      background: linear-gradient(135deg, #38bdf8, #a855f7);
    }

    .section-list {
      list-style: none;
      display: grid;
      gap: 8px;
      font-size: 13px;
      color: var(--text-soft);
    }

    .section-list strong {
      color: var(--text-main);
      font-weight: 500;
    }

    .section-list a {
      color: var(--accent);
      text-decoration: none;
      font-weight: 500;
    }

    .section-list a:hover {
      text-decoration: underline;
    }

    .inline-label {
      font-size: 12px;
      text-transform: uppercase;
      letter-spacing: 0.08em;
      color: var(--text-soft);
      margin-bottom: 4px;
    }

    .mono {
      font-family: "JetBrains Mono", ui-monospace, SFMono-Regular, Menlo, Monaco, Consolas,
        "Liberation Mono", "Courier New", monospace;
      font-size: 12px;
      color: var(--text-soft);
      background: rgba(15, 23, 42, 0.9);
      border-radius: 12px;
      padding: 7px 10px;
      border: 1px dashed rgba(55, 65, 81, 0.8);
      word-break: break-all;
    }

    /* Social */
    .social-row {
      display: flex;
      flex-wrap: wrap;
      gap: 8px;
      margin-top: 6px;
    }

    .social-pill {
      display: inline-flex;
      align-items: center;
      gap: 6px;
      padding: 6px 11px;
      border-radius: 999px;
      font-size: 12px;
      background: var(--chip-bg);
      border: 1px solid rgba(55, 65, 81, 0.9);
      color: var(--text-soft);
      text-decoration: none;
      transition: background var(--transition-fast), transform var(--transition-fast),
        border var(--transition-fast);
    }

    .social-pill:hover {
      background: rgba(15, 23, 42, 1);
      transform: translateY(-1px);
      border-color: rgba(148, 163, 184, 0.9);
    }

    .social-pill span.handle {
      color: var(--text-main);
    }

    /* Skills chips */
    .chips-grid {
      display: flex;
      flex-wrap: wrap;
      gap: 6px;
      margin-top: 5px;
    }

    .chip {
      font-size: 11px;
      padding: 5px 9px;
      border-radius: 999px;
      background: var(--chip-bg);
      border: 1px solid rgba(51, 65, 85, 0.9);
      color: var(--text-soft);
      white-space: nowrap;
    }

    /* Icon grid */
    .icon-grid {
      display: flex;
      flex-wrap: wrap;
      gap: 12px;
      margin-top: 10px;
    }

    .icon-grid a {
      display: flex;
      align-items: center;
      justify-content: center;
      width: 38px;
      height: 38px;
      border-radius: 12px;
      background: rgba(15, 23, 42, 1);
      border: 1px solid rgba(51, 65, 85, 0.9);
      transition: transform var(--transition-fast), box-shadow var(--transition-fast),
        border var(--transition-fast), background var(--transition-fast);
    }

    .icon-grid a:hover {
      transform: translateY(-2px) scale(1.03);
      background: rgba(15, 23, 42, 0.96);
      border-color: rgba(148, 163, 184, 0.95);
      box-shadow: 0 12px 25px rgba(15, 23, 42, 0.9);
    }

    .icon-grid img {
      max-width: 26px;
      max-height: 26px;
    }

    /* Stats / trophies row */
    .wide-row {
      margin-top: 22px;
      display: grid;
      grid-template-columns: minmax(0, 1.2fr) minmax(0, 1fr);
      gap: 18px;
    }

    @media (max-width: 900px) {
      .wide-row {
        grid-template-columns: minmax(0, 1fr);
      }
    }

    .wide-row img {
      width: 100%;
      border-radius: 16px;
      border: 1px solid rgba(55, 65, 81, 0.9);
      background: #020617;
    }

    .badge-img {
      margin-top: 8px;
      display: inline-block;
    }

    /* Support */
    .support-row {
      display: flex;
      flex-wrap: wrap;
      gap: 12px;
      align-items: center;
      margin-top: 6px;
    }

    .support-row img {
      border-radius: 999px;
      box-shadow: 0 12px 26px rgba(250, 204, 21, 0.4);
    }

    footer {
      margin-top: 14px;
      font-size: 11px;
      color: var(--text-soft);
      text-align: right;
    }
  </style>
</head>
<body>
  <div class="page">
    <div class="glass-card">
      <!-- HERO -->
      <section class="hero">
        <div class="hero-left">
          <div class="badge-row">
            <div class="pill">
              <span>👨‍💻</span>
              <span>Frontend • Cybersecurity</span>
            </div>
            <span class="hero-mini">GitHub: <strong>@dhruvit2312parmar</strong></span>
          </div>

          <h1 class="hero-title">
            Hi 👋, I'm <span>Dhruvitkumar Parmar</span>
          </h1>
          <p class="hero-subtitle">
            A passionate Frontend Developer &amp; Cybersecurity Learner from India
            <span class="flag">🇮🇳</span>
          </p>

          <div class="meta">
            <span><strong>Email:</strong> dhruvitpc@gmail.com</span>
            <span><strong>Phone:</strong> +91 9016710369</span>
            <span><strong>Role:</strong> B.Sc CS • MCA Student • Cybersecurity Trainee</span>
          </div>

          <div class="hero-actions">
            <a href="https://github.com/dhruvit2312parmar" class="btn btn-primary" target="_blank" rel="noreferrer">
              🔗 View GitHub
            </a>
            <a href="https://twitter.com/_dhruvitparmar" class="btn btn-ghost" target="_blank" rel="noreferrer">
              🐦 @_dhruvitparmar
            </a>
          </div>

          <p class="hero-mini">
            ⚡ Fun fact: I think I am funny &amp; I work with <strong>100% focus</strong>!
          </p>
        </div>

        <div class="hero-right">
          <div class="hero-card">
            <div class="hero-card-inner">
              <div class="hero-avatar">
                <!-- You can replace this GIF with your own photo -->
                <img
                  src="https://raw.githubusercontent.com/devSouvik/devSouvik/master/gif3.gif"
                  alt="coding animation"
                />
              </div>
              <p class="hero-tag">Full Stack • Cybersecurity • Learner</p>
              <p class="hero-name">Dhruvitkumar Parmar</p>
              <span class="hero-username">@dhruvit2312parmar</span>
              <div class="hero-stats">
                <div class="tiny-stat">🎯 Focus: <span>Frontend &amp; MERN</span></div>
                <div class="tiny-stat">🛡 Cybersecurity: <span>DFIR &amp; Pentest</span></div>
              </div>
            </div>
          </div>
        </div>
      </section>

      <!-- MAIN SECTIONS -->
      <section class="sections-grid">
        <!-- LEFT COLUMN -->
        <div class="section-card">
          <h2 class="section-heading">
            <span class="accent-dot"></span>
            Overview
          </h2>
          <ul class="section-list">
            <li>
              <strong>🔭 Currently working on:</strong><br />
              <a href="#" title="Project Link Coming Soon">
                Cybersecurity Vulnerability Scanner Portal (MERN)
              </a>
            </li>
            <li>
              <strong>🌱 Currently learning:</strong><br />
              MERN Stack • Cybersecurity (Digital Forensics &amp; Penetration Testing) • React.js &amp; Node.js
            </li>
            <li>
              <strong>👯 Looking to collaborate on:</strong><br />
              <a href="#" title="Open for collaboration">
                Web Development &amp; Cybersecurity Projects
              </a>
            </li>
            <li>
              <strong>🤝 Looking for help with:</strong><br />
              <a href="#" title="Learning phase">
                Advanced Penetration Testing &amp; Bug Hunting
              </a>
            </li>
            <li>
              <strong>👨‍💻 Projects:</strong><br />
              <span>🌐 Portfolio Coming Soon</span>
            </li>
            <li>
              <strong>📝 Articles / Blog:</strong><br />
              <span>✍️ Blog Coming Soon</span>
            </li>
            <li>
              <strong>💬 Ask me about:</strong><br />
              HTML • CSS • JavaScript • PHP • Bootstrap • React • Cybersecurity Basics
            </li>
          </ul>
        </div>

        <!-- RIGHT COLUMN -->
        <div class="section-card">
          <h2 class="section-heading">
            <span class="accent-dot"></span>
            Social &amp; Handles
          </h2>
          <p class="inline-label">Main handles</p>
          <div class="social-row">
            <a
              class="social-pill"
              href="https://github.com/dhruvit2312parmar"
              target="_blank"
              rel="noreferrer"
            >
              <span>🐱 GitHub</span> <span class="handle">@dhruvit2312parmar</span>
            </a>
            <a
              class="social-pill"
              href="https://twitter.com/_dhruvitparmar"
              target="_blank"
              rel="noreferrer"
            >
              <span>🐦 Twitter</span> <span class="handle">@_dhruvitparmar</span>
            </a>
            <a
              class="social-pill"
              href="https://linkedin.com/in/dhruvit23parmar"
              target="_blank"
              rel="noreferrer"
            >
              <span>🔗 LinkedIn</span> <span class="handle">/in/dhruvit23parmar</span>
            </a>
            <a
              class="social-pill"
              href="https://kaggle.com/dhruvitkumarparmar"
              target="_blank"
              rel="noreferrer"
            >
              <span>📊 Kaggle</span> <span class="handle">/dhruvitkumarparmar</span>
            </a>
            <a
              class="social-pill"
              href="https://fb.com/dhruvit parmar`"
              target="_blank"
              rel="noreferrer"
            >
              <span>📘 Facebook</span> <span class="handle">dhruvit parmar</span>
            </a>
            <a
              class="social-pill"
              href="https://instagram.com/_dhruvitpar"
              target="_blank"
              rel="noreferrer"
            >
              <span>📸 Instagram</span> <span class="handle">@_dhruvitpar</span>
            </a>
            <a
              class="social-pill"
              href="https://www.youtube.com/c/dxtutorials"
              target="_blank"
              rel="noreferrer"
            >
              <span>▶️ YouTube</span> <span class="handle">DX Tutorials</span>
            </a>
            <a
              class="social-pill"
              href="https://www.leetcode.com/dhruvitparmar"
              target="_blank"
              rel="noreferrer"
            >
              <span>🏆 LeetCode</span> <span class="handle">@dhruvitparmar</span>
            </a>
          </div>

          <p class="inline-label" style="margin-top: 10px;">Extra usernames (for reference)</p>
          <div class="mono">
            _dhruvitparmar • dhruvit23parmar • dhruvitkumarparmar • dhruvit parmar •
            _dhruvitpar • dxtutorials • dhruvitparmar
          </div>
        </div>
      </section>

      <!-- STATS + TROPHY + TWITTER BADGE -->
      <section class="wide-row">
        <div class="section-card">
          <h2 class="section-heading">
            <span class="accent-dot"></span>
            GitHub Stats &amp; Achievements
          </h2>
          <span class="inline-label">Profile views</span>
          <span class="badge-img">
            <img
              src="https://komarev.com/ghpvc/?username=dhruvit2312parmar&label=Profile%20views&color=0e75b6&style=flat"
              alt="Profile views"
            />
          </span>

          <div style="margin-top: 14px; display: grid; gap: 10px;">
            <img
              src="https://github-readme-stats.vercel.app/api?username=dhruvit2312parmar&show_icons=true&theme=radical"
              alt="GitHub Stats"
            />
            <img
              src="https://github-readme-stats.vercel.app/api/top-langs/?username=dhruvit2312parmar&layout=compact&theme=radical"
              alt="Top Languages"
            />
            <img
              src="https://github-readme-streak-stats.herokuapp.com/?user=dhruvit2312parmar&theme=radical"
              alt="GitHub Streak"
            />
          </div>
        </div>

        <div class="section-card">
          <h2 class="section-heading">
            <span class="accent-dot"></span>
            Trophies &amp; Twitter
          </h2>
          <img
            src="https://github-profile-trophy.vercel.app/?username=dhruvit2312parmar"
            alt="GitHub Trophies"
          />

          <div style="margin-top: 12px;">
            <span class="inline-label">Twitter badge</span><br />
            <img
              class="badge-img"
              src="https://img.shields.io/twitter/follow/_dhruvitparmar?logo=twitter&style=for-the-badge"
              alt="Twitter Follow Badge"
            />
          </div>
        </div>
      </section>

      <!-- LANGUAGES & TOOLS -->
      <section class="section-card" style="margin-top: 22px;">
        <h2 class="section-heading">
          <span class="accent-dot"></span>
          Languages &amp; Tools
        </h2>
        <p class="inline-label">Quick list (text)</p>
        <div class="chips-grid">
          <span class="chip">Android</span>
          <span class="chip">Arduino</span>
          <span class="chip">AWS</span>
          <span class="chip">Azure</span>
          <span class="chip">Bash</span>
          <span class="chip">Blender</span>
          <span class="chip">Bootstrap</span>
          <span class="chip">C</span>
          <span class="chip">C++</span>
          <span class="chip">Dart</span>
          <span class="chip">Django</span>
          <span class="chip">Docker</span>
          <span class="chip">.NET</span>
          <span class="chip">Express</span>
          <span class="chip">Firebase</span>
          <span class="chip">Flask</span>
          <span class="chip">Flutter</span>
          <span class="chip">GCP</span>
          <span class="chip">Git</span>
          <span class="chip">HTML5</span>
          <span class="chip">Java</span>
          <span class="chip">JavaScript</span>
          <span class="chip">Kubernetes</span>
          <span class="chip">Laravel</span>
          <span class="chip">Linux</span>
          <span class="chip">MongoDB</span>
          <span class="chip">MSSQL</span>
          <span class="chip">MySQL</span>
          <span class="chip">Node.js</span>
          <span class="chip">OpenCV</span>
          <span class="chip">Oracle</span>
          <span class="chip">Pandas</span>
          <span class="chip">Photoshop</span>
          <span class="chip">PHP</span>
          <span class="chip">PostgreSQL</span>
          <span class="chip">Python</span>
          <span class="chip">React</span>
          <span class="chip">Redux</span>
          <span class="chip">SQLite</span>
          <span class="chip">Tailwind</span>
          <span class="chip">TensorFlow</span>
          <span class="chip">Unity</span>
          <span class="chip">Unreal</span>
          <!-- Add or remove chips as you like -->
        </div>

        <p class="inline-label" style="margin-top: 12px;">Icon view</p>
        <div class="icon-grid">
          <!-- Same icons you used in README -->
          <a href="https://developer.android.com" target="_blank" rel="noreferrer">
            <img
              src="https://raw.githubusercontent.com/devicons/devicon/master/icons/android/android-original-wordmark.svg"
              alt="android"
            />
          </a>
          <a href="https://www.arduino.cc/" target="_blank" rel="noreferrer">
            <img src="https://cdn.worldvectorlogo.com/logos/arduino-1.svg" alt="arduino" />
          </a>
          <a href="https://aws.amazon.com" target="_blank" rel="noreferrer">
            <img
              src="https://raw.githubusercontent.com/devicons/devicon/master/icons/amazonwebservices/amazonwebservices-original-wordmark.svg"
              alt="aws"
            />
          </a>
          <a href="https://azure.microsoft.com/en-in/" target="_blank" rel="noreferrer">
            <img src="https://www.vectorlogo.zone/logos/microsoft_azure/microsoft_azure-icon.svg" alt="azure" />
          </a>
          <a href="https://www.gnu.org/software/bash/" target="_blank" rel="noreferrer">
            <img src="https://www.vectorlogo.zone/logos/gnu_bash/gnu_bash-icon.svg" alt="bash" />
          </a>
          <a href="https://www.blender.org/" target="_blank" rel="noreferrer">
            <img
              src="https://download.blender.org/branding/community/blender_community_badge_white.svg"
              alt="blender"
            />
          </a>
          <a href="https://getbootstrap.com" target="_blank" rel="noreferrer">
            <img
              src="https://raw.githubusercontent.com/devicons/devicon/master/icons/bootstrap/bootstrap-plain-wordmark.svg"
              alt="bootstrap"
            />
          </a>
          <a href="https://www.cprogramming.com/" target="_blank" rel="noreferrer">
            <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/c/c-original.svg" alt="c" />
          </a>
          <a href="https://www.chartjs.org" target="_blank" rel="noreferrer">
            <img src="https://www.chartjs.org/media/logo-title.svg" alt="chartjs" />
          </a>
          <a href="https://www.w3schools.com/cpp/" target="_blank" rel="noreferrer">
            <img
              src="https://raw.githubusercontent.com/devicons/devicon/master/icons/cplusplus/cplusplus-original.svg"
              alt="cplusplus"
            />
          </a>
          <a href="https://www.w3schools.com/css/" target="_blank" rel="noreferrer">
            <img
              src="https://raw.githubusercontent.com/devicons/devicon/master/icons/css3/css3-original-wordmark.svg"
              alt="css3"
            />
          </a>
          <a href="https://dart.dev" target="_blank" rel="noreferrer">
            <img src="https://www.vectorlogo.zone/logos/dartlang/dartlang-icon.svg" alt="dart" />
          </a>
          <a href="https://www.djangoproject.com/" target="_blank" rel="noreferrer">
            <img src="https://cdn.worldvectorlogo.com/logos/django.svg" alt="django" />
          </a>
          <a href="https://www.docker.com/" target="_blank" rel="noreferrer">
            <img
              src="https://raw.githubusercontent.com/devicons/devicon/master/icons/docker/docker-original-wordmark.svg"
              alt="docker"
            />
          </a>
          <a href="https://dotnet.microsoft.com/" target="_blank" rel="noreferrer">
            <img
              src="https://raw.githubusercontent.com/devicons/devicon/master/icons/dot-net/dot-net-original-wordmark.svg"
              alt="dotnet"
            />
          </a>
          <a href="https://expressjs.com" target="_blank" rel="noreferrer">
            <img
              src="https://raw.githubusercontent.com/devicons/devicon/master/icons/express/express-original-wordmark.svg"
              alt="express"
            />
          </a>
          <a href="https://firebase.google.com/" target="_blank" rel="noreferrer">
            <img src="https://www.vectorlogo.zone/logos/firebase/firebase-icon.svg" alt="firebase" />
          </a>
          <a href="https://flask.palletsprojects.com/" target="_blank" rel="noreferrer">
            <img src="https://www.vectorlogo.zone/logos/pocoo_flask/pocoo_flask-icon.svg" alt="flask" />
          </a>
          <a href="https://flutter.dev" target="_blank" rel="noreferrer">
            <img src="https://www.vectorlogo.zone/logos/flutterio/flutterio-icon.svg" alt="flutter" />
          </a>
          <a href="https://cloud.google.com" target="_blank" rel="noreferrer">
            <img src="https://www.vectorlogo.zone/logos/google_cloud/google_cloud-icon.svg" alt="gcp" />
          </a>
          <a href="https://git-scm.com/" target="_blank" rel="noreferrer">
            <img src="https://www.vectorlogo.zone/logos/git-scm/git-scm-icon.svg" alt="git" />
          </a>
          <a href="https://www.w3.org/html/" target="_blank" rel="noreferrer">
            <img
              src="https://raw.githubusercontent.com/devicons/devicon/master/icons/html5/html5-original-wordmark.svg"
              alt="html5"
            />
          </a>
          <a href="https://www.java.com" target="_blank" rel="noreferrer">
            <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/java/java-original.svg" alt="java" />
          </a>
          <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript" target="_blank" rel="noreferrer">
            <img
              src="https://raw.githubusercontent.com/devicons/devicon/master/icons/javascript/javascript-original.svg"
              alt="javascript"
            />
          </a>
          <a href="https://kubernetes.io" target="_blank" rel="noreferrer">
            <img src="https://www.vectorlogo.zone/logos/kubernetes/kubernetes-icon.svg" alt="kubernetes" />
          </a>
          <a href="https://laravel.com/" target="_blank" rel="noreferrer">
            <img
              src="https://raw.githubusercontent.com/devicons/devicon/master/icons/laravel/laravel-plain-wordmark.svg"
              alt="laravel"
            />
          </a>
          <a href="https://www.linux.org/" target="_blank" rel="noreferrer">
            <img
              src="https://raw.githubusercontent.com/devicons/devicon/master/icons/linux/linux-original.svg"
              alt="linux"
            />
          </a>
          <a href="https://www.mongodb.com/" target="_blank" rel="noreferrer">
            <img
              src="https://raw.githubusercontent.com/devicons/devicon/master/icons/mongodb/mongodb-original-wordmark.svg"
              alt="mongodb"
            />
          </a>
          <a href="https://www.microsoft.com/en-us/sql-server" target="_blank" rel="noreferrer">
            <img src="https://www.svgrepo.com/show/303229/microsoft-sql-server-logo.svg" alt="mssql" />
          </a>
          <a href="https://www.mysql.com/" target="_blank" rel="noreferrer">
            <img
              src="https://raw.githubusercontent.com/devicons/devicon/master/icons/mysql/mysql-original-wordmark.svg"
              alt="mysql"
            />
          </a>
          <a href="https://nodejs.org" target="_blank" rel="noreferrer">
            <img
              src="https://raw.githubusercontent.com/devicons/devicon/master/icons/nodejs/nodejs-original-wordmark.svg"
              alt="nodejs"
            />
          </a>
          <a href="https://opencv.org/" target="_blank" rel="noreferrer">
            <img src="https://www.vectorlogo.zone/logos/opencv/opencv-icon.svg" alt="opencv" />
          </a>
          <a href="https://www.oracle.com/" target="_blank" rel="noreferrer">
            <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/oracle/oracle-original.svg" alt="oracle" />
          </a>
          <a href="https://pandas.pydata.org/" target="_blank" rel="noreferrer">
            <img
              src="https://raw.githubusercontent.com/devicons/devicon/2ae2a900d2f041da66e950e4d48052658d850630/icons/pandas/pandas-original.svg"
              alt="pandas"
            />
          </a>
          <a href="https://www.photoshop.com/en" target="_blank" rel="noreferrer">
            <img
              src="https://raw.githubusercontent.com/devicons/devicon/master/icons/photoshop/photoshop-line.svg"
              alt="photoshop"
            />
          </a>
          <a href="https://www.php.net" target="_blank" rel="noreferrer">
            <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/php/php-original.svg" alt="php" />
          </a>
          <a href="https://www.postgresql.org" target="_blank" rel="noreferrer">
            <img
              src="https://raw.githubusercontent.com/devicons/devicon/master/icons/postgresql/postgresql-original-wordmark.svg"
              alt="postgresql"
            />
          </a>
          <a href="https://www.python.org" target="_blank" rel="noreferrer">
            <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/python/python-original.svg" alt="python" />
          </a>
          <a href="https://reactjs.org/" target="_blank" rel="noreferrer">
            <img
              src="https://raw.githubusercontent.com/devicons/devicon/master/icons/react/react-original-wordmark.svg"
              alt="react"
            />
          </a>
          <a href="https://redux.js.org" target="_blank" rel="noreferrer">
            <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/redux/redux-original.svg" alt="redux" />
          </a>
          <a href="https://www.sqlite.org/" target="_blank" rel="noreferrer">
            <img src="https://www.vectorlogo.zone/logos/sqlite/sqlite-icon.svg" alt="sqlite" />
          </a>
          <a href="https://tailwindcss.com/" target="_blank" rel="noreferrer">
            <img src="https://www.vectorlogo.zone/logos/tailwindcss/tailwindcss-icon.svg" alt="tailwind" />
          </a>
          <a href="https://www.tensorflow.org" target="_blank" rel="noreferrer">
            <img src="https://www.vectorlogo.zone/logos/tensorflow/tensorflow-icon.svg" alt="tensorflow" />
          </a>
          <a href="https://unity.com/" target="_blank" rel="noreferrer">
            <img src="https://www.vectorlogo.zone/logos/unity3d/unity3d-icon.svg" alt="unity" />
          </a>
          <a href="https://unrealengine.com/" target="_blank" rel="noreferrer">
            <img
              src="https://raw.githubusercontent.com/kenangundogan/fontisto/036b7eca71aab1bef8e6a0518f7329f13ed62f6b/icons/svg/brand/unreal-engine.svg"
              alt="unreal"
            />
          </a>
        </div>
      </section>

      <!-- SUPPORT -->
      <section class="section-card" style="margin-top: 22px;">
        <h2 class="section-heading">
          <span class="accent-dot"></span>
          Support
        </h2>
        <p style="font-size: 13px; color: var(--text-soft); margin-bottom: 6px;">
          If you like my work, you can support me here:
        </p>
        <div class="support-row">
          <a href="https://www.buymeacoffee.com/dhruvitparmar" target="_blank" rel="noreferrer">
            <img
              src="https://cdn.buymeacoffee.com/buttons/v2/default-yellow.png"
              height="46"
              width="190"
              alt="Buy Me a Coffee - dhruvitparmar"
            />
          </a>
        </div>
      </section>

      <footer>
        Built with ❤️ by Dhruvitkumar Parmar • Frontend &amp; Cybersecurity Learner
      </footer>
    </div>
  </div>
</body>
</html>
