<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.5"/>
  <title>Jamie_creates</title>
  <style>
    * { margin: 0; padding: 0; box-sizing: border-box; }

    body {
      background: #0a0a14;
      font-family: 'Segoe UI', sans-serif;
      color: white;
      min-height: 100vh;
    }

    nav {
      background: #0a0a14;
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding: 18px 40px;
      border-bottom: 1px solid #1a1a2e;
    }

    .nav-logo { font-weight: 700; font-size: 1rem; color: white; }
    .nav-links { display: flex; gap: 32px; }
    .nav-links a { color: #aaa; text-decoration: none; font-size: 0.95rem; }
    .nav-links a:hover { color: white; }

    .hire-btn {
      background: #7c3aed;
      color: white;
      border: none;
      padding: 10px 20px;
      border-radius: 8px;
      font-weight: 600;
      cursor: pointer;
      font-size: 0.9rem;
    }

    .grid {
      display: grid;
      grid-template-columns: 1.4fr 1fr 0.6fr;
      grid-template-rows: auto auto;
      gap: 16px;
      padding: 24px 40px;
    }

    .card {
      background: #11111e;
      border-radius: 16px;
      border: 1px solid #1e1e32;
      padding: 36px;
    }

    .card-hero {
      grid-column: 1;
      grid-row: 1 / 3;
    }

    .card-visits {
      grid-column: 2;
      grid-row: 1;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: flex-start;
      padding: 32px;
    }

    .card-avatar {
      grid-column: 3;
      grid-row: 1;
      display: flex;
      justify-content: center;
      align-items: center;
      padding: 20px;
    }

    .card-project {
      grid-column: 2 / 4;
      grid-row: 2;
      padding: 28px 32px;
    }

    .hero-name {
      font-size: 3.4rem;
      font-weight: 800;
      line-height: 1.05;
      margin-bottom: 12px;
    }

    .hero-title {
      color: #7c3aed;
      font-size: 1.05rem;
      font-weight: 600;
    }

    .visits-number {
      font-size: 2.8rem;
      font-weight: 800;
      background: linear-gradient(90deg, #38bdf8, #818cf8);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
      line-height: 1;
      margin-bottom: 8px;
    }

    .visits-label {
      color: #555;
      font-size: 0.75rem;
      letter-spacing: 0.12em;
      text-transform: uppercase;
      font-weight: 600;
    }

    .avatar-placeholder {
      width: 90px;
      height: 110px;
      background: #1e1e32;
      border-radius: 8px;
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 2.5rem;
    }

    .project-tag {
      display: inline-block;
      background: #7c3aed;
      color: white;
      font-size: 0.65rem;
      font-weight: 700;
      letter-spacing: 0.1em;
      text-transform: uppercase;
      padding: 4px 10px;
      border-radius: 5px;
      margin-bottom: 14px;
    }

    .project-title {
      font-size: 1.3rem;
      font-weight: 700;
      margin-bottom: 8px;
    }

    .project-meta {
      color: #555;
      font-size: 0.85rem;
    }
  </style>
</head>
<body>

  <nav>
    <span class="nav-logo">Jamie_creates</span>
    <div class="nav-links">
      <a href="#">Work</a>
      <a href="#">About</a>
      <a href="#">Collabs</a>
    </div>
    <button class="hire-btn">Hire Me</button>
  </nav>

  <div class="grid">

    <div class="card card-hero">
      <h1 class="hero-name">Jamie_creates</h1>
      <p class="hero-title">Roblox Developer</p>
    </div>

    <div class="card card-visits">
      <div class="visits-number">24,849,236</div>
      <div class="visits-label">Total Visits</div>
    </div>

    <div class="card card-avatar">
      <div class="avatar-placeholder">🧍</div>
    </div>

    <div class="card card-project">
      <span class="project-tag">Featured Project</span>
      <div class="project-title"> Hide the friend</div>
      <div class="project-meta">ead quality assurance • 50.000.000 visits • XXX playing</div>
    </div>

  </div>

</body>
</html>
