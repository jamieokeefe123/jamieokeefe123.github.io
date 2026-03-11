<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Jamie_creates — Roblox Developer</title>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700;800&display=swap" rel="stylesheet">

    <style>
/* =====================================================
   JAMIE_CREATES - BENTO GRID PORTFOLIO
   ===================================================== */

:root {
    --bg-dark: #0a0a0f;
    --bg-card: #12121a;
    --bg-card-hover: #1a1a26;

    --text: #ffffff;
    --text-secondary: rgba(255, 255, 255, 0.7);
    --text-muted: rgba(255, 255, 255, 0.45);

    --accent: #f59e0b;
    --accent-light: #fbbf24;
    --accent-2: #06b6d4;
    --success: #22c55e;
    --discord: #5865F2;
    --roblox: #ff4444;
    --primary: #f59e0b;
    --primary-dark: #d97706;
    --text-main: #ffffff;
    --text-dim: rgba(255, 255, 255, 0.5);

    --border: rgba(255, 255, 255, 0.06);
    --border-hover: rgba(245, 158, 11, 0.5);

    --font: 'Inter', -apple-system, sans-serif;
    --radius: 16px;
    --radius-sm: 10px;

    --shadow: 0 4px 24px rgba(0, 0, 0, 0.2);
    --shadow-lg: 0 12px 40px rgba(0, 0, 0, 0.3);
}

* { margin: 0; padding: 0; box-sizing: border-box; }

html { scroll-behavior: smooth; scroll-padding-top: 80px; }

body {
    font-family: var(--font);
    background: var(--bg-dark);
    color: var(--text);
    line-height: 1.5;
    -webkit-font-smoothing: antialiased;
}

.container { max-width: 1200px; margin: 0 auto; padding: 0 20px; }

/* Mosaic Background */
.thumbnail-mosaic {
    position: fixed; inset: 0; pointer-events: none;
    z-index: -3; overflow: hidden; opacity: 0.12;
}
.mosaic-inner {
    position: absolute; inset: -50%; width: 200%; height: 200%;
    transform: rotate(-15deg); display: flex; flex-direction: column;
    justify-content: center; gap: 16px;
}
.mosaic-overlay {
    position: fixed; inset: 0; pointer-events: none; z-index: -2;
    background:
        radial-gradient(ellipse 80% 60% at 50% 50%, transparent 20%, var(--bg-dark) 70%),
        linear-gradient(to bottom, var(--bg-dark) 0%, transparent 15%, transparent 85%, var(--bg-dark) 100%);
}
.mosaic-row { display: flex; gap: 16px; width: max-content; flex-shrink: 0; }
.mosaic-row img { width: 280px; height: 158px; object-fit: cover; border-radius: 12px; flex-shrink: 0; }
.mosaic-row:nth-child(odd)  { animation: mosaic-scroll-left  var(--speed) linear infinite; }
.mosaic-row:nth-child(even) { animation: mosaic-scroll-right var(--speed) linear infinite; }
@keyframes mosaic-scroll-left  { 0% { transform: translateX(0); }    100% { transform: translateX(-50%); } }
@keyframes mosaic-scroll-right { 0% { transform: translateX(-50%); } 100% { transform: translateX(0); } }

.bg-gradient {
    position: fixed; inset: 0; pointer-events: none; z-index: -1;
    background:
        radial-gradient(ellipse 80% 50% at 40% -10%, rgba(245, 158, 11, 0.12), transparent 50%),
        radial-gradient(ellipse 60% 40% at 90% 80%, rgba(6, 182, 212, 0.1), transparent 50%);
}

/* Navigation */
.navbar {
    position: fixed; top: 0; left: 0; right: 0; z-index: 100;
    padding: 14px 20px; background: rgba(10, 10, 15, 0.9);
    backdrop-filter: blur(20px); border-bottom: 1px solid var(--border);
}
.nav-container {
    max-width: 1200px; margin: 0 auto;
    display: flex; align-items: center; justify-content: space-between;
}
.logo { font-size: 18px; font-weight: 700; color: var(--text); text-decoration: none; }
.nav-links { display: flex; list-style: none; gap: 32px; }
.nav-links a { font-size: 14px; font-weight: 500; color: var(--text-secondary); text-decoration: none; transition: 0.2s; }
.nav-links a:hover { color: var(--text); }
.nav-cta {
    font-size: 13px; padding: 8px 18px; background: var(--accent);
    color: #0a0a0f; text-decoration: none; border-radius: 8px;
    font-weight: 700; transition: 0.2s;
}
.nav-cta:hover { transform: translateY(-1px); box-shadow: 0 4px 20px rgba(245, 158, 11, 0.4); }

.mobile-menu-btn {
    display: none; flex-direction: column; gap: 5px;
    background: none; border: none; cursor: pointer; padding: 8px;
}
.mobile-menu-btn span { width: 20px; height: 2px; background: var(--text); transition: 0.2s; }
.mobile-menu {
    display: none; position: fixed; top: 55px; left: 0; right: 0;
    background: var(--bg-dark); padding: 20px; flex-direction: column;
    gap: 12px; border-bottom: 1px solid var(--border); z-index: 99;
    opacity: 0; pointer-events: none; transition: 0.2s;
}
.mobile-menu.active { opacity: 1; pointer-events: auto; }
.mobile-menu a { font-size: 16px; color: var(--text); text-decoration: none; padding: 10px 0; }

/* Hero Bento Grid */
.hero { padding: 100px 20px 60px; }
.hero-grid {
    max-width: 1200px; margin: 0 auto;
    display: grid; grid-template-columns: repeat(4, 1fr);
    grid-auto-rows: minmax(100px, auto); gap: 14px;
}
.bento-card {
    background: var(--bg-card); border: 1px solid var(--border);
    border-radius: var(--radius); transition: 0.3s ease; overflow: hidden;
}
.bento-card:hover { border-color: var(--border-hover); transform: translateY(-2px); }

.bento-main {
    grid-column: span 2; grid-row: span 2; padding: 40px;
    display: flex; flex-direction: column; justify-content: center;
}
.status-pill {
    display: inline-flex; align-items: center; gap: 8px; padding: 6px 14px;
    background: rgba(34, 197, 94, 0.12); border: 1px solid rgba(34, 197, 94, 0.25);
    border-radius: 100px; font-size: 13px; font-weight: 500;
    color: var(--success); width: fit-content; margin-bottom: 24px;
}
.status-dot {
    width: 7px; height: 7px; background: var(--success);
    border-radius: 50%; animation: pulse 2s infinite;
}
@keyframes pulse { 0%, 100% { opacity: 1; } 50% { opacity: 0.4; } }

.hero-name {
    font-size: clamp(44px, 6vw, 60px); font-weight: 800;
    letter-spacing: -0.03em; margin-bottom: 4px;
    background: linear-gradient(135deg, #fff 40%, var(--accent-light) 100%);
    -webkit-background-clip: text; -webkit-text-fill-color: transparent; background-clip: text;
}
.hero-role { font-size: 18px; color: var(--accent); font-weight: 600; margin-bottom: 16px; }
.hero-desc { font-size: 15px; color: var(--text-secondary); line-height: 1.7; margin-bottom: 32px; max-width: 420px; }
.hero-ctas { display: flex; gap: 12px; }
.btn-primary {
    padding: 12px 24px; background: linear-gradient(135deg, var(--accent) 0%, #d97706 100%);
    color: #0a0a0f; text-decoration: none; border-radius: var(--radius-sm);
    font-size: 14px; font-weight: 700; transition: 0.2s;
}
.btn-primary:hover { transform: translateY(-2px); box-shadow: 0 8px 28px rgba(245, 158, 11, 0.45); }
.btn-outline {
    padding: 12px 24px; background: transparent; color: var(--text-secondary);
    text-decoration: none; border: 1px solid var(--border);
    border-radius: var(--radius-sm); font-size: 14px; font-weight: 500; transition: 0.2s;
}
.btn-outline:hover { color: var(--text); border-color: var(--text-muted); }

/* Bento Stats */
.bento-stats {
    padding: 28px; display: flex; align-items: center; justify-content: center;
    background: linear-gradient(135deg, var(--bg-card) 0%, rgba(245, 158, 11, 0.06) 100%);
}
.stat-big { text-align: center; }
.stat-number {
    display: block; font-size: 36px; font-weight: 800;
    background: linear-gradient(135deg, var(--accent-light), var(--accent-2));
    -webkit-background-clip: text; -webkit-text-fill-color: transparent; background-clip: text;
}
.stat-label { font-size: 11px; color: var(--text-muted); margin-top: 6px; text-transform: uppercase; letter-spacing: 0.5px; }

/* Bento Avatar */
.bento-avatar {
    padding: 24px; display: flex; align-items: center; justify-content: center;
    background: linear-gradient(135deg, rgba(6, 182, 212, 0.06), var(--bg-card));
}
.avatar-img { width: 100%; max-width: 100px; border-radius: 14px; box-shadow: var(--shadow); }

/* Bento Featured */
.bento-featured { grid-column: span 2; min-height: 160px; position: relative; cursor: pointer; }
.featured-bg {
    position: absolute; inset: 0;
    background: linear-gradient(135deg, #1a1a2e, #16213e);
    background-size: cover; background-position: center; transition: 0.4s;
}
.bento-featured:hover .featured-bg { transform: scale(1.05); }
.featured-overlay {
    position: absolute; inset: 0;
    background: linear-gradient(to top, rgba(10, 10, 15, 0.95) 0%, rgba(10, 10, 15, 0.2) 100%);
}
.featured-content { position: absolute; bottom: 0; left: 0; right: 0; padding: 24px; z-index: 1; }
.featured-tag {
    display: inline-block; padding: 4px 10px;
    background: linear-gradient(135deg, var(--accent), #d97706);
    color: #0a0a0f; border-radius: 6px; font-size: 10px; font-weight: 700;
    text-transform: uppercase; letter-spacing: 0.8px; margin-bottom: 10px;
}
.featured-title { font-size: 20px; font-weight: 700; margin-bottom: 4px; }
.featured-role { font-size: 13px; color: var(--text-secondary); }

/* Bento Links */
.bento-links { padding: 16px; display: flex; flex-direction: column; gap: 8px; }
.quick-link {
    display: flex; align-items: center; gap: 10px; padding: 12px 14px;
    background: rgba(255, 255, 255, 0.02); border: 1px solid transparent;
    border-radius: var(--radius-sm); text-decoration: none;
    color: var(--text-secondary); font-size: 13px; font-weight: 500; transition: 0.2s;
}
.quick-link svg { width: 18px; height: 18px; }
.quick-link.discord:hover { background: rgba(88,101,242,0.12); border-color: rgba(88,101,242,0.3); color: var(--discord); }
.quick-link.roblox:hover  { background: rgba(255,68,68,0.1);   border-color: rgba(255,68,68,0.3);  color: var(--roblox); }

/* Bento Projects / Location / Experience */
.bento-projects {
    padding: 20px; display: flex; flex-direction: column;
    align-items: center; justify-content: center; text-align: center;
    background: linear-gradient(135deg, var(--bg-card), rgba(245, 158, 11, 0.04));
}
.projects-number {
    font-size: 44px; font-weight: 800;
    background: linear-gradient(135deg, #fff, var(--accent-light));
    -webkit-background-clip: text; -webkit-text-fill-color: transparent; background-clip: text;
}
.projects-label { font-size: 11px; color: var(--text-muted); text-transform: uppercase; letter-spacing: 0.5px; }

.bento-location {
    padding: 20px; display: flex; flex-direction: column;
    align-items: center; justify-content: center; text-align: center;
    background: linear-gradient(135deg, rgba(34, 197, 94, 0.06), var(--bg-card));
}
.location-icon { font-size: 32px; margin-bottom: 8px; }
.location-text { font-size: 20px; font-weight: 700; }
.location-sub { font-size: 11px; color: var(--text-muted); text-transform: uppercase; letter-spacing: 0.5px; margin-top: 4px; }

.bento-experience {
    padding: 20px; display: flex; flex-direction: column;
    align-items: center; justify-content: center; text-align: center;
    background: linear-gradient(135deg, rgba(6, 182, 212, 0.06), var(--bg-card));
}
.exp-number {
    font-size: 44px; font-weight: 800;
    background: linear-gradient(135deg, var(--accent-2), #22d3ee);
    -webkit-background-clip: text; -webkit-text-fill-color: transparent; background-clip: text;
}
.exp-label { font-size: 11px; color: var(--text-muted); text-transform: uppercase; letter-spacing: 0.5px; margin-top: 4px; }

/* Sections */
.section { padding: 80px 0; }
.section-dark { background: var(--bg-card); }
.section-header { text-align: center; margin-bottom: 48px; }
.section-header h2 { font-size: 32px; font-weight: 700; margin-bottom: 8px; }
.section-header p { font-size: 15px; color: var(--text-muted); }

/* Games Grid */
.games-grid { display: grid; grid-template-columns: repeat(2, 1fr); gap: 24px; }
.game-card {
    background: var(--bg-card); border: 1px solid var(--border);
    border-radius: var(--radius); overflow: hidden; text-decoration: none;
    color: inherit; transition: 0.3s; display: block;
}
.game-card:hover { transform: translateY(-4px); border-color: var(--border-hover); }
.game-thumb-wrap {
    width: 100%; aspect-ratio: 16 / 9;
    background: linear-gradient(135deg, var(--bg-card), var(--bg-card-hover));
    overflow: hidden; position: relative; border-bottom: 1px solid var(--border);
}
.game-thumb { width: 100%; height: 100%; object-fit: cover; transition: transform 0.5s ease; }
.game-thumb.broken { display: none; }
.game-card:hover .game-thumb { transform: scale(1.04); }
.game-info { padding: 18px; }
.game-name { font-size: 17px; font-weight: 600; margin-bottom: 4px; }
.game-creator { font-size: 13px; color: var(--text-muted); margin-bottom: 14px; }
.game-meta { display: flex; justify-content: space-between; align-items: center; }
.game-stats { display: flex; gap: 16px; }
.game-stat { display: flex; align-items: center; gap: 5px; font-size: 13px; color: var(--text-secondary); }
.game-stat svg { width: 14px; height: 14px; opacity: 0.5; }
.game-role-tag {
    padding: 4px 10px; background: linear-gradient(135deg, var(--accent), #d97706);
    color: #0a0a0f; border-radius: 6px; font-size: 11px; font-weight: 700; text-transform: uppercase;
}

/* Skeleton */
.skeleton-thumb {
    width: 100%; aspect-ratio: 16/9;
    background: linear-gradient(90deg, #1a1a24 25%, #252530 50%, #1a1a24 75%);
    background-size: 200% 100%; animation: shimmer 1.5s infinite;
}
.skeleton-info {
    height: 90px; margin: 18px;
    background: linear-gradient(90deg, #1a1a24 25%, #252530 50%, #1a1a24 75%);
    background-size: 200% 100%; border-radius: 8px; animation: shimmer 1.5s infinite;
}
@keyframes shimmer { 0% { background-position: 200% 0; } 100% { background-position: -200% 0; } }

/* About */
.about-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 60px; align-items: start; }
.about-text h2 { font-size: 28px; font-weight: 700; margin-bottom: 28px; }
.about-points { display: flex; flex-direction: column; gap: 16px; }
.about-point {
    display: flex; gap: 16px; padding: 20px; background: var(--bg-dark);
    border: 1px solid var(--border); border-radius: var(--radius-sm); transition: 0.2s;
}
.about-point:hover { border-color: var(--accent); transform: translateX(4px); }
.point-icon {
    font-size: 22px; width: 48px; height: 48px;
    background: linear-gradient(135deg, rgba(245,158,11,0.15), rgba(245,158,11,0.05));
    border-radius: 12px; display: flex; align-items: center; justify-content: center; flex-shrink: 0;
}
.about-point strong { display: block; font-size: 15px; margin-bottom: 4px; }
.about-point p { font-size: 13px; color: var(--text-secondary); line-height: 1.6; }

/* Reviews — styles preserved, section hidden from display */
.reviews-col h3 { font-size: 18px; font-weight: 600; margin-bottom: 20px; color: var(--text-secondary); }
.reviews-stack { display: flex; flex-direction: column; gap: 12px; }
.review-card { background: var(--bg-dark); border: 1px solid var(--border); border-radius: var(--radius-sm); padding: 20px; }
.review-header { display: flex; align-items: center; gap: 12px; margin-bottom: 14px; }
.review-avatar {
    width: 48px; height: 48px; border-radius: 50%; overflow: hidden;
    background: var(--bg-card-hover); display: flex; align-items: center;
    justify-content: center; flex-shrink: 0;
}
.review-avatar img { width: 100%; height: 100%; object-fit: cover; }
.review-link-wrapper, .review-name-link { text-decoration: none; color: inherit; transition: opacity 0.2s; }
.review-link-wrapper:hover, .review-name-link:hover { opacity: 0.8; }
.review-meta { flex: 1; }
.review-name { font-weight: 600; font-size: 1rem; color: var(--text-main); display: flex; align-items: center; }
.review-role { font-size: 0.85rem; color: var(--text-dim); margin-top: 2px; }
.review-stars { display: flex; gap: 2px; }
.review-stars svg { width: 14px; height: 14px; fill: #fbbf24; }
.review-text { font-size: 14px; color: var(--text-secondary); line-height: 1.65; font-style: italic; }

/* Contact */
.contact-box {
    display: flex; justify-content: space-between; align-items: center; gap: 40px; padding: 52px;
    background: linear-gradient(135deg, rgba(245,158,11,0.08), rgba(6,182,212,0.04));
    border: 1px solid var(--border); border-radius: var(--radius);
}
.contact-left h2 { font-size: 30px; font-weight: 700; margin-bottom: 10px; }
.contact-left p { font-size: 15px; color: var(--text-secondary); }
.contact-right { display: flex; gap: 14px; }
.contact-btn {
    display: flex; align-items: center; gap: 10px; padding: 14px 26px;
    border-radius: var(--radius-sm); text-decoration: none;
    font-size: 14px; font-weight: 600; color: white; transition: 0.2s;
}
.contact-btn svg { width: 20px; height: 20px; }
.contact-btn.discord { background: linear-gradient(135deg, var(--discord), #7289da); }
.contact-btn.roblox  { background: linear-gradient(135deg, var(--roblox),  #ff6b6b); }
.contact-btn:hover { transform: translateY(-3px); box-shadow: 0 10px 30px rgba(0,0,0,0.3); }

/* Footer */
.footer { padding: 28px; text-align: center; font-size: 13px; color: var(--text-muted); border-top: 1px solid var(--border); }

/* Services Grid */
.services-grid { display: grid; grid-template-columns: repeat(4, 1fr); gap: 20px; margin-top: 40px; }
.service-card {
    background: var(--bg-dark); border: 1px solid var(--border);
    border-radius: var(--radius-sm); padding: 32px 24px; text-align: center; transition: 0.3s;
}
.service-card:hover { border-color: var(--accent); transform: translateY(-5px); background: var(--bg-card-hover); }
.service-icon { font-size: 32px; margin-bottom: 16px; display: block; }
.service-card h3 { font-size: 18px; font-weight: 700; margin-bottom: 12px; }
.service-card p { font-size: 14px; color: var(--text-secondary); line-height: 1.6; }

.sr-only {
    position: absolute; width: 1px; height: 1px; padding: 0; margin: -1px;
    overflow: hidden; clip: rect(0,0,0,0); white-space: nowrap; border-width: 0;
}

/* Responsive */
@media (max-width: 1024px) {
    .hero-grid { grid-template-columns: repeat(2, 1fr); }
    .bento-main, .bento-featured { grid-column: span 2; }
    .about-grid { grid-template-columns: 1fr; gap: 40px; }
    .services-grid { grid-template-columns: repeat(2, 1fr); }
}
@media (max-width: 768px) {
    .nav-links, .nav-cta { display: none; }
    .mobile-menu-btn { display: flex; }
    .mobile-menu { display: flex; }
    .hero-grid { grid-template-columns: 1fr 1fr; }
    .bento-main, .bento-featured { grid-column: span 2; }
    .hero-name { font-size: 36px; }
    .bento-main { padding: 28px; }
    .games-grid { grid-template-columns: 1fr; }
    .contact-box { flex-direction: column; text-align: center; padding: 36px 24px; }
    .contact-right { flex-direction: column; width: 100%; }
    .contact-btn { justify-content: center; }
}
@media (max-width: 640px) {
    .services-grid { grid-template-columns: 1fr; }
}
    </style>
</head>
<body>

    <!-- Mosaic Background -->
    <div class="thumbnail-mosaic" id="thumbnailMosaic"></div>
    <div class="mosaic-overlay"></div>
    <div class="bg-gradient"></div>

    <!-- Navigation -->
    <nav class="navbar">
        <div class="nav-container">
            <a href="#" class="logo">Jamie_creates</a>
            <ul class="nav-links">
                <li><a href="#games">Games</a></li>
                <li><a href="#about">About</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
            <a href="#contact" class="nav-cta">Hire Me</a>
            <button class="mobile-menu-btn" aria-label="Menu">
                <span></span><span></span><span></span>
            </button>
        </div>
    </nav>

    <!-- Mobile Menu -->
    <div class="mobile-menu">
        <a href="#games">Games</a>
        <a href="#about">About</a>
        <a href="#contact">Contact</a>
    </div>

    <!-- Hero Bento -->
    <section class="hero">
        <div class="hero-grid">

            <!-- Main intro -->
            <div class="bento-card bento-main">
                <div class="status-pill">
                    <span class="status-dot"></span>
                    Available for work
                </div>
                <h1 class="hero-name">Jamie_creates</h1>
                <div class="hero-role">Roblox Developer</div>
                <p class="hero-desc">
                    Building immersive Roblox experiences with millions of plays.
                    Specialising in game systems, UI, and polished gameplay.
                </p>
                <div class="hero-ctas">
                    <a href="#games" class="btn-primary">View Games</a>
                    <a href="#contact" class="btn-outline">Get in Touch</a>
                </div>
            </div>

            <!-- Total Visits -->
            <div class="bento-card bento-stats">
                <div class="stat-big">
                    <span class="stat-number" id="heroVisits">0</span>
                    <div class="stat-label">Total Visits</div>
                </div>
            </div>

            <!-- Avatar -->
            <div class="bento-card bento-avatar">
                <img src="profile.png" alt="Jamie_creates" class="avatar-img"
                     onerror="this.style.opacity='0.3'">
            </div>

            <!-- Featured Game -->
            <div class="bento-card bento-featured" id="featuredGame">
                <div class="featured-bg"></div>
                <div class="featured-overlay"></div>
                <div class="featured-content">
                    <span class="featured-tag">⭐ Featured</span>
                    <div class="featured-title">Loading...</div>
                    <div class="featured-role"></div>
                </div>
            </div>

            <!-- Quick Links -->
            <div class="bento-card bento-links">
                <a href="#" class="quick-link discord">
                    <svg viewBox="0 0 24 24" fill="currentColor">
                        <path d="M20.317 4.37a19.791 19.791 0 0 0-4.885-1.515.074.074 0 0 0-.079.037c-.21.375-.444.864-.608 1.25a18.27 18.27 0 0 0-5.487 0 12.64 12.64 0 0 0-.617-1.25.077.077 0 0 0-.079-.037A19.736 19.736 0 0 0 3.677 4.37a.07.07 0 0 0-.032.027C.533 9.046-.32 13.58.099 18.057a.082.082 0 0 0 .031.057 19.9 19.9 0 0 0 5.993 3.03.078.078 0 0 0 .084-.028c.462-.63.874-1.295 1.226-1.994a.076.076 0 0 0-.041-.106 13.107 13.107 0 0 1-1.872-.892.077.077 0 0 1-.008-.128 10.2 10.2 0 0 0 .372-.292.074.074 0 0 1 .077-.01c3.928 1.793 8.18 1.793 12.062 0a.074.074 0 0 1 .078.01c.12.098.246.198.373.292a.077.077 0 0 1-.006.127 12.299 12.299 0 0 1-1.873.892.077.077 0 0 0-.041.107c.36.698.772 1.362 1.225 1.993a.076.076 0 0 0 .084.028 19.839 19.839 0 0 0 6.002-3.03.077.077 0 0 0 .032-.054c.5-5.177-.838-9.674-3.549-13.66a.061.061 0 0 0-.031-.03z"/>
                    </svg>
                    Discord
                </a>
                <a href="https://www.roblox.com/users/search?keyword=Jamie_creates" target="_blank" class="quick-link roblox">
                    <svg viewBox="0 0 24 24" fill="currentColor">
                        <path d="M3.44 17.777L6.22 3.443l14.334 2.779-2.779 14.334z"/>
                    </svg>
                    Roblox Profile
                </a>
            </div>

            <!-- Projects -->
            <div class="bento-card bento-projects">
                <div class="projects-number">5</div>
                <div class="projects-label">Games Built</div>
            </div>

            <!-- Location -->
            <div class="bento-card bento-location">
                <div class="location-icon">🌍</div>
                <div class="location-text">Remote</div>
                <div class="location-sub">Worldwide</div>
            </div>

            <!-- Experience -->
            <div class="bento-card bento-experience">
                <div class="exp-number">4+</div>
                <div class="exp-label">Years Experience</div>
            </div>

        </div>
    </section>

    <!-- Games Section -->
    <section class="section" id="games">
        <div class="container">
            <div class="section-header">
                <h2>Games</h2>
                <p>Projects I've built and contributed to</p>
            </div>
            <div class="games-grid" id="gamesGrid">
                <!-- Skeletons while loading -->
                <div class="game-card skeleton">
                    <div class="skeleton-thumb"></div>
                    <div class="skeleton-info"></div>
                </div>
                <div class="game-card skeleton">
                    <div class="skeleton-thumb"></div>
                    <div class="skeleton-info"></div>
                </div>
                <div class="game-card skeleton">
                    <div class="skeleton-thumb"></div>
                    <div class="skeleton-info"></div>
                </div>
                <div class="game-card skeleton">
                    <div class="skeleton-thumb"></div>
                    <div class="skeleton-info"></div>
                </div>
            </div>
        </div>
    </section>

    <!-- About Section -->
    <section class="section section-dark" id="about">
        <div class="container">
            <div class="about-grid">
                <div class="about-text">
                    <h2>About Me</h2>
                    <div class="about-points">
                        <div class="about-point">
                            <div class="point-icon">🎮</div>
                            <div>
                                <strong>Game Development</strong>
                                <p>Scripting complex game systems, smooth mechanics, and satisfying player loops in Roblox Studio.</p>
                            </div>
                        </div>
                        <div class="about-point">
                            <div class="point-icon">🎨</div>
                            <div>
                                <strong>UI / UX Design</strong>
                                <p>Clean, readable interfaces that feel polished and keep players engaged.</p>
                            </div>
                        </div>
                    </div>
                </div>

                <!-- Services -->
                <div>
                    <div class="services-grid" style="margin-top:0; grid-template-columns: repeat(2,1fr);">
                        <div class="service-card">
                            <span class="service-icon">⚙️</span>
                            <h3>Scripting</h3>
                            <p>Lua / Luau systems, datastores, remotes, and more.</p>
                        </div>
                        <div class="service-card">
                            <span class="service-icon">🖼️</span>
                            <h3>UI Design</h3>
                            <p>Responsive, animated GUIs that feel great on any device.</p>
                        </div>
                        <div class="service-card">
                            <span class="service-icon">🗺️</span>
                            <h3>Game Design</h3>
                            <p>Tycoons, obbies, RPGs — full gameplay loop planning.</p>
                        </div>
                        <div class="service-card">
                            <span class="service-icon">🚀</span>
                            <h3>Optimisation</h3>
                            <p>Performance audits, lag fixes, and memory management.</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section class="section section-dark" id="contact">
        <div class="container">
            <div class="contact-box">
                <div class="contact-left">
                    <h2>Let's Work Together</h2>
                    <p>Got a project in mind? Reach out on Discord or Roblox.</p>
                </div>
                <div class="contact-right">
                    <a href="#" class="contact-btn discord">
                        <svg viewBox="0 0 24 24" fill="currentColor">
                            <path d="M20.317 4.37a19.791 19.791 0 0 0-4.885-1.515.074.074 0 0 0-.079.037c-.21.375-.444.864-.608 1.25a18.27 18.27 0 0 0-5.487 0 12.64 12.64 0 0 0-.617-1.25.077.077 0 0 0-.079-.037A19.736 19.736 0 0 0 3.677 4.37a.07.07 0 0 0-.032.027C.533 9.046-.32 13.58.099 18.057a.082.082 0 0 0 .031.057 19.9 19.9 0 0 0 5.993 3.03.078.078 0 0 0 .084-.028c.462-.63.874-1.295 1.226-1.994a.076.076 0 0 0-.041-.106 13.107 13.107 0 0 1-1.872-.892.077.077 0 0 1-.008-.128 10.2 10.2 0 0 0 .372-.292.074.074 0 0 1 .077-.01c3.928 1.793 8.18 1.793 12.062 0a.074.074 0 0 1 .078.01c.12.098.246.198.373.292a.077.077 0 0 1-.006.127 12.299 12.299 0 0 1-1.873.892.077.077 0 0 0-.041.107c.36.698.772 1.362 1.225 1.993a.076.076 0 0 0 .084.028 19.839 19.839 0 0 0 6.002-3.03.077.077 0 0 0 .032-.054c.5-5.177-.838-9.674-3.549-13.66a.061.061 0 0 0-.031-.03z"/>
                        </svg>
                        Discord
                    </a>
                    <a href="https://www.roblox.com/users/search?keyword=Jamie_creates" target="_blank" class="contact-btn roblox">
                        <svg viewBox="0 0 24 24" fill="currentColor">
                            <path d="M3.44 17.777L6.22 3.443l14.334 2.779-2.779 14.334z"/>
                        </svg>
                        Roblox
                    </a>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="footer">
        <p>© 2025 Jamie_creates · Roblox Developer</p>
    </footer>

    <script>
/* =====================================================
   JAMIE_CREATES PORTFOLIO - JAVASCRIPT
   ===================================================== */

const CONFIG = {
    games: [
        { placeId: "94282122066477",   universeId: "7811316908", role: "Head Developer", featured: true },
        { placeId: "130967462823996",  universeId: "8023196202", role: "Owner" },
        { placeId: "14958096162",      universeId: "5152857750", role: "Head Developer" },
        { placeId: "13421499226",      universeId: "4671081879", role: "Developer" },
        { placeId: "100989019560808",  universeId: "9439392511", role: "Developer" }
    ],

    // Reviews data preserved — section hidden from display
    reviews: [
        {
            text: "chill guy did a pretty nice job",
            name: "sapoperro",
            role: "Roblox Developer",
            avatar: "https://thumbnails.roblox.com/v1/users/avatar-headshot?userIds=352535647&size=150x150&format=Png&isCircular=true",
            profileUrl: "https://www.roblox.com/users/352535647/profile"
        },
        {
            text: "Did an awesome job, polished everything up.",
            name: "Shrani_Blind",
            role: "Game Builder",
            avatar: "https://thumbnails.roblox.com/v1/users/avatar-headshot?userIds=2357507092&size=150x150&format=Png&isCircular=true",
            profileUrl: "https://www.roblox.com/users/2357507092/profile"
        },
        {
            text: "Reliable lad",
            name: "Drak",
            role: "Project Manager",
            avatar: "https://thumbnails.roblox.com/v1/users/avatar-headshot?userIds=2328178033&size=150x150&format=Png&isCircular=true",
            profileUrl: "https://www.roblox.com/users/2328178033/profile"
        }
    ],

    debug: true
};

const Log = {
    info:  (msg) => { if (CONFIG.debug) console.log(`%c[INFO] ${msg}`, 'color: #f59e0b'); },
    warn:  (msg) => { if (CONFIG.debug) console.warn(`[WARN] ${msg}`); },
    error: (msg) => { if (CONFIG.debug) console.error(`[ERROR] ${msg}`); }
};

function formatNumber(num) {
    if (num >= 1e9) return (num / 1e9).toFixed(1) + 'B';
    if (num >= 1e6) return (num / 1e6).toFixed(1) + 'M';
    if (num >= 1e3) return (num / 1e3).toFixed(1) + 'K';
    return num.toString();
}

function formatFull(num) {
    return num.toLocaleString('en-US');
}

function animateCounter(el, target, duration = 2000) {
    const start = performance.now();
    function update(now) {
        const progress = Math.min((now - start) / duration, 1);
        const eased = 1 - Math.pow(1 - progress, 3);
        el.textContent = formatFull(Math.floor(target * eased));
        if (progress < 1) requestAnimationFrame(update);
    }
    requestAnimationFrame(update);
}

const PROXY_BASE = 'https://roblox-proxy.hohimihi.workers.dev';

async function fetchWithRetry(path, query) {
    const targetUrl = path.startsWith('http') ? path + query : `https://games.roblox.com/v1/${path}${query}`;
    const url = `${PROXY_BASE}/?url=${encodeURIComponent(targetUrl)}`;
    Log.info(`Fetching via proxy: ${targetUrl}`);
    const res = await fetch(url);
    if (!res.ok) throw new Error(`Proxy returned ${res.status}`);
    const data = await res.json();
    Log.info('Successfully fetched data');
    return data;
}

const FALLBACK_GAMES = [
    {
        name: "Arise Army Tycoon", visits: 1000000, playing: 500, role: "Developer",
        creator: "Jamie_creates",
        thumbnail: "https://www.roblox.com/asset-thumbnail/image?assetId=94282122066477&width=768&height=432&format=png",
        url: "https://www.roblox.com/games/94282122066477"
    },
    {
        name: "Obby But You're Glitched", visits: 235400, playing: 42, role: "Owner",
        creator: "Jamie_creates",
        thumbnail: "https://www.roblox.com/asset-thumbnail/image?assetId=130967462823996&width=768&height=432&format=png",
        url: "https://www.roblox.com/games/130967462823996"
    },
    {
        name: "Evolve [Sniffer!]", visits: 12100000, playing: 130, role: "Head Developer",
        creator: "Jamie_creates",
        thumbnail: "https://www.roblox.com/asset-thumbnail/image?assetId=14958096162&width=768&height=432&format=png",
        url: "https://www.roblox.com/games/14958096162"
    },
    {
        name: "Space Station Tycoon", visits: 2600000, playing: 15, role: "Developer",
        creator: "Jamie_creates",
        thumbnail: "https://www.roblox.com/asset-thumbnail/image?assetId=13421499226&width=768&height=432&format=png",
        url: "https://www.roblox.com/games/13421499226"
    },
    {
        name: "Knife or Die", visits: 0, playing: 0, role: "Developer",
        creator: "Unknown",
        thumbnail: "https://www.roblox.com/asset-thumbnail/image?assetId=100989019560808&width=768&height=432&format=png",
        url: "https://www.roblox.com/games/100989019560808"
    }
];

async function fetchGames() {
    const gameConfigs = CONFIG.games;
    const cacheKey = `roblox_cache_${gameConfigs.length}_v2`;
    const universeIds = gameConfigs.map(g => g.universeId).join(',');

    try {
        const [gamesRes, thumbRes, mosaicThumbRes] = await Promise.all([
            fetchWithRetry('https://games.roblox.com/v1/games', `?universeIds=${universeIds}`),
            fetchWithRetry('https://thumbnails.roblox.com/v1/games/multiget/thumbnails', `?universeIds=${universeIds}&countPerUniverse=1&size=768x432&format=Webp`),
            fetchWithRetry('https://thumbnails.roblox.com/v1/games/multiget/thumbnails', `?universeIds=${universeIds}&countPerUniverse=10&size=480x270&format=Webp`)
        ]);

        const gamesList = gamesRes.data || [];
        const thumbsList = thumbRes.data || [];
        const thumbsMap = {};
        thumbsList.forEach(item => {
            if (item.universeId && item.thumbnails?.[0]?.imageUrl)
                thumbsMap[item.universeId] = item.thumbnails[0].imageUrl;
        });

        const allThumbnails = [];
        (mosaicThumbRes.data || []).forEach(item => {
            if (item.thumbnails?.length)
                item.thumbnails.forEach(t => { if (t.imageUrl) allThumbnails.push(t.imageUrl); });
        });

        const finalGames = gameConfigs.map(config => {
            const gameData = gamesList.find(g => String(g.id) === String(config.universeId));
            if (!gameData) return null;
            return {
                name: gameData.name, creator: gameData.creator.name,
                visits: gameData.visits, playing: gameData.playing,
                role: config.role, thumbnail: thumbsMap[config.universeId] || null,
                url: `https://www.roblox.com/games/${config.placeId}`
            };
        }).filter(Boolean);

        if (finalGames.length > 0) {
            localStorage.setItem(cacheKey, JSON.stringify({ data: finalGames, allThumbnails, timestamp: Date.now() }));
            return { games: finalGames, allThumbnails };
        }
    } catch (e) {
        console.warn('Live fetch failed, using fallback/cache:', e.message);
    }
    return null;
}

function renderFeaturedGame(game) {
    const el = document.getElementById('featuredGame');
    if (!el || !game) return;
    const bgDiv = el.querySelector('.featured-bg');
    if (game.thumbnail) {
        bgDiv.style.backgroundImage = `url(${game.thumbnail})`;
        bgDiv.style.opacity = '1';
    }
    el.querySelector('.featured-title').textContent = game.name;
    el.querySelector('.featured-role').textContent = `${game.role} • ${formatNumber(game.visits)} visits • ${formatNumber(game.playing)} playing`;
    el.onclick = () => window.open(game.url, '_blank');
}

function renderGames(games) {
    const grid = document.getElementById('gamesGrid');
    if (!grid) return;
    grid.innerHTML = games.map(game => `
        <a href="${game.url}" target="_blank" class="game-card">
            <div class="game-thumb-wrap">
                <img class="game-thumb" src="${game.thumbnail || ''}" alt="${game.name}"
                     onerror="this.onerror=null;this.src='https://www.roblox.com/asset-thumbnail/image?assetId='+this.closest('a').href.split('/').pop()+'&width=768&height=432&format=png'">
            </div>
            <div class="game-info">
                <div class="game-name">${game.name}</div>
                <div class="game-creator">by ${game.creator}</div>
                <div class="game-meta">
                    <div class="game-stats">
                        <span class="game-stat">
                            <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M1 12s4-8 11-8 11 8 11 8-4 8-11 8-11-8-11-8z"/><circle cx="12" cy="12" r="3"/></svg>
                            ${formatNumber(game.visits)}
                        </span>
                        <span class="game-stat">
                            <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M20 21v-2a4 4 0 0 0-4-4H8a4 4 0 0 0-4 4v2"/><circle cx="12" cy="7" r="4"/></svg>
                            ${formatNumber(game.playing)}
                        </span>
                    </div>
                    <span class="game-role-tag">${game.role}</span>
                </div>
            </div>
        </a>
    `).join('');
}

// Reviews are hidden from the UI — config data above is preserved for future use
function renderReviews() {}

function initMobileMenu() {
    const btn  = document.querySelector('.mobile-menu-btn');
    const menu = document.querySelector('.mobile-menu');
    btn?.addEventListener('click', () => {
        btn.classList.toggle('active');
        menu.classList.toggle('active');
    });
    menu?.querySelectorAll('a').forEach(a => {
        a.addEventListener('click', () => {
            btn.classList.remove('active');
            menu.classList.remove('active');
        });
    });
}

function updateUI(games, allThumbnails) {
    if (!games) return;
    Log.info('Updating UI with games data');

    const grid = document.getElementById('gamesGrid');
    if (grid) grid.classList.add('loaded');

    games.sort((a, b) => b.playing - a.playing);
    renderGames(games);

    const featuredGame = games.find(g => {
        const config = CONFIG.games.find(c => c.placeId === g.url.split('/').pop());
        return config && config.featured;
    }) || [...games].sort((a, b) => b.visits - a.visits)[0];
    renderFeaturedGame(featuredGame);

    const totalVisits = games.reduce((sum, g) => sum + g.visits, 0);
    const heroVisitsEl = document.getElementById('heroVisits');
    if (heroVisitsEl) animateCounter(heroVisitsEl, totalVisits, 2000);

    const thumbs = allThumbnails || games.map(g => g.thumbnail).filter(Boolean);
    if (thumbs.length && !document.querySelector('.mosaic-row')) buildMosaic(thumbs);
}

async function init() {
    try {
        if (window.location.search.includes('debug')) CONFIG.debug = true;
        Log.info('Initializing portfolio...');

        initMobileMenu();

        setTimeout(() => {
            document.querySelectorAll('.skeleton').forEach(el => el.classList.remove('skeleton'));
        }, 5000);

        let initialGames = FALLBACK_GAMES;
        let initialThumbs = null;
        const cacheKey = `roblox_cache_${CONFIG.games.length}_v2`;

        try {
            const cached = localStorage.getItem(cacheKey);
            if (cached) {
                const parsed = JSON.parse(cached);
                if (Array.isArray(parsed.data)) initialGames = parsed.data;
                if (Array.isArray(parsed.allThumbnails)) initialThumbs = parsed.allThumbnails;
            }
        } catch (e) { Log.warn('Cache read failed'); }

        updateUI(initialGames, initialThumbs);

        Log.info('Starting background validation...');
        const liveResult = await fetchGames();
        if (liveResult) {
            Log.info('Updating UI with live data');
            updateUI(liveResult.games, liveResult.allThumbnails);
        }
    } catch (e) {
        Log.error(`Critical Init Error: ${e.message}`);
        updateUI(FALLBACK_GAMES);
    }
}

function buildMosaic(thumbnails) {
    const container = document.getElementById('thumbnailMosaic');
    if (!container || !thumbnails.length) return;

    container.innerHTML = '';
    const inner = document.createElement('div');
    inner.className = 'mosaic-inner';

    const rowCount = 6;
    const speeds = [180, 140, 200, 160, 190, 150];

    Promise.all(thumbnails.map(url => new Promise(resolve => {
        const img = new Image();
        img.onload = () => resolve(url);
        img.onerror = () => resolve(null);
        img.src = url;
    }))).then(loaded => {
        const valid = loaded.filter(Boolean);
        if (!valid.length) return;

        for (let i = 0; i < rowCount; i++) {
            const row = document.createElement('div');
            row.className = 'mosaic-row';
            row.style.setProperty('--speed', speeds[i] + 's');

            const shuffled = [...valid].sort(() => Math.random() - 0.5);
            [...shuffled, ...shuffled].forEach(url => {
                const img = document.createElement('img');
                img.src = url; img.alt = '';
                row.appendChild(img);
            });

            inner.appendChild(row);
        }

        container.appendChild(inner);
    });
}

document.addEventListener('DOMContentLoaded', init);
    </script>
</body>
</html>
