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
        body { font-family: 'Inter', sans-serif; background: #000; color: white; overflow-x: hidden; }
        .font-sync { font-family: 'Syncopate', sans-serif; }
        .font-mono { font-family: 'Space Mono', monospace; }
        
        .bg-animate {
            background: radial-gradient(circle at 50% 10%, #2e1065 0%, #000000 90%);
            position: fixed; inset: 0; z-index: -1;
        }

        .glass { 
            background: rgba(255, 255, 255, 0.02); 
            backdrop-filter: blur(30px); 
            border: 1px solid rgba(255, 255, 255, 0.1); 
            border-radius: 1rem;
            transition: 0.3s ease;
            position: relative;
            overflow: hidden;
        }
        .glass::after {
            content: ""; position: absolute; top: 0; left: 0; width: 100%; height: 2px;
            background: linear-gradient(90deg, transparent, var(--neon-purple), transparent);
            animation: scan 3s linear infinite;
        }
        @keyframes scan { 0% { transform: translateX(-100%); } 100% { transform: translateX(100%); } }

        /* Ticker Animation */
        @keyframes scroll { 0% { transform: translateX(100%); } 100% { transform: translateX(-100%); } }
        .ticker { white-space: nowrap; animation: scroll 25s linear infinite; }

        #overlay { position: fixed; inset: 0; background: black; z-index: 1000; display: flex; align-items: center; justify-content: center; cursor: pointer; }
    </style>
</head>
<body class="min-h-screen">
    <div class="bg-animate"></div>

    <div id="overlay" onclick="this.style.display='none'">
        <div class="text-center">
            <h1 class="text-4xl font-sync font-bold tracking-[0.5em] text-white animate-pulse uppercase">INITIATING NEXUS</h1>
            <p class="mt-4 text-purple-500 font-mono text-xs tracking-widest">[ ACCESS GRANTED ]</p>
        </div>
    </div>

    <div class="w-full bg-purple-900/20 border-b border-purple-500/30 py-2 overflow-hidden sticky top-0 z-50 backdrop-blur-md">
        <div class="ticker font-mono text-[10px] tracking-widest text-purple-400 uppercase font-bold">
            ESTABLISHED 2026 // VRC_GROUP_ID: JON_JON_FRIENDS // 999 ENERGY ACTIVE // OVO SOUND SYSTEM: ON // NO NEGATIVITY DETECTED // MEMBERS: [VERIFIED] // LEGENDS NEVER DIE // LATE NIGHT VIBES //
        </div>
    </div>

    <header class="flex flex-col items-center justify-center text-center py-12 px-6">
        <a href="https://vrchat.com/home/group/grp_e6ecca5a-828b-4706-9c23-db1723469436" target="_blank">
            <img src="logo.png" alt="Jon Jon Sticker" class="w-64 md:w-80 drop-shadow-[0_0_40px_rgba(188,19,254,0.5)] mb-8 hover:scale-110 transition-transform cursor-pointer">
        </a>
        <h1 class="text-5xl md:text-8xl font-sync font-bold tracking-tighter uppercase leading-none">
            The Inner Circle
        </h1>
    </header>

    <main class="max-w-7xl mx-auto px-6 grid grid-cols-1 md:grid-cols-3 gap-6 pb-24">
        
        <div class="flex flex-col gap-6">
            <div class="glass p-8 h-64 border-l-2 border-purple-500">
                <h3 class="text-purple-400 font-sync text-[10px] mb-4 tracking-widest flex justify-between">
                    <span>THE VISION</span>
                    <span class="animate-pulse">●</span>
                </h3>
                <p class="text-gray-300 text-sm leading-relaxed italic font-light">
                    "Late night melodies, palm trees, and the family that never sleeps. We are the elite late-night collective of VRChat."
                </p>
                <div class="mt-6 font-mono text-[9px] text-gray-600 uppercase">
                    ENCRYPTION: AES-256 // VIBE_SYNC: 100%
                </div>
            </div>
            
            <div class="glass p-8 bg-gradient-to-br from-blue-900/10 to-transparent">
                <h3 class="font-sync text-[10px] mb-6 text-blue-400 tracking-widest uppercase italic">Group Metrics</h3>
                <div class="grid grid-cols-2 gap-4 mb-6">
                    <div class="bg-white/5 p-3 rounded-lg border border-white/5">
                        <p class="text-[9px] text-gray-500 font-bold uppercase">Status</p>
                        <p class="text-lg font-sync text-green-400">LIVE</p>
                    </div>
                    <div class="bg-white/5 p-3 rounded-lg border border-white/5">
                        <p class="text-[9px] text-gray-500 font-bold uppercase">Uptime</p>
                        <p class="text-lg font-sync text-white">24/7</p>
                    </div>
                </div>
                <div class="font-mono text-[10px] text-gray-500 space-y-1">
                    <p>> FREQUENCY: 432Hz</p>
                    <p>> CORE: 999_OVO</p>
                    <p>> REGION: GLOBAL_VR</p>
                </div>
            </div>
        </div>

        <div class="flex flex-col gap-6">
            <div class="glass p-8 border-t-2 border-purple-600">
                <h3 class="font-sync text-[11px] mb-8 tracking-[0.4em] text-center text-gray-400">STAFF_DIRECTORY</h3>
                <div class="space-y-6">
                    <div class="flex items-center gap-4 bg-white/5 p-5 rounded-xl border border-white/5 hover:bg-white/10 transition">
                        <div class="w-12 h-12 rounded-full border border-purple-500 flex items-center justify-center font-bold text-purple-500 shadow-[0_0_10px_rgba(168,85,247,0.3)]">JJ</div>
                        <div>
                            <p class="font-sync text-sm">Jon Jon</p>
                            <p class="text-[11px] text-purple-400 font-mono tracking-tighter">(JonnyM85)</p>
                        </div>
                    </div>
                    <div class="flex items-center gap-4 bg-white/5 p-5 rounded-xl border border-white/5 hover:bg-white/10 transition">
                        <div class="w-12 h-12 rounded-full border border-blue-500 flex items-center justify-center font-bold text-blue-500 shadow-[0_0_10px_rgba(59,130,246,0.3)]">AM</div>
                        <div>
                            <p class="font-sync text-sm">Aubrey D Graham</p>
                            <p class="text-[11px] text-blue-400 font-mono tracking-tighter italic">Co-Owner</p>
                            <p class="text-[11px] text-blue-300 font-mono tracking-tighter">Mikey</p>
                        </div>
                    </div>
                </div>
                <button onclick="window.open('https://vrchat.com/home/group/grp_e6ecca5a-828b-4706-9c23-db1723469436')" 
                        class="w-full mt-10 py-4 rounded-lg bg-white text-black font-sync text-[10px] font-bold hover:bg-purple-600 hover:text-white transition-all shadow-xl">
                    REQUEST INVITE
                </button>
            </div>
        </div>

        <div class="flex flex-col gap-6">
            <div class="glass p-8 border-r-2 border-white/10 flex flex-col h-full">
                <h3 class="font-sync text-[10px] mb-8 text-right tracking-widest text-gray-400">MAP_DATABASE</h3>
                <div class="flex-grow space-y-4 font-mono">
                    <div class="p-4 bg-purple-900/10 rounded-lg border border-purple-500/20">
                        <p class="text-[9px] text-purple-400 mb-2">// PRIMARY_HANG</p>
                        <a href="#" class="text-sm hover:text-purple-400 transition tracking-tighter block uppercase">01. MCDONALD'S</a>
                    </div>
                    <div class="p-4 bg-blue-900/10 rounded-lg border border-blue-500/20">
                        <p class="text-[9px] text-blue-400 mb-2">// UTILITY_SPACE</p>
                        <a href="#" class="text-sm hover:text-blue-400 transition tracking-tighter block uppercase">02. OPTIMIZE BOX</a>
                    </div>
                </div>
                <div class="mt-8 pt-6 border-t border-white/5 text-center">
                    <div class="text-xs font-mono text-gray-600 tracking-widest mb-2 animate-pulse">TRANSMITTING...</div>
                    <p class="text-[10px] font-sync text-white uppercase italic">Legends Never Die</p>
                </div>
            </div>
        </div>
    </main>

    <footer class="w-full pt-12 pb-20 text-center flex flex-col items-center gap-4">
        <div class="flex gap-10 opacity-20 font-mono text-[8px] tracking-[0.3em]">
            <span>NODE_01: ONLINE</span>
            <span>NODE_02: ONLINE</span>
            <span>NODE_03: ONLINE</span>
        </div>
        <p class="text-[9px] font-sync tracking-[2em] opacity-30 mt-4 uppercase">Jon Jon x Friends // MMXXVI</p>
    </footer>

</body>
</html>
