<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>JON JON & FRIENDS | THE NEXUS</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://fonts.googleapis.com/css2?family=Syncopate:wght@400;700&family=Inter:wght@300;900&family=Space+Mono&display=swap" rel="stylesheet">
    <style>
        body { font-family: 'Inter', sans-serif; background: #000; color: white; margin: 0; overflow-x: hidden; }
        .font-sync { font-family: 'Syncopate', sans-serif; }
        .font-mono { font-family: 'Space Mono', monospace; }

        /* INTRO OVERLAY */
        #overlay { 
            position: fixed; inset: 0; 
            background: radial-gradient(circle at center, #110022 0%, #000000 100%); 
            z-index: 9999; display: flex; align-items: center; justify-content: center; cursor: crosshair; 
        }

        /* NEW LOADING SCREEN */
        #loading-screen {
            position: fixed; inset: 0; background: #000; z-index: 9998;
            display: none; align-items: center; justify-content: center;
        }

        /* THE FIX: BACKGROUND REMOVAL & SIZING */
        .loading-logo {
            /* 1. Reset original colors (makes white background disappear against dark void) */
            mix-blend-mode: screen; 
            
            /* 2. Optional: If the mix-blend makes them too bright, force them back to black/gold */
            /* filter: invert(1) brightness(1.5); */ /* Uncomment if they become too invisible */

            /* 3. SIZE DOWN (Adjust 'max-width' if needed) */
            max-width: 150px; 
            height: auto; 
            opacity: 0; /* Starts invisible for fade-in */
            animation: fadeInLogo 1s forwards;
        }

        @keyframes fadeInLogo {
            to { opacity: 1; }
        }

        /* Pulse 999 */
        .juice-logo-fixed {
            animation: pulse-purple 2s infinite;
            color: #bc13fe; font-family: 'Syncopate'; font-weight: 900;
            text-shadow: 0 0 30px #bc13fe;
        }

        /* Spin Owl (If you are using the actual 🦉 emoji, keep this, else use the image class above) */
        .spin-owl {
            animation: spin-gold 4s linear infinite;
            filter: drop-shadow(0 0 20px #fbbf24);
        }

        @keyframes pulse-purple {
            0%, 100% { opacity: 0.3; transform: scale(0.9); }
            50% { opacity: 1; transform: scale(1.1); }
        }

        @keyframes spin-gold {
            from { transform: rotate(0deg); }
            to { transform: rotate(360deg); }
        }

        /* MAIN CONTENT STYLES */
        .overload-bg { position: fixed; inset: 0; z-index: -2; background: radial-gradient(circle at 50% 50%, #1e1b4b, #000, #000); }
        .particles { position: fixed; inset: 0; z-index: -1; background-image: url('https://www.transparenttextures.com/patterns/stardust.png'); opacity: 0.3; }
        .glass { background: rgba(255, 255, 255, 0.02); backdrop-filter: blur(25px); border: 1px solid rgba(255, 255, 255, 0.1); border-radius: 1rem; }
        .gallery-track { display: flex; width: calc(300px * 20); animation: scroll-gallery 45s linear infinite; }
        @keyframes scroll-gallery { 0% { transform: translateX(0); } 100% { transform: translateX(calc(-300px * 10)); } }
        .ticker { white-space: nowrap; animation: ticker-move 40s linear infinite; }
        @keyframes ticker-move { 0% { transform: translateX(100%); } 100% { transform: translateX(-100%); } }
        
        .gallery-item { width: 300px; height: 400px; flex-shrink: 0; border-radius: 1rem; border: 1px solid rgba(255, 255, 255, 0.1); overflow: hidden; cursor: pointer; transition: 0.5s ease; }
        .gallery-item img { width: 100%; height: 100%; object-fit: cover; pointer-events: none; }

        #easter-flash { position: fixed; inset: 0; z-index: 9000; opacity: 0; pointer-events: none; display: flex; align-items: center; justify-content: center; }
        .flash-active { opacity: 0.4 !important; }
    </style>
</head>
<body class="min-h-screen">

    <div id="easter-flash"></div>

    <div id="overlay" onclick="startLoading()">
        <div class="text-center px-10 max-w-3xl">
            <h1 class="text-4xl md:text-6xl font-sync font-black tracking-tighter uppercase italic text-white glitch">Searching for the Light</h1>
            <p class="mt-6 text-purple-500 font-mono text-xs md:text-sm tracking-[0.5em] uppercase opacity-70">The Abyss is only scary if you're afraid to find yourself</p>
            <div class="mt-12 flex flex-col items-center gap-2">
                <span class="w-[1px] h-16 bg-gradient-to-b from-purple-600 to-transparent animate-pulse"></span>
                <p class="text-[10px] font-mono text-gray-600 tracking-[1em] uppercase">Tap to Transcend</p>
            </div>
        </div>
    </div>

    <div id="loading-screen">
        <div class="flex items-center justify-between w-full max-w-5xl px-20">
            
            <div class="juice-logo-fixed">
                <img src="st,small,507x507-pad,600x600,f8f8f8.u2.jpg" alt="999" class="loading-logo">
            </div>
            
            <div class="flex flex-col items-center">
                <div class="w-48 h-[2px] bg-gray-900 overflow-hidden relative">
                    <div id="progress-bar" class="absolute inset-y-0 left-0 bg-white transition-all duration-300" style="width: 0%"></div>
                </div>
                <p id="load-text" class="mt-4 font-mono text-[10px] tracking-[1em] uppercase text-gray-500 italic">Syncing Duality...</p>
            </div>

            <div class="spin-owl">
                <img src="drake-juicy-j-ovo-owl-11563499796p8md9xraom.png" alt="OVO Owl" class="loading-logo">
            </div>
            
        </div>
    </div>

    <div id="main-wrapper" class="opacity-0 transition-opacity duration-1000">
        <div class="overload-bg"></div>
        <div class="particles"></div>

        <div class="w-full bg-black/80 border-b border-white/10 py-2 overflow-hidden sticky top-0 z-50 backdrop-blur-xl">
            <div id="system-ticker" class="ticker font-mono text-[10px] tracking-widest uppercase font-bold text-purple-400 italic">ESTABLISHED 2026 // 999 FOREVER // OVO SOUND SYSTEM // CONNECTING TO THE VOID // NO NEGATIVITY // LEGENDS NEVER DIE // </div>
        </div>

        <header class="flex flex-col items-center justify-center text-center pt-20 pb-12 px-6">
            <img src="logo.png" alt="Sticker" class="w-64 md:w-80 drop-shadow-[0_0_60px_rgba(168,85,247,0.7)] mb-8">
            <h1 class="text-5xl md:text-8xl font-sync font-bold tracking-tighter uppercase italic leading-none">The Inner Circle</h1>
        </header>

        <section class="w-full py-10 overflow-hidden bg-white/5 border-y border-white/10 mb-12">
            <div class="gallery-track gap-6 px-4">
                <div class="gallery-item" onclick="ovoEffect()"><img src="drake1.jpg"></div>
                <div class="gallery-item" onclick="ovoEffect()"><img src="drake2.jpg"></div>
                <div class="gallery-item" onclick="ovoEffect()"><img src="drake3.jpg"></div>
                <div class="gallery-item" onclick="paradoxEffect()"><img src="juice1.jpg"></div>
                <div class="gallery-item" onclick="paradoxEffect()"><img src="juice2.jpg"></div>
                <div class="gallery-item" onclick="paradoxEffect()"><img src="juice3.jpg"></div>
                <div class="gallery-item" onclick="paradoxEffect()"><img src="juice4.jpg"></div>
                <div class="gallery-item" onclick="paradoxEffect()"><img src="juice5.jpg"></div>
                <div class="gallery-item" onclick="paradoxEffect()"><img src="juice6.jpg"></div>
                <div class="gallery-item" onclick="paradoxEffect()"><img src="juice7.jpg"></div>
            </div>
        </section>

        <main class="max-w-7xl mx-auto px-6 grid grid-cols-1 md:grid-cols-4 gap-4 pb-32">
            <div class="glass p-8 md:col-span-2 border-l-8 border-purple-600">
                <h3 class="font-sync text-xs mb-4 text-purple-400">CORE MISSION</h3>
                <p class="text-2xl font-light italic leading-snug text-balance italic">"Turning negativity into something positive. Late night melodies, palm trees, and the family that never sleeps."</p>
            </div>
            <div class="glass p-6 text-center border-t-2 border-green-500">
                <h3 class="font-sync text-[10px] mb-4 text-gray-500 uppercase">System Health</h3>
                <div class="text-4xl font-black text-green-400 mb-2 uppercase">Online</div>
                <p class="text-[10px] font-mono text-gray-600 uppercase italic">Uptime 99.9%</p>
            </div>
            <div class="glass p-6 border-r-8 border-blue-600">
                <h3 class="font-sync text-[10px] mb-4 text-blue-400 uppercase font-bold italic">Uptime Session</h3>
                <p class="font-mono text-[10px] uppercase">Tuesdays Active<br>Sometimes Thursdays<br>Every Other Weekend</p>
            </div>
            <div class="glass p-6 border border-purple-500/20"><div class="flex items-center gap-4"><div class="w-12 h-12 bg-purple-600 rounded-full flex items-center justify-center font-bold">JJ</div><div><p class="font-sync text-sm italic">Jon Jon</p><p class="text-[10px] font-mono opacity-50 uppercase">(JonnyM85)</p></div></div></div>
            <div class="glass p-6 border border-blue-500/20"><div class="flex items-center gap-4"><div class="w-12 h-12 bg-blue-600 rounded-full flex items-center justify-center font-bold text-white">AM</div><div><p class="font-sync text-sm italic mb-1">Aubrey D Graham</p><p class="text-[10px] font-mono opacity-60 uppercase">Co-Owner / Mikey</p></div></div></div>
            <div class="glass p-8 md:col-span-2 grid grid-cols-3 gap-4 border-b border-white/5">
                <div class="text-center p-2"><p class="text-[9px] font-mono text-purple-400 uppercase italic">01 Hang</p><p class="text-[10px] font-sync uppercase italic">McDonald's</p></div>
                <div class="text-center p-2"><p class="text-[9px] font-mono text-blue-400 uppercase italic">02 Utility</p><p class="text-[10px] font-sync uppercase italic">Optimize Box</p></div>
                <div class="text-center p-2"><p class="text-[9px] font-mono text-red-400 uppercase italic">03 Rec</p><p class="text-[10px] font-sync uppercaseitalic">Among Us</p></div>
            </div>
        </main>

        <footer class="text-center py-20">
            <button onclick="window.open('https://vrchat.com/home/group/grp_e6ecca5a-828b-4706-9c23-db1723469436')" class="bg-white text-black px-12 py-6 rounded-full font-sync text-lg font-bold hover:scale-110 transition-all uppercase italic">Join Collective</button>
            <p class="mt-20 font-sync text-[10px] tracking-[2em] opacity-20 uppercase">Legends Never Die</p>
        </footer>
    </div>

    <script>
        function startLoading() {
            document.getElementById('overlay').style.display = 'none';
            const loadScreen = document.getElementById('loading-screen');
            const progress = document.getElementById('progress-bar');
            const loadText = document.getElementById('load-text');
            loadScreen.style.display = 'flex';

            let width = 0;
            const interval = setInterval(() => {
                if (width >= 100) {
                    clearInterval(interval);
                    loadText.innerText = "ACCESS GRANTED";
                    setTimeout(() => { 
                        loadScreen.style.opacity = '0'; 
                        setTimeout(() => { loadScreen.style.display = 'none'; }, 500); 
                        // Show main site
                        document.getElementById('main-wrapper').style.opacity = '1';
                    }, 1000);
                } else {
                    width += Math.random() * 5;
                    progress.style.width = width + '%';
                    if(width > 40) loadText.innerText = "PARADOX PROTOCOL...";
                    if(width > 75) loadText.innerText = "OVO SYSTEM SYNC...";
                }
            }, 100);
        }

        const flash = document.getElementById('easter-flash');
        function paradoxEffect() {
            flash.style.background = '#bc13fe';
            flash.classList.add('flash-active');
            setTimeout(() => flash.classList.remove('flash-active'), 200);
        }
        function ovoEffect() {
            flash.style.background = '#fbbf24';
            flash.classList.add('flash-active');
            setTimeout(() => flash.classList.remove('flash-active'), 200);
        }
    </script>
</body>
</html>
