<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Larion | Best Serverside</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
    <style>
        body {
            background-color: #020617;
            color: white;
            font-family: 'Inter', sans-serif;
            background-image: radial-gradient(#1e293b 0.5px, transparent 0.5px);
            background-size: 30px 30px;
            margin: 0;
            overflow-x: hidden;
        }

        /* Navigation Box */
        #nav-overlay {
            display: none;
            position: fixed;
            top: 70px;
            right: 20px;
            width: 260px;
            background: rgba(7, 10, 24, 0.98);
            border: 1px solid rgba(255, 255, 255, 0.08);
            border-radius: 12px;
            padding: 15px;
            z-index: 1000;
            box-shadow: 0 20px 50px rgba(0,0,0,0.9);
        }

        .menu-label {
            color: #475569;
            font-size: 10px;
            font-weight: 800;
            text-transform: uppercase;
            letter-spacing: 1.5px;
            margin: 15px 0 8px 5px;
        }

        .menu-btn {
            display: flex;
            align-items: center;
            gap: 12px;
            color: #94a3b8;
            font-size: 13px;
            padding: 10px;
            border-radius: 6px;
            cursor: pointer;
            transition: 0.2s;
        }

        .menu-btn:hover {
            background: rgba(59, 130, 246, 0.1);
            color: white;
        }

        .glow-blue { text-shadow: 0 0 20px rgba(59, 130, 246, 0.6); }

        .glass-card {
            background: rgba(15, 23, 42, 0.5);
            border: 1px solid rgba(51, 65, 85, 0.4);
            backdrop-filter: blur(10px);
        }

        .page-section { display: none; }
        .page-section.active { display: block; animation: fadeIn 0.4s ease; }

        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(10px); }
            to { opacity: 1; transform: translateY(0); }
        }

        .video-container {
            position: relative;
            padding-bottom: 56.25%; /* 16:9 Aspect Ratio */
            height: 0;
            overflow: hidden;
            border-radius: 12px;
        }

        .video-container iframe {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            border: none;
        }
    </style>
</head>
<body>

    <nav class="flex justify-between items-center px-8 py-6 border-b border-slate-900 bg-[#020617]/80 backdrop-blur-md sticky top-0 z-[1001]">
        <div class="text-blue-500 font-bold tracking-widest text-lg uppercase cursor-pointer" onclick="showPage('home')">LARION</div>
        <div class="cursor-pointer text-slate-400 text-xl" onclick="toggleMenu()"><i class="fas fa-bars"></i></div>
    </nav>

    <div id="nav-overlay">
        <div class="menu-label" style="margin-top: 0;">Community</div>
        <div class="menu-btn" onclick="showPage('showcases')"><i class="fas fa-video"></i> Showcases</div>
        <div class="menu-btn" onclick="showPage('reviews')"><i class="fas fa-star"></i> Reviews</div>
        <div class="menu-btn" onclick="showPage('home')"><i class="fas fa-home"></i> Home</div>

        <div class="menu-label">Legal</div>
        <div class="menu-btn" onclick="showPage('tos')"><i class="fas fa-file-alt"></i> Terms Of Service</div>

        <div class="menu-label">Support</div>
        <a href="https://discord.gg/zCXtU47zM" target="_blank" class="menu-btn" style="text-decoration:none">
            <i class="fab fa-discord"></i> Discord Server
        </a>
    </div>

    <main id="home" class="page-section active flex flex-col items-center justify-center min-h-[85vh] px-6 text-center">
        <div class="bg-blue-900/20 border border-blue-500/30 text-blue-400 text-[10px] font-bold px-4 py-1 rounded-full mb-6 tracking-widest uppercase">● Trusted by 190+ members</div>
        <h1 class="text-6xl font-extrabold mb-2 glow-blue text-blue-100 uppercase tracking-tighter">Larion</h1>
        <p class="text-slate-400 tracking-[0.2em] text-[10px] uppercase mb-6">The <span class="text-blue-500 font-bold">Best Serverside</span> on the market</p>
        <p class="text-slate-500 text-sm max-w-xs mb-8 leading-relaxed">The best internal serverside across 60+ Roblox games, and 24/7 support from moderators.</p>
        <a href="https://discord.gg/zCXtU47zM" target="_blank" class="glass-card px-10 py-3 rounded-lg flex items-center gap-3 hover:bg-slate-800 transition border-slate-700">
            <i class="fab fa-discord text-blue-400"></i> Join Community
        </a>
    </main>

    <main id="showcases" class="page-section py-16 px-6 max-w-5xl mx-auto">
        <h1 class="text-4xl font-bold mb-12 glow-blue text-blue-400 text-center">Showcases</h1>
        <div class="grid grid-cols-1 md:grid-cols-2 gap-8">
            <div class="glass-card p-2 rounded-2xl">
                <div class="video-container">
                    <iframe src="https://www.youtube.com/embed/j_N6GofD4zE" allowfullscreen></iframe>
                </div>
            </div>
            <div class="glass-card p-2 rounded-2xl">
                <div class="video-container">
                    <iframe src="https://www.youtube.com/embed/RkIPr5560b4" allowfullscreen></iframe>
                </div>
            </div>
            <div class="glass-card p-2 rounded-2xl">
                <div class="video-container">
                    <iframe src="https://www.youtube.com/embed/6_9o_v3oKys" allowfullscreen></iframe>
                </div>
            </div>
            <div class="glass-card p-2 rounded-2xl">
                <div class="video-container">
                    <iframe src="https://www.youtube.com/embed/PzG0B0e6N38" allowfullscreen></iframe>
                </div>
            </div>
        </div>
    </main>

    <main id="reviews" class="page-section py-16 px-6 max-w-2xl mx-auto">
        <h1 class="text-4xl font-bold mb-10 glow-blue text-blue-400 text-center">Reviews</h1>
        <div class="space-y-3">
            <div class="glass-card p-4 rounded-lg text-sm text-slate-300">8/10 good mods and owners, decent games, cheap, ui could be a bit better</div>
            <div class="glass-card p-4 rounded-lg text-sm text-slate-300">5/10 Ui good but no good games could be a bit better</div>
            <div class="glass-card p-4 rounded-lg text-sm text-slate-300 font-bold">BRO THIS IS COOL SHOULD DEFO BUY!</div>
            <div class="glass-card p-4 rounded-lg text-sm text-slate-300">10/10 i dont have it but its soooooo good</div>
            <div class="glass-card p-4 rounded-lg text-sm text-slate-300">Showcasing, it too bright and is too transparent, also the script has 2 copies...</div>
            <div class="glass-card p-4 rounded-lg text-sm text-slate-300">10/10 tuff ui tuff execution</div>
            <div class="glass-card p-4 rounded-lg text-sm text-slate-300">10/10 best logging games ever</div>
        </div>
    </main>

    <main id="tos" class="page-section py-16 px-6 max-w-2xl mx-auto">
        <h1 class="text-4xl font-bold mb-10 glow-blue text-blue-400 text-center">Terms Of Service</h1>
        <div class="space-y-2">
            <div class="glass-card p-3 rounded-lg text-[11px] text-slate-300">1 - No stealing games for your ss</div>
            <div class="glass-card p-3 rounded-lg text-[11px] text-slate-300">2 - No NSFW Scripts (as long as there not too Sexual)</div>
            <div class="glass-card p-3 rounded-lg text-[11px] text-slate-300">3 - No Nazi Scripts (Blacklist)</div>
            <div class="glass-card p-3 rounded-lg text-[11px] text-slate-300">4 - No Gore Scripts (Blacklist)</div>
            <div class="glass-card p-3 rounded-lg text-[11px] text-slate-300">5 - No Snitching (Warn)</div>
            <div class="glass-card p-3 rounded-lg text-[11px] text-slate-300">6 - No skiddy guis</div>
            <div class="glass-card p-3 rounded-lg text-[11px] text-slate-300">7 - No mass banning/kicking</div>
            <div class="glass-card p-3 rounded-lg text-[11px] text-slate-300">8 - No using any other executors other than larion</div>
        </div>
    </main>

    <script>
        function toggleMenu() {
            const menu = document.getElementById('nav-overlay');
            menu.style.display = (menu.style.display === 'block') ? 'none' : 'block';
        }

        function showPage(pageId) {
            document.querySelectorAll('.page-section').forEach(p => p.classList.remove('active'));
            document.getElementById(pageId).classList.add('active');
            document.getElementById('nav-overlay').style.display = 'none';
            window.scrollTo(0,0);
        }
    </script>
</body>
</html>
