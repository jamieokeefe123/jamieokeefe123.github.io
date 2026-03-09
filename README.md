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
