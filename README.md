<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Jon Jon & Friends | VRChat</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;700;900&display=swap" rel="stylesheet">
    <style>
        body {
            font-family: 'Inter', sans-serif;
            background: radial-gradient(circle at top right, #1a1a2e, #0f0f0f);
            color: white;
            overflow-x: hidden;
            margin: 0;
        }
        .glass {
            background: rgba(255, 255, 255, 0.03);
            backdrop-filter: blur(10px);
            border: 1px solid rgba(255, 255, 255, 0.1);
            transition: all 0.3s ease;
        }
        .gradient-text {
            background: linear-gradient(90deg, #a78bfa, #f472b6, #fb923c);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            font-weight: 900;
        }
        /* The Entry Overlay */
        #overlay {
            position: fixed;
            inset: 0;
            background: black;
            z-index: 100;
            display: flex;
            align-items: center;
            justify-content: center;
            cursor: pointer;
            transition: opacity 0.8s ease, visibility 0.8s;
        }
        .hidden-overlay {
            opacity: 0;
            visibility: hidden;
        }
    </style>
</head>
<body class="min-h-screen">

    <div id="overlay" onclick="enterSite()">
        <div class="text-center">
            <h2 class="text-2xl font-black tracking-widest animate-pulse uppercase">Click to enter the party</h2>
            <p class="text-gray-500 mt-2 text-sm">999 Energy Only</p>
        </div>
    </div>

    <section class="flex flex-col items-center justify-center text-center py-24 px-4">
        <h1 class="text-6xl md:text-8xl gradient-text mb-4 tracking-tighter uppercase">Jon Jon & Friends</h1>
        <p class="text-xl md:text-2xl text-gray-400 font-light mb-8 italic">"Welcome to the party, we don't want it to end."</p>
        
        <a href="https://vrchat.com/home/group/grp_e6ecca5a-828b-4706-9c23-db1723469436" 
           target="_blank"
           class="bg-white text-black px-10 py-4 rounded-full font-bold text-lg hover:scale-105 transition-transform shadow-[0_0_20px_rgba(167,139,250,0.5)]">
            JOIN THE GROUP
        </a>
    </section>

    <main class="max-w-6xl mx-auto px-6 pb-20">
        <div class="grid grid-cols-1 md:grid-cols-3 gap-6">
            
            <div class="glass p-8 rounded-3xl md:col-span-2">
                <h2 class="text-3xl font-bold mb-4">The Community</h2>
                <p class="text-gray-400 leading-relaxed text-lg">
                    A place for real ones. Late-night world hopping, good music, and genuine vibes. 
                    Positive vibes only. Legends never die.
                </p>
                <div class="mt-6 flex gap-4">
                    <span class="px-4 py-1 rounded-full border border-purple-500/30 text-purple-400 text-xs uppercase tracking-widest font-bold">999</span>
                    <span class="px-4 py-1 rounded-full border border-blue-500/30 text-blue-400 text-xs uppercase tracking-widest font-bold">OVO</span>
                    <span class="px-4 py-1 rounded-full border border-orange-500/30 text-orange-400 text-xs uppercase tracking-widest font-bold">VRChat</span>
                </div>
            </div>

            <div class="glass p-4 rounded-3xl border-t-2 border-purple-500 overflow-hidden">
                <h3 class="text-sm font-bold text-gray-400 mb-3 ml-2 uppercase tracking-tighter">The Vibe Station</h3>
                <iframe style="border-radius:12px" 
                    src="https://open.spotify.com/embed/playlist/37i9dQZF1DX6pGi9Yp5L6I?utm_source=generator&theme=0" 
                    width="100%" 
                    height="152" 
                    frameBorder="0" 
                    allowfullscreen="" 
                    allow="autoplay; clipboard-write; encrypted-media; fullscreen; picture-in-picture" 
                    loading="lazy">
                </iframe>
                <p class="text-[10px] text-gray-600 mt-2 text-center">Press play to start the session</p>
            </div>

            <div class="glass p-8 rounded-3xl border-l-4 border-purple-500">
                <h3 class="text-2xl font-bold mb-2">999 Energy</h3>
                <p class="text-gray-400">Turning negativity into something positive. Music that hits the soul.</p>
            </div>

            <div class="glass p-8 rounded-3xl border-l-4 border-blue-500">
                <h3 class="text-2xl font-bold mb-2">The 6 Side</h3>
                <p class="text-gray-400">Late-night energy. Melodic flows. Staying focused on the vision.</p>
            </div>

            <div class="glass p-8 rounded-3xl flex items-center justify-center text-center">
                <p class="text-2xl font-black uppercase tracking-widest opacity-30">Legends Never Die</p>
            </div>

        </div>
    </main>

    <footer class="text-center py-10 border-t border-white/5">
        <p class="text-gray-600 text-sm italic">Jon Jon and Friends • 2026</p>
    </footer>

    <script>
        function enterSite() {
            const overlay = document.getElementById('overlay');
            overlay.classList.add('hidden-overlay');
        }
    </script>

</body>
</html>
