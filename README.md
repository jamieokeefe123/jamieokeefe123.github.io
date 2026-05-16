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
                        <i class="fa-brands fa-discord mr-2 text-xl"></i> jamie_creates
                    </a>
                </div>
            </div>
        </div>

        <div class="max-w-6xl mx-auto px-6 py-20 text-left">
            <div class="bg-[#450a0a] border border-red-500/30 p-8 rounded-2xl text-center shadow-md mb-20">
                <h4 class="text-sm font-bold text-red-300 uppercase tracking-widest mb-6">Skills</h4>
                <div class="flex flex-wrap justify-center gap-8 text-white font-black text-lg md:text-xl">
                    <div class="flex items-center hover:text-red-400 transition-colors cursor-default"><i class="fa-solid fa-layer-group text-2xl mr-2 text-red-400"></i> Game Production</div>
                    <div class="flex items-center hover:text-blue-400 transition-colors cursor-default"><i class="fa-solid fa-pen-nib text-2xl mr-2 text-blue-400"></i> Game Design</div>
                    <div class="flex items-center hover:text-purple-400 transition-colors cursor-default"><i class="fa-solid fa-list-check text-2xl mr-2 text-purple-400"></i> Project Management</div>
                    <div class="flex items-center hover:text-orange-400 transition-colors cursor-default"><i class="fa-solid fa-bug-slash text-2xl mr-2 text-orange-400"></i> Quality Assurance</div>
                    <div class="flex items-center hover:text-green-400 transition-colors cursor-default"><i class="fa-solid fa-users text-2xl mr-2 text-green-400"></i> Team Leadership</div>
                    <div class="flex items-center hover:text-cyan-400 transition-colors cursor-default"><i class="fa-solid fa-magnifying-glass-chart text-2xl mr-2 text-cyan-400"></i> Acquisition Scouting</div>
                </div>
            </div>

            <h3 class="text-3xl font-bold mb-10 text-center text-slate-900 dark:text-white border-b border-slate-200 dark:border-slate-800 pb-4">My Core Expertise</h3>
            <div class="grid md:grid-cols-3 gap-8 mb-10">
                <div class="bg-[#450a0a] p-8 rounded-2xl border border-red-500/30 shadow-lg glass-card text-white">
                    <i class="fa-solid fa-clipboard-check text-4xl text-blue-400 mb-4"></i>
                    <h4 class="text-xl font-bold mb-3 text-white">Game Production</h4>
                    <p class="text-slate-300">Overseeing complete project lifecycles, coordinating multi-disciplinary teams, and ensuring developmental milestones are met efficiently.</p>
                </div>
                <div class="bg-[#450a0a] p-8 rounded-2xl border border-red-500/30 shadow-lg glass-card text-white">
                    <i class="fa-solid fa-shield-halved text-4xl text-orange-400 mb-4"></i>
                    <h4 class="text-xl font-bold mb-3 text-white">Quality Assurance</h4>
                    <p class="text-slate-300">Rigorous playtesting, bug tracking, and edge-case identification to guarantee a flawless, lag-free user experience.</p>
                </div>
                <div class="bg-[#450a0a] p-8 rounded-2xl border border-red-500/30 shadow-lg glass-card text-white">
                    <i class="fa-solid fa-magnifying-glass-dollar text-4xl text-green-400 mb-4"></i>
                    <h4 class="text-xl font-bold mb-3 text-white">Acquisition Scouting</h4>
                    <p class="text-slate-300">Finding upcoming games, contacting game owners, and helping people invest in highly promising projects on the platform.</p>
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
                <div class="block bg-[#12121a] border border-red-500/50 rounded-3xl p-8 md:p-12 shadow-2xl relative overflow-hidden">
                    <div class="absolute top-0 right-0 w-64 h-64 bg-red-500/10 rounded-full blur-3xl"></div>
                    
                    <div class="relative z-10 flex flex-col lg:flex-row items-center justify-between gap-10">
                        <div class="flex-1 text-center lg:text-left">
                            <div class="inline-flex items-center justify-center w-16 h-16 rounded-2xl bg-red-500/20 text-red-500 text-3xl mb-6">
                                <span class="font-black tracking-tighter">SB</span>
                            </div>
                            <h3 class="text-4xl font-black text-white mb-2">SimpleBricks</h3>
                            <p class="text-red-400 font-bold uppercase tracking-widest text-sm mb-6">Featured Studio Contribution</p>
                            <p class="text-slate-400 text-lg leading-relaxed">
                                Managing production metrics, scouting high-potential acquisitions, and validating system quality infrastructure across an immersive title ecosystem.
                            </p>
                        </div>

                        <div class="flex-1 w-full bg-black/40 rounded-2xl p-8 border border-white/5">
                            <div class="flex flex-col gap-6 text-center">
                                <div class="grid grid-cols-2 gap-4">
                                    <div>
                                        <i class="fa-solid fa-gamepad text-red-500 text-2xl mb-2"></i>
                                        <div class="text-3xl font-black text-white">289M+</div>
                                        <div class="text-[10px] text-slate-500 uppercase tracking-widest font-bold">Total Visits</div>
                                    </div>
                                    <div>
                                        <i class="fa-solid fa-users text-red-500 text-2xl mb-2"></i>
                                        <div class="text-3xl font-black text-white">13.4M+</div>
                                        <div class="text-[10px] text-slate-500 uppercase tracking-widest font-bold font-sans">Group Members</div>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>

            <h3 class="text-2xl font-bold mb-8 text-slate-900 dark:text-white border-b border-slate-800 pb-4"><i class="fa-solid fa-folder-open mr-2 text-red-500"></i> Managed Projects & Contributions</h3>
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6 mb-16">
                
                <a href="https://www.roblox.com/games/108564524217399/Dig-A-Lucky-Block-For-Brainrots" target="_blank" class="bg-[#12121a] border border-slate-800 hover:border-red-500/50 rounded-2xl overflow-hidden flex flex-col transition-all duration-300 hover:-translate-y-2 shadow-lg">
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
                                <div class="text-lg font-black text-white">154K+</div>
                                <div class="text-[9px] text-slate-400 uppercase tracking-widest">Visits</div>
                            </div>
                            <div class="text-center w-1/2">
                                <div class="text-lg font-black text-white">120</div>
                                <div class="text-[9px] text-slate-400 uppercase tracking-widest">Playing</div>
                            </div>
                        </div>
                    </div>
                </a>

                <a href="https://simplebricks.com.au/" target="_blank" class="bg-[#12121a] border border-slate-800 hover:border-red-500/50 rounded-2xl overflow-hidden flex flex-col transition-all duration-300 hover:-translate-y-2 shadow-lg">
                    <div class="relative w-full h-44 bg-slate-800">
                        <img src="https://images.unsplash.com/photo-1605379399642-870262d3d051?auto=format&fit=crop&w=600&q=80" alt="SimpleBricks" class="w-full h-full object-cover opacity-80">
                        <div class="absolute top-3 right-3 bg-black/80 backdrop-blur-sm text-white text-[10px] font-bold px-3 py-1 rounded shadow">
                            Quality Assurance & Acquisition Scout
                        </div>
                    </div>
                    <div class="p-6 flex flex-col flex-1">
                        <h3 class="text-xl font-bold text-white mb-4 text-center">SimpleBricks Studio</h3>
                        <div class="flex justify-center items-center mt-auto bg-black/30 p-3 rounded-lg border border-white/5">
                            <span class="text-xs text-red-400 font-bold uppercase tracking-wider">View Studio Hub</span>
                        </div>
                    </div>
                </a>

                <a href="https://www.roblox.com/games/135690330157046/Word-Hunt-Battles" target="_blank" class="bg-[#12121a] border border-slate-800 hover:border-red-500/50 rounded-2xl overflow-hidden flex flex-col transition-all duration-300 hover:-translate-y-2 shadow-lg">
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
                                <div class="text-lg font-black text-white">50K+</div>
                                <div class="text-[9px] text-slate-400 uppercase tracking-widest">Visits</div>
                            </div>
                            <div class="text-center w-1/2">
                                <div class="text-lg font-black text-white">45</div>
                                <div class="text-[9px] text-slate-400 uppercase tracking-widest">Playing</div>
                            </div>
                        </div>
                    </div>
                </a>

                <div class="bg-[#12121a] border border-slate-800 hover:border-red-500/50 rounded-2xl overflow-hidden flex flex-col transition-all duration-300 hover:-translate-y-2 shadow-lg">
                    <div class="relative w-full h-44 bg-slate-800">
                        <img src="https://images.unsplash.com/photo-1542751371-adc38448a05e?auto=format&fit=crop&w=600&q=80" alt="RoJam 2026" class="w-full h-full object-cover opacity-50 grayscale">
                        <div class="absolute top-3 right-3 bg-black/80 backdrop-blur-sm text-white text-[10px] font-bold px-3 py-1 rounded shadow">
                            Team Leader & Game Producer
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

                <a href="https://www.roblox.com/games/98138235237704/Hide-the-Friend" target="_blank" class="bg-[#12121a] border border-slate-800 hover:border-red-500/50 rounded-2xl overflow-hidden flex flex-col transition-all duration-300 hover:-translate-y-2 shadow-lg">
                    <div class="relative w-full h-44 bg-slate-800">
                        <img src="https://images.unsplash.com/photo-1550745165-9bc0b252726f?auto=format&fit=crop&w=600&q=80" alt="Hide the Friend" class="w-full h-full object-cover opacity-80">
                        <div class="absolute top-3 right-3 bg-black/80 backdrop-blur-sm text-white text-[10px] font-bold px-3 py-1 rounded shadow">
                            Lead Quality Assurance
                        </div>
                    </div>
                    <div class="p-6 flex flex-col flex-1">
                        <h3 class="text-xl font-bold text-white mb-4 text-center">Hide the Friend</h3>
                        <div class="flex justify-between items-center mt-auto bg-black/30 p-3 rounded-lg border border-white/5">
                            <div class="text-center w-1/2 border-r border-slate-700/50">
                                <div class="text-lg font-black text-white">25M+</div>
                                <div class="text-[9px] text-slate-400 uppercase tracking-widest">Visits</div>
                            </div>
                            <div class="text-center w-1/2">
                                <div class="text-lg font-black text-white">5.4K</div>
                                <div class="text-[9px] text-slate-400 uppercase tracking-widest">Playing</div>
                            </div>
                        </div>
                    </div>
                </a>

                <a href="https://www.roblox.com/games/81525595245099/Build-a-Golem-Army" target="_blank" class="bg-[#12121a] border border-slate-800 hover:border-red-500/50 rounded-2xl overflow-hidden flex flex-col transition-all duration-300 hover:-translate-y-2 shadow-lg">
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
                                <div class="text-lg font-black text-white">10.5M+</div>
                                <div class="text-[9px] text-slate-400 uppercase tracking-widest">Visits</div>
                            </div>
                            <div class="text-center w-1/2">
                                <div class="text-lg font-black text-white">1.2K</div>
                                <div class="text-[9px] text-slate-400 uppercase tracking-widest">Playing</div>
                            </div>
                        </div>
                    </div>
                </a>

            </div>

            <div class="grid md:grid-cols-2 gap-8">
                <div class="bg-white dark:bg-[#12121a] p-8 rounded-2xl border border-slate-200 dark:border-slate-800 shadow-lg glass-card md:col-span-2">
                    <i class="fa-solid fa-building text-3xl mb-4 text-purple-500"></i>
                    <h3 class="text-xl font-bold mb-4 text-slate-900 dark:text-white">Teams & Studios</h3>
                    <ul class="space-y-4 font-medium text-lg">
                        <li><span class="text-slate-900 dark:text-white font-bold"><i class="fa-solid fa-briefcase text-sm mr-3 text-yellow-500"></i> Team Leader & Game Producer @ RoJam 2026</span></li>
                        <li><span class="text-slate-900 dark:text-white font-bold"><i class="fa-solid fa-magnifying-glass text-sm mr-3 text-blue-400"></i> Quality Assurance & Acquisition Scout @ SimpleBricks</span></li>
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
                        </div>
                    </div>
                </div>

                <div class="bg-[#12121a] p-8 rounded-xl border border-slate-800 shadow-lg relative overflow-hidden flex flex-col">
                    <div class="absolute top-0 right-0 p-4 opacity-10 text-6xl"><i class="fa-solid fa-bug-slash"></i></div>
                    <h3 class="text-2xl font-bold mb-6 text-white relative z-10"><i class="fa-solid fa-bug-slash mr-2 text-orange-500"></i> Quality Assurance</h3>
                    <div class="space-y-4 text-slate-300 font-medium relative z-10 flex-1 flex items-center justify-center">
                        <div class="text-center">
                            <span class="text-2xl font-bold text-orange-400">Contact me for pricing</span>
                        </div>
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
                        </div>
                    </div>
                </details>
            </div>
        </div>
    </main>

    <script>
        function showPage(pageId) {
            document.querySelectorAll('.page-section').forEach(section => {
                section.classList.remove('active');
            });
            document.querySelectorAll('.nav-link').forEach(link => {
                link.classList.remove('active');
            });
            
            const targetSection = document.getElementById(pageId);
            if (targetSection) targetSection.classList.add('active');
            
            const targetLink = document.getElementById('nav-' + pageId);
            if (targetLink) targetLink.classList.add('active');
            
            window.scrollTo({top: 0, behavior: 'smooth'});
        }
    </script>
</body>
</html>
