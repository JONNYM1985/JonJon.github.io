<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Jon Jon & Friends | VRChat</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;700;900&display=swap" rel="stylesheet">
    <style>
        body { font-family: 'Inter', sans-serif; background: radial-gradient(circle at top right, #1a1a2e, #0f0f0f); color: white; margin: 0; }
        .glass { background: rgba(255, 255, 255, 0.03); backdrop-filter: blur(10px); border: 1px solid rgba(255, 255, 255, 0.1); transition: 0.3s; }
        .gradient-text { background: linear-gradient(90deg, #a78bfa, #f472b6, #fb923c); -webkit-background-clip: text; -webkit-text-fill-color: transparent; font-weight: 900; }
        
        /* VR-Compatible Overlay */
        #overlay { 
            position: fixed; 
            inset: 0; 
            background: black; 
            z-index: 999; 
            display: flex; 
            align-items: center; 
            justify-content: center; 
            cursor: pointer; 
            opacity: 1;
            transition: opacity 0.5s ease;
        }
    </style>
</head>
<body class="min-h-screen">

    <div id="overlay" onclick="document.getElementById('overlay').style.display='none'">
        <div class="text-center">
            <h2 class="text-3xl font-black tracking-widest animate-pulse uppercase">Click to Enter</h2>
            <p class="text-gray-500 mt-2 text-sm uppercase">999 x OVO Energy</p>
        </div>
    </div>

    <section class="flex flex-col items-center justify-center text-center py-20 px-4">
        <h1 class="text-6xl md:text-8xl gradient-text mb-4 tracking-tighter uppercase leading-none">Jon Jon & Friends</h1>
        <p class="text-xl text-gray-400 font-light mb-8 italic">"Welcome to the party, we don't want it to end."</p>
        <a href="https://vrchat.com/home/group/grp_e6ecca5a-828b-4706-9c23-db1723469436" 
           target="_blank"
           class="bg-white text-black px-10 py-4 rounded-full font-bold text-lg hover:scale-110 transition-all shadow-[0_0_30px_rgba(255,255,255,0.2)]">
            JOIN THE GROUP
        </a>
    </section>

    <main class="max-w-6xl mx-auto px-6 pb-20">
        <div class="grid grid-cols-1 md:grid-cols-3 gap-6">
            
            <div class="glass p-8 rounded-3xl md:col-span-2">
                <h2 class="text-3xl font-bold mb-4">The Community</h2>
                <p class="text-gray-400 text-lg leading-relaxed">
                    A place for real ones. Late-night world hopping, good music, and genuine vibes. 
                    We're building a family here. Positive vibes only. Legends never die.
                </p>
            </div>

            <div class="glass p-8 rounded-3xl border-t-2 border-purple-500 text-center flex flex-col items-center justify-center">
                <h3 class="text-xs font-bold text-purple-400 mb-4 uppercase tracking-widest">The Vibe Station</h3>
                
                <a href="https://open.spotify.com/playlist/37i9dQZF1E4vT8XG1m7n9D" target="_blank" 
                   class="bg-green-500/10 hover:bg-green-500/20 border border-green-500/50 p-6 rounded-2xl w-full transition-all group shadow-[0_0_15px_rgba(34,197,94,0.1)]">
                    <p class="text-2xl font-black text-white group-hover:scale-105 transition-transform">LISTEN ON SPOTIFY 🎶</p>
                    <p class="text-[10px] text-green-400 mt-2 uppercase font-bold tracking-widest">Juice WRLD • Drake • Melodic</p>
                </a>
                
                <p class="text-[10px] text-gray-600 mt-4 uppercase font-bold">Opens Playlist in New Tab</p>
            </div>

            <div class="glass p-8 rounded-3xl border-l-4 border-purple-500">
                <h3 class="text-xl font-bold mb-2 uppercase">999 Energy</h3>
                <p class="text-gray-400 text-sm italic">"Turning negativity into something positive."</p>
            </div>

            <div class="glass p-8 rounded-3xl border-l-4 border-blue-500">
                <h3 class="text-xl font-bold mb-2 uppercase">The 6 Side</h3>
                <p class="text-gray-400 text-sm italic">"Late-night energy. Melodic flows."</p>
            </div>

            <div class="glass p-8 rounded-3xl flex items-center justify-center text-center">
                <p class="text-2xl font-black uppercase tracking-widest opacity-20 italic">VRChat Community</p>
            </div>

        </div>
    </main>

    <footer class="text-center py-10 opacity-40">
        <p class="text-sm">Jon Jon & Friends • 2026</p>
    </footer>

</body>
</html>
