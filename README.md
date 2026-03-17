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

        /* INFINITE PARADOX BACKGROUND */
        .tropical-bg { position: fixed; inset: 0; z-index: -2; background: linear-gradient(to bottom, #0f0c29, #24243e); animation: sky-drift 300s ease-in-out infinite alternate; }
        @keyframes sky-drift { 0% { background-color: #0f0c29; } 100% { background-color: #240b36; } }
        .palm-silhouette { position: fixed; bottom: -50px; opacity: 0.15; z-index: -1; pointer-events: none; filter: blur(2px); }
        .palm-left { left: -5%; width: 40%; animation: sway 8s ease-in-out infinite; }
        .palm-right { right: -5%; width: 35%; animation: sway 10s ease-in-out infinite reverse; }
        @keyframes sway { 0%, 100% { transform: rotate(-2deg) translateY(0); } 50% { transform: rotate(3deg) translateY(-10px); } }
        .ocean-mist { position: fixed; inset: 0; z-index: -1; background: radial-gradient(circle at 50% 120%, rgba(0, 255, 255, 0.05) 0%, transparent 50%); animation: pulse-mist 10s infinite alternate; }
        @keyframes pulse-mist { from { opacity: 0.2; } to { opacity: 0.5; } }

        /* LOADING PHASE FIX: UNCROPPED LOGOS */
        #overlay { position: fixed; inset: 0; background: #000; z-index: 9999; display: flex; align-items: center; justify-content: center; cursor: pointer; }
        #loading-screen { position: fixed; inset: 0; background: #000; z-index: 9998; display: none; flex-direction: column; align-items: center; justify-content: center; transition: opacity 1.5s ease; }
        @media (min-width: 768px) { #loading-screen { flex-direction: row; gap: 2rem; } }

        .logo-frame { 
            width: 220px; height: 220px; /* Increased size to prevent any edge clipping */
            display: flex; align-items: center; justify-content: center; 
            background: transparent; margin: 10px; 
            overflow: visible; 
        }

        .juice-img { width: 90%; height: auto; animation: pulse-logo 2s infinite; mix-blend-mode: screen; filter: drop-shadow(0 0 30px rgba(188, 19, 254, 0.6)); }
        .ovo-img { width: 90%; height: auto; animation: spin-logo 12s linear infinite; mix-blend-mode: screen; filter: drop-shadow(0 0 30px rgba(251, 191, 36, 0.4)); }
        @keyframes pulse-logo { 0%, 100% { transform: scale(0.95); opacity: 0.8; } 50% { transform: scale(1.05); opacity: 1; } }
        @keyframes spin-logo { from { transform: rotate(0deg); } to { transform: rotate(360deg); } }

        /* MAIN WRAPPER */
        #main-wrapper { opacity: 0; transition: opacity 2s ease-in-out; }
        .glass { background: rgba(0, 0, 0, 0.55); backdrop-filter: blur(25px); border: 1px solid rgba(255, 255, 255, 0.08); border-radius: 1.5rem; }
        .active-day { background: rgba(188, 19, 254, 0.25); border: 1px solid #bc13fe !important; color: #bc13fe; box-shadow: 0 0 25px rgba(188, 19, 254, 0.3); }

        /* GALLERY & TICKER */
        .ticker { white-space: nowrap; animation: ticker-move 35s linear infinite; }
        @keyframes ticker-move { 0% { transform: translateX(100%); } 100% { transform: translateX(-100%); } }
        .gallery-track { display: flex; width: max-content; animation: scroll-gallery 60s linear infinite; }
        @keyframes scroll-gallery { 0% { transform: translateX(0); } 100% { transform: translateX(-50%); } }
        .gallery-item { width: 280px; height: 380px; flex-shrink: 0; border-radius: 1rem; border: 1px solid rgba(255, 255, 255, 0.1); overflow: hidden; cursor: pointer; transition: 0.4s; }
        .gallery-item:hover { border-color: #bc13fe; transform: translateY(-10px); }

        /* MUSIC BAR */
        .music-bar { position: fixed; bottom: 0; left: 0; right: 0; background: rgba(0, 0, 0, 0.92); backdrop-filter: blur(20px); border-top: 1px solid rgba(255, 255, 255, 0.1); padding: 15px 25px; display: flex; align-items: center; justify-content: space-between; z-index: 100; }
        .live-dot { width: 8px; height: 8px; background: #ff0055; border-radius: 50%; margin-right: 12px; animation: blink 1.5s infinite; }
        @keyframes blink { 0%, 100% { opacity: 1; transform: scale(1); } 50% { opacity: 0.4; transform: scale(1.2); } }
        .visualizer { display: flex; align-items: flex-end; gap: 2px; height: 12px; margin-left: 15px; }
        .bar { width: 3px; background: #00ffff; animation: equalize 1s ease-in-out infinite; }
        .bar:nth-child(1) { height: 60%; animation-duration: 0.8s; }
        .bar:nth-child(2) { height: 100%; animation-duration: 1.2s; }
        .bar:nth-child(3) { height: 40%; animation-duration: 0.9s; }
        @keyframes equalize { 0%, 100% { transform: scaleY(0.5); } 50% { transform: scaleY(1); } }

        #easter-flash { position: fixed; inset: 0; z-index: 9000; opacity: 0; pointer-events: none; transition: 0.2s; }
        .flash-active { opacity: 0.4 !important; }
        .btn-glow { transition: 0.4s; box-shadow: 0 0 10px rgba(188, 19, 254, 0); }
        .btn-glow:hover { box-shadow: 0 0 40px rgba(188, 19, 254, 0.8); background: #bc13fe !important; color: white !important; }
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
            <h1 class="text-5xl md:text-8xl font-sync font-black uppercase italic text-white tracking-tighter drop-shadow-2xl">Searching for the Light</h1>
            <p class="mt-4 text-cyan-400 font-mono text-xs tracking-[1em] uppercase opacity-70">Tap to Transcend</p>
        </div>
    </div>

    <div id="loading-screen">
        <div class="logo-frame">
            <img src="juice-999.jpg" class="juice-img" alt="999">
        </div>
        <div class="flex flex-col items-center mx-10">
            <div class="w-48 h-[2px] bg-white/10 relative"><div id="progress-bar" class="absolute inset-y-0 left-0 bg-cyan-400" style="width: 0%"></div></div>
            <p class="mt-6 font-mono text-[10px] tracking-[0.8em] text-cyan-400 uppercase">Synchronizing...</p>
        </div>
        <div class="logo-frame">
            <img src="ovo-owl.png" class="ovo-img" alt="OVO">
        </div>
    </div>

    <div id="main-wrapper">
        <div class="w-full bg-black/40 backdrop-blur-md border-b border-white/10 py-3 overflow-hidden sticky top-0 z-50">
            <div class="ticker font-mono text-[10px] tracking-[0.5em] uppercase font-bold text-cyan-400 italic">999 x OVO // THE NEXUS // NO NEGATIVITY // LEGENDS NEVER DIE // </div>
        </div>

        <header class="flex flex-col items-center pt-24 pb-12 px-6 text-center">
            <img src="logo.png" alt="Sticker" class="w-56 md:w-80 mb-10 drop-shadow-[0_0_80px_rgba(0,255,255,0.4)]">
            <h1 class="text-5xl md:text-9xl font-sync font-bold uppercase italic tracking-tighter leading-none">The Inner Circle</h1>
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

            <div class="glass p-6 border-r-4 border-purple-500 flex flex-col gap-4">
                <h3 class="font-sync text-[10px] mb-2 text-purple-400 uppercase font-bold italic tracking-widest">Schedule</h3>
                <div id="day-tue" class="p-4 rounded font-mono text-[10px] uppercase border border-white/5 leading-tight">Every Tuesday</div>
                <div id="day-thu" class="p-4 rounded font-mono text-[10px] uppercase border border-white/5 leading-tight">Sometimes Thursday</div>
                <div id="day-wknd" class="p-4 rounded font-mono text-[10px] uppercase border border-white/5 leading-tight">Other Weekend</div>
            </div>

            <div class="glass p-8 flex items-center gap-5 border border-white/5">
                <div class="w-14 h-14 bg-gradient-to-tr from-purple-600 to-cyan-600 rounded-full flex items-center justify-center font-bold text-lg">JJ</div>
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
                <a href="https://vrchat.com/home/world/wrld_6b77c061-a1bf-48eb-b107-c4d944490198/info" target="_blank" class="text-center p-4 border border-white/5 hover:border-purple-500 rounded-xl group transition-all bg-white/5">
                    <p class="text-[10px] font-sync uppercase italic text-white group-hover:text-purple-400">McDonald's</p>
                    <p class="text-[8px] font-mono text-gray-400 uppercase mt-2 group-hover:text-white">Official Nexus VR Hangout. Enter the golden arches.</p>
                </a>
                <a href="https://vrchat.com/home/world/wrld_1a8b8684-3b19-4770-a4a7-288762f57b29/info" target="_blank" class="text-center p-4 border border-white/5 hover:border-blue-500 rounded-xl group transition-all bg-white/5">
                    <p class="text-[10px] font-sync uppercase italic text-white group-hover:text-blue-400">1's Optimized Box</p>
                    <p class="text-[8px] font-mono text-gray-400 uppercase mt-2 group-hover:text-white">High-performance zone. Sync your protocol here.</p>
                </a>
                <a href="https://vrchat.com/home/world/wrld_dd036610-a246-4f52-bf01-9d7cea3405d7/info" target="_blank" class="text-center p-4 border border-white/5 hover:border-red-500 rounded-xl group transition-all bg-white/5">
                    <p class="text-[10px] font-sync uppercase italic text-white group-hover:text-red-400">Among Us</p>
                    <p class="text-[8px] font-mono text-gray-400 uppercase mt-2 group-hover:text-white">The Rec Zone. Trust no one, survive the paradox.</p>
                </a>
            </div>
        </main>

        <footer class="text-center pb-48">
            <button onclick="window.open('https://vrchat.com/home/group/grp_e6ecca5a-828b-4706-9c23-db1723469436')" class="btn-glow bg-white text-black px-16 py-6 rounded-full font-sync text-lg font-bold uppercase italic">Join Collective</button>
            <p class="mt-24 font-sync text-[10px] tracking-[2.5em] opacity-20 uppercase">Legends Never Die</p>
        </footer>

        <div class="music-bar">
            <div class="flex items-center">
                <div class="live-dot"></div>
                <div class="flex flex-col">
                    <span class="text-[7px] font-sync text-gray-500 uppercase tracking-widest">Broadcasting Live</span>
                    <div class="flex items-center">
                        <span class="text-[11px] font-mono text-cyan-400 uppercase italic">999 x OVO: Tropical Paradox Sessions</span>
                        <div class="visualizer">
                            <div class="bar"></div>
                            <div class="bar"></div>
                            <div class="bar"></div>
                        </div>
                    </div>
                </div>
            </div>
            <div class="hidden md:flex gap-4">
                <div class="h-4 w-[1px] bg-white/20"></div>
                <span class="text-[10px] font-mono text-purple-400 tracking-tighter uppercase">High Fidelity Sync</span>
            </div>
        </div>
    </div>

    <script>
        function updateSchedule() {
            const now = new Date();
            const day = now.getDay();
            const tue = document.getElementById('day-tue');
            const thu = document.getElementById('day-thu');
            const wknd = document.getElementById('day-wknd');
            const status = document.getElementById('current-status');
            const subtext = document.getElementById('status-subtext');

            if (day === 2) { tue.classList.add('active-day'); status.innerText = "ACTIVE"; subtext.innerText = "Tuesday Sync Live"; } 
            else if (day === 4) { thu.classList.add('active-day'); status.innerText = "SYNCED"; subtext.innerText = "Thursday Mode"; } 
            else if (day === 0 || day === 6) { wknd.classList.add('active-day'); status.innerText = "WEEKEND"; subtext.innerText = "Collective Mode"; } 
            else { status.innerText = "STANDBY"; subtext.innerText = "Next sync: Tuesday"; }
        }

        function startLoading() {
            document.getElementById('overlay').style.display = 'none';
            const loadScreen = document.getElementById('loading-screen');
            const progress = document.getElementById('progress-bar');
            loadScreen.style.display = 'flex';
            updateSchedule();
            let width = 0;
            const interval = setInterval(() => {
                if (width >= 100) { clearInterval(interval); setTimeout(() => { loadScreen.style.opacity = '0'; setTimeout(() => { loadScreen.style.display = 'none'; document.getElementById('main-wrapper').style.opacity = '1'; }, 1000); }, 500); } 
                else { width += Math.random() * 8; progress.style.width = width + '%'; }
            }, 100);
        }

        function paradoxEffect() { const flash = document.getElementById('easter-flash'); flash.style.background = '#bc13fe'; flash.classList.add('flash-active'); setTimeout(() => flash.classList.remove('flash-active'), 300); }
        function ovoEffect() { const flash = document.getElementById('easter-flash'); flash.style.background = '#fbbf24'; flash.classList.add('flash-active'); setTimeout(() => flash.classList.remove('flash-active'), 300); }
    </script>
</body>
</html>
