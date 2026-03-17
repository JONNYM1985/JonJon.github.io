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

        /* NEBULA BACKGROUND */
        .overload-bg {
            position: fixed; inset: 0; z-index: -2;
            background: radial-gradient(circle at 50% 50%, #1e1b4b, #000, #000);
        }
        .particles {
            position: fixed; inset: 0; z-index: -1;
            background-image: url('https://www.transparenttextures.com/patterns/stardust.png');
            opacity: 0.3; animation: pulse 10s infinite;
        }
        @keyframes pulse { 0%, 100% { opacity: 0.2; } 50% { opacity: 0.5; } }

        .glass { 
            background: rgba(255, 255, 255, 0.02); 
            backdrop-filter: blur(25px); 
            border: 1px solid rgba(255, 255, 255, 0.1); 
            border-radius: 1rem;
        }

        /* 10-IMAGE CUSTOM GALLERY TRACK */
        .gallery-track {
            display: flex;
            width: calc(300px * 20); /* Doubled for infinite loop */
            animation: scroll-gallery 45s linear infinite;
        }
        @keyframes scroll-gallery {
            0% { transform: translateX(0); }
            100% { transform: translateX(calc(-300px * 10)); }
        }

        .ticker { white-space: nowrap; animation: ticker-move 40s linear infinite; }
        @keyframes ticker-move { 0% { transform: translateX(100%); } 100% { transform: translateX(-100%); } }

        #overlay { position: fixed; inset: 0; background: black; z-index: 9999; display: flex; align-items: center; justify-content: center; cursor: pointer; }
        
        .gallery-item {
            width: 300px; height: 400px; flex-shrink: 0; border-radius: 1rem; 
            border: 1px solid rgba(255, 255, 255, 0.1); overflow: hidden;
            transition: 0.5s ease;
        }
        .gallery-item:hover { border-color: #a855f7; transform: scale(1.05); z-index: 10; }
        .gallery-item img { width: 100%; height: 100%; object-cover: cover; }
    </style>
</head>
<body class="min-h-screen">
    <div class="overload-bg"></div>
    <div class="particles"></div>

    <div id="overlay" onclick="this.style.display='none'">
        <div class="text-center">
            <h1 class="text-5xl font-sync font-black tracking-widest uppercase animate-pulse">Accessing Vault</h1>
            <p class="mt-4 text-xs font-mono tracking-[1em] text-purple-500 uppercase">10GB Energy Loaded</p>
        </div>
    </div>

    <div class="w-full bg-black/80 border-b border-white/10 py-2 overflow-hidden sticky top-0 z-50 backdrop-blur-xl">
        <div class="ticker font-mono text-[10px] tracking-widest uppercase font-bold text-purple-400">
            ESTABLISHED 2026 // 999 FOREVER // OVO SOUND SYSTEM // CONNECTING TO THE VOID // NO NEGATIVITY // LEGENDS NEVER DIE // 
        </div>
    </div>

    <header class="flex flex-col items-center justify-center text-center pt-20 pb-12 px-6">
        <img src="logo.png" alt="Sticker" class="w-64 md:w-80 drop-shadow-[0_0_60px_rgba(168,85,247,0.7)] mb-8 hover:scale-110 transition-transform">
        <h1 class="text-5xl md:text-8xl font-sync font-bold tracking-tighter uppercase italic leading-none">The Inner Circle</h1>
    </header>

    <section class="w-full py-10 overflow-hidden bg-white/5 border-y border-white/10 mb-12">
        <div class="gallery-track gap-6 px-4">
            <div class="gallery-item"><img src="drake1.jpg" alt="Drake 1"></div>
            <div class="gallery-item"><img src="drake2.jpg" alt="Drake 2"></div>
            <div class="gallery-item"><img src="drake3.jpg" alt="Drake 3"></div>
            
            <div class="gallery-item"><img src="juice1.jpg" alt="Juice 1"></div>
            <div class="gallery-item"><img src="juice2.jpg" alt="Juice 2"></div>
            <div class="gallery-item"><img src="juice3.jpg" alt="Juice 3"></div>
            <div class="gallery-item"><img src="juice4.jpg" alt="Juice 4"></div>
            <div class="gallery-item"><img src="juice5.jpg" alt="Juice 5"></div>
            <div class="gallery-item"><img src="juice6.jpg" alt="Juice 6"></div>
            <div class="gallery-item"><img src="juice7.jpg" alt="Juice 7"></div>

            <div class="gallery-item"><img src="drake1.jpg"></div>
            <div class="gallery-item"><img src="drake2.jpg"></div>
            <div class="gallery-item"><img src="drake3.jpg"></div>
            <div class="gallery-item"><img src="juice1.jpg"></div>
            <div class="gallery-item"><img src="juice2.jpg"></div>
            <div class="gallery-item"><img src="juice3.jpg"></div>
            <div class="gallery-item"><img src="juice4.jpg"></div>
            <div class="gallery-item"><img src="juice5.jpg"></div>
            <div class="gallery-item"><img src="juice6.jpg"></div>
            <div class="gallery-item"><img src="juice7.jpg"></div>
        </div>
    </section>

    <main class="max-w-7xl mx-auto px-6 grid grid-cols-1 md:grid-cols-4 gap-4 pb-32">
        <div class="glass p-8 md:col-span-2 border-l-8 border-purple-600">
            <h3 class="font-sync text-xs mb-4 tracking-widest text-purple-400">CORE MISSION</h3>
            <p class="text-2xl font-light italic leading-snug">"Turning negativity into something positive. Late night melodies, palm trees, and the family that never sleeps."</p>
        </div>

        <div class="glass p-6 text-center border-t-2 border-green-500">
            <h3 class="font-sync text-[10px] mb-4 text-gray-500 uppercase">System Health</h3>
            <div class="text-4xl font-black text-green-400 mb-2 uppercase">Online</div>
            <div class="text-[10px] font-mono text-gray-600 uppercase">Uptime 99.9%</div>
        </div>

        <div class="glass p-6 border-r-8 border-blue-600">
            <h3 class="font-sync text-[10px] mb-4 text-blue-400 uppercase font-bold">Uptime Session</h3>
            <div class="space-y-2 font-mono text-[10px] uppercase">
                <p class="text-white">Tuesdays Active</p>
                <p class="text-white/60">Sometimes Thursdays</p>
                <p class="text-white/60">Every Other Weekend</p>
            </div>
        </div>

        <div class="glass p-6 hover:bg-purple-900/10 transition border border-purple-500/20">
            <div class="flex items-center gap-4">
                <div class="w-12 h-12 bg-purple-600 rounded-full flex items-center justify-center font-bold">JJ</div>
                <div>
                    <p class="font-sync text-sm">Jon Jon</p>
                    <p class="text-[10px] font-mono opacity-50 uppercase">(JonnyM85)</p>
                </div>
            </div>
        </div>

        <div class="glass p-6 hover:bg-blue-900/10 transition border border-blue-500/20">
            <div class="flex items-center gap-4">
                <div class="w-12 h-12 bg-blue-600 rounded-full flex items-center justify-center font-bold text-white">AM</div>
                <div>
                    <p class="font-sync text-sm leading-none mb-2">Aubrey D Graham</p>
                    <p class="text-[10px] font-mono opacity-60 uppercase tracking-tighter">Co-Owner</p>
                    <p class="text-[10px] font-mono opacity-60 uppercase tracking-tighter">Mikey</p>
                </div>
            </div>
        </div>

        <div class="glass p-8 md:col-span-2 grid grid-cols-3 gap-4 border-b border-white/10">
            <div class="text-center p-2 border border-white/5 rounded-lg flex flex-col justify-center">
                <p class="text-[9px] font-mono text-purple-400 uppercase italic">01 Hang</p>
                <p class="text-[10px] font-sync uppercase">McDonald's</p>
            </div>
            <div class="text-center p-2 border border-white/5 rounded-lg flex flex-col justify-center">
                <p class="text-[9px] font-mono text-blue-400 uppercase italic">02 Utility</p>
                <p class="text-[10px] font-sync uppercase">Optimize Box</p>
            </div>
            <div class="text-center p-2 border border-white/5 rounded-lg flex flex-col justify-center">
                <p class="text-[9px] font-mono text-red-400 uppercase italic">03 Rec</p>
                <p class="text-[10px] font-sync uppercase">Among Us</p>
            </div>
        </div>

        <div class="glass p-6 md:col-span-4 font-mono text-[10px] text-gray-500 h-32 overflow-hidden leading-relaxed uppercase">
            <p>> Booting Jon Jon Nexus...</p>
            <p>> 999 Juice Wrld Database Loaded [7 Files Detected]</p>
            <p>> OVO Sound Libs Loaded [3 Files Detected]</p>
            <p>> Scanning For Negativity... 0 Found</p>
            <p>> System Status: The Inner Circle Is Live.</p>
        </div>
    </main>

    <footer class="text-center py-20">
        <button onclick="window.open('https://vrchat.com/home/group/grp_e6ecca5a-828b-4706-9c23-db1723469436')" 
                class="bg-white text-black px-12 py-6 rounded-full font-sync text-lg font-bold hover:scale-110 transition-all shadow-[0_0_50px_rgba(255,255,255,0.3)] uppercase">
            Join the Collective
        </button>
        <p class="mt-20 font-sync text-[10px] tracking-[2em] opacity-20 uppercase">Legends Never Die</p>
    </footer>

</body>
</html>
