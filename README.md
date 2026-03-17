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

        /* ENTRY SCREEN */
        #overlay { 
            position: fixed; inset: 0; 
            background: radial-gradient(circle at center, #110022 0%, #000000 100%); 
            z-index: 9999; display: flex; align-items: center; justify-content: center; cursor: pointer; 
        }

        /* LOADING PHASE */
        #loading-screen {
            position: fixed; inset: 0; background: #000; z-index: 9998;
            display: none; align-items: center; justify-content: center;
            transition: opacity 2s ease-in-out;
        }

        /* THE HARD FIX: CROP & SIZE */
        .logo-frame {
            width: 140px; /* Locked size - not too big, not too small */
            height: 140px;
            overflow: hidden;
            border-radius: 50%; /* This turns the square white background into a circle */
            display: flex;
            align-items: center;
            justify-content: center;
            background: black; /* Fills in the corners with black */
            border: 2px solid rgba(255,255,255,0.1);
        }

        .juice-img {
            width: 110%; /* Slight zoom to hide the white edges */
            height: auto;
            animation: pulse-logo 2s infinite;
            mix-blend-mode: screen; /* Removes pure white */
        }

        .ovo-img {
            width: 100%;
            height: auto;
            animation: spin-logo 10s linear infinite;
            mix-blend-mode: screen;
        }

        @keyframes pulse-logo {
            0%, 100% { transform: scale(0.95); opacity: 0.7; }
            50% { transform: scale(1.05); opacity: 1; }
        }

        @keyframes spin-logo {
            from { transform: rotate(0deg); }
            to { transform: rotate(360deg); }
        }

        /* MAIN WRAPPER FADE */
        #main-wrapper { opacity: 0; transition: opacity 3s ease; }

        .overload-bg { position: fixed; inset: 0; z-index: -2; background: radial-gradient(circle at 50% 50%, #1e1b4b, #000, #000); }
        .particles { position: fixed; inset: 0; z-index: -1; background-image: url('https://www.transparenttextures.com/patterns/stardust.png'); opacity: 0.3; }
        .glass { background: rgba(255, 255, 255, 0.02); backdrop-filter: blur(25px); border: 1px solid rgba(255, 255, 255, 0.1); border-radius: 1rem; }
        
        /* TICKER & GALLERY */
        .ticker-wrap { white-space: nowrap; animation: ticker-move 40s linear infinite; }
        @keyframes ticker-move { 0% { transform: translateX(100%); } 100% { transform: translateX(-100%); } }
        
        .gallery-track { display: flex; width: calc(300px * 20); animation: scroll-gallery 45s linear infinite; }
        @keyframes scroll-gallery { 0% { transform: translateX(0); } 100% { transform: translateX(calc(-300px * 10)); } }
        .gallery-item { width: 300px; height: 400px; flex-shrink: 0; border-radius: 1rem; border: 1px solid rgba(255, 255, 255, 0.1); overflow: hidden; }
        .gallery-item img { width: 100%; height: 100%; object-fit: cover; }

        #easter-flash { position: fixed; inset: 0; z-index: 9000; opacity: 0; pointer-events: none; }
        .flash-active { opacity: 0.4 !important; }
    </style>
</head>
<body>

    <div id="easter-flash"></div>

    <div id="overlay" onclick="startLoading()">
        <div class="text-center px-10">
            <h1 class="text-4xl md:text-6xl font-sync font-black tracking-tighter uppercase italic text-white">Searching for the Light</h1>
            <p class="mt-6 text-purple-500 font-mono text-xs tracking-[0.5em] uppercase opacity-70">Tap to Transcend</p>
        </div>
    </div>

    <div id="loading-screen">
        <div class="flex flex-col md:flex-row items-center justify-center gap-12 w-full px-10">
            
            <div class="logo-frame" style="box-shadow: 0 0 30px #bc13fe;">
                <img src="juice-999.jpg" class="juice-img" alt="999">
            </div>
            
            <div class="flex flex-col items-center">
                <div class="w-48 h-[1px] bg-white/10 relative">
                    <div id="progress-bar" class="absolute inset-y-0 left-0 bg-white transition-all duration-300" style="width: 0%"></div>
                </div>
                <p id="load-text" class="mt-4 font-mono text-[9px] tracking-[1em] uppercase text-gray-500">Decrypting...</p>
            </div>

            <div class="logo-frame" style="box-shadow: 0 0 30px #fbbf24;">
                <img src="ovo-owl.png" class="ovo-img" alt="OVO">
            </div>
            
        </div>
    </div>

    <div id="main-wrapper">
        <div class="overload-bg"></div>
        <div class="particles"></div>

        <div class="w-full bg-black/80 border-b border-white/10 py-2 overflow-hidden sticky top-0 z-50">
            <div class="ticker-wrap font-mono text-[10px] tracking-widest uppercase font-bold text-purple-400 italic">999 FOREVER // OVO SOUND // CONNECTING TO THE VOID // NO NEGATIVITY // </div>
        </div>

        <header class="flex flex-col items-center justify-center text-center pt-20 pb-12 px-6">
            <img src="logo.png" alt="Logo" class="w-64 md:w-80 mb-8 drop-shadow-[0_0_60px_rgba(168,85,247,0.7)]">
            <h1 class="text-5xl md:text-8xl font-sync font-bold tracking-tighter uppercase italic leading-none">The Inner Circle</h1>
        </header>

        <section class="w-full py-10 overflow-hidden bg-white/5 border-y border-white/10 mb-12">
            <div class="gallery-track gap-6 px-4">
                <div class="gallery-item" onclick="ovoEffect()"><img src="drake1.jpg"></div>
                <div class="gallery-item" onclick="ovoEffect()"><img src="drake2.jpg"></div>
                <div class="gallery-item" onclick="paradoxEffect()"><img src="juice1.jpg"></div>
                <div class="gallery-item" onclick="paradoxEffect()"><img src="juice2.jpg"></div>
                <div class="gallery-item" onclick="paradoxEffect()"><img src="juice3.jpg"></div>
                <div class="gallery-item" onclick="paradoxEffect()"><img src="juice4.jpg"></div>
                <div class="gallery-item" onclick="ovoEffect()"><img src="drake1.jpg"></div>
            </div>
        </section>

        <main class="max-w-7xl mx-auto px-6 grid grid-cols-1 md:grid-cols-4 gap-4 pb-32">
            <div class="glass p-8 md:col-span-2 border-l-8 border-purple-600">
                <h3 class="font-sync text-xs mb-4 text-purple-400 uppercase">Core Mission</h3>
                <p class="text-2xl font-light italic text-white/80 italic">"Turning negativity into something positive. Late night melodies, palm trees, and the family that never sleeps."</p>
            </div>
            <div class="glass p-6 text-center border-t-2 border-green-500">
                <h3 class="font-sync text-[10px] mb-4 text-gray-500 uppercase">System Health</h3>
                <div class="text-4xl font-black text-green-400 uppercase">Online</div>
            </div>
            <div class="glass p-6 border-r-8 border-blue-600">
                <h3 class="font-sync text-[10px] mb-4 text-blue-400 uppercase font-bold italic">Session</h3>
                <p class="font-mono text-[10px] uppercase">Always Active // 999 Live</p>
            </div>
            
            <div class="glass p-6 border border-purple-500/20 flex items-center gap-4">
                <div class="w-10 h-10 bg-purple-600 rounded-full flex items-center justify-center font-bold">JJ</div>
                <div><p class="font-sync text-sm italic">Jon Jon</p></div>
            </div>
            <div class="glass p-6 border border-blue-500/20 flex items-center gap-4">
                <div class="w-10 h-10 bg-blue-600 rounded-full flex items-center justify-center font-bold">AM</div>
                <div><p class="font-sync text-sm italic">Aubrey Graham</p></div>
            </div>

            <div class="glass p-8 md:col-span-2 grid grid-cols-3 gap-4 border-b border-white/5">
                <div class="text-center p-2"><p class="text-[10px] font-sync uppercase italic">McDonald's</p></div>
                <div class="text-center p-2"><p class="text-[10px] font-sync uppercase italic">Optimize Box</p></div>
                <div class="text-center p-2"><p class="text-[10px] font-sync uppercase italic">Among Us</p></div>
            </div>
        </main>

        <footer class="text-center py-20">
            <button onclick="window.open('https://vrchat.com/home/group/grp_e6ecca5a-828b-4706-9c23-db1723469436')" class="bg-white text-black px-12 py-6 rounded-full font-sync text-lg font-bold uppercase italic">Join Collective</button>
            <p class="mt-20 font-sync text-[10px] tracking-[2em] opacity-20 uppercase">Legends Never Die</p>
        </footer>
    </div>

    <script>
        function startLoading() {
            document.getElementById('overlay').style.display = 'none';
            const loadScreen = document.getElementById('loading-screen');
            const progress = document.getElementById('progress-bar');
            loadScreen.style.display = 'flex';

            let width = 0;
            const interval = setInterval(() => {
                if (width >= 100) {
                    clearInterval(interval);
                    setTimeout(() => { 
                        loadScreen.style.opacity = '0'; 
                        setTimeout(() => { 
                            loadScreen.style.display = 'none'; 
                            document.getElementById('main-wrapper').style.opacity = '1';
                        }, 2000);
                    }, 500);
                } else {
                    width += Math.random() * 5;
                    progress.style.width = width + '%';
                }
            }, 100);
        }

        const flash = document.getElementById('easter-flash');
        function paradoxEffect() { flash.style.background = '#bc13fe'; flash.classList.add('flash-active'); setTimeout(() => flash.classList.remove('flash-active'), 200); }
        function ovoEffect() { flash.style.background = '#fbbf24'; flash.classList.add('flash-active'); setTimeout(() => flash.classList.remove('flash-active'), 200); }
    </script>
</body>
</html>
