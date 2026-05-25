<!DOCTYPE html>
<html lang="en" class="dark">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Jamie_creates - Professional Game Producer, Game Designer, Project Manager, and Quality Assurance Lead.">
    
    <title>Jamie_creates | Professional Game Producer</title>
    
    <link rel="icon" href="data:image/svg+xml,<svg xmlns=%22http://www.w3.org/2000/svg%22 viewBox=%220 0 100 100%22><text y=%22.9em%22 font-size=%2290%22>🎮</text></svg>">
    
    <script src="https://cdn.tailwindcss.com"></script>
    <script>
        tailwind.config = {
            darkMode: 'class',
            theme: { 
                extend: { 
                    fontFamily: { sans: ['Inter', 'sans-serif'] },
                    colors: {
                        brand: {
                            red: '#ef4444',
                            dark: '#0a0a0f',
                            card: '#12121a'
                        }
                    }
                } 
            }
        }
    </script>
    
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;800;900&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">

    <style>
        body { transition: background-color 0.3s ease, color 0.3s ease; scroll-behavior: smooth; overflow-x: hidden; }
        .nav-link { cursor: pointer; transition: 0.3s; padding-bottom: 4px; }
        .nav-link:hover, .nav-link.active { color: #ef4444; border-bottom: 2px solid #ef4444; }
        .page-section { display: none; animation: fadeIn 0.4s ease-in-out; }
        .page-section.active { display: block; }
        .glass-card { transition: all 0.3s ease; }
        .glass-card:hover { transform: translateY(-5px); }
        
        .glow-red { text-shadow: 0 0 12px rgba(239, 68, 68, 0.8), 0 0 25px rgba(239, 68, 68, 0.4); }

        details > summary { list-style: none; }
        details > summary::-webkit-details-marker { display: none; }

        @keyframes fadeIn { from { opacity: 0; transform: translateY(10px); } to { opacity: 1; transform: translateY(0); } }
        
        /* Animated Hero Background */
        @keyframes gradientMove {
            0% { background-position: 0% 50%; }
            50% { background-position: 100% 50%; }
            100% { background-position: 0% 50%; }
        }
        .hero-bg {
            background: linear-gradient(-45deg, #0a0a0f, #450a0a, #0a0a0f, #171717);
            background-size: 400% 400%;
            animation: gradientMove 15s ease infinite;
        }

        /* Developer Grid Background */
        .bg-grid-pattern {
            background-image: linear-gradient(to right, rgba(239, 68, 68, 0.05) 1px, transparent 1px),
                              linear-gradient(to bottom, rgba(239, 68, 68, 0.05) 1px, transparent 1px);
            background-size: 40px 40px;
        }

        /* Premium Custom Scrollbar */
        ::-webkit-scrollbar { width: 10px; }
        ::-webkit-scrollbar-track { background: #0a0a0f; }
        ::-webkit-scrollbar-thumb { background: #ef4444; border-radius: 5px; }
        ::-webkit-scrollbar-thumb:hover { background: #dc2626; }
    </style>
</head>
<body class="bg-slate-50 text-slate-800 dark:bg-[#0a0a0f] dark:text-slate-100 antialiased font-sans relative">

    <div class="fixed bottom-6 right-6 z-50 flex flex-col gap-3">
        <button onclick="window.scrollTo({top: 0, behavior: 'smooth'})" class="bg-slate-800 dark:bg-slate-800 hover:bg-slate-700 text-white p-3 rounded-full shadow-lg hover:scale-110 transition-transform flex items-center justify-center opacity-70 hover:opacity-100">
            <i class="fa-solid fa-chevron-up"></i>
        </button>
        <button onclick="showPage('contact')" class="bg-red-600 hover:bg-red-500 text-white p-4 rounded-full shadow-lg shadow-red-500/40 hover:scale-110 transition-transform flex items-center justify-center group relative">
            <i class="fa-solid fa-envelope text-xl group-hover:-translate-y-1 transition-transform"></i>
        </button>
    </div>

    <nav class="bg-white/90 dark:bg-[#0a0a0f]/90 backdrop-blur-md border-b border-slate-200 dark:border-slate-800 sticky top-0 z-50 transition-colors">
        <div class="max-w-6xl mx-auto px-6 py-4 flex flex-col md:flex-row justify-between items-center gap-4 md:gap-0">
            <div class="flex items-center gap-4">
                <div class="text-2xl font-extrabold tracking-widest text-slate-900 dark:text-white cursor-pointer select-none">
                    Jamie_creates <span class="text-red-500 font-light">| DEVELOPER</span>
                </div>
            </div>
            
            <div class="flex flex-wrap justify-center gap-4 md:gap-6 font-semibold text-sm md:text-base text-slate-600 dark:text-slate-300">
                <a onclick="showPage('home')" class="nav-link active" id="nav-home">Home</a>
                <a onclick="showPage('portfolio')" class="nav-link" id="nav-portfolio">Portfolio</a>
                <a onclick="showPage('pricing')" class="nav-link" id="nav-pricing">Project Management</a>
                <a onclick="showPage('contact')" class="nav-link" id="nav-contact">Contact</a>
            </div>
        </div>
    </nav>

    <main id="home" class="page-section active">
        <div class="hero-bg py-32 px-6 text-center text-white border-b border-slate-800 shadow-2xl relative overflow-hidden">
            <div class="max-w-6xl mx-auto relative z-10">
                <span class="bg-red-500/20 text-red-300 border border-red-400/30 text-sm font-bold px-4 py-1.5 rounded-full uppercase tracking-wider mb-6 inline-block backdrop-blur-sm">Available for Roblox Commissions</span>
                
                <h1 class="text-5xl md:text-7xl font-extrabold mb-6 drop-shadow-lg">Hi, I'm Jamie.</h1>
                <h2 class="text-xl md:text-2xl text-red-400 mb-8 font-bold tracking-wide drop-shadow-md uppercase">Game Producer, Game Designer, Project manager & QA</h2>
                
                <p class="text-lg text-slate-300 max-w-3xl mx-auto leading-relaxed mb-10 drop-shadow-md">
                    I’m an experienced, professional, and passionate Game Producer, Game Designer, Project Manager, and QA specialist focused on creating high-quality Roblox games. I specialize in leading large-scale projects and teams, and I’m currently leading <strong>RoJam 2026</strong>.
                </p>

                <div class="flex justify-center gap-4 flex-wrap mb-12">
                    <button onclick="showPage('portfolio')" class="bg-red-600 hover:bg-red-500 text-white px-8 py-3 rounded-full font-bold transition shadow-lg shadow-red-500/30">See My Games</button>
                    <a href="https://discord.com/users/1100530188896448603" target="_blank" class="bg-[#5865F2] hover:bg-[#4752C4] text-white px-8 py-3 rounded-full font-bold transition shadow-lg shadow-[#5865F2]/30 flex items-center">
                        <i class="fa-brands fa-discord mr-2 text-xl"></i> Discord
                    </a>
                </div>
            </div>
        </div>

        <div class="max-w-6xl mx-auto px-6 py-20 text-left">
            <div class="bg-white dark:bg-slate-800 p-8 rounded-2xl text-center border border-slate-200 dark:border-slate-700 shadow-md mb-20">
                <h4 class="text-sm font-bold text-slate-500 dark:text-slate-400 uppercase tracking-widest mb-6">Skills</h4>
                <div class="flex flex-wrap justify-center gap-6 md:gap-8 text-slate-800 dark:text-white font-black text-sm md:text-lg">
                    <div class="flex items-center"><i class="fa-solid fa-clipboard-check text-blue-500 mr-2"></i> Game Production</div>
                    <div class="flex items-center"><i class="fa-solid fa-pen-ruler text-purple-500 mr-2"></i> Game Design</div>
                    <div class="flex items-center"><i class="fa-solid fa-list-check text-green-500 mr-2"></i> Project Management</div>
                    <div class="flex items-center"><i class="fa-solid fa-bug-slash text-orange-500 mr-2"></i> Quality Assurance</div>
                    <div class="flex items-center"><i class="fa-solid fa-users text-red-500 mr-2"></i> Team Leadership</div>
                    <div class="flex items-center"><i class="fa-solid fa-magnifying-glass-chart text-cyan-500 mr-2"></i> Acquisition Scouting</div>
                </div>
            </div>

            <h3 class="text-3xl font-bold mb-10 text-center text-slate-900 dark:text-white border-b border-slate-200 dark:border-slate-800 pb-4">My Core Expertise</h3>
            <div class="grid md:grid-cols-3 gap-8 mb-10">
                <div class="bg-white dark:bg-slate-800 p-8 rounded-2xl border border-slate-200 dark:border-slate-700 shadow-lg glass-card">
                    <i class="fa-solid fa-clipboard-check text-4xl text-blue-500 mb-4"></i>
                    <h4 class="text-xl font-bold mb-3 text-slate-900 dark:text-white">Game Production</h4>
                    <p class="text-slate-600 dark:text-slate-400">Overseeing complete project lifecycles, coordinating multi-disciplinary teams, and ensuring developmental milestones are met efficiently.</p>
                </div>
                <div class="bg-white dark:bg-slate-800 p-8 rounded-2xl border border-slate-200 dark:border-slate-700 shadow-lg glass-card">
                    <i class="fa-solid fa-shield-halved text-4xl text-orange-500 mb-4"></i>
                    <h4 class="text-xl font-bold mb-3 text-slate-900 dark:text-white">Quality Assurance</h4>
                    <p class="text-slate-600 dark:text-slate-400">Rigorous playtesting, bug tracking, and edge-case identification to guarantee a flawless, lag-free user experience.</p>
                </div>
                <div class="bg-white dark:bg-slate-800 p-8 rounded-2xl border border-slate-200 dark:border-slate-700 shadow-lg glass-card">
                    <i class="fa-solid fa-magnifying-glass-chart text-4xl text-green-500 mb-4"></i>
                    <h4 class="text-xl font-bold mb-3 text-slate-900 dark:text-white">Acquisition Scouting</h4>
                    <p class="text-slate-600 dark:text-slate-400">Finding upcoming games, contacting game owners and helping people invest into high-potential projects.</p>
                </div>
            </div>
        </div>
    </main>

    <main id="portfolio" class="page-section bg-grid-pattern min-h-screen">
        <div class="max-w-6xl mx-auto px-6 py-20">
            <div class="text-center mb-16">
                <h2 class="text-4xl md:text-5xl font-black mb-4 text-slate-900 dark:text-white uppercase tracking-tight">Managed Projects</h2>
                <p class="text-slate-600 dark:text-slate-400 text-lg">Live updating statistics from my top managed projects and contributions.</p>
            </div>

            <div class="mb-12">
                <a href="https://simplebricks.com.au/" target="_blank" class="block bg-brand-card border border-red-500/30 hover:border-red-500 rounded-3xl p-8 md:p-12 transition-all duration-300 shadow-2xl hover:shadow-red-500/20 group relative overflow-hidden">
                    <div class="absolute top-0 right-0 w-64 h-64 bg-red-500/10 rounded-full blur-3xl group-hover:bg-red-500/20 transition-colors"></div>
                    
                    <div class="relative z-10 flex flex-col md:flex-row items-center justify-between gap-10">
                        <div class="flex-1 text-center md:text-left">
                            <div class="inline-flex items-center justify-center w-16 h-16 rounded-2xl bg-red-500/20 text-red-500 text-3xl mb-6">
                                <span class="font-black tracking-tighter">SB</span>
                            </div>
                            <h3 class="text-4xl font-black text-white mb-2">SimpleBricks</h3>
                            <p class="text-red-400 font-bold uppercase tracking-widest text-sm mb-6">Quality Assurance & Acquisition Scout</p>
                            <p class="text-slate-400 text-lg"> Quality assurance and scouting top acquisitions for the premier Oceania-based studio.</p>
                        </div>

                        <div class="flex-1 w-full bg-black/40 rounded-2xl p-8 border border-white/5">
                            <div class="flex flex-col gap-8 text-center">
                                <div>
                                    <i class="fa-solid fa-gamepad text-red-500 text-3xl mb-3"></i>
                                    <div class="text-4xl font-black text-white mb-1"><span class="counter" data-target="289080608">0</span>+</div>
                                    <div class="text-xs text-slate-500 uppercase tracking-widest font-bold">Total Visits</div>
                                </div>
                                <div class="w-full h-px bg-white/10"></div>
                                <div>
                                    <i class="fa-solid fa-users text-red-500 text-3xl mb-3"></i>
                                    <div class="text-4xl font-black text-white mb-1"><span class="counter" data-target="13406439">0</span>+</div>
                                    <div class="text-xs text-slate-500 uppercase tracking-widest font-bold">Members</div>
                                </div>
                            </div>
                        </div>
                    </div>
                </a>
            </div>

            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6">
                
                <a href="https://www.roblox.com/games/108564524217399/Dig-A-Lucky-Block-For-Brainrots" target="_blank" class="bg-[#12121a] border border-slate-800 hover:border-red-500/50 rounded-2xl p-4 flex flex-col transition-all duration-300 hover:-translate-y-2 group">
                    <div class="relative w-full aspect-video rounded-xl overflow-hidden mb-5 bg-slate-800">
                        <img src="https://placehold.co/600x337/1e1e2e/ef4444?text=Dig+A+Lucky+Block" class="w-full h-full object-cover group-hover:scale-105 transition-transform duration-500" alt="Game Thumbnail">
                        <span class="absolute top-2 right-2 bg-black/80 text-white text-[10px] font-bold px-2 py-1 rounded border border-white/10 shadow-lg backdrop-blur-md">Project Producer</span>
                    </div>
                    <h3 class="text-lg font-bold text-white mb-4 text-center">Dig A Lucky Block For Brainrots</h3>
                    <div class="flex justify-between items-center mt-auto bg-black/40 rounded-lg p-3 border border-white/5">
                        <div class="text-center w-full">
                            <i class="fa-solid fa-play text-slate-500 text-sm mb-1"></i>
                            <div class="text-lg font-black text-white"><span class="counter" id="visits-dlb" data-target="1k">0</span>+</div>
                            <div class="text-[9px] text-slate-500 uppercase tracking-widest font-bold">Visits</div>
                        </div>
                        <div class="w-px h-8 bg-white/10 mx-2"></div>
                        <div class="text-center w-full">
                            <i class="fa-solid fa-user-group text-slate-500 text-sm mb-1"></i>
                            <div class="text-lg font-black text-white"><span class="counter" id="playing-dlb" data-target="120">0</span></div>
                            <div class="text-[9px] text-slate-500 uppercase tracking-widest font-bold">Active</div>
                        </div>
                    </div>
                </a>

                <a href="https://www.roblox.com/games/98138235237704/Hide-the-Friend" target="_blank" class="bg-[#12121a] border border-slate-800 hover:border-red-500/50 rounded-2xl p-4 flex flex-col transition-all duration-300 hover:-translate-y-2 group">
                    <div class="relative w-full aspect-video rounded-xl overflow-hidden mb-5 bg-slate-800">
                        <img src="https://placehold.co/600x337/1e1e2e/ef4444?text=Hide+the+Friend" class="w-full h-full object-cover group-hover:scale-105 transition-transform duration-500" alt="Game Thumbnail">
                        <span class="absolute top-2 right-2 bg-black/80 text-white text-[10px] font-bold px-2 py-1 rounded border border-white/10 shadow-lg backdrop-blur-md">Lead QA</span>
                    </div>
                    <h3 class="text-lg font-bold text-white mb-4 text-center">Hide the Friend</h3>
                    <div class="flex justify-between items-center mt-auto bg-black/40 rounded-lg p-3 border border-white/5">
                        <div class="text-center w-full">
                            <i class="fa-solid fa-play text-slate-500 text-sm mb-1"></i>
                            <div class="text-lg font-black text-white"><span class="counter" id="visits-htf" data-target="25000000">0</span>+</div>
                            <div class="text-[9px] text-slate-500 uppercase tracking-widest font-bold">Visits</div>
                        </div>
                        <div class="w-px h-8 bg-white/10 mx-2"></div>
                        <div class="text-center w-full">
                            <i class="fa-solid fa-user-group text-slate-500 text-sm mb-1"></i>
                            <div class="text-lg font-black text-white"><span class="counter" id="playing-htf" data-target="5400">0</span></div>
                            <div class="text-[9px] text-slate-500 uppercase tracking-widest font-bold">Active</div>
                        </div>
                    </div>
                </a>

                <a href="https://www.roblox.com/games/81525595245099/Build-a-Golem-Army" target="_blank" class="bg-[#12121a] border border-slate-800 hover:border-red-500/50 rounded-2xl p-4 flex flex-col transition-all duration-300 hover:-translate-y-2 group">
                    <div class="relative w-full aspect-video rounded-xl overflow-hidden mb-5 bg-slate-800">
                        <img src="https://placehold.co/600x337/1e1e2e/ef4444?text=Build+a+Golem+Army" class="w-full h-full object-cover group-hover:scale-105 transition-transform duration-500" alt="Game Thumbnail">
                        <span class="absolute top-2 right-2 bg-black/80 text-white text-[10px] font-bold px-2 py-1 rounded border border-white/10 shadow-lg backdrop-blur-md">QA</span>
                    </div>
                    <h3 class="text-lg font-bold text-white mb-4 text-center">Build a Golem Army</h3>
                    <div class="flex justify-between items-center mt-auto bg-black/40 rounded-lg p-3 border border-white/5">
                        <div class="text-center w-full">
                            <i class="fa-solid fa-play text-slate-500 text-sm mb-1"></i>
                            <div class="text-lg font-black text-white"><span class="counter" id="visits-golem" data-target="10500000">0</span>+</div>
                            <div class="text-[9px] text-slate-500 uppercase tracking-widest font-bold">Visits</div>
                        </div>
                        <div class="w-px h-8 bg-white/10 mx-2"></div>
                        <div class="text-center w-full">
                            <i class="fa-solid fa-user-group text-slate-500 text-sm mb-1"></i>
                            <div class="text-lg font-black text-white"><span class="counter" id="playing-golem" data-target="1200">0</span></div>
                            <div class="text-[9px] text-slate-500 uppercase tracking-widest font-bold">Active</div>
                        </div>
                    </div>
                </a>

                <a href="https://www.roblox.com/games/135690330157046/Word-Hunt-Battles" target="_blank" class="bg-[#12121a] border border-slate-800 hover:border-red-500/50 rounded-2xl p-4 flex flex-col transition-all duration-300 hover:-translate-y-2 group">
                    <div class="relative w-full aspect-video rounded-xl overflow-hidden mb-5 bg-slate-800">
                        <img src="https://placehold.co/600x337/1e1e2e/ef4444?text=Word+Hunt+Battles" class="w-full h-full object-cover group-hover:scale-105 transition-transform duration-500" alt="Game Thumbnail">
                        <span class="absolute top-2 right-2 bg-black/80 text-white text-[10px] font-bold px-2 py-1 rounded border border-white/10 shadow-lg backdrop-blur-md">Contributor</span>
                    </div>
                    <h3 class="text-lg font-bold text-white mb-4 text-center">Word Hunt Battles</h3>
                    <div class="flex justify-between items-center mt-auto bg-black/40 rounded-lg p-3 border border-white/5">
                        <div class="text-center w-full">
                            <i class="fa-solid fa-play text-slate-500 text-sm mb-1"></i>
                            <div class="text-lg font-black text-white"><span class="counter" id="visits-whb" data-target="1400000">0</span>+</div>
                            <div class="text-[9px] text-slate-500 uppercase tracking-widest font-bold">Visits</div>
                        </div>
                        <div class="w-px h-8 bg-white/10 mx-2"></div>
                        <div class="text-center w-full">
                            <i class="fa-solid fa-user-group text-slate-500 text-sm mb-1"></i>
                            <div class="text-lg font-black text-white"><span class="counter" id="playing-whb" data-target="361">0</span></div>
                            <div class="text-[9px] text-slate-500 uppercase tracking-widest font-bold">Active</div>
                        </div>
                    </div>
                </a>

            </div>

            <div class="mt-16">
                <h3 class="text-3xl font-bold mb-8 text-center text-slate-900 dark:text-white border-b border-slate-200 dark:border-slate-800 pb-4">Teams & Studios</h3>
                <div class="flex flex-col items-center gap-4">
                    <div class="w-full max-w-2xl bg-white dark:bg-slate-800 p-6 rounded-2xl border border-slate-200 dark:border-slate-700 shadow-lg flex items-center gap-4">
                        <i class="fa-solid fa-briefcase text-2xl text-yellow-500 w-8 text-center"></i>
                        <span class="text-slate-900 dark:text-white font-bold text-lg">Team Leader & Game Producer @ RoJam 2026</span>
                    </div>
                    <div class="w-full max-w-2xl bg-white dark:bg-slate-800 p-6 rounded-2xl border border-slate-200 dark:border-slate-700 shadow-lg flex items-center gap-4">
                        <i class="fa-solid fa-magnifying-glass text-2xl text-blue-400 w-8 text-center"></i>
                        <span class="text-slate-900 dark:text-white font-bold text-lg">QA & Acquisition Scout @ SimpleBricks</span>
                    </div>
                </div>
            </div>

            <div class="mt-16">
                <h3 class="text-3xl font-bold mb-8 text-center text-slate-900 dark:text-white border-t border-slate-200 dark:border-slate-800 pt-16">Client Vouches</h3>
                <div class="grid md:grid-cols-2 gap-6 max-w-4xl mx-auto">
                    <div class="bg-slate-100 dark:bg-slate-800/50 p-6 rounded-xl border-l-4 border-blue-500 italic text-slate-700 dark:text-slate-300 relative">
                        <i class="fa-solid fa-quote-right absolute top-4 right-4 text-3xl opacity-10 text-blue-500"></i>
                        "Jamie is an incredibly dedicated producer. The QA process was exactly what we needed, perfectly organized, and helped us launch flawlessly. Highly recommended."
                        <div class="font-bold text-slate-900 dark:text-white mt-4 not-italic text-sm">— Major Studio Owner</div>
                    </div>
                    
                    <div class="bg-slate-100 dark:bg-slate-800/50 p-6 rounded-xl border-l-4 border-purple-500 italic text-slate-700 dark:text-slate-300 relative">
                        <i class="fa-solid fa-quote-right absolute top-4 right-4 text-3xl opacity-10 text-purple-500"></i>
                        "Not only is the bug testing top-tier, but the communication was excellent. It's hard to find reliable managers, but Jamie is definitely one of them. Will be hiring again!"
                        <div class="font-bold text-slate-900 dark:text-white mt-4 not-italic text-sm">— Past Commissioner</div>
                    </div>
                </div>
            </div>
        </div>
    </main>

    <main id="pricing" class="page-section bg-grid-pattern relative">
        <div class="max-w-6xl mx-auto px-6 py-20 relative z-10">
            <h2 class="text-4xl font-bold mb-12 text-center text-slate-900 dark:text-white bg-white/80 dark:bg-slate-900/80 backdrop-blur-sm inline-block px-8 py-2 rounded-full border border-slate-200 dark:border-slate-800 mx-auto block w-max">Project Management</h2>
            
            <h3 class="text-2xl font-bold mb-8 text-center text-slate-900 dark:text-white">Services & Rates</h3>
            <div class="grid md:grid-cols-2 gap-8 mb-16">
                <div class="bg-slate-900 p-8 rounded-xl border border-slate-700 shadow-lg relative overflow-hidden">
                    <div class="absolute top-0 right-0 p-4 opacity-10 text-6xl"><i class="fa-solid fa-list-check"></i></div>
                    <h3 class="text-2xl font-bold mb-6 text-white relative z-10"><i class="fa-solid fa-list-check mr-2"></i> Project Management</h3>
                    <div class="space-y-4 text-slate-300 font-medium relative z-10">
                        <div class="flex justify-between border-b border-slate-700/50 pb-2"><span>Agile/Scrum Setup</span><span class="font-bold text-blue-500">Contact me for pricing</span></div>
                        <div class="flex justify-between border-b border-slate-700/50 pb-2"><span>Team Coordination (Weekly)</span><span class="font-bold text-blue-500">Contact me for pricing</span></div>
                        <div class="flex justify-between border-b border-slate-700/50 pb-2"><span>Workflow Optimization</span><span class="font-bold text-blue-500">Contact me for pricing</span></div>
                        <div class="flex justify-between"><span>Full Game Lifecycle</span><span class="font-bold text-blue-500">Custom Quote</span></div>
                    </div>
                </div>

                <div class="bg-slate-900 p-8 rounded-xl border border-slate-700 shadow-lg relative overflow-hidden">
                    <div class="absolute top-0 right-0 p-4 opacity-10 text-6xl"><i class="fa-solid fa-bug-slash"></i></div>
                    <h3 class="text-2xl font-bold mb-6 text-white relative z-10"><i class="fa-solid fa-bug-slash mr-2"></i> Quality Assurance</h3>
                    <div class="space-y-4 text-slate-300 font-medium relative z-10">
                        <div class="flex justify-between border-b border-slate-700/50 pb-2"><span>Basic Playtesting</span><span class="font-bold text-orange-500">Contact me for pricing</span></div>
                        <div class="flex justify-between border-b border-slate-700/50 pb-2"><span>Full Bug Report</span><span class="font-bold text-orange-500">Contact me for pricing</span></div>
                        <div class="flex justify-between border-b border-slate-700/50 pb-2"><span>Mechanics Stress Test</span><span class="font-bold text-orange-500">Contact me for pricing</span></div>
                        <div class="flex justify-between"><span>Continuous QA Support</span><span class="font-bold text-orange-500">Custom Quote</span></div>
                    </div>
                </div>
            </div>

            <div class="space-y-4 max-w-4xl mx-auto mb-16">
                <details class="bg-red-50/90 dark:bg-red-900/20 backdrop-blur-md rounded-xl shadow-md border border-red-200 dark:border-red-900/50 group cursor-pointer" open>
                    <summary class="p-6 font-bold text-xl text-red-600 dark:text-red-400 flex justify-between items-center outline-none">
                        <span><i class="fa-solid fa-scroll mr-2"></i> Terms of Service (ToS)</span>
                        <i class="fa-solid fa-chevron-down transition-transform group-open:rotate-180 text-red-400"></i>
                    </summary>
                    <div class="p-6 pt-0 border-t border-red-200 dark:border-red-900/50">
                        <ul class="list-disc pl-5 mt-4 space-y-2 text-sm text-slate-700 dark:text-slate-300">
                            <li><strong>I work by contract.</strong> Formal agreements are required before initiation of large-scale management or QA services.</li>
                            <li>I reserve the right to decline any commission if I feel it does not fit my schedule.</li>
                            <li><strong>No refunds</strong> will be issued after the service period has officially begun.</li>
                            <li>Platform fees or currency exchange fees must be covered by the client.</li>
                            <li>Estimated deadlines are approximations; quality takes time. I will communicate any delays.</li>
                        </ul>
                    </div>
                </details>
            </div>
        </div>
    </main>

    <main id="contact" class="page-section max-w-4xl mx-auto px-6 py-20 text-center">
        <h2 class="text-4xl font-bold mb-6 text-slate-900 dark:text-white">Let's Work Together</h2>
        
        <div class="bg-slate-200 dark:bg-slate-800 inline-block px-6 py-3 rounded-full mb-10 border border-slate-300 dark:border-slate-700 shadow-sm">
            <i class="fa-regular fa-clock text-red-500 mr-2 animate-pulse"></i> 
            <span class="text-slate-600 dark:text-slate-300 font-bold">My Local Time (CET): <span id="local-time" class="text-slate-900 dark:text-white">Loading...</span></span>
        </div>
        
        <div class="max-w-2xl mx-auto flex flex-col gap-6">
            
            <a href="https://www.roblox.com/share?code=d0f7afb99a958a48b7874a51df8a9656&type=Profile&source=ProfileShare&stamp=1778661904863" target="_blank" class="w-full bg-slate-900 border border-slate-700 hover:border-slate-500 hover:-translate-y-1 transition-all duration-300 rounded-2xl p-6 flex items-center shadow-lg group">
                <div class="w-14 h-14 bg-white rounded-xl flex items-center justify-center mr-6 group-hover:scale-110 transition-transform">
                    <img src="https://upload.wikimedia.org/wikipedia/commons/3/3a/Roblox_player_icon_black.svg" class="w-8 h-8" alt="Roblox">
                </div>
                <div class="text-left">
                    <div class="text-white font-bold text-xl mb-1">Roblox Profile</div>
                    <div class="text-slate-400 text-sm">View my official developer profile on the platform.</div>
                </div>
                <i class="fa-solid fa-arrow-up-right-from-square ml-auto text-slate-600 group-hover:text-white transition-colors"></i>
            </a>

            <a href="https://discord.com/users/1100530188896448603" target="_blank" class="w-full bg-[#5865F2]/10 border border-[#5865F2]/30 hover:border-[#5865F2] hover:-translate-y-1 transition-all duration-300 rounded-2xl p-6 flex items-center shadow-lg group">
                <div class="w-14 h-14 bg-[#5865F2] text-white rounded-xl flex items-center justify-center mr-6 group-hover:scale-110 transition-transform text-3xl">
                    <i class="fa-brands fa-discord"></i>
                </div>
                <div class="text-left">
                    <div class="text-white font-bold text-xl mb-1">DM @Jamie</div>
                    <div class="text-[#5865F2] text-sm font-semibold">Discord ID 1100530188896448603</div>
                </div>
                <i class="fa-solid fa-arrow-up-right-from-square ml-auto text-slate-600 group-hover:text-white transition-colors"></i>
            </a>

        </div>
    </main>

    <footer class="text-center py-8 border-t border-slate-200 dark:border-slate-800 text-slate-500 dark:text-slate-400 bg-white dark:bg-[#0a0a0f] mt-20 transition-colors pb-24 md:pb-8">
        <p>&copy; 2026 Jamie_creates | DEVELOPER.</p>
    </footer>

    <script>
        // Page Navigation
        function showPage(pageId) {
            document.querySelectorAll('.page-section').forEach(page => page.classList.remove('active'));
            document.querySelectorAll('.nav-link').forEach(link => link.classList.remove('active'));
            document.getElementById(pageId).classList.add('active');
            
            let navLink = document.getElementById('nav-' + pageId);
            if(navLink) navLink.classList.add('active');
            
            window.scrollTo({ top: 0, behavior: 'smooth' });
        }

        // Local Time Clock (CET)
        function updateClock() {
            const timeElement = document.getElementById('local-time');
            if(timeElement) {
                const now = new Date();
                timeElement.innerText = now.toLocaleTimeString('en-GB', { timeZone: 'Europe/Berlin', hour: '2-digit', minute: '2-digit', hour12: true });
            }
        }
        setInterval(updateClock, 1000);
        updateClock();

        // ----------------------------------------------------
        // LIVE STATS FETCHING & ANIMATED COUNTER LOGIC
        // ----------------------------------------------------
        
        // Define Universe IDs for the games to fetch live data
        const GAMES = [
            { universeId: "7338561074", visitsEl: "visits-golem", playingEl: "playing-golem" },
            { universeId: "8228371304", visitsEl: "visits-htf", playingEl: "playing-htf" },
            // Add actual Universe IDs here if known for Word Hunt and Dig a Lucky Block
            // { universeId: "XXXXXXXXXX", visitsEl: "visits-whb", playingEl: "playing-whb" },
            // { universeId: "YYYYYYYYYY", visitsEl: "visits-dlb", playingEl: "playing-dlb" },
        ];

        const PROXY = "https://corsproxy.io/?url=";

        async function proxy(url) {
            const res = await fetch(PROXY + encodeURIComponent(url));
            if (!res.ok) throw new Error(res.status);
            return res.json();
        }

        async function loadGameStats() {
            try {
                const ids = GAMES.map(g => g.universeId).filter(Boolean).join(",");
                if(ids) {
                    const data = await proxy(`https://games.roblox.com/v1/games?universeIds=${ids}`);
                    (data.data || []).forEach(stats => {
                        const game = GAMES.find(g => String(g.universeId) === String(stats.id));
                        if (game) {
                            const vEl = document.getElementById(game.visitsEl);
                            const pEl = document.getElementById(game.playingEl);
                            if(vEl) vEl.setAttribute('data-target', stats.visits);
                            if(pEl) pEl.setAttribute('data-target', stats.playing);
                        }
                    });
                }
            } catch(e) {
                console.warn("Failed to fetch live game stats (using fallbacks):", e.message);
            } finally {
                // Run the counter animation regardless of success/fail so numbers tick up
                runCounters();
            }
        }

        // Animated Counters with Comma Formatting
        function formatNumberWithCommas(x) {
            return Math.floor(x).toString().replace(/\B(?=(\d{3})+(?!\d))/g, ",");
        }

        function runCounters() {
            const counters = document.querySelectorAll('.counter');
            counters.forEach(counter => {
                const target = +counter.getAttribute('data-target');
                if (isNaN(target) || target === 0) return;
                
                let count = 0; 
                // Adjust speed divisor based on number size for smooth animation
                const speed = 40; 
                const inc = target / speed;
                
                const updateCount = () => {
                    count += inc;
                    if (count < target) {
                        counter.innerText = formatNumberWithCommas(count);
                        requestAnimationFrame(updateCount);
                    } else {
                        counter.innerText = formatNumberWithCommas(target);
                    }
                };
                counter.innerText = '0'; 
                updateCount();
            });
        }

        document.addEventListener("DOMContentLoaded", () => {
            loadGameStats(); // Fetches data then runs counters
        });

    </script>
</body>
</html>
