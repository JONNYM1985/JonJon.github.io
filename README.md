<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>JON JON & FRIENDS | THE INNER CIRCLE</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://fonts.googleapis.com/css2?family=Syncopate:wght@400;700&family=Inter:wght@300;600;900&display=swap" rel="stylesheet">
    <style>
        :root { --neon-purple: #bc13fe; --neon-blue: #00d2ff; }
        body { font-family: 'Inter', sans-serif; background: #020202; color: white; overflow-x: hidden; }
        .font-sync { font-family: 'Syncopate', sans-serif; }
        
        .bg-animate {
            background: radial-gradient(circle at 50% 10%, #2e1065 0%, #020202 80%);
            position: fixed; inset: 0; z-index: -1;
        }

        .glass { 
            background: rgba(255, 255, 255, 0.01); 
            backdrop-filter: blur(25px); 
            border: 1px solid rgba(255, 255, 255, 0.08); 
            border-radius: 1.5rem;
            transition: 0.4s ease;
        }
        .glass:hover { border-color: var(--neon-purple); transform: translateY(-5px); box-shadow: 0 10px 40px rgba(188, 19, 254, 0.15); }

        @keyframes pulse-border { 0% { opacity: 0.3; } 50% { opacity: 1; } 100% { opacity: 0.3; } }
        .live-glow { animation: pulse-border 2s infinite; }

        #overlay { position: fixed; inset: 0; background: black; z-index: 1000; display: flex; align-items: center; justify-content: center; cursor: pointer; }
    </style>
</head>
<body class="min-h-screen">
    <div class="bg-animate"></div>

    <div id="overlay" onclick="this.style.display='none'">
        <div class="text-center">
            <h1 class="text-4xl font-sync font-bold tracking-[0.5em] text-white animate-pulse uppercase">Enter the Void</h1>
            <p class="mt-4 text-gray-500 font-mono text-xs italic tracking-widest">999 x OVO Protocol Active</p>
        </div>
    </div>

    <header class="flex flex-col items-center justify-center text-center py-16 px-6">
        <a href="https://vrchat.com/home/group/grp_e6ecca5a-828b-4706-9c23-db1723469436" target="_blank">
            <img src="logo.png" alt="Jon Jon Sticker" class="w-72 md:w-96 drop-shadow-[0_0_35px_rgba(188,19,254,0.4)] mb-8 hover:scale-105 transition-transform">
        </a>
        <h1 class="text-6xl md:text-8xl font-sync font-bold tracking-tighter uppercase leading-none">
            The Inner Circle
        </h1>
        <div class="mt-6 flex items-center gap-2 px-4 py-1 bg-purple-900/30 rounded-full border border-purple-500/50">
            <div class="w-2 h-2 rounded-full bg-green-500 live-glow"></div>
            <span class="text-[10px] font-sync text-purple-300 tracking-widest uppercase">Live Group Status: Active</span>
        </div>
    </header>

    <main class="max-w-7xl mx-auto px-6 grid grid-cols-1 md:grid-cols-3 gap-8 pb-24">
        
        <div class="flex flex-col gap-8">
            <div class="glass p-8 h-64 flex flex-col justify-center">
                <h3 class="text-purple-500 font-sync text-[12px] mb-4 tracking-widest">THE VISION</h3>
                <p class="text-gray-400 text-sm leading-relaxed italic font-light">
                    "Late night melodies, palm trees, and the family that never sleeps. We are the elite late-night collective of VRChat."
                </p>
            </div>
            
            <div class="glass p-8 bg-gradient-to-b from-purple-900/10 to-transparent">
                <h3 class="font-sync text-[12px] mb-6 text-blue-400 tracking-widest uppercase">Group Status</h3>
                <div class="space-y-6">
                    <div>
                        <p class="text-[10px] text-gray-500 uppercase font-bold mb-1">Current Capacity</p>
                        <p class="text-2xl font-sync text-white">RECRUITING</p>
                    </div>
                    <div>
                        <p class="text-[10px] text-gray-500 uppercase font-bold mb-1">Vibe Frequency</p>
                        <p class="text-2xl font-sync text-white">999 / OVO</p>
                    </div>
                </div>
            </div>
        </div>

        <div class="flex flex-col gap-8">
            <div class="glass p-8 border-t-4 border-purple-600">
                <h3 class="font-sync text-[12px] mb-8 tracking-[0.3em] text-center">STAFF DIRECTORY</h3>
                <div class="space-y-6">
                    <div class="flex items-center gap-4 bg-white/5 p-4 rounded-2xl border border-white/5">
                        <div class="w-12 h-12 rounded-full bg-gradient-to-tr from-purple-600 to-pink-500 flex items-center justify-center font-bold shadow-lg">JJ</div>
                        <div>
                            <p class="font-sync text-sm">Jon Jon</p>
                            <p class="text-[10px] text-purple-400 uppercase tracking-widest">Founder / Elite</p>
                        </div>
                    </div>
                    <div class="flex items-center gap-4 bg-white/5 p-4 rounded-2xl border border-white/5">
                        <div class="w-12 h-12 rounded-full bg-gradient-to-tr from-blue-600 to-indigo-500 flex items-center justify-center font-bold shadow-lg">AM</div>
                        <div>
                            <p class="font-sync text-sm">Aubrey D Graham</p>
                            <p class="text-[10px] text-blue-400 uppercase tracking-widest">Co-Owner / Mikey</p>
                        </div>
                    </div>
                </div>
                <button onclick="window.open('https://vrchat.com/home/group/grp_e6ecca5a-828b-4706-9c23-db1723469436')" 
                        class="w-full mt-8 py-4 rounded-xl bg-white text-black font-sync text-xs font-bold hover:bg-purple-500 hover:text-white transition-all">
                    APPLY FOR ACCESS
                </button>
            </div>
        </div>

        <div class="flex flex-col gap-8">
            <div class="glass p-8 border-r-4 border-white/10 flex flex-col h-full">
                <h3 class="font-sync text-[12px] mb-8 text-right tracking-widest">PORTALS</h3>
                <div class="flex-grow space-y-4">
                    <a href="https://vrchat.com/home/world/wrld_f8d4e7d4-8d9e-4e8c-8d3e-7e9c8d3e7e9c" target="_blank" 
                       class="flex items-center justify-between p-5 bg-white/5 rounded-2xl hover:bg-white/10 border border-white/5 group transition-all">
                        <span class="font-mono text-sm tracking-tighter">01. MCDONALD'S</span>
                        <span class="text-xs opacity-0 group-hover:opacity-100 transition-opacity">JOIN →</span>
                    </a>
                    <a href="https://vrchat.com/home/world/wrld_a1b2c3d4-e5f6-g7h8-i9j0-k1l2m3n4o5p6" target="_blank" 
                       class="flex items-center justify-between p-5 bg-white/5 rounded-2xl hover:bg-white/10 border border-white/5 group transition-all">
                        <span class="font-mono text-sm tracking-tighter">02. OPTIMIZE BOX</span>
                        <span class="text-xs opacity-0 group-hover:opacity-100 transition-opacity">JOIN →</span>
                    </a>
                </div>
                <div class="mt-8 pt-8 border-t border-white/5 text-center">
                    <p class="text-4xl mb-2">🌃</p>
                    <p class="text-[10px] font-sync text-gray-500 uppercase">Legends Never Die</p>
                </div>
            </div>
        </div>
    </main>

    <footer class="w-full py-16 text-center opacity-20 hover:opacity-100 transition-opacity">
        <p class="text-[9px] font-sync tracking-[2em]">JON JON x FRIENDS // COLLECTIVE ACCESS 2026</p>
    </footer>

</body>
</html>
