<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>JON JON & FRIENDS | THE INNER CIRCLE</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://fonts.googleapis.com/css2?family=Syncopate:wght@400;700&family=Inter:wght@300;600;900&family=Space+Mono&display=swap" rel="stylesheet">
    <style>
        :root { --neon-purple: #bc13fe; --neon-blue: #00d2ff; }
        body { font-family: 'Inter', sans-serif; background: #000; color: white; margin: 0; }
        .font-sync { font-family: 'Syncopate', sans-serif; }
        .font-mono { font-family: 'Space Mono', monospace; }

        /* HYPNOTIC ANIMATED NEBULA */
        .bg-wrapper {
            position: fixed; inset: 0; z-index: -1;
            background: #000;
            overflow: hidden;
        }
        .nebula {
            position: absolute; width: 150%; height: 150%;
            top: -25%; left: -25%;
            background: radial-gradient(circle at 50% 50%, rgba(76, 29, 149, 0.4), transparent 50%),
                        radial-gradient(circle at 20% 30%, rgba(188, 19, 254, 0.2), transparent 40%),
                        radial-gradient(circle at 80% 70%, rgba(30, 58, 138, 0.3), transparent 40%);
            filter: blur(80px);
            animation: drift 20s ease-in-out infinite alternate;
        }
        @keyframes drift {
            from { transform: rotate(0deg) scale(1); }
            to { transform: rotate(5deg) scale(1.1); }
        }

        .glass { 
            background: rgba(255, 255, 255, 0.03); 
            backdrop-filter: blur(20px); 
            border: 1px solid rgba(255, 255, 255, 0.1); 
            border-radius: 1.5rem;
            transition: 0.4s ease;
        }
        .glass:hover { border-color: var(--neon-purple); box-shadow: 0 0 30px rgba(188, 19, 254, 0.2); }

        @keyframes scroll { 0% { transform: translateX(100%); } 100% { transform: translateX(-100%); } }
        .ticker { white-space: nowrap; animation: scroll 30s linear infinite; }

        #overlay { position: fixed; inset: 0; background: black; z-index: 1000; display: flex; align-items: center; justify-content: center; cursor: pointer; }
        .text-balance { text-wrap: balance; }
    </style>
</head>
<body class="min-h-screen">
    <div class="bg-wrapper"><div class="nebula"></div></div>

    <div id="overlay" onclick="this.style.display='none'">
        <div class="text-center p-6">
            <h1 class="text-3xl md:text-5xl font-sync font-bold tracking-[0.4em] animate-pulse">ENTER THE VOID</h1>
            <p class="mt-4 text-purple-500 font-mono text-xs tracking-[0.2em] uppercase">Vibe Protocol Engaged</p>
        </div>
    </div>

    <div class="w-full bg-black/60 border-b border-white/10 py-2 overflow-hidden sticky top-0 z-50 backdrop-blur-md">
        <div class="ticker font-mono text-[10px] tracking-widest text-purple-400 uppercase font-bold">
            ESTABLISHED 2026 // GROUP ID JON JON FRIENDS // 999 ENERGY // OVO SOUND // NO NEGATIVITY // MEMBERS VERIFIED // LATE NIGHT VIBES // LEGENDS NEVER DIE //
        </div>
    </div>

    <header class="flex flex-col items-center justify-center text-center pt-16 pb-12 px-6">
        <a href="https://vrchat.com/home/group/grp_e6ecca5a-828b-4706-9c23-db1723469436" target="_blank">
            <img src="logo.png" alt="Jon Jon Sticker" class="w-64 md:w-80 drop-shadow-[0_0_50px_rgba(188,19,254,0.6)] mb-10 hover:scale-105 transition-transform">
        </a>
        <h1 class="text-4xl md:text-7xl font-sync font-bold tracking-tighter uppercase leading-tight text-balance">
            The Inner Circle
        </h1>
    </header>

    <main class="max-w-7xl mx-auto px-6 grid grid-cols-1 md:grid-cols-3 gap-8 pb-24">
        
        <div class="flex flex-col gap-8">
            <div class="glass p-8 border-l-4 border-purple-600">
                <h3 class="text-purple-400 font-sync text-[10px] mb-4 tracking-widest italic">THE VISION</h3>
                <p class="text-gray-300 text-sm leading-relaxed italic font-light text-balance">
                    "Late night melodies, palm trees, and the family that never sleeps. We are the elite late-night collective of VRChat."
                </p>
            </div>
            
            <div class="glass p-8">
                <h3 class="font-sync text-[10px] mb-6 text-blue-400 tracking-widest uppercase">Group Metrics</h3>
                <div class="bg-white/5 p-4 rounded-xl border border-white/5">
                    <p class="text-[9px] text-gray-500 font-bold uppercase mb-1">Uptime Schedule</p>
                    <p class="text-xs font-sync text-white leading-normal">TUESDAYS</p>
                    <p class="text-[10px] font-mono text-blue-300 opacity-80">Sometimes Thursdays</p>
                    <p class="text-[10px] font-mono text-blue-300 opacity-80">Every other weekend</p>
                </div>
            </div>
        </div>

        <div class="flex flex-col gap-8">
            <div class="glass p-8 border-t-2 border-purple-500/50">
                <h3 class="font-sync text-[11px] mb-8 tracking-[0.4em] text-center text-gray-400 uppercase">Staff Directory</h3>
                <div class="space-y-6">
                    <div class="flex items-center gap-4 bg-white/5 p-5 rounded-2xl border border-white/5">
                        <div class="w-12 h-12 rounded-full border-2 border-purple-500 flex items-center justify-center font-bold text-purple-500 shadow-lg shadow-purple-500/20">JJ</div>
                        <div>
                            <p class="font-sync text-sm leading-none mb-1">Jon Jon</p>
                            <p class="text-[10px] text-purple-400 font-mono tracking-tighter">(JonnyM85)</p>
                        </div>
                    </div>
                    <div class="flex items-center gap-4 bg-white/5 p-5 rounded-2xl border border-white/5">
                        <div class="w-12 h-12 rounded-full border-2 border-blue-500 flex items-center justify-center font-bold text-blue-500 shadow-lg shadow-blue-500/20">AM</div>
                        <div>
                            <p class="font-sync text-sm leading-none mb-1">Aubrey D Graham</p>
                            <p class="text-[10px] text-blue-400 font-mono tracking-tighter italic">Co-Owner</p>
                            <p class="text-[10px] text-blue-300 font-mono tracking-tighter">Mikey</p>
                        </div>
                    </div>
                </div>
                <button onclick="window.open('https://vrchat.com/home/group/grp_e6ecca5a-828b-4706-9c23-db1723469436')" 
                        class="w-full mt-10 py-5 rounded-xl bg-white text-black font-sync text-[10px] font-bold hover:bg-purple-600 hover:text-white transition-all uppercase">
                    Request Invite
                </button>
            </div>
        </div>

        <div class="flex flex-col gap-8">
            <div class="glass p-8 border-r-4 border-white/10">
                <h3 class="font-sync text-[10px] mb-8 text-right tracking-widest text-gray-400 uppercase">Map Database</h3>
                <div class="space-y-4">
                    <div class="p-4 bg-purple-900/10 rounded-xl border border-purple-500/20 group hover:bg-purple-900/20 transition-all">
                        <p class="text-[9px] text-purple-400 mb-1 font-mono tracking-widest italic">// PRIMARY HANG</p>
                        <p class="text-sm font-sync uppercase">McDonald's</p>
                    </div>
                    <div class="p-4 bg-blue-900/10 rounded-xl border border-blue-500/20 group hover:bg-blue-900/20 transition-all">
                        <p class="text-[9px] text-blue-400 mb-1 font-mono tracking-widest italic">// UTILITY SPACE</p>
                        <p class="text-sm font-sync uppercase">Optimize Box</p>
                    </div>
                    <div class="p-4 bg-red-900/10 rounded-xl border border-red-500/20 group hover:bg-red-900/20 transition-all">
                        <p class="text-[9px] text-red-400 mb-1 font-mono tracking-widest italic">// RECREATION</p>
                        <p class="text-sm font-sync uppercase">Among Us</p>
                    </div>
                </div>
            </div>
        </div>
    </main>

    <footer class="w-full py-16 text-center opacity-30">
        <p class="text-[9px] font-sync tracking-[2em] uppercase">Jon Jon x Friends // MMXXVI</p>
    </footer>

</body>
</html>
