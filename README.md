<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>JON JON & FRIENDS | 999 OVO NEXUS</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://fonts.googleapis.com/css2?family=Syncopate:wght@400;700&family=Inter:wght@300;900&family=Space+Mono&display=swap" rel="stylesheet">
    <style>
        :root { --juice-purple: #a855f7; --drake-owl: #fbbf24; }
        body { font-family: 'Inter', sans-serif; background: #000; color: white; margin: 0; overflow-x: hidden; }
        .font-sync { font-family: 'Syncopate', sans-serif; }
        .font-mono { font-family: 'Space Mono', monospace; }

        /* HEAVY ANIMATED BACKGROUND */
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
            position: relative; overflow: hidden;
        }

        /* AUTO-SCROLLING GALLERY */
        .gallery-track {
            display: flex; width: calc(300px * 12);
            animation: scroll-gallery 30s linear infinite;
        }
        @keyframes scroll-gallery {
            0% { transform: translateX(0); }
            100% { transform: translateX(calc(-300px * 6)); }
        }

        .glitch { animation: glitch 1s linear infinite; text-shadow: 2px 0 #ff00ff, -2px 0 #00ffff; }
        @keyframes glitch {
            2%, 64% { transform: translate(2px,0) skew(0deg); }
            4%, 60% { transform: translate(-2px,0) skew(0deg); }
            62% { transform: translate(0,0) skew(5deg); }
        }

        .ticker { white-space: nowrap; animation: ticker-move 40s linear infinite; }
        @keyframes ticker-move { 0% { transform: translateX(100%); } 100% { transform: translateX(-100%); } }

        #overlay { position: fixed; inset: 0; background: black; z-index: 9999; display: flex; align-items: center; justify-content: center; cursor: pointer; }
    </style>
</head>
<body class="min-h-screen">
    <div class="overload-bg"></div>
    <div class="particles"></div>

    <div id="overlay" onclick="this.style.display='none'">
        <div class="text-center">
            <h1 class="text-6xl font-sync font-black tracking-widest glitch uppercase">Accessing Nexus</h1>
            <p class="mt-4 text-xs font-mono tracking-[1em] text-purple-500 uppercase">Bypass Firewall Activated</p>
        </div>
    </div>

    <div class="w-full bg-white/5 border-b border-white/10 py-2 overflow-hidden sticky top-0 z-50 backdrop-blur-xl">
        <div class="ticker font-mono text-[10px] tracking-widest uppercase">
            ESTABLISHED 2026 // 999 FOREVER // OVO SOUND SYSTEM // CONNECTING TO THE VOID // NO NEGATIVITY // LEGENDS NEVER DIE // 
        </div>
    </div>

    <header class="flex flex-col items-center justify-center text-center pt-20 pb-12 px-6">
        <img src="logo.png" alt="Sticker" class="w-64 md:w-96 drop-shadow-[0_0_60px_rgba(168,85,247,0.7)] mb-8 hover:scale-110 transition-transform">
        <h1 class="text-5xl md:text-9xl font-sync font-black tracking-tighter uppercase leading-none italic">
            The Inner Circle
        </h1>
    </header>

    <section class="w-full py-10 overflow-hidden bg-white/5 border-y border-white/10 mb-12">
        <div class="gallery-track gap-6 px-4">
            <div class="w-[300px] h-[400px] flex-shrink-0 rounded-2xl border border-purple-500/30 overflow-hidden">
                <img src="https://static.independent.co.uk/s3fs-public/thumbnails/image/2019/12/08/19/juice-wrld.jpg" class="w-full h-full object-cover">
            </div>
            <div class="w-[300px] h-[400px] flex-shrink-0 rounded-2xl border border-blue-500/30 overflow-hidden">
                <img src="https://hips.hearstapps.com/hmg-prod/images/drake-gettyimages-1135833471.jpg" class="w-full h-full object-cover">
            </div>
            <div class="w-[300px] h-[400px] flex-shrink-0 rounded-2xl border border-purple-500/30 overflow-hidden">
                <img src="https://images.complex.com/complex/images/c_fill,dpr_auto,f_auto,q_auto,w_1400/fl_lossy,pg_1/vclm70v6vky6ecl049qy/juice-wrld-999" class="w-full h-full object-cover">
            </div>
            <div class="w-[300px] h-[400px] flex-shrink-0 rounded-2xl border border-blue-500/30 overflow-hidden">
                <img src="https://media.gq.com/photos/569e9999933ca32128766159/master/pass/drake-owl.jpg" class="w-full h-full object-cover">
            </div>
            <div class="w-[300px] h-[400px] flex-shrink-0 rounded-2xl border border-purple-500/30 overflow-hidden">
                <img src="https://static.independent.co.uk/s3fs-public/thumbnails/image/2019/12/08/19/juice-wrld.jpg" class="w-full h-full object-cover">
            </div>
            <div class="w-[300px] h-[400px] flex-shrink-0 rounded-2xl border border-blue-500/30 overflow-hidden">
                <img src="https://hips.hearstapps.com/hmg-prod/images/drake-gettyimages-1135833471.jpg" class="w-full h-full object-cover">
            </div>
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
            <div class="text-[10px] font-mono text-gray-600 tracking-widest uppercase">Uptime 99.9%</div>
        </div>

        <div class="glass p-6 border-r-8 border-blue-600">
            <h3 class="font-sync text-[10px] mb-4 text-blue-400 uppercase">Uptime Session</h3>
            <div class="space-y-2 font-mono text-[10px] uppercase">
                <p>Tuesdays Active</p>
                <p>Sometimes Thursdays</p>
                <p>Every Other Weekend</p>
            </div>
        </div>

        <div class="glass p-6 hover:bg-purple-900/10 transition">
            <div class="flex items-center gap-4">
                <div class="w-12 h-12 bg-purple-600 rounded-full flex items-center justify-center font-bold">JJ</div>
                <div>
                    <p class="font-sync text-sm">Jon Jon</p>
                    <p class="text-[10px] font-mono opacity-50 uppercase">(JonnyM85)</p>
                </div>
            </div>
        </div>

        <div class="glass p-6 hover:bg-blue-900/10 transition">
            <div class="flex items-center gap-4">
                <div class="w-12 h-12 bg-blue-600 rounded-full flex items-center justify-center font-bold">AM</div>
                <div>
                    <p class="font-sync text-sm leading-none mb-1">Aubrey D Graham</p>
                    <p class="text-[10px] font-mono opacity-50 uppercase">Co-Owner</p>
                    <p class="text-[10px] font-mono opacity-50 uppercase">Mikey</p>
                </div>
            </div>
        </div>

        <div class="glass p-8 md:col-span-2 grid grid-cols-3 gap-4">
            <div class="text-center p-2 border border-white/5 rounded-lg flex flex-col justify-center">
                <p class="text-[9px] font-mono text-purple-400 tracking-widest uppercase">01 Hang</p>
                <p class="text-[10px] font-sync uppercase">McDonald's</p>
            </div>
            <div class="text-center p-2 border border-white/5 rounded-lg flex flex-col justify-center">
                <p class="text-[9px] font-mono text-blue-400 tracking-widest uppercase">02 Utility</p>
                <p class="text-[10px] font-sync uppercase">Optimize Box</p>
            </div>
            <div class="text-center p-2 border border-white/5 rounded-lg flex flex-col justify-center">
                <p class="text-[9px] font-mono text-red-400 tracking-widest uppercase">03 Rec</p>
                <p class="text-[10px] font-sync uppercase">Among Us</p>
            </div>
        </div>

        <div class="glass p-6 md:col-span-4 font-mono text-[10px] text-gray-500 h-32 overflow-hidden leading-relaxed uppercase">
            <p>> Booting Jon Jon Nexus...</p>
            <p>> 999 Juice Wrld Database Loaded</p>
            <p>> OVO Sound Libs Loaded</p>
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
