<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Jamie_creates</title>
  <style>
    * { margin: 0; padding: 0; box-sizing: border-box; }

    body {
      background: #0d0d12;
      font-family: 'Segoe UI', sans-serif;
      color: white;
      min-height: 100vh;
    }

    nav {
      background: #0d0d12;
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding: 18px 40px;
      border-bottom: 1px solid #1e1e2e;
    }

    .nav-logo { font-weight: 700; font-size: 1rem; color: white; }

    .nav-links { display: flex; gap: 32px; }
    .nav-links a { color: #ccc; text-decoration: none; font-size: 0.95rem; }
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

    .hero {
      padding: 40px;
      display: flex;
      gap: 20px;
    }

    .hero-card {
      background: #13131f;
      border-radius: 16px;
      padding: 36px;
      max-width: 580px;
      flex: 1;
    }

    .badge {
      display: inline-flex;
      align-items: center;
      gap: 8px;
      background: transparent;
      border: 1.5px solid #22c55e;
      color: #22c55e;
      font-size: 0.8rem;
      padding: 6px 14px;
      border-radius: 999px;
      margin-bottom: 28px;
      font-weight: 500;
    }

    .badge-dot {
      width: 8px; height: 8px;
      background: #22c55e;
      border-radius: 50%;
    }

    .hero-name {
      font-size: 3.6rem;
      font-weight: 800;
      line-height: 1.05;
      margin-bottom: 12px;
      color: white;
    }

    .hero-title {
      color: #7c3aed;
      font-size: 1.1rem;
      font-weight: 600;
      margin-bottom: 16px;
    }

    .hero-desc {
      color: #888;
      font-size: 0.95rem;
      margin-bottom: 32px;
    }

    .btn-group { display: flex; gap: 12px; }

    .btn-primary {
      background: #7c3aed;
      color: white;
      border: none;
      padding: 13px 24px;
      border-radius: 10px;
      font-weight: 700;
      font-size: 0.95rem;
      cursor: pointer;
    }

    .btn-secondary {
      background: transparent;
      color: white;
      border: 1.5px solid #333;
      padding: 13px 24px;
      border-radius: 10px;
      font-weight: 600;
      font-size: 0.95rem;
      cursor: pointer;
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

  <div class="hero">
    <div class="hero-card">
      <div class="badge">
        <span class="badge-dot"></span>
        Available for Roblox Commissions
      </div>
      <h1 class="hero-name">Jamie_creates</h1>
      <p class="hero-title">Roblox Developer</p>
      <p class="hero-desc">why you reading this just hire me gang</p>
      <div class="btn-group">
        <button class="btn-primary">See My Games</button>
        <button class="btn-secondary">Contact</button>
      </div>
    </div>
  </div>

</body>
</html>

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
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

    /* Grid layout */
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

    /* Left hero card — spans 2 rows */
    .card-hero {
      grid-column: 1;
      grid-row: 1 / 3;
    }

    /* Top middle — visits */
    .card-visits {
      grid-column: 2;
      grid-row: 1;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: flex-start;
      padding: 32px;
    }

    /* Top right — avatar */
    .card-avatar {
      grid-column: 3;
      grid-row: 1;
      display: flex;
      justify-content: center;
      align-items: center;
      padding: 20px;
    }

    /* Bottom middle+right — featured project */
    .card-project {
      grid-column: 2 / 4;
      grid-row: 2;
      padding: 28px 32px;
    }

    /* Badge */
    .badge {
      display: inline-flex;
      align-items: center;
      gap: 8px;
      border: 1.5px solid #22c55e;
      color: #22c55e;
      font-size: 0.78rem;
      padding: 6px 14px;
      border-radius: 999px;
      margin-bottom: 28px;
      font-weight: 500;
    }
    .badge-dot {
      width: 7px; height: 7px;
      background: #22c55e;
      border-radius: 50%;
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
      margin-bottom: 14px;
    }

    .hero-desc {
      color: #666;
      font-size: 0.9rem;
      margin-bottom: 32px;
    }

    .btn-group { display: flex; gap: 12px; }

    .btn-primary {
      background: #7c3aed;
      color: white;
      border: none;
      padding: 13px 22px;
      border-radius: 10px;
      font-weight: 700;
      font-size: 0.9rem;
      cursor: pointer;
    }

    .btn-secondary {
      background: transparent;
      color: white;
      border: 1.5px solid #2a2a3e;
      padding: 13px 22px;
      border-radius: 10px;
      font-weight: 600;
      font-size: 0.9rem;
      cursor: pointer;
    }

    /* Visits card */
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

    /* Avatar */
    .roblox-avatar {
      width: 90px;
      height: 110px;
      object-fit: contain;
    }

    /* Avatar placeholder (pixelated roblox-style) */
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

    /* Featured project */
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

    <!-- Hero card -->
    <div class="card card-hero">
      <div class="badge">
        <span class="badge-dot"></span>
        Available for Roblox Commissions
      </div>
      <h1 class="hero-name">Jamie_creates</h1>
      <p class="hero-title">Roblox Developer</p>
      <p class="hero-desc">why you reading this just hire me gang</p>
      <div class="btn-group">
        <button class="btn-primary">See My Games</button>
        <button class="btn-secondary">Contact</button>
      </div>
    </div>

    <!-- Visits card -->
    <div class="card card-visits">
      <div class="visits-number">24,849,236</div>
      <div class="visits-label">Total Visits</div>
    </div>

    <!-- Avatar card -->
    <div class="card card-avatar">
      <div class="avatar-placeholder">🧍</div>
    </div>

    <!-- Featured project card -->
    <div class="card card-project">
      <span class="project-tag">Featured Project</span>
      <div class="project-title">[UPD 🔥] Arise Army Tycoon 🚀</div>
      <div class="project-meta">Head Developer • 6.4M visits • 271 playing</div>
    </div>

  </div>

</body>
</html>
