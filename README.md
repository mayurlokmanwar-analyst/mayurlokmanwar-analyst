<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8"/>
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
<title>Mayuresh Lokmanwar — Data Analyst</title>
<link rel="preconnect" href="https://fonts.googleapis.com"/>
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin/>
<link href="https://fonts.googleapis.com/css2?family=Space+Mono:wght@400;700&family=DM+Sans:ital,opsz,wght@0,9..40,300;0,9..40,400;0,9..40,500;0,9..40,600;1,9..40,400&display=swap" rel="stylesheet"/>
<style>
  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

  :root {
    --ink: #0d0d0d;
    --ink2: #3a3a3a;
    --ink3: #888;
    --surface: #ffffff;
    --surface2: #f5f4f0;
    --surface3: #eceae3;
    --accent: #1a6bff;
    --accent2: #00c896;
    --accent3: #ff5a2c;
    --border: 1px solid #e0ddd6;
    --radius: 14px;
  }

  html { font-size: 16px; }

  body {
    background: #f0ede6;
    font-family: 'DM Sans', sans-serif;
    color: var(--ink);
    min-height: 100vh;
    padding: 2rem 1rem 4rem;
  }

  .wrap {
    max-width: 820px;
    margin: 0 auto;
  }

  /* ── HERO ── */
  .hero {
    position: relative;
    background: var(--ink);
    border-radius: 20px;
    padding: 2.5rem 2rem 2.2rem;
    margin-bottom: 1.5rem;
    overflow: hidden;
  }
  .hero-grid {
    position: absolute;
    inset: 0;
    background-image:
      linear-gradient(rgba(255,255,255,.04) 1px, transparent 1px),
      linear-gradient(90deg, rgba(255,255,255,.04) 1px, transparent 1px);
    background-size: 32px 32px;
    pointer-events: none;
  }
  .hero-glow1 {
    position: absolute;
    width: 260px; height: 260px;
    border-radius: 50%;
    background: var(--accent);
    opacity: .12;
    top: -80px; right: -60px;
    filter: blur(50px);
    pointer-events: none;
  }
  .hero-glow2 {
    position: absolute;
    width: 200px; height: 200px;
    border-radius: 50%;
    background: var(--accent2);
    opacity: .1;
    bottom: -60px; left: 20px;
    filter: blur(40px);
    pointer-events: none;
  }
  .hero-inner { position: relative; z-index: 1; }

  .status-pill {
    display: inline-flex;
    align-items: center;
    gap: 7px;
    background: rgba(255,255,255,.07);
    border: 1px solid rgba(255,255,255,.12);
    border-radius: 100px;
    padding: 5px 14px;
    font-size: 12px;
    color: rgba(255,255,255,.55);
    font-family: 'Space Mono', monospace;
    margin-bottom: 1.1rem;
    letter-spacing: .03em;
  }
  .status-dot {
    width: 7px; height: 7px;
    border-radius: 50%;
    background: var(--accent2);
    animation: pulse 1.8s ease-in-out infinite;
  }
  @keyframes pulse { 0%,100%{opacity:1} 50%{opacity:.25} }

  .hero-name {
    font-size: clamp(30px, 5.5vw, 48px);
    font-weight: 600;
    color: #fff;
    letter-spacing: -.025em;
    line-height: 1.08;
    margin-bottom: .5rem;
  }
  .hero-name span { color: var(--accent2); }

  .hero-tagline {
    font-size: 12.5px;
    color: rgba(255,255,255,.38);
    font-family: 'Space Mono', monospace;
    margin-bottom: 1.8rem;
    line-height: 1.5;
  }

  .hero-socials { display: flex; flex-wrap: wrap; gap: 8px; }
  .s-btn {
    display: inline-flex;
    align-items: center;
    gap: 6px;
    padding: 7px 15px;
    border-radius: 100px;
    font-size: 12.5px;
    font-weight: 500;
    text-decoration: none;
    transition: background .15s, transform .15s;
    border: 1px solid rgba(255,255,255,.12);
    color: rgba(255,255,255,.72);
    background: rgba(255,255,255,.06);
    font-family: 'DM Sans', sans-serif;
  }
  .s-btn:hover { background: rgba(255,255,255,.13); transform: translateY(-1px); }
  .s-btn svg { width: 13px; height: 13px; flex-shrink: 0; }

  /* ── SECTION LABEL ── */
  .section-label {
    font-size: 10.5px;
    font-weight: 600;
    letter-spacing: .12em;
    text-transform: uppercase;
    color: var(--ink3);
    font-family: 'Space Mono', monospace;
    margin-bottom: 1rem;
  }

  /* ── ABOUT CARDS ── */
  .about-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 10px;
    margin-bottom: 1.5rem;
  }
  .about-card {
    background: var(--surface);
    border: var(--border);
    border-radius: var(--radius);
    padding: 1.1rem 1.2rem;
    transition: border-color .2s, transform .15s;
  }
  .about-card:hover { border-color: #b5b0a8; transform: translateY(-2px); }
  .about-card-icon { font-size: 20px; margin-bottom: .55rem; }
  .about-card-text { font-size: 13.5px; color: var(--ink2); line-height: 1.6; }
  .about-card-text strong { color: var(--ink); font-weight: 600; }

  /* ── STACK ── */
  .stack-section { margin-bottom: 1.5rem; }
  .stack-pills { display: flex; flex-wrap: wrap; gap: 8px; margin-top: .75rem; }
  .pill {
    display: inline-flex;
    align-items: center;
    gap: 7px;
    padding: 7px 15px;
    border-radius: 100px;
    font-size: 13px;
    font-weight: 500;
    border: var(--border);
    background: var(--surface);
    color: var(--ink2);
  }
  .pill-dot { width: 8px; height: 8px; border-radius: 50%; flex-shrink: 0; }
  .p-excel .pill-dot { background: #217346; }
  .p-pbi   .pill-dot { background: #d4a800; }
  .p-tab   .pill-dot { background: #E97627; }
  .p-sql   .pill-dot { background: #4479A1; }
  .p-py    .pill-dot { background: #3670A0; }

  /* ── STATS ── */
  .stats-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 10px;
    margin-bottom: 1.5rem;
  }
  .stat-card {
    background: var(--surface);
    border: var(--border);
    border-radius: var(--radius);
    overflow: hidden;
  }
  .stat-card img { width: 100%; display: block; }
  .stat-card-wide {
    grid-column: 1 / -1;
    background: var(--surface);
    border: var(--border);
    border-radius: var(--radius);
    overflow: hidden;
  }
  .stat-card-wide img { width: 100%; display: block; }

  /* ── SO CARD ── */
  .so-card {
    background: var(--surface);
    border: var(--border);
    border-radius: var(--radius);
    padding: 1.1rem 1.2rem;
    margin-bottom: 1.5rem;
  }
  .so-card a img { width: 100%; display: block; border-radius: 8px; margin-top: .75rem; }

  /* ── TROPHIES ── */
  .trophies-card {
    background: var(--surface);
    border: var(--border);
    border-radius: var(--radius);
    padding: 1.1rem 1.2rem;
    margin-bottom: 1.5rem;
  }
  .trophies-card img { width: 100%; display: block; border-radius: 6px; margin-top: .75rem; }

  /* ── CONTRIB ── */
  .contrib-card {
    background: var(--ink);
    border-radius: var(--radius);
    padding: 1.1rem 1.2rem;
    margin-bottom: 1.5rem;
  }
  .contrib-card .section-label { color: rgba(255,255,255,.35); }
  .contrib-card img { width: 100%; display: block; border-radius: 6px; margin-top: .75rem; }

  /* ── FOOTER ── */
  .footer {
    display: flex;
    align-items: center;
    justify-content: space-between;
    flex-wrap: wrap;
    gap: 12px;
    padding-top: 1.2rem;
    border-top: var(--border);
  }
  .footer-note {
    font-size: 11.5px;
    color: var(--ink3);
    font-family: 'Space Mono', monospace;
  }

  /* ── RESPONSIVE ── */
  @media (max-width: 540px) {
    .about-grid { grid-template-columns: 1fr; }
    .stats-grid { grid-template-columns: 1fr; }
    .stat-card-wide { grid-column: 1; }
    .hero { padding: 2rem 1.4rem 1.8rem; }
  }
</style>
</head>
<body>
<div class="wrap">

  <!-- HERO -->
  <div class="hero">
    <div class="hero-grid"></div>
    <div class="hero-glow1"></div>
    <div class="hero-glow2"></div>
    <div class="hero-inner">
      <div class="status-pill">
        <span class="status-dot"></span>
        data analyst &nbsp;·&nbsp; open to opportunities
      </div>
      <h1 class="hero-name">Mayuresh<br><span>Lokmanwar</span></h1>
      <p class="hero-tagline">// I believe everything is a data point —<br>even my morning coffee routine has a trend line.</p>
      <div class="hero-socials">
        <!-- LinkedIn -->
        <a class="s-btn" href="https://linkedin.com/in/mayuresh07" target="_blank" rel="noopener">
          <svg viewBox="0 0 24 24" fill="currentColor"><path d="M20.447 20.452h-3.554v-5.569c0-1.328-.027-3.037-1.852-3.037-1.853 0-2.136 1.445-2.136 2.939v5.667H9.351V9h3.414v1.561h.046c.477-.9 1.637-1.85 3.37-1.85 3.601 0 4.267 2.37 4.267 5.455v6.286zM5.337 7.433a2.062 2.062 0 01-2.063-2.065 2.064 2.064 0 112.063 2.065zm1.782 13.019H3.555V9h3.564v11.452zM22.225 0H1.771C.792 0 0 .774 0 1.729v20.542C0 23.227.792 24 1.771 24h20.451C23.2 24 24 23.227 24 22.271V1.729C24 .774 23.2 0 22.222 0h.003z"/></svg>
          LinkedIn
        </a>
        <!-- Stack Overflow -->
        <a class="s-btn" href="https://stackoverflow.com/users/story/mayuresh-lokmanwar" target="_blank" rel="noopener">
          <svg viewBox="0 0 24 24" fill="currentColor"><path d="M18.986 21.865v-6.404h2.134V24H1.844v-8.539h2.13v6.404h15.012zM6.111 19.731H16.85v-2.137H6.111v2.137zm.259-4.852l10.48 2.189.451-2.07-10.478-2.187-.453 2.068zm1.359-5.056l9.705 4.53.903-1.95-9.706-4.53-.902 1.95zm2.715-4.785l8.217 6.855 1.359-1.62-8.216-6.853-1.36 1.618zM15.751 0l-1.62 1.36 6.851 8.216 1.62-1.359L15.751 0z"/></svg>
          Stack Overflow
        </a>
        <!-- Pinterest -->
        <a class="s-btn" href="https://pinterest.com/mayureshlokamanwar" target="_blank" rel="noopener">
          <svg viewBox="0 0 24 24" fill="currentColor"><path d="M12 0C5.373 0 0 5.373 0 12c0 5.084 3.163 9.426 7.627 11.174-.105-.949-.2-2.405.042-3.441.218-.937 1.407-5.965 1.407-5.965s-.359-.719-.359-1.782c0-1.668.967-2.914 2.171-2.914 1.023 0 1.518.769 1.518 1.69 0 1.029-.655 2.568-.994 3.995-.283 1.194.599 2.169 1.777 2.169 2.133 0 3.772-2.249 3.772-5.495 0-2.873-2.064-4.882-5.012-4.882-3.414 0-5.418 2.561-5.418 5.207 0 1.031.397 2.138.893 2.738a.36.36 0 01.083.345l-.333 1.36c-.053.22-.174.267-.402.161-1.499-.698-2.436-2.889-2.436-4.649 0-3.785 2.75-7.262 7.929-7.262 4.163 0 7.398 2.967 7.398 6.931 0 4.136-2.607 7.464-6.227 7.464-1.216 0-2.359-.632-2.75-1.378l-.748 2.853c-.271 1.043-1.002 2.35-1.492 3.146C9.57 23.812 10.763 24 12 24c6.627 0 12-5.373 12-12S18.627 0 12 0z"/></svg>
          Pinterest
        </a>
        <!-- Reddit -->
        <a class="s-btn" href="https://reddit.com/user/NoParticular2320" target="_blank" rel="noopener">
          <svg viewBox="0 0 24 24" fill="currentColor"><path d="M12 0A12 12 0 0 0 0 12a12 12 0 0 0 12 12 12 12 0 0 0 12-12A12 12 0 0 0 12 0zm5.01 4.744c.688 0 1.25.561 1.25 1.249a1.25 1.25 0 0 1-2.498.056l-2.597-.547-.8 3.747c1.824.07 3.48.632 4.674 1.488.308-.309.73-.491 1.207-.491.968 0 1.754.786 1.754 1.754 0 .716-.435 1.333-1.01 1.614a3.111 3.111 0 0 1 .042.52c0 2.694-3.13 4.87-7.004 4.87-3.874 0-7.004-2.176-7.004-4.87 0-.183.015-.366.043-.534A1.748 1.748 0 0 1 4.028 12c0-.968.786-1.754 1.754-1.754.463 0 .898.196 1.207.49 1.207-.883 2.878-1.43 4.744-1.487l.885-4.182a.342.342 0 0 1 .14-.197.35.35 0 0 1 .238-.042l2.906.617a1.214 1.214 0 0 1 1.108-.701zM9.25 12C8.561 12 8 12.562 8 13.25c0 .687.561 1.248 1.25 1.248.687 0 1.248-.561 1.248-1.249 0-.688-.561-1.249-1.249-1.249zm5.5 0c-.687 0-1.248.561-1.248 1.25 0 .687.561 1.248 1.249 1.248.688 0 1.249-.561 1.249-1.249 0-.687-.562-1.249-1.25-1.249zm-5.466 3.99a.327.327 0 0 0-.231.094.33.33 0 0 0 0 .463c.842.842 2.484.913 2.961.913.477 0 2.105-.056 2.961-.913a.361.361 0 0 0 .029-.463.33.33 0 0 0-.464 0c-.547.533-1.684.73-2.512.73-.828 0-1.979-.196-2.512-.73a.326.326 0 0 0-.232-.095z"/></svg>
          Reddit
        </a>
        <!-- Email -->
        <a class="s-btn" href="mailto:mayurlokmanwar@gmail.com">
          <svg viewBox="0 0 24 24" fill="currentColor"><path d="M24 5.457v13.909c0 .904-.732 1.636-1.636 1.636h-3.819V11.73L12 16.64l-6.545-4.91v9.273H1.636A1.636 1.636 0 0 1 0 19.366V5.457c0-2.023 2.309-3.178 3.927-1.964L5.455 4.64 12 9.548l6.545-4.91 1.528-1.145C21.69 2.28 24 3.434 24 5.457z"/></svg>
          Email
        </a>
      </div>
    </div>
  </div>

  <!-- ABOUT -->
  <p class="section-label">what I'm building</p>
  <div class="about-grid">
    <div class="about-card">
      <div class="about-card-icon">⚡</div>
      <p class="about-card-text"><strong>End-to-end data pipelines</strong> and interactive dashboards using SQL and Power BI.</p>
    </div>
    <div class="about-card">
      <div class="about-card-icon">🐍</div>
      <p class="about-card-text"><strong>Open-source data analysis</strong> projects and automated reporting scripts using Python.</p>
    </div>
    <div class="about-card">
      <div class="about-card-icon">☁️</div>
      <p class="about-card-text"><strong>Advanced statistical modeling</strong> and cloud-based data warehousing in AWS/Snowflake.</p>
    </div>
    <div class="about-card">
      <div class="about-card-icon">📊</div>
      <p class="about-card-text"><strong>Predictive analytics</strong> and advanced data storytelling to drive business decision-making.</p>
    </div>
    <div class="about-card">
      <div class="about-card-icon">🔧</div>
      <p class="about-card-text"><strong>SQL query optimization,</strong> data cleaning with Pandas, and visualization best practices.</p>
    </div>
  </div>

  <!-- TECH STACK -->
  <div class="stack-section">
    <p class="section-label">tech stack</p>
    <div class="stack-pills">
      <span class="pill p-excel"><span class="pill-dot"></span>Microsoft Excel</span>
      <span class="pill p-pbi"><span class="pill-dot"></span>Power BI</span>
      <span class="pill p-tab"><span class="pill-dot"></span>Tableau</span>
      <span class="pill p-sql"><span class="pill-dot"></span>MySQL</span>
      <span class="pill p-py"><span class="pill-dot"></span>Python</span>
    </div>
  </div>

  <!-- GITHUB STATS -->
  <p class="section-label">github stats</p>
  <div class="stats-grid">
    <div class="stat-card">
      <img
        src="https://github-readme-stats.vercel.app/api?username=mayurlokmanwar-analyst&theme=radical&hide_border=true&include_all_commits=true&count_private=true&bg_color=0d0d0d&title_color=00c896&text_color=ffffff&icon_color=1a6bff"
        alt="GitHub Stats"
        loading="lazy"
      />
    </div>
    <div class="stat-card">
      <img
        src="https://nirzak-streak-stats.vercel.app/?user=mayurlokmanwar-analyst&theme=radical&hide_border=true&background=0d0d0d&ring=00c896&fire=ff5a2c&currStreakLabel=00c896"
        alt="GitHub Streak"
        loading="lazy"
      />
    </div>
    <div class="stat-card-wide">
      <img
        src="https://github-readme-stats.vercel.app/api/top-langs/?username=mayurlokmanwar-analyst&theme=radical&hide_border=true&layout=compact&bg_color=0d0d0d&title_color=00c896&text_color=ffffff"
        alt="Top Languages"
        loading="lazy"
      />
    </div>
  </div>

  <!-- STACK OVERFLOW -->
  <div class="so-card">
    <p class="section-label">stack overflow activity</p>
    <a href="https://stackoverflow.com/users/story/mayuresh-lokmanwar" target="_blank" rel="noopener">
      <img
        src="https://stackoverflow-card.vercel.app/?author=mayuresh-lokmanwar&theme=tokyonight"
        alt="Stack Overflow Activity"
        loading="lazy"
      />
    </a>
  </div>

  <!-- TROPHIES -->
  <div class="trophies-card">
    <p class="section-label">github trophies</p>
    <img
      src="https://github-profile-trophy.vercel.app/?username=mayurlokmanwar-analyst&theme=radical&no-frame=true&no-bg=true&margin-w=4&column=7"
      alt="GitHub Trophies"
      loading="lazy"
    />
  </div>

  <!-- TOP CONTRIB -->
  <div class="contrib-card">
    <p class="section-label">top contributed repos</p>
    <img
      src="https://github-contributor-stats.vercel.app/api?username=mayurlokmanwar-analyst&limit=5&theme=radical&combine_all_yearly_contributions=true"
      alt="Top Contributed Repos"
      loading="lazy"
    />
  </div>

  <!-- FOOTER / VISIT COUNT -->
  <div class="footer">
    <span class="footer-note">// profile views</span>
    <a href="https://visitcount.itsvg.in" target="_blank" rel="noopener">
      <img
        src="https://visitcount.itsvg.in/api?id=mayurlokmanwar-analyst&icon=0&color=4"
        alt="Visit Count"
        loading="lazy"
      />
    </a>
  </div>

</div>
</body>
</html>
