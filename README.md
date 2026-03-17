<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>JON JON & FRIENDS | THE NEXUS</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://fonts.googleapis.com/css2?family=Syncopate:wght@400;700&family=Inter:wght@300;900&family=Space+Mono&display=swap" rel="stylesheet">
    <style>
        body { font-family: 'Inter', sans-serif; background: #05000a; color: white; margin: 0; overflow-x: hidden; }
        .font-sync { font-family: 'Syncopate', sans-serif; }
        .font-mono { font-family: 'Space Mono', monospace; }

        /* 1. THE 5-MINUTE COLOR DRIFT */
        .tropical-bg {
            position: fixed; inset: 0; z-index: -2;
            background: linear-gradient(to bottom, #0f0c29, #24243e);
            animation: sky-drift 300s ease-in-out infinite alternate;
        }
        @keyframes sky-drift {
            0% { background-color: #0f0c29; } 
            100% { background-color: #240b36; } 
        }

        /* 2. SWAYING PALMS */
        .palm-silhouette { position: fixed; bottom: -50px; opacity: 0.15; z-index: -1; pointer-events: none; filter: blur(2px); }
        .palm-left { left: -5%; width: 40%; animation: sway 8s ease-in-out infinite; }
        .palm-right { right: -5%; width: 35%; animation: sway 10s ease-in-out infinite reverse; }
        @keyframes sway { 0%, 100% { transform: rotate(-2deg) translateY(0); } 50% { transform: rotate(3deg) translateY(-10px); } }
        
        .ocean-mist { position: fixed; inset: 0; z-index: -1; background: radial-gradient(circle at 50% 120%, rgba(0, 255, 255, 0.05) 0%, transparent 50%); animation: pulse-mist 10s infinite alternate; }

        /* 3. LOGO CIRCLES */
        #overlay { position: fixed; inset: 0; background: #000; z-index: 9999; display: flex; align-items: center; justify-content: center; cursor: pointer; }
        #loading-screen { position: fixed; inset: 0; background: #000; z-index: 9998; display: none; flex-direction: column; align-items: center; justify-content: center; transition: opacity 1.5s ease; }
        @media (min-width: 768px) { #loading-screen { flex-direction: row; gap: 4rem; } }

        .logo-circle { 
            width: 180px; height: 180px; 
            border-radius: 50%; 
            border: 3px solid rgba(255, 255, 255, 0.15);
            overflow: hidden;
            display: flex; align-items: center; justify-content: center;
            background: #000;
            box-shadow: 0 0 40px rgba(188, 19, 254, 0.2);
        }
        .juice-img { width: 100%; height: 100%; object-fit: cover; animation: pulse-logo 2s infinite; mix-blend-mode: screen; }
        .ovo-img { width: 100%; height: 100%; object-fit: cover; animation: spin-logo 15s linear infinite; mix-blend-mode: screen; }
        @keyframes pulse-logo { 0%, 100% { transform: scale(1); opacity: 0.8; } 50% { transform: scale(1.08); opacity: 1; } }
        @keyframes spin-logo { from { transform: rotate(0deg); } to { transform: rotate(360deg); } }

        /* 4. MAIN LAYOUT */
        #main-wrapper { opacity: 0; transition: opacity 2s ease-in-out; }
        .glass { background: rgba(0, 0, 0, 0.65); backdrop-filter: blur(25px); border: 1px solid rgba(255, 255, 255, 0.1); border-radius: 1.5rem; }
        .active-day { background: rgba(188, 19, 254, 0.25); border: 1px solid #bc13fe !important; color: #bc13fe; box-shadow: 0 0 25px rgba(188, 19, 254, 0.3); }

        .ticker { white-space: nowrap; animation: ticker-move 35s linear infinite; }
        @keyframes ticker-move { 0% { transform: translateX(100%); } 100% { transform: translateX(-100%); } }
        
        .gallery-track { display: flex; width: max-content; animation: scroll-gallery 60s linear infinite; }
        @keyframes scroll-gallery { 0% { transform: translateX(0); } 100% { transform: translateX(-50%); } }
        .gallery-item { width: 300px; height: 400px; flex-shrink: 0; border-radius: 1rem; border: 1px solid rgba(255, 255, 255, 0.1); overflow: hidden; }
        .gallery-item img { width: 100%; height: 100%; object-fit: cover; }

        /* 5. FIX: SCHEDULE BOX ROOM */
        .schedule-container {
            min-width: 200px; /* Forces enough width for the word 'Schedule' */
        }

        .location-card {
            min-height: 140px;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            text-align: center;
            padding: 1.5rem;
            transition: 0.4s cubic-bezier(0.4, 0, 0.2, 1);
            border: 1px solid rgba(255, 255, 255, 0.05);
            background: rgba(255,255,255,0.03);
        }
        .location-card:hover { background: rgba(255,255,255,0.08); border-color: rgba(255,255,255,0.3); transform: translateY(-5px); }

        /* 6. MUSIC BAR */
        .music-bar { position: fixed; bottom: 0; left: 0; right: 0; background: rgba(0, 0, 0, 0.95); backdrop-filter: blur(20px); border-top: 1px solid rgba(255, 255, 255, 0.1); padding: 15px 25px; display: flex; align-items: center; justify-content: space-between; z-index: 100; }
        .visualizer { display: flex; align-items: flex-end; gap: 2px; height: 12px; }
        .bar { width: 3px; background: #00ffff; animation: equalize 1s ease-in-out infinite; }
        @keyframes equalize { 0%, 100% { transform: scaleY(0.5); } 50% { transform: scaleY(1); } }

        #easter-flash { position: fixed; inset: 0; z-index: 9000; opacity: 0; pointer-events: none; transition: 0.2s; }
        .flash-active { opacity: 0.4 !important; }
    </style>
</head>
<body>

    <div id="easter-flash"></div>
    <div class="tropical-bg"></div>
    <div class="ocean-mist"></div>
    
    <svg class="palm-silhouette palm-left" viewBox="0 0 512 512" fill="black"><path d="M480 448c-100-30-150-120-150-120s-20-40-20-100c0-80 50-150 50-150S300 120 256 200c-44-80-104-122-104-122s50 70 50 150c0 60-20 100-20 100S132 418 32 448h448z"/></svg>
    <svg class="palm-silhouette palm-right" viewBox="0 0 512 512" fill="black"><path d="M480 448c-100-30-150-120-150-120s-20-40-20-100c0-80 50-150 50-150S300 120 256 200c-44-80-104-122-104-122s50 70 50 150c0 60-20 100-20 100S132 418 32 448h448z"/></svg>

    <div id="overlay" onclick="startLoading()">
        <div class="text-center px-6">
            <h1 class="text-5xl md:text-8xl font-sync font-black uppercase italic text-white tracking-tighter">Searching for the Light</h1>
            <p class="mt-4 text-cyan-400 font-mono text-xs tracking-[1em] uppercase opacity-70">Tap to Enter</p>
        </div>
    </div>

    <div id="loading-screen">
        <div class="logo-circle"><img src="juice-999.jpg" class="juice-img"></div>
        <div class="flex flex-col items-center mx-10 my-10">
            <div class="w-48 h-[2px] bg-white/10 relative"><div id="progress-bar" class="absolute inset-y-0 left-0 bg-cyan-400" style="width: 0%"></div></div>
            <p class="mt-6 font-mono text-[10px] tracking-[0.8em] text-cyan-400 uppercase">Synchronizing</p>
        </div>
        <div class="logo-circle"><img src="ovo-owl.png" class="ovo-img"></div>
    </div>

    <div id="main-wrapper">
        <div class="w-full bg-black/40 py-3 overflow-hidden sticky top-0 z-50 border-b border-white/5">
            <div class="ticker font-mono text-[10px] tracking-[0.5em] uppercase font-bold text-cyan-400 italic">999 x OVO // THE NEXUS // NO NEGATIVITY // LEGENDS NEVER DIE // </div>
        </div>

        <header class="flex flex-col items-center pt-24 pb-12 px-6 text-center">
            <img src="logo.png" class="w-64 md:w-80 mb-10 drop-shadow-[0_0_80px_rgba(0,255,255,0.4)]">
            <h1 class="text-5xl md:text-9xl font-sync font-bold uppercase italic tracking-tighter">The Inner Circle</h1>
        </header>

        <section class="w-full py-12 overflow-hidden bg-black/20 border-y border-white/5 mb-16">
            <div class="gallery-track gap-6 px-4">
                <div class="gallery-item" onclick="ovoEffect()"><img src="drake1.jpg"></div>
                <div class="gallery-item" onclick="paradoxEffect()"><img src="juice1.jpg"></div>
                <div class="gallery-item" onclick="ovoEffect()"><img src="drake2.jpg"></div>
                <div class="gallery-item" onclick="paradoxEffect()"><img src="juice2.jpg"></div>
            </div>
        </section>

        <main class="max-w-6xl mx-auto px-6 grid grid-cols-1 md:grid-cols-4 gap-6 pb-48">
            <div class="glass p-10 md:col-span-2 border-l-4 border-cyan-400">
                <h3 class="font-sync text-[10px] mb-6 text-cyan-400 uppercase tracking-[0.3em]">Core Mission</h3>
                <p class="text-2xl md:text-3xl font-light italic text-white/90">"Turning negativity into something positive. Late night melodies, palm trees, and the family that never sleeps."</p>
            </div>

            <div class="glass p-6 text-center border-t-2 border-green-400">
                <h3 class="font-sync text-[10px] mb-2 text-gray-500 uppercase">System Status</h3>
                <div id="current-status" class="text-4xl font-black text-green-400 uppercase italic">Online</div>
                <p id="status-subtext" class="text-[9px] font-mono text-gray-600 uppercase mt-2 italic tracking-widest">Active Protocol</p>
            </div>

            <div class="glass p-6 border-r-4 border-purple-500 flex flex-col gap-3 schedule-container">
                <h3 class="font-sync text-[10px] mb-2 text-purple-400 uppercase font-bold italic tracking-widest whitespace-nowrap">Schedule</h3>
                <div id="day-tue" class="p-3 rounded font-mono text-[10px] uppercase border border-white/5">Every Tuesday</div>
                <div id="day-thu" class="p-3 rounded font-mono text-[10px] uppercase border border-white/5">Sometimes Thursday</div>
                <div id="day-wknd" class="p-3 rounded font-mono text-[10px] uppercase border border-white/5">Other Weekend</div>
            </div>

            <div class="glass p-8 flex items-center gap-5 border border-white/5">
                <div class="w-14 h-14 bg-gradient-to-tr from-purple-600 to-indigo-600 rounded-full flex items-center justify-center font-bold text-lg">JJ</div>
                <div>
                    <p class="font-sync text-sm italic">Jon Jon</p>
                    <p class="text-[10px] font-mono text-purple-400 uppercase font-black">Owner</p>
                    <p class="text-[8px] font-mono opacity-50 uppercase mt-1">JonnyM85</p>
                </div>
            </div>

            <div class="glass p-8 flex items-center gap-5 border border-white/5">
                <div class="w-14 h-14 bg-gradient-to-tr from-blue-600 to-indigo-600 rounded-full flex items-center justify-center font-bold text-lg">AM</div>
                <div>
                    <p class="font-sync text-sm italic">Aubrey Graham</p>
                    <p class="text-[10px] font-mono text-blue-400 uppercase font-black">Co-Owner</p>
                    <p class="text-[8px] font-mono opacity-50 uppercase mt-1">Mikey</p>
                </div>
            </div>

            <div class="glass p-8 md:col-span-2 grid grid-cols-1 md:grid-cols-3 gap-6">
                <a href="https://vrchat.com/home/world/wrld_6b77c061-a1bf-48eb-b107-c4d944490198/info" target="_blank" class="location-card rounded-2xl">
                    <p class="text-[11px] font-sync uppercase italic text-white tracking-widest">McDonald's</p>
                    <p class="text-[8px] font-mono text-gray-500 uppercase mt-3">The Nexus Hangout</p>
                </a>
                <a href="https://vrchat.com/home/world/wrld_1a8b8684-3b19-4770-a4a7-288762f57b29/info" target="_blank" class="location-card rounded-2xl">
                    <p class="text-[11px] font-sync uppercase italic text-white tracking-widest whitespace-nowrap">1's Optimized Box</p>
                    <p class="text-[8px] font-mono text-gray-500 uppercase mt-3">Utility Zone</p>
                </a>
                <a href="https://vrchat.com/home/world/wrld_dd036610-a246-4f52-bf01-9d7cea3405d7/info" target="_blank" class="location-card rounded-2xl">
                    <p class="text-[11px] font-sync uppercase italic text-white tracking-widest">Among Us</p>
                    <p class="text-[8px] font-mono text-gray-500 uppercase mt-3">Rec Zone</p>
                </a>
            </div>
        </main>

        <footer class="text-center pb-48">
            <button onclick="window.open('https://vrchat.com/home/group/grp_e6ecca5a-828b-4706-9c23-db1723469436')" class="bg-white text-black px-16 py-6 rounded-full font-sync text-lg font-bold uppercase italic hover:scale-105 transition-transform shadow-[0_0_30px_rgba(255,255,255,0.2)]">Join Collective</button>
        </footer>

        <div class="music-bar">
            <div class="flex items-center">
                <div class="w-2 h-2 bg-red-600 rounded-full mr-3 animate-pulse"></div>
                <div class="flex flex-col">
                    <span class="text-[11px] font-mono text-cyan-400 uppercase italic">999 x OVO: Tropical Paradox Sessions</span>
                    <div class="visualizer mt-1">
                        <div class="bar" style="animation-duration: 0.8s"></div>
                        <div class="bar" style="animation-duration: 1.2s"></div>
                        <div class="bar" style="animation-duration: 0.9s"></div>
                    </div>
                </div>
            </div>
        </div>
    </div>

    <script>
        function updateSchedule() {
            const day = new Date().getDay();
            if (day === 2) document.getElementById('day-tue').classList.add('active-day');
            else if (day === 4) document.getElementById('day-thu').classList.add('active-day');
            else if (day === 0 || day === 6) document.getElementById('day-wknd').classList.add('active-day');
        }

        function startLoading() {
            document.getElementById('overlay').style.display = 'none';
            const loadScreen = document.getElementById('loading-screen');
            const progress = document.getElementById('progress-bar');
            loadScreen.style.display = 'flex';
            updateSchedule();
            let width = 0;
            const interval = setInterval(() => {
                if (width >= 100) { 
                    clearInterval(interval); 
                    setTimeout(() => { 
                        loadScreen.style.opacity = '0'; 
                        setTimeout(() => { loadScreen.style.display = 'none'; document.getElementById('main-wrapper').style.opacity = '1'; }, 1000); 
                    }, 500); 
                } else { width += Math.random() * 10; progress.style.width = width + '%'; }
            }, 120);
        }

        function paradoxEffect() { const flash = document.getElementById('easter-flash'); flash.style.background = '#bc13fe'; flash.classList.add('flash-active'); setTimeout(() => flash.classList.remove('flash-active'), 300); }
        function ovoEffect() { const flash = document.getElementById('easter-flash'); flash.style.background = '#fbbf24'; flash.classList.add('flash-active'); setTimeout(() => flash.classList.remove('flash-active'), 300); }
    </script>
</body>
</html>
