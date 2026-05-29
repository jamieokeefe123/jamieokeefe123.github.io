<html lang="en" class="dark">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
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
<body class="bg-brand-dark text-white font-sans antialiased bg-grid-pattern min-h-screen">

    <nav class="fixed top-0 left-0 w-full z-50 bg-brand-dark/80 backdrop-blur-md border-b border-white/5 py-4 px-6 md:px-12 flex justify-between items-center">
        <div class="text-xl font-black tracking-wider glow-red text-brand-red">JAMIE_CREATES</div>
        <div class="flex space-x-6 text-sm font-semibold tracking-wide">
            <span class="nav-link active" onclick="showPage('home')">Home</span>
            <span class="nav-link" onclick="showPage('services')">Services</span>
            <span class="nav-link" onclick="showPage('portfolio')">Portfolio</span>
            <span class="nav-link" onclick="showPage('contact')">Contact</span>
        </div>
    </nav>

    <main class="pt-24 min-h-screen">
        
        <section id="home" class="page-section active max-w-6xl mx-auto px-6 py-12">
            <div class="hero-bg rounded-3xl p-8 md:p-16 border border-brand-red/20 relative overflow-hidden mb-12 shadow-2xl">
                <div class="relative z-10 max-w-2xl">
                    <span class="text-brand-red uppercase tracking-widest font-black text-xs px-3 py-1 bg-brand-red/10 border border-brand-red/20 rounded-full">Game Producer</span>
                    <h1 class="text-4xl md:text-6xl font-black tracking-tight mt-4 mb-6 leading-tight">Bringing Virtual Worlds To Life.</h1>
                    <p class="text-gray-400 text-lg leading-relaxed mb-8">Managing scope, timeline, and creative vision to deliver high-quality gaming experiences on time and within budget.</p>
                    <button onclick="showPage('contact')" class="bg-brand-red hover:bg-red-600 transition font-bold px-8 py-4 rounded-xl shadow-lg shadow-brand-red/20 tracking-wide uppercase text-sm">Let's Work Together</button>
                </div>
            </div>

            <div class="mt-16">
                <h2 class="text-3xl font-black tracking-tight text-brand-red mb-8 uppercase">Skills</h2>
                
                <div class="grid grid-cols-1 md:grid-cols-3 gap-6">
                    <div class="glass-card bg-brand-card border border-white/5 p-6 rounded-2xl">
                        <div class="text-brand-red text-2xl mb-4"><i class="fa-solid fa-users-gear"></i></div>
                        <h3 class="text-xl font-bold mb-2">Team Leadership</h3>
                        <p class="text-gray-400 text-sm leading-relaxed">Coordinating cross-functional teams of developers, artists, and designers towards a unified goal.</p>
                    </div>
                    <div class="glass-card bg-brand-card border border-white/5 p-6 rounded-2xl">
                        <div class="text-brand-red text-2xl mb-4"><i class="fa-solid fa-timeline"></i></div>
                        <h3 class="text-xl font-bold mb-2">Agile Production</h3>
                        <p class="text-gray-400 text-sm leading-relaxed">Sprints, backlog grooming, and milestone planning utilizing modern workflow methodologies.</p>
                    </div>
                    <div class="glass-card bg-brand-card border border-white/5 p-6 rounded-2xl">
                        <div class="text-brand-red text-2xl mb-4"><i class="fa-solid fa-triangle-exclamation"></i></div>
                        <h3 class="text-xl font-bold mb-2">Risk Mitigation</h3>
                        <p class="text-gray-400 text-sm leading-relaxed">Identifying delivery bottlenecks early, optimizing scope, and protecting team health.</p>
                    </div>
                </div>
            </div>
        </section>

        <section id="services" class="page-section max-w-6xl mx-auto px-6 py-12">
            <h2 class="text-3xl font-black text-white mb-4 uppercase tracking-tight">Services</h2>
            <p class="text-gray-400 mb-8">Production workflows, scoping, and game consulting strategies.</p>
        </section>

        <section id="portfolio" class="page-section max-w-6xl mx-auto px-6 py-12">
            <h2 class="text-3xl font-black text-white mb-4 uppercase tracking-tight">Portfolio</h2>
            <p class="text-gray-400 mb-8">Selected titles and projects.</p>
        </section>

        <section id="contact" class="page-section max-w-6xl mx-auto px-6 py-12">
            <h2 class="text-3xl font-black text-white mb-4 uppercase tracking-tight">Contact</h2>
            <p class="text-gray-400 mb-8">Let's build something epic together.</p>
        </section>

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
            if(targetSection) {
                targetSection.classList.add('active');
            }
            
            if(event && event.currentTarget) {
                event.currentTarget.classList.add('active');
            }
            
            window.scrollTo(0, 0);
        }
    </script>
</body>
</html>
