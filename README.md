<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>JON JON & FRIENDS | THE NEXUS</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://fonts.googleapis.com/css2?family=Syncopate:wght@400;700&family=Inter:wght@300;600;900&display=swap" rel="stylesheet">
    <style>
        :root { --neon-purple: #bc13fe; --neon-blue: #00d2ff; }
        body { font-family: 'Inter', sans-serif; background: #050505; color: white; overflow-x: hidden; }
        .font-sync { font-family: 'Syncopate', sans-serif; }
        
        /* Insane Animated Background */
        .bg-animate {
            background: radial-gradient(circle at 50% 50%, #1a1033 0%, #050505 100%);
            position: fixed; inset: 0; z-index: -1;
        }

        .glass { 
            background: rgba(255, 255, 255, 0.02); 
            backdrop-filter: blur(20px); 
            border: 1px solid rgba(255, 255, 255, 0.1); 
            box-shadow: 0 8px 32px 0 rgba(0, 0, 0, 0.8);
            transition: 0.4s cubic-bezier(0.175, 0.885, 0.32, 1.275);
        }
        .glass:hover { transform: scale(1.02); border-color: var(--neon-purple); box-shadow: 0 0 20px rgba(188, 19, 254, 0.3); }

        /* Ticker Animation */
        @keyframes scroll { 0% { transform: translateX(100%); } 100% { transform: translateX(-100%); } }
        .ticker { white-space: nowrap; animation: scroll 20s linear infinite; }

        #overlay { position: fixed; inset: 0; background: black; z-index: 1000; display: flex; align-items: center; justify-content: center; cursor: crosshair; }
        .logo-main { filter: drop-shadow(0 0 30px rgba(188, 19, 254, 0.6)); }
    </style>
</head>
<body class="min-h-screen">
    <div class="bg-animate"></div>

    <div id="overlay" onclick="this.style.display='none'">
        <div class="text-center">
            <div class="text-xs font-sync tracking-[1em] mb-4 opacity-50">INITIALIZING CORE...</div>
            <h1 class="text-5xl font-sync font-bold text-white animate-pulse">ACCESS SYSTEM</h1>
            <p class="mt-4 text-purple-500 font-mono">[ CLICK TO ENGAGE ]</p>
        </div>
    </div>

    <div class="w-full bg-purple-900/20 border-b border-purple-500/30 py-2 overflow-hidden sticky top-0 z-50 backdrop-blur-md">
        <div class="ticker font-mono text-xs tracking-widest text-purple-400 uppercase">
            SYSTEM STATUS: ONLINE // MEMBER COUNT: GROWING // CURRENT VIBE: 999 // LOCATION: THE VOID // LEGENDS NEVER DIE // OVO ENERGY // 
        </div>
    </div>

    <header class="flex flex-col items-center justify-center text-center py-16 px-6">
        <a href="https://vrchat.com/home/group/grp_e6ecca5a-828b-4706-9c23-db1723469436" target="_blank">
            <img src="logo.png" alt="Jon Jon Sticker" class="w-72 md:w-96 logo-main mb-8 hover:rotate-2 transition-transform">
        </a>
        <h1 class="text-6xl md:text-9xl font-sync font-black tracking-tighter text-transparent bg-clip-text bg-gradient-to-b from-white to-purple-800 uppercase">
            Jon Jon
        </h1>
        <p class="text-purple-400 font-mono tracking-widest mt-4">CORE PROTOCOL: POSITIVE VIBES ONLY</p>
    </header>

    <main class="max-w-7xl mx-auto px-6 grid grid-cols-1 md:grid-cols-3 gap-8 pb-24">
        
        <div class="flex flex-col gap-8">
            <div class="glass p-6 font-mono text-sm overflow-hidden h-64">
                <h3 class="text-purple-500 border-b border-purple-500/30 mb-4 pb-2 font-sync text-[10px]">INTERNAL_LOGS</h3>
                <div class="text-gray-500 leading-loose">
                    [01:23] WORLD_HOP_INITIATED<br>
                    [02:45] NEW_MEMBER_DETECTED: [REDACTED]<br>
                    [03:12] VIBE_CHECK: 100% SUCCESS<br>
                    [04:00] JUICE_WRLD_TRIBUTE_ACTIVE<br>
                    [05:55] DRAKE_MELODIES_SYNCED...<br>
                    [06:01] SYSTEM_STABLE_999
                </div>
            </div>
            <div class="glass p-8">
                <h3 class="font-sync text-lg mb-4 italic">THE VISION</h3>
                <p class="text-gray-400 text-sm leading-relaxed">
                    Building the most elite late-night community in VRChat. We aren't just a group; we are the family you choose when the sun goes down.
                </p>
            </div>
        </div>

        <div class="flex flex-col gap-8">
            <div class="glass p-8 border-l-4 border-blue-500">
                <h3 class="font-sync text-xl mb-6">MEMBER_FILES</h3>
                <div class="space-y-4">
                    <div class="flex items-center gap-4 bg-white/5 p-3 rounded-xl">
                        <div class="w-10 h-10 rounded-full bg-purple-600 animate-pulse"></div>
                        <div><p class="font-bold text-sm">Jon Jon</p><p class="text-[10px] text-gray-500">FOUNDER / 999</p></div>
                    </div>
                    <div class="flex items-center gap-4 bg-white/5 p-3 rounded-xl opacity-50">
                        <div class="w-10 h-10 rounded-full bg-blue-600"></div>
                        <div><p class="font-bold text-sm text-gray-400">Join Us</p><p class="text-[10px] text-gray-500">PENDING...</p></div>
                    </div>
                </div>
            </div>
            <div class="glass p-8 text-center bg-gradient-to-br from-purple-900/20 to-black">
                <h3 class="font-sync text-3xl mb-2">999</h3>
                <p class="text-[10px] tracking-[0.5em] text-purple-400 mb-4">ENERGY CORE</p>
                <p class="text-gray-400 text-sm italic">"Turn negativity into something positive."</p>
            </div>
        </div>

        <div class="flex flex-col gap-8">
            <div class="glass p-8 border-r-4 border-pink-500">
                <h3 class="font-sync text-xl mb-4 text-right underline">PORTALS</h3>
                <div class="space-y-3">
                    <a href="#" class="block p-4 bg-white/5 rounded-2xl hover:bg-white/10 transition text-sm font-mono border border-white/5">>> THE BLACK CAT</a>
                    <a href="#" class="block p-4 bg-white/5 rounded-2xl hover:bg-white/10 transition text-sm font-mono border border-white/5">>> MIDNIGHT ROOFTOP</a>
                    <a href="#" class="block p-4 bg-white/5 rounded-2xl hover:bg-white/10 transition text-sm font-mono border border-white/5">>> DRIVING SIM</a>
                </div>
            </div>
            <div class="glass p-8 h-full flex flex-col items-center justify-center">
                <div class="text-6xl mb-4">🏝️</div>
                <h3 class="font-sync text-sm text-center">PALM TREE<br>PROTECTION</h3>
            </div>
        </div>
    </main>

    <footer class="w-full py-12 border-t border-white/5 text-center">
        <p class="text-[10px] font-sync text-gray-600 tracking-[1em]">ALL RIGHTS RESERVED // JON JON 2026</p>
    </footer>

</body>
</html>
