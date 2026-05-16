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
            <i class="fa-solid fa-paper-plane text-xl group-hover:-translate-y-1 group-hover:translate-x-1 transition-transform"></i>
        </button>
    </div>

    <nav class="bg-white/90 dark:bg-[#0a0a0f]/90 backdrop-blur-md border-b border-slate-200 dark:border-slate-800 sticky top-0 z-50 transition-colors">
        <div class="max-w-6xl mx-auto px-6 py-4 flex flex-col md:flex-row justify-between items-center gap-4 md:gap-0">
            <div class="flex items-center gap-4">
                <div class="text-2xl font-extrabold tracking-widest text-slate-900 dark:text-white cursor-pointer select-none">
                    Jamie <span class="text-red-500 font-light">| DEVELOPER</span>
                </div>
            </div>
            
            <div class="flex flex-wrap justify-center gap-4 md:gap-6 font-semibold text-sm md:text-base text-slate-600 dark:text-slate-300">
                <a onclick="showPage('home')" class="nav-link active" id="nav-home">Home</a>
                <a onclick="showPage('portfolio')" class="nav-link" id="nav-portfolio">Portfolio</a>
                <a onclick="showPage('pricing')" class="nav-link" id="nav-pricing">Services</a>
                <a onclick="showPage('contact')" class="nav-link" id="nav-contact">Contact</a>
            </div>
        </div>
    </nav>

    <main id="home" class="page-section active">
        <div class="hero-bg py-32 px-6 text-center text-white border-b border-slate-800 shadow-2xl relative overflow-hidden">
            <div class="max-w-6xl mx-auto relative z-10">
                <span class="bg-red-500/20 text-red-300 border border-red-400/30 text-sm font-bold px-4 py-1.5 rounded-full uppercase tracking-wider mb-6 inline-block backdrop-blur-sm">Available for Commissions</span>
                
                <h1 class="text-5xl md:text-7xl font-extrabold mb-6 drop-shadow-lg">Hi, I'm Jamie.</h1>
                <h2 class="text-2xl md:text-3xl text-red-400 mb-8 font-light drop-shadow-md">Game Producer, Game Designer, Project Manager & QA</h2>
                
                <p class="text-lg text-slate-300 max-w-3xl mx-auto leading-relaxed mb-10 drop-shadow-md">
                    I’m an experienced, professional, and passionate Game Producer, Game Designer, Project Manager, and QA specialist focused on creating high-quality Roblox games. I specialize in leading large-scale projects and teams, and I’m currently leading RoJam 2026.
                </p>

                <div class="flex justify-center gap-4 flex-wrap mb-12">
                    <button onclick="showPage('portfolio')" class="bg-red-600 hover:bg-red-500 text-white px-8 py-3 rounded-full font-bold transition shadow-lg shadow-red-500/30">See My Games</button>
                    <a href="https://discordapp.com/users/1100530188896448603" target="_blank" class="bg-[#5865F2] hover:bg-[#4752C4] text-white px-8 py-3 rounded-full font-bold transition shadow-lg shadow-[#5865F2]/30 flex items-center">
                        <i class="fa-brands fa-discord mr-2 text-xl"></i> Discord
                    </a>
                </div>
            </div>
        </div>

        <div class="max-w-6xl mx-auto px-6 py-20 text-left">
            <div class="bg-white dark:bg-[#12121a] p-8 rounded-2xl text-center border border-slate-200 dark:border-slate-800 shadow-md mb-20">
                <h4 class="text-sm font-bold text-slate-500 dark:text-slate-400 uppercase tracking-widest mb-6">Skills</h4>
                <div class="flex flex-wrap justify-center gap-8 text-slate-800 dark:text-white font-black text-lg md:text-xl">
                    <div class="flex items-center hover:text-red-500 transition-colors cursor-default"><i class="fa-solid fa-layer-group text-2xl mr-2 text-red-500"></i> Game Production</div>
                    <div class="flex items-center hover:text-blue-500 transition-colors cursor-default"><i class="fa-solid fa-pen-nib text-2xl mr-2 text-blue-500"></i> Game Design</div>
                    <div class="flex items-center hover:text-purple-400 transition-colors cursor-default"><i class="fa-solid fa-list-check text-2xl mr-2 text-purple-400"></i> Project Management</div>
                    <div class="flex items-center hover:text-orange-500 transition-colors cursor-default"><i class="fa-solid fa-bug-slash text-2xl mr-2 text-orange-500"></i> Quality Assurance</div>
                    <div class="flex items-center hover:text-green-500 transition-colors cursor-default"><i class="fa-solid fa-users text-2xl mr-2 text-green-500"></i> Team Leadership</div>
                    <div class="flex items-center hover:text-cyan-400 transition-colors cursor-default"><i class="fa-solid fa-magnifying-glass-chart text-2xl mr-2 text-cyan-400"></i> Acquisition Scouting</div>
                </div>
            </div>

            <h3 class="text-3xl font-bold mb-10 text-center text-slate-900 dark:text-white border-b border-slate-200 dark:border-slate-800 pb-4">My Core Expertise</h3>
            <div class="grid md:grid-cols-3 gap-8 mb-10">
                <div class="bg-white dark:bg-[#12121a] p-8 rounded-2xl border border-slate-200 dark:border-slate-800 shadow-lg glass-card">
                    <i class="fa-solid fa-clipboard-check text-4xl text-blue-500 mb-4"></i>
                    <h4 class="text-xl font-bold mb-3 text-slate-900 dark:text-white">Game Production</h4>
                    <p class="text-slate-600 dark:text-slate-400">Overseeing complete project lifecycles, coordinating multi-disciplinary teams, and ensuring developmental milestones are met efficiently.</p>
                </div>
                <div class="bg-white dark:bg-[#12121a] p-8 rounded-2xl border border-slate-200 dark:border-slate-800 shadow-lg glass-card">
                    <i class="fa-solid fa-shield-halved text-4xl text-orange-500 mb-4"></i>
                    <h4 class="text-xl font-bold mb-3 text-slate-900 dark:text-white">Quality Assurance</h4>
                    <p class="text-slate-600 dark:text-slate-400">Rigorous playtesting, bug tracking, and edge-case identification to guarantee a flawless, lag-free user experience.</p>
                </div>
                <div class="bg-white dark:bg-[#12121a] p-8 rounded-2xl border border-slate-200 dark:border-slate-800 shadow-lg glass-card">
                    <i class="fa-solid fa-magnifying-glass-dollar text-4xl text-green-500 mb-4"></i>
                    <h4 class="text-xl font-bold mb-3 text-slate-900 dark:text-white">Acquisition Scouting</h4>
                    <p class="text-slate-600 dark:text-slate-400">Finding upcoming games, contacting game owners, and helping people invest in highly promising projects on the platform.</p>
                </div>
            </div>
        </div>
    </main>

    <main id="portfolio" class="page-section bg-grid-pattern min-h-screen">
        <div class="max-w-6xl mx-auto px-6 py-20">
            <div class="text-center mb-16">
                <h2 class="text-4xl md:text-5xl font-black mb-4 text-slate-900 dark:text-white uppercase tracking-tight">My Work & Experience</h2>
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
                            <p class="text-slate-400 text-lg">Leading quality assurance and scouting top acquisitions for the premier Oceania-based studio.</p>
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

            <h3 class="text-2xl font-bold mb-8 text-slate-900 dark:text-white border-b border-slate-800 pb-4"><i class="fa-solid fa-folder-open mr-2 text-red-500"></i> Managed Projects</h3>
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6 mb-16">
                
                <a href="https://www.roblox.com/games/108564524217399/Dig-A-Lucky-Block-For-Brainrots" target="_blank" class="bg-brand-card border border-slate-800 hover:border-red-500/50 rounded-2xl overflow-hidden flex flex-col transition-all duration-300 hover:-translate-y-2 shadow-lg">
                    <div class="relative w-full h-44 bg-slate-800">
                        <img src="https://images.unsplash.com/photo-1623934199716-ba29247eb9eb?auto=format&fit=crop&w=600&q=80" alt="Dig A Lucky Block" class="w-full h-full object-cover opacity-80">
                        <div class="absolute top-3 right-3 bg-black/80 backdrop-blur-sm text-white text-[10px] font-bold px-3 py-1 rounded shadow">
                            Project Manager
                        </div>
                    </div>
                    <div class="p-6 flex flex-col flex-1">
                        <h3 class="text-xl font-bold text-white mb-4 text-center">Dig A Lucky Block</h3>
                        <div class="flex justify-between items-center mt-auto bg-black/30 p-3 rounded-lg border border-white/5">
                            <div class="text-center w-1/2 border-r border-slate-700/50">
                                <div class="text-lg font-black text-white"><span class="counter" id="visits-dlb" data-target="154000">0</span>+</div>
                                <div class="text-[9px] text-slate-400 uppercase tracking-widest">Visits</div>
                            </div>
                            <div class="text-center w-1/2">
                                <div class="text-lg font-black text-white"><span class="counter" id="playing-dlb" data-target="120">0</span></div>
                                <div class="text-[9px] text-slate-400 uppercase tracking-widest">Playing</div>
                            </div>
                        </div>
                    </div>
                </a>

                <a href="https://www.roblox.com/games/98138235237704/Hide-the-Friend" target="_blank" class="bg-brand-card border border-slate-800 hover:border-red-500/50 rounded-2xl overflow-hidden flex flex-col transition-all duration-300 hover:-translate-y-2 shadow-lg">
                    <div class="relative w-full h-44 bg-slate-800">
                        <img src="https://images.unsplash.com/photo-1550745165-9bc0b252726f?auto=format&fit=crop&w=600&q=80" alt="Hide the Friend" class="w-full h-full object-cover opacity-80">
                        <div class="absolute top-3 right-3 bg-black/80 backdrop-blur-sm text-white text-[10px] font-bold px-3 py-1 rounded shadow">
                            Lead QA
                        </div>
                    </div>
                    <div class="p-6 flex flex-col flex-1">
                        <h3 class="text-xl font-bold text-white mb-4 text-center">Hide the Friend</h3>
                        <div class="flex justify-between items-center mt-auto bg-black/30 p-3 rounded-lg border border-white/5">
                            <div class="text-center w-1/2 border-r border-slate-700/50">
                                <div class="text-lg font-black text-white"><span class="counter" id="visits-htf" data-target="25000000">0</span>+</div>
                                <div class="text-[9px] text-slate-400 uppercase tracking-widest">Visits</div>
                            </div>
                            <div class="text-center w-1/2">
                                <div class="text-lg font-black text-white"><span class="counter" id="playing-htf" data-target="5400">0</span></div>
                                <div class="text-[9px] text-slate-400 uppercase tracking-widest">Playing</div>
                            </div>
                        </div>
                    </div>
                </a>

                <a href="https://www.roblox.com/games/81525595245099/Build-a-Golem-Army" target="_blank" class="bg-brand-card border border-slate-800 hover:border-red-500/50 rounded-2xl overflow-hidden flex flex-col transition-all duration-300 hover:-translate-y-2 shadow-lg">
                    <div class="relative w-full h-44 bg-slate-800">
                        <img src="https://images.unsplash.com/photo-1605379399642-870262d3d051?auto=format&fit=crop&w=600&q=80" alt="Build a Golem Army" class="w-full h-full object-cover opacity-80">
                        <div class="absolute top-3 right-3 bg-black/80 backdrop-blur-sm text-white text-[10px] font-bold px-3 py-1 rounded shadow">
                            Quality Assurance
                        </div>
                    </div>
                    <div class="p-6 flex flex-col flex-1">
                        <h3 class="text-xl font-bold text-white mb-4 text-center">Build a Golem Army</h3>
                        <div class="flex justify-between items-center mt-auto bg-black/30 p-3 rounded-lg border border-white/5">
                            <div class="text-center w-1/2 border-r border-slate-700/50">
                                <div class="text-lg font-black text-white"><span class="counter" id="visits-golem" data-target="10500000">0</span>+</div>
                                <div class="text-[9px] text-slate-400 uppercase tracking-widest">Visits</div>
                            </div>
                            <div class="text-center w-1/2">
                                <div class="text-lg font-black text-white"><span class="counter" id="playing-golem" data-target="1200">0</span></div>
                                <div class="text-[9px] text-slate-400 uppercase tracking-widest">Playing</div>
                            </div>
                        </div>
                    </div>
                </a>

                <a href="https://www.roblox.com/games/135690330157046/Word-Hunt-Battles" target="_blank" class="bg-brand-card border border-slate-800 hover:border-red-500/50 rounded-2xl overflow-hidden flex flex-col transition-all duration-300 hover:-translate-y-2 shadow-lg">
                    <div class="relative w-full h-44 bg-slate-800">
                        <img src="https://images.unsplash.com/photo-1633519828511-7eb9ddb96a94?auto=format&fit=crop&w=600&q=80" alt="Word Hunt Battles" class="w-full h-full object-cover opacity-80">
                        <div class="absolute top-3 right-3 bg-black/80 backdrop-blur-sm text-white text-[10px] font-bold px-3 py-1 rounded shadow">
                            Contributor
                        </div>
                    </div>
                    <div class="p-6 flex flex-col flex-1">
                        <h3 class="text-xl font-bold text-white mb-4 text-center">Word Hunt Battles</h3>
                        <div class="flex justify-between items-center mt-auto bg-black/30 p-3 rounded-lg border border-white/5">
                            <div class="text-center w-1/2 border-r border-slate-700/50">
                                <div class="text-lg font-black text-white"><span class="counter" id="visits-whb" data-target="50000">0</span>+</div>
                                <div class="text-[9px] text-slate-400 uppercase tracking-widest">Visits</div>
                            </div>
                            <div class="text-center w-1/2">
                                <div class="text-lg font-black text-white"><span class="counter" id="playing-whb" data-target="45">0</span></div>
                                <div class="text-[9px] text-slate-400 uppercase tracking-widest">Playing</div>
                            </div>
                        </div>
                    </div>
                </a>

                <div class="bg-brand-card border border-slate-800 hover:border-red-500/50 rounded-2xl overflow-hidden flex flex-col transition-all duration-300 hover:-translate-y-2 shadow-lg">
                    <div class="relative w-full h-44 bg-slate-800">
                        <img src="https://images.unsplash.com/photo-1542751371-adc38448a05e?auto=format&fit=crop&w=600&q=80" alt="RoJam 2026" class="w-full h-full object-cover opacity-50 grayscale">
                        <div class="absolute top-3 right-3 bg-black/80 backdrop-blur-sm text-white text-[10px] font-bold px-3 py-1 rounded shadow">
                            Team Leader & Producer
                        </div>
                        <div class="absolute inset-0 flex items-center justify-center">
                            <span class="bg-black/60 px-4 py-2 rounded-lg font-bold tracking-widest text-sm border border-white/10 text-white">IN DEVELOPMENT</span>
                        </div>
                    </div>
                    <div class="p-6 flex flex-col flex-1">
                        <h3 class="text-xl font-bold text-white mb-4 text-center">RoJam 2026</h3>
                        <div class="flex justify-center items-center mt-auto bg-black/30 p-3 rounded-lg border border-white/5">
                            <div class="text-center w-full">
                                <div class="text-sm font-bold text-slate-400 mt-1 uppercase tracking-widest">Status: Pre-Alpha</div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>

            <div class="grid md:grid-cols-2 gap-8">
                <div class="bg-white dark:bg-[#12121a] p-8 rounded-2xl border border-slate-200 dark:border-slate-800 shadow-lg glass-card md:col-span-2">
                    <i class="fa-solid fa-building text-3xl mb-4 text-purple-500"></i>
                    <h3 class="text-xl font-bold mb-4 text-slate-900 dark:text-white">Teams & Studios</h3>
                    <ul class="space-y-4 font-medium text-lg">
                        <li><span class="text-slate-900 dark:text-white font-bold"><i class="fa-solid fa-briefcase text-sm mr-3 text-yellow-500"></i> Team Leader & Producer @ RoJam 2026</span></li>
                        <li><span class="text-slate-900 dark:text-white font-bold"><i class="fa-solid fa-magnifying-glass text-sm mr-3 text-blue-400"></i> QA & Scout @ SimpleBricks</span></li>
                    </ul>
                </div>
            </div>

            <h3 class="text-3xl font-bold mb-8 text-center text-slate-900 dark:text-white border-t border-slate-200 dark:border-slate-800 pt-16 mt-16">Client Vouches</h3>
            
            <div class="grid md:grid-cols-2 gap-6">
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
    </main>

    <main id="pricing" class="page-section bg-grid-pattern relative min-h-screen">
        <div class="max-w-6xl mx-auto px-6 py-20 relative z-10">
            <h2 class="text-4xl font-bold mb-12 text-center text-slate-900 dark:text-white bg-white/80 dark:bg-[#0a0a0f]/80 backdrop-blur-sm inline-block px-8 py-2 rounded-full border border-slate-200 dark:border-slate-800 mx-auto block w-max">Project Management Services</h2>
            
            <h3 class="text-2xl font-bold mb-8 text-center text-slate-900 dark:text-white">Base Commission Rates</h3>
            <div class="grid md:grid-cols-2 gap-8 mb-16">
                <div class="bg-[#12121a] p-8 rounded-xl border border-slate-800 shadow-lg relative overflow-hidden flex flex-col">
                    <div class="absolute top-0 right-0 p-4 opacity-10 text-6xl"><i class="fa-solid fa-list-check"></i></div>
                    <h3 class="text-2xl font-bold mb-6 text-white relative z-10"><i class="fa-solid fa-list-check mr-2 text-blue-500"></i> Project Management</h3>
                    <div class="space-y-4 text-slate-300 font-medium relative z-10 flex-1 flex items-center justify-center">
                        <div class="text-center">
                            <span class="text-2xl font-bold text-blue-400">Contact me for pricing</span>
                            <p class="text-sm text-slate-500 mt-2">Custom quotes available for Agile/Scrum Setup, Team Coordination, Workflow Optimization, and Full Game Lifecycles.</p>
                        </div>
                    </div>
                </div>

                <div class="bg-[#12121a] p-8 rounded-xl border border-slate-800 shadow-lg relative overflow-hidden">
                    <div class="absolute top-0 right-0 p-4 opacity-10 text-6xl"><i class="fa-solid fa-bug-slash"></i></div>
                    <h3 class="text-2xl font-bold mb-6 text-white relative z-10"><i class="fa-solid fa-bug-slash mr-2 text-orange-500"></i> Quality Assurance</h3>
                    <div class="space-y-4 text-slate-300 font-medium relative z-10">
                        <div class="flex justify-between border-b border-slate-700/50 pb-2"><span>Basic Playtesting</span><span class="font-bold text-orange-500">20 - 50 USD</span></div>
                        <div class="flex justify-between border-b border-slate-700/50 pb-2"><span>Full Bug Report</span><span class="font-bold text-orange-500">100 - 200 USD</span></div>
                        <div class="flex justify-between border-b border-slate-700/50 pb-2"><span>Mechanics Stress Test</span><span class="font-bold text-orange-500">150 - 300 USD</span></div>
                        <div class="flex justify-between"><span>Continuous QA Support</span><span class="font-bold text-orange-500">Custom Quote</span></div>
                    </div>
                </div>
            </div>

            <h3 class="text-2xl font-bold mb-8 text-center text-slate-900 dark:text-white">Deep Dive & Explanations</h3>
            <div class="space-y-4 max-w-4xl mx-auto mb-16">
                <details class="bg-white/90 dark:bg-slate-800/90 backdrop-blur-md rounded-xl shadow-md border border-slate-200 dark:border-slate-700 group cursor-pointer">
                    <summary class="p-6 font-bold text-xl text-blue-600 dark:text-blue-400 flex justify-between items-center outline-none">
                        <span><i class="fa-solid fa-list-check mr-2"></i> What's included in Project Management?</span>
                        <i class="fa-solid fa-chevron-down transition-transform group-open:rotate-180 text-slate-400"></i>
                    </summary>
                    <div class="p-6 pt-0 border-t border-slate-200 dark:border-slate-700">
                        <div class="grid md:grid-cols-2 gap-4 mt-6">
                            <div class="bg-slate-50 dark:bg-slate-900 p-5 rounded-lg border border-slate-200 dark:border-slate-700">
                                <h5 class="font-bold text-slate-900 dark:text-white mb-2">Sprint Planning</h5>
                                <p class="text-sm text-slate-600 dark:text-slate-400">Organizing milestones, delegating tasks to developers, and maintaining roadmaps to ensure your game ships on time.</p>
                            </div>
                            <div class="bg-slate-50 dark:bg-slate-900 p-5 rounded-lg border border-slate-200 dark:border-slate-700">
                                <h5 class="font-bold text-slate-900 dark:text-white mb-2">Team Coordination</h5>
                                <p class="text-sm text-slate-600 dark:text-slate-400">Acting as the bridge between programmers, artists, and sound designers to maintain a unified creative vision.</p>
                            </div>
                        </div>
                    </div>
                </details>
                <details class="bg-white/90 dark:bg-slate-800/90 backdrop-blur-md rounded-xl shadow-md border border-slate-200 dark:border-slate-700 group cursor-pointer">
                    <summary class="p-6 font-bold text-xl text-orange-500 dark:text-orange-400 flex justify-between items-center outline-none">
                        <span><i class="fa-solid fa-bug-slash mr-2"></i> What's included in Quality Assurance?</span>
                        <i class="fa-solid fa-chevron-down transition-transform group-open:rotate-180 text-slate-400"></i>
                    </summary>
                    <div class="p-6 pt-0 border-t border-slate-200 dark:border-slate-700">
                        <div class="grid md:grid-cols-2 gap-4 mt-6">
                            <div class="bg-slate-50 dark:bg-slate-900 p-5 rounded-lg border border-slate-200 dark:border-slate-700">
                                <h5 class="font-bold text-slate-900 dark:text-white mb-2">Bug Tracking</h5>
                                <p class="text-sm text-slate-600 dark:text-slate-400">Detailed reproduction steps, video evidence, and organized Jira/Trello boards to help your developers squash bugs fast.</p>
                            </div>
                            <div class="bg-slate-50 dark:bg-slate-900 p-5 rounded-lg border border-slate-200 dark:border-slate-700">
                                <h5 class="font-bold text-slate-900 dark:text-white mb-2">Edge Case Testing</h5>
                                <p class="text-sm text-slate-600 dark:text-slate-400">Intentionally trying to break mechanics, economy systems, and collision to ensure exploit-proof gameplay before launch.</p>
                            </div>
                        </div>
                    </div>
                </details>
                
                <details class="bg-red-50/90 dark:bg-red-900/20 backdrop-blur-md rounded-xl shadow-md border border-red-200 dark:border-red-900/50 group cursor-pointer">
                    <summary class="p-6 font-bold text-xl text-red-600 dark:text-red-400 flex justify-between items-center outline-none">
                        <span><i class="fa-solid fa-scroll mr-2"></i> Terms of Service (TOS)</span>
                        <i class="fa-solid fa-chevron-down transition-transform group-open:rotate-180 text-red-400"></i>
                    </summary>
                    <div class="p-6 pt-0 border-t border-red-200 dark:border-red-900/50">
                        <ul class="list-disc pl-5 mt-4 space-y-2 text-sm text-slate-700 dark:text-slate-300">
                            <li><strong>I work by contract.</strong> Specific terms and milestones will be agreed upon before start.</li>
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

    <main id="contact" class="page-section max-w-4xl mx-auto px-6 py-20 text-center min-h-screen flex flex-col justify-center">
        <h2 class="text-5xl font-black mb-6 text-slate-900 dark:text-white uppercase tracking-tight">Let's Work Together</h2>
        <p class="text-lg text-slate-400 mb-10">Ready to take your game to the next level? Reach out directly via the links below.</p>
        
        <div class="bg-slate-200 dark:bg-slate-800/50 inline-flex items-center px-6 py-3 rounded-full mb-12 border border-slate-300 dark:border-slate-700 shadow-sm mx-auto w-max">
            <i class="fa-regular fa-clock text-red-500 mr-2 animate-pulse text-lg"></i> 
            <span class="text-slate-600 dark:text-slate-300 font-bold">My Local Time (CET): <span id="local-time" class="text-slate-900 dark:text-white ml-1">Loading...</span></span>
        </div>
        
        <div class="grid md:grid-cols-2 gap-8 max-w-3xl mx-auto w-full">
            <a href="https://www.roblox.com/share?code=d0f7afb99a958a48b7874a51df8a9656&type=Profile&source=ProfileShare&stamp=1778661904863" target="_blank" rel="noopener" class="bg-[#12121a] hover:bg-[#1a1a24] border border-slate-800 hover:border-red-500 transition-all duration-300 p-10 rounded-3xl flex flex-col items-center justify-center gap-6 shadow-xl hover:-translate-y-2 group">
                <div class="w-20 h-20 rounded-2xl bg-red-500/10 flex items-center justify-center group-hover:scale-110 transition-transform duration-300">
                    <svg class="w-12 h-12 fill-red-500" viewBox="0 0 24 24"><path d="M5.164 0L0 18.627 18.836 24 24 5.373 5.164 0zm9.086 14.442l-4.649-1.186 1.185-4.65 4.65 1.186-1.186 4.65z"/></svg>
                </div>
                <div class="text-center">
                    <h3 class="text-2xl font-black text-white mb-2">Roblox Profile</h3>
                    <p class="text-slate-400 font-medium text-sm">View my portfolio and previous work directly on the platform.</p>
                </div>
                <div class="mt-4 px-6 py-2 bg-red-500/20 text-red-400 font-bold rounded-full text-sm uppercase tracking-wide group-hover:bg-red-500 group-hover:text-white transition-colors">Connect</div>
            </a>

            <a href="https://discordapp.com/users/1100530188896448603" target="_blank" rel="noopener" class="bg-[#12121a] hover:bg-[#1a1a24] border border-slate-800 hover:border-[#5865F2] transition-all duration-300 p-10 rounded-3xl flex flex-col items-center justify-center gap-6 shadow-xl hover:-translate-y-2 group">
                <div class="w-20 h-20 rounded-2xl bg-[#5865F2]/10 flex items-center justify-center group-hover:scale-110 transition-transform duration-300">
                    <i class="fa-brands fa-discord text-[50px] text-[#5865F2]"></i>
                </div>
                <div class="text-center">
                    <h3 class="text-2xl font-black text-white mb-2">DM @Jamie</h3>
                    <p class="text-slate-400 font-medium text-sm">Discord ID: <br><span class="text-white bg-white/10 px-2 py-1 rounded inline-block mt-1">1100530188896448603</span></p>
                </div>
                <div class="mt-4 px-6 py-2 bg-[#5865F2]/20 text-[#5865F2] font-bold rounded-full text-sm uppercase tracking-wide group-hover:bg-[#5865F2] group-hover:text-white transition-colors">Message Me</div>
            </a>
        </div>
    </main>

    <footer class="text-center py-8 border-t border-slate-200 dark:border-slate-800 text-slate-500 dark:text-slate-400 bg-white dark:bg-[#0a0a0f] transition-colors pb-24 md:pb-8">
        <p>&copy; 2026 Jamie | DEVELOPER.</p>
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
                            // Update the data-target attributes with live fetched data
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
