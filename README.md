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

        /* 1. ENTRY SCREEN */
        #overlay { 
            position: fixed; inset: 0; 
            background: radial-gradient(circle at center, #110022 0%, #000000 100%); 
            z-index: 9999; display: flex; align-items: center; justify-content: center; cursor: pointer; 
        }

        /* 2. LOADING SCREEN - RESPONSIVE STACKING */
        #loading-screen {
            position: fixed; inset: 0; background: #000; z-index: 9998;
            display: none; flex-direction: column; align-items: center; justify-content: center;
            transition: opacity 1.5s ease;
        }
        @media (min-width: 768px) { #loading-screen { flex-direction: row; } }

        .logo-frame {
            width: 120px; height: 120px;
            overflow: hidden; border-radius: 50%;
            display: flex; align-items: center; justify-content: center;
            background: black; border: 2px solid rgba(255,255,255,0.1);
            margin: 20px;
        }

        .juice-img { width: 110%; height: auto; animation: pulse-logo 2s infinite; mix-blend-mode: screen; }
        .ovo-img { width: 100%; height: auto; animation: spin-logo 10s linear infinite; mix-blend-mode: screen; }

        @keyframes pulse-logo { 0%, 100% { transform: scale(0.95); opacity: 0.7; } 50% { transform: scale(1.05); opacity: 1; } }
        @keyframes spin-logo { from { transform: rotate(0deg); } to { transform: rotate(360deg); } }

        /* 3. MAIN SITE FADE IN */
        #main-wrapper { opacity: 0; transition: opacity 3s ease-in-out; }

        .overload-bg { position: fixed; inset: 0; z-index: -2; background: radial-gradient(circle at 50% 50%, #1e1b4b, #000, #000); }
        .glass { background: rgba(255, 255, 255, 0.03); backdrop-filter: blur(20px); border: 1px solid rgba(255, 255, 255, 0.1); border-radius: 1.5rem; }
        
        /* GALLERY SCROLLING */
        .gallery-track { display: flex; width: max-content; animation: scroll-gallery 50s linear infinite; }
        @keyframes scroll-gallery { 0% { transform: translateX(0); } 100% { transform: translateX(-50%); } }
        .gallery-item { width: 260px; height: 350px; flex-shrink: 0; border-radius: 1rem; border: 1px solid rgba(255, 255, 255, 0.1); overflow: hidden; cursor: pointer; transition: transform 0.3s; }
        .gallery-item:active { transform: scale(0.95); }
        .gallery-item img { width: 100%; height: 100%; object-fit: cover; }

        /* FLASH EFFECT LAYER */
        #easter-flash { position: fixed; inset: 0; z-index: 9000; opacity: 0; pointer-events: none; transition: opacity 0.2s; }
        .flash-active { opacity: 0.5 !important; }

        .ticker { white-space: nowrap; animation: ticker-move 30s linear infinite; }
        @keyframes ticker-move { 0% { transform: translateX(100%); } 100% { transform: translateX(-100%); } }
    </style>
</head>
<body>

    <div id="easter-flash"></div>

    <div id="overlay" onclick="startLoading()">
        <div class="text-center px-6">
            <h1 class="text-3xl md:text-6xl font-sync font-black uppercase italic text-white tracking-tighter">Searching for the Light</h1>
            <p class="mt-4 text-purple-500 font-mono text-xs tracking-widest uppercase">Tap to Transcend</p>
        </div>
    </div>

    <div id="loading-screen">
        <div class="logo-frame" style="box-shadow: 0 0 40px #bc13fe;">
            <img src="juice-999.jpg" class="juice-img" alt="999">
        </div>
        
        <div class="flex flex-col items-center mx-10">
            <div class="w-40 h-[1px] bg-white/20 relative">
                <div id="progress-bar" class="absolute inset-y-0 left-0 bg-white" style="width: 0%"></div>
            </div>
            <p id="load-text" class="mt-4 font-mono text-[10px] tracking-[0.8em] text-gray-500 uppercase">Syncing...</p>
        </div>

        <div class="logo-frame" style="box-shadow: 0 0 40px #fbbf24;">
            <img src="ovo-owl.png" class="ovo-img" alt="OVO">
        </div>
    </div>

    <div id="main-wrapper">
        <div class="overload-bg"></div>

        <div class="w-full bg-black/80 border-b border-white/10 py-2 overflow-hidden sticky top-0 z-50">
            <div class="ticker font-mono text-[9px] tracking-widest uppercase font-bold text-purple-400 italic">999 FOREVER // OVO SOUND SYSTEM // CONNECTING... // NO NEGATIVITY // </div>
        </div>

        <header class="flex flex-col items-center pt-12 pb-8 px-6 text-center">
            <img src="logo.png" alt="Sticker" class="w-48 md:w-72 mb-6 drop-shadow-[0_0_40px_rgba(168,85,247,0.6)]">
            <h1 class="text-4xl md:text-7xl font-sync font-bold uppercase italic tracking-tighter">The Inner Circle</h1>
        </header>

        <section class="w-full py-8 overflow-hidden bg-white/5 border-y border-white/5 mb-8">
            <div class="gallery-track gap-4 px-4">
                <div class="gallery-item" onclick="ovoEffect()"><img src="drake1.jpg"></div>
                <div class="gallery-item" onclick="ovoEffect()"><img src="drake2.jpg"></div>
                <div class="gallery-item" onclick="ovoEffect()"><img src="drake3.jpg"></div>
                <div class="gallery-item" onclick="paradoxEffect()"><img src="juice1.jpg"></div>
                <div class="gallery-item" onclick="paradoxEffect()"><img src="juice2.jpg"></div>
                <div class="gallery-item" onclick="paradoxEffect()"><img src="juice3.jpg"></div>
                <div class="gallery-item" onclick="paradoxEffect()"><img src="juice4.jpg"></div>
                <div class="gallery-item" onclick="ovoEffect()"><img src="drake1.jpg"></div>
                <div class="gallery-item" onclick="paradoxEffect()"><img src="juice1.jpg"></div>
            </div>
        </section>

        <main class="max-w-6xl mx-auto px-6 grid grid-cols-1 md:grid-cols-4 gap-4 pb-24">
            <div class="glass p-8 md:col-span-2 border-l-4 border-purple-600">
                <h3 class="font-sync text-[10px] mb-4 text-purple-400 uppercase tracking-widest">Core Mission</h3>
                <p class="text-xl md:text-2xl font-light italic text-white/90">"Turning negativity into something positive. Late night melodies, palm trees, and the family that never sleeps."</p>
            </div>

            <div class="glass p-6 text-center border-t-2 border-green-500">
                <h3 class="font-sync text-[10px] mb-2 text-gray-500 uppercase">System Status</h3>
                <div class="text-3xl font-black text-green-400 uppercase">Online</div>
                <p class="text-[9px] font-mono text-gray-600 uppercase">Uptime 99.9%</p>
            </div>

            <div class="glass p-6 border-r-4 border-blue-600">
                <h3 class="font-sync text-[10px] mb-4 text-blue-400 uppercase font-bold">Session</h3>
                <p class="font-mono text-[10px] uppercase text-white/70">Tuesdays Active<br>Thursdays Variable<br>Weekend Collective</p>
            </div>

            <div class="glass p-6 flex items-center gap-4">
                <div class="w-10 h-10 bg-purple-600 rounded-full flex items-center justify-center font-bold text-xs">JJ</div>
                <div>
                    <p class="font-sync text-xs italic">Jon Jon</p>
                    <p class="text-[9px] font-mono text-purple-400 uppercase font-bold">Owner</p>
                    <p class="text-[8px] font-mono opacity-40 uppercase">JonnyM85</p>
                </div>
            </div>

            <div class="glass p-6 flex items-center gap-4">
                <div class="w-10 h-10 bg-blue-600 rounded-full flex items-center justify-center font-bold text-xs">AM</div>
                <div>
                    <p class="font-sync text-xs italic">Aubrey Graham</p>
                    <p class="text-[9px] font-mono text-blue-400 uppercase font-bold">Co-Owner</p>
                    <p class="text-[8px] font-mono opacity-40 uppercase">Mikey</p>
                </div>
            </div>

            <div class="glass p-6 md:col-span-2 grid grid-cols-3 gap-2">
                <div class="text-center"><p class="text-[8px] font-mono text-gray-500 uppercase">01</p><p class="text-[10px] font-sync uppercase italic">McDonald's</p></div>
                <div class="text-center"><p class="text-[8px] font-mono text-gray-500 uppercase">02</p><p class="text-[10px] font-sync uppercase italic">Optimize Box</p></div>
                <div class="text-center"><p class="text-[8px] font-mono text-gray-500 uppercase">03</p><p class="text-[10px] font-sync uppercase italic">Among Us</p></div>
            </div>
        </main>

        <footer class="text-center pb-20">
            <button onclick="window.open('https://vrchat.com/home/group/grp_e6ecca5a-828b-4706-9c23-db1723469436')" class="bg-white text-black px-10 py-5 rounded-full font-sync text-sm font-bold uppercase italic hover:scale-105 transition-transform">Join Collective</button>
            <p class="mt-12 font-sync text-[8px] tracking-[1.5em] opacity-20 uppercase">Legends Never Die</p>
        </footer>
    </div>

    <script>
        function startLoading() {
            document.getElementById('overlay').style.display = 'none';
            const loadScreen = document.getElementById('loading-screen');
            const progress = document.getElementById('progress-bar');
            const main = document.getElementById('main-wrapper');
            loadScreen.style.display = 'flex';

            let width = 0;
            const interval = setInterval(() => {
                if (width >= 100) {
                    clearInterval(interval);
                    setTimeout(() => { 
                        loadScreen.style.opacity = '0'; 
                        setTimeout(() => { 
                            loadScreen.style.display = 'none'; 
                            main.style.opacity = '1';
                        }, 1500);
                    }, 500);
                } else {
                    width += Math.random() * 8;
                    progress.style.width = width + '%';
                }
            }, 150);
        }

        const flash = document.getElementById('easter-flash');
        // FLASH PURPLE FOR JUICE
        function paradoxEffect() {
            flash.style.background = '#bc13fe';
            flash.classList.add('flash-active');
            setTimeout(() => flash.classList.remove('flash-active'), 300);
        }
        // FLASH GOLD FOR DRAKE
        function ovoEffect() {
            flash.style.background = '#fbbf24';
            flash.classList.add('flash-active');
            setTimeout(() => flash.classList.remove('flash-active'), 300);
        }
    </script>
</body>
</html>
