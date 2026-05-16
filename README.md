<!DOCTYPE html>
<html lang="en" class="dark">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Jamie - Professional Game Producer, Game Designer, Project Manager & QA.">
    <title>Jamie | Professional Game Producer</title>
    <link rel="icon" href="data:image/svg+xml,<svg xmlns=%22http://www.w3.org/2000/svg%22 viewBox=%220 0 100 100%22><text y=%22.9em%22 font-size=%2290%22>🎮</text></svg>">
    <script src="https://cdn.tailwindcss.com"></script>
    <script>
        tailwind.config = {
            darkMode: 'class',
            theme: { 
                extend: { 
                    fontFamily: { sans: ['Inter', 'sans-serif'] },
                    colors: { brand: { red: '#ef4444', dark: '#0a0a0f', card: '#12121a' } }
                } 
            }
        }
    </script>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;800;900&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
    <style>
        body { background-color: #0a0a0f; color: #f1f5f9; font-family: 'Inter', sans-serif; scroll-behavior: smooth; overflow-x: hidden; }
        .nav-link { cursor: pointer; transition: 0.3s; padding-bottom: 4px; border-bottom: 2px solid transparent; }
        .nav-link:hover, .nav-link.active { color: #ef4444; border-bottom-color: #ef4444; }
        .page-section { display: none; animation: fadeIn 0.4s ease-in-out; }
        .page-section.active { display: block !important; }
        @keyframes fadeIn { from { opacity: 0; transform: translateY(10px); } to { opacity: 1; transform: translateY(0); } }
        .hero-bg { background: linear-gradient(-45deg, #0a0a0f, #450a0a, #0a0a0f, #171717); background-size: 400% 400%; }
        .bg-grid-pattern { background-image: linear-gradient(to right, rgba(239, 68, 68, 0.05) 1px, transparent 1px), linear-gradient(to bottom, rgba(239, 68, 68, 0.05) 1px, transparent 1px); background-size: 40px 40px; }
    </style>
</head>
<body class="antialiased relative">
    <nav class="bg-[#0a0a0f]/90 border-b border-slate-800 sticky top-0 z-50 p-4">
        <div class="max-w-6xl mx-auto flex flex-col md:flex-row justify-between items-center gap-4">
            <div class="text-xl font-extrabold tracking-widest text-white">Jamie <span class="text-red-500 font-light">| DEVELOPER</span></div>
            <div class="flex gap-6 font-semibold text-sm text-slate-300">
                <a onclick="showPage('home')" class="nav-link active" id="nav-home">Home</a>
                <a onclick="showPage('portfolio')" class="nav-link" id="nav-portfolio">Portfolio</a>
                <a onclick="showPage('pricing')" class="nav-link" id="nav-pricing">Services</a>
            </div>
        </div>
    </nav>

    <!-- Home Section -->
    <main id="home" class="page-section active">
        <div class="hero-bg py-24 px-6 text-center border-b border-slate-800">
            <span class="bg-red-500/20 text-red-300 border border-red-400/30 text-xs font-bold px-4 py-1.5 rounded-full uppercase mb-4 inline-block">Available for Commissions</span>
            <h1 class="text-4xl font-extrabold mb-2 text-white">Hi, I'm Jamie.</h1>
            <h2 class="text-lg text-red-400 mb-6 font-light">Game Producer, Project Manager & QA</h2>
            <p class="text-sm text-slate-300 max-w-xl mx-auto leading-relaxed mb-6">I’m an experienced, professional, and passionate Game Producer focused on creating high-quality Roblox games. I specialize in leading large-scale projects and teams, and I’m currently leading RoJam 2026.</p>
            <button onclick="showPage('portfolio')" class="bg-red-600 text-white px-6 py-2.5 rounded-full font-bold">See My Games</button>
        </div>
        
        <div class="max-w-6xl mx-auto px-6 py-10">
            <div class="bg-[#12121a] p-6 rounded-2xl border border-slate-800 text-center">
                <h4 class="text-sm font-black text-red-400 uppercase tracking-widest mb-6">Skills & My Core Expertise</h4>
                <div class="grid grid-cols-2 gap-4 text-left max-w-xs mx-auto text-sm text-slate-200">
                    <div><i class="fa-solid fa-layer-group text-red-500 mr-2"></i> Production</div>
                    <div><i class="fa-solid fa-pen-nib text-blue-500 mr-2"></i> Design</div>
                    <div><i class="fa-solid fa-list-check text-purple-400 mr-2"></i> Management</div>
                    <div><i class="fa-solid fa-bug-slash text-orange-500 mr-2"></i> QA Testing</div>
                </div>
            </div>
        </div>
    </main>

    <!-- Portfolio Section -->
    <main id="portfolio" class="page-section bg-grid-pattern min-h-screen px-6 py-10">
        <h2 class="text-2xl font-black text-center text-white uppercase mb-8">My Work & Experience</h2>
        <div class="space-y-6 max-w-md mx-auto">
            <div class="bg-[#12121a] border border-red-500/30 rounded-2xl p-6">
                <h3 class="text-xl font-black text-white">SimpleBricks</h3>
                <p class="text-red-400 font-bold text-xs uppercase mb-4">Quality Assurance & Scout</p>
                <div class="grid grid-cols-2 gap-2 bg-black/40 p-4 rounded-xl text-center">
                    <div><div class="text-lg font-black text-white">289M+</div><div class="text-[9px] text-slate-500 uppercase font-bold tracking-wider">Visits</div></div>
                    <div><div class="text-lg font-black text-white">13M+</div><div class="text-[9px] text-slate-500 uppercase font-bold tracking-wider">Members</div></div>
                </div>
            </div>
        </div>
    </main>

    <!-- Services Section -->
    <main id="pricing" class="page-section bg-grid-pattern min-h-screen px-6 py-10">
        <h2 class="text-2xl font-bold text-center text-white mb-8">QA Rates</h2>
        <div class="bg-[#12121a] p-6 rounded-xl border border-slate-800 max-w-md mx-auto space-y-4">
            <div class="flex justify-between border-b border-slate-700 pb-2 text-sm"><span>Basic Playtesting</span><span class="font-bold text-orange-400">20 - 50 USD</span></div>
            <div class="flex justify-between border-b border-slate-700 pb-2 text-sm"><span>Full Bug Report</span><span class="font-bold text-orange-400">100 - 200 USD</span></div>
        </div>
        <div class="text-center mt-10">
            <a href="https://discordapp.com/users/1100530188896448603" target="_blank" class="inline-flex items-center bg-[#5865F2] text-white px-6 py-3 rounded-full font-bold text-sm shadow-lg"><i class="fa-brands fa-discord mr-2 text-lg"></i> Contact on Discord</a>
        </div>
    </main>

    <script>
        function showPage(pageId) {
            // Hide all sections cleanly
            document.querySelectorAll('.page-section').forEach(section => {
                section.classList.remove('active');
            });
            // Remove active style from links
            document.querySelectorAll('.nav-link').forEach(link => {
                link.classList.remove('active');
            });
            
            // Activate target section and link
            const targetElement = document.getElementById(pageId);
            if(targetElement) targetElement.classList.add('active');
            
            const targetLink = document.getElementById(`nav-${pageId}`);
            if(targetLink) targetLink.classList.add('active');
            
            window.scrollTo({ top: 0, behavior: 'smooth' });
        }

        // Fresh start enforcement on load/refresh
        window.addEventListener('DOMContentLoaded', () => {
            showPage('home');
        });
    </script>
</body>
</html>
