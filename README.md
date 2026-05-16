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
<body class="bg-slate-50 text-slate-800 dark:bg-[#0a0a0f] dark:text-slate-100 antialiased font-sans relative min-h-screen flex flex-col justify-between">

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
                <div onclick="showPage('home')" class="text-2xl font-extrabold tracking-widest text-slate-900 dark:text-white cursor-pointer select-none">
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

    <main class="flex-grow max-w-6xl w-full mx-auto px-6 py-12">
        
        <section id="home" class="page-section active hero-bg bg-grid-pattern rounded-3xl p-8 md:p-16 border border-slate-200 dark:border-red-950/30 shadow-2xl relative overflow-hidden">
            <div class="relative z-10 max-w-2xl">
                <span class="text-red-500 font-bold tracking-widest text-xs uppercase bg-red-500/10 px-3 py-1 rounded-full border border-red-500/20">Available for Contract</span>
                <h1 class="text-4xl md:text-6xl font-black mt-4 mb-2 tracking-tight">Jamie</h1>
                <h2 class="text-xl md:text-2xl font-semibold text-red-500 mb-6 tracking-wide">Game Producer & Designer</h2>
                <p class="text-slate-400 text-base md:text-lg leading-relaxed mb-8">
                    Specializing in production pipeline optimization, systems architecture, agile team leadership, and rigorous QA engineering. Bringing complex interactive worlds from concept to execution.
                </p>
                <div class="flex flex-wrap gap-4">
                    <button onclick="showPage('portfolio')" class="bg-red-600 hover:bg-red-500 text-white font-bold px-6 py-3 rounded-xl shadow-lg shadow-red-600/30 transition-all transform hover:-translate-y-0.5">
                        View Portfolio
                    </button>
                    <button onclick="showPage('contact')" class="bg-transparent border-2 border-slate-700 hover:border-slate-500 text-slate-300 font-bold px-6 py-3 rounded-xl transition-all">
                        Let's Talk
                    </button>
                </div>
            </div>
        </section>

        <section id="portfolio" class="page-section space-y-8">
            <div>
                <h2 class="text-3xl font-black tracking-tight mb-2">Featured Projects</h2>
                <p class="text-slate-400">A collection of systems architecture, production milestones, and engineering roles.</p>
            </div>
            
            <div class="grid md:grid-cols-2 lg:grid-cols-3 gap-6">
                <div class="glass-card bg-[#12121a] border border-slate-800 rounded-2xl p-6 relative overflow-hidden group">
                    <div class="text-red-500 text-3xl mb-4"><i class="fa-solid fa-gamepad"></i></div>
                    <h3 class="text-xl font-bold mb-2">Project Alpha: AAA Pipeline</h3>
                    <p class="text-slate-400 text-sm mb-4">Lead Producer role optimizing Scrum sprint methodologies, smoothing dependency pipelines, and driving feature readiness timelines.</p>
                    <span class="text-xs font-semibold bg-slate-800 px-2.5 py-1 rounded-md text-slate-300">Production</span>
                </div>
                <div class="glass-card bg-[#12121a] border border-slate-800 rounded-2xl p-6 relative overflow-hidden group">
                    <div class="text-red-500 text-3xl mb-4"><i class="fa-solid fa-diagram-project"></i></div>
                    <h3 class="text-xl font-bold mb-2">Project Beta: Economy Design</h3>
                    <p class="text-slate-400 text-sm mb-4">Systems Architect modeling numerical balancing arrays, monetization metrics, and standard gameplay progression curves.</p>
                    <span class="text-xs font-semibold bg-slate-800 px-2.5 py-1 rounded-md text-slate-300">Game Design</span>
                </div>
                <div class="glass-card bg-[#12121a] border border-slate-800 rounded-2xl p-6 relative overflow-hidden group">
                    <div class="text-red-500 text-3xl mb-4"><i class="fa-solid fa-bug"></i></div>
                    <h3 class="text-xl font-bold mb-2">Project Gamma: QA Pipeline</h3>
                    <p class="text-slate-400 text-sm mb-4">Engineered structured automation play-testing workflows, platform certification passes, and regression tracking schemas.</p>
                    <span class="text-xs font-semibold bg-slate-800 px-2.5 py-1 rounded-md text-slate-300">Quality Assurance</span>
                </div>
            </div>
        </section>

        <section id="pricing" class="page-section space-y-8">
            <div>
                <h2 class="text-3xl font-black tracking-tight mb-2">Services & Capabilities</h2>
                <p class="text-slate-400">Available formats for Studio Consultations, Milestones, and Contract Agreements.</p>
            </div>
            
            <div class="overflow-x-auto rounded-2xl border border-slate-800 bg-[#12121a]">
                <table class="w-full text-left border-collapse">
                    <thead>
                        <tr class="border-b border-slate-800 bg-slate-900/50">
                            <th class="p-4 font-bold text-sm tracking-wide text-slate-200">Focus Area</th>
                            <th class="p-4 font-bold text-sm tracking-wide text-slate-200">Engagement Scope</th>
                            <th class="p-4 font-bold text-sm tracking-wide text-slate-200">Ideal For</th>
                        </tr>
                    </thead>
                    <tbody class="divide-y divide-slate-800 text-slate-300 text-sm">
                        <tr>
                            <td class="p-4 font-semibold text-white">Production Consulting</td>
                            <td class="p-4">Sprint Audits, Roadmap Scaling, Tool Pipeline Overhauls</td>
                            <td class="p-4">Indie/AA Teams setting up major milestones</td>
                        </tr>
                        <tr>
                            <td class="p-4 font-semibold text-white">Systems Frameworks</td>
                            <td class="p-4">Economy Balance Modeling, Game Design Document (GDD) Architecture</td>
                            <td class="p-4">Studios requiring system balancing layers</td>
                        </tr>
                        <tr>
                            <td class="p-4 font-semibold text-white">End-to-End QA Automation</td>
                            <td class="p-4">Test Case Structures, Platform Submission Passes, Playtest Telemetry</td>
                            <td class="p-4">Teams prepping Beta/Launch-ready builds</td>
                        </tr>
                    </tbody>
                </table>
            </div>
        </section>

        <section id="contact" class="page-section max-w-xl mx-auto space-y-6">
            <div class="text-center">
                <h2 class="text-3xl font-black tracking-tight mb-2">Get In Touch</h2>
                <p class="text-slate-400">Let's coordinate on your next game release or production cycle.</p>
            </div>
            
            <form class="space-y-4 bg-[#12121a] border border-slate-800 p-6 rounded-2xl" onsubmit="event.preventDefault(); alert('Form wrapper functioning! Connect an endpoint to process live email actions.');">
                <div>
                    <label class="block text-xs font-bold uppercase tracking-wider text-slate-400 mb-2">Name</label>
                    <input type="text" required class="w-full bg-slate-900 border border-slate-800 rounded-xl p-3 text-sm focus:outline-none focus:border-red-500 transition-colors" placeholder="Studio Director">
                </div>
                <div>
                    <label class="block text-xs font-bold uppercase tracking-wider text-slate-400 mb-2">Email Address</label>
                    <input type="email" required class="w-full bg-slate-900 border border-slate-800 rounded-xl p-3 text-sm focus:outline-none focus:border-red-500 transition-colors" placeholder="name@studio.com">
                </div>
                <div>
                    <label class="block text-xs font-bold uppercase tracking-wider text-slate-400 mb-2">Project Brief</label>
                    <textarea rows="4" required class="w-full bg-slate-900 border border-slate-800 rounded-xl p-3 text-sm focus:outline-none focus:border-red-500 transition-colors" placeholder="Tell me about your scope, timelines, and engine..."></textarea>
                </div>
                <button type="submit" class="w-full bg-red-600 hover:bg-red-500 text-white font-bold py-3 rounded-xl shadow-lg shadow-red-600/20 transition-colors">
                    Dispatch Message
                </button>
            </form>
        </section>

    </main>

    <footer class="border-t border-slate-200 dark:border-slate-800 py-6 text-center text-xs text-slate-500">
        <p>&copy; 2026 Jamie. Built for high-performance creative execution.</p>
    </footer>

    <script>
        function showPage(pageId) {
            // Target all data pages and clear visibility
            const pages = document.querySelectorAll('.page-section');
            pages.forEach(page => page.classList.remove('active'));
            
            // Clean navigation states
            const links = document.querySelectorAll('.nav-link');
            links.forEach(link => link.classList.remove('active'));
            
            // Activate selected page anchor
            const targetPage = document.getElementById(pageId);
            if(targetPage) {
                targetPage.classList.add('active');
            }
            
            // Toggle focus state for the corresponding link item
            const targetLink = document.getElementById('nav-' + pageId);
            if(targetLink) {
                targetLink.classList.add('active');
            }

            // Lock viewport focus to top index immediately on change
            window.scrollTo({top: 0, behavior: 'instant'});
        }
    </script>
</body>
</html>

        container.appendChild(inner);
    });
}

document.addEventListener('DOMContentLoaded', init);
    </script>
</body>
</html>
