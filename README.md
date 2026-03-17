<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Jon Jon & Friends | OVO 999</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;700;900&display=swap" rel="stylesheet">
    <style>
        body { font-family: 'Inter', sans-serif; background: #0a0a0c; color: white; margin: 0; overflow-x: hidden; }
        /* Background inspired by your sticker */
        .bg-gradient {
            background: radial-gradient(circle at top right, #4c1d95, #000000, #1e1b4b);
            background-attachment: fixed;
        }
        .glass { background: rgba(255, 255, 255, 0.03); backdrop-filter: blur(15px); border: 1px solid rgba(255, 255, 255, 0.1); border-radius: 2rem; }
        .gradient-text { background: linear-gradient(90deg, #d8b4fe, #f472b6, #818cf8); -webkit-background-clip: text; -webkit-text-fill-color: transparent; font-weight: 900; }
        
        #overlay { position: fixed; inset: 0; background: black; z-index: 1000; display: flex; align-items: center; justify-content: center; cursor: pointer; }
        .hidden-overlay { display: none !important; }
        
        .logo-glow { filter: drop-shadow(0 0 20px rgba(167, 139, 250, 0.5)); transition: 0.3s; }
        .logo-glow:hover { transform: scale(1.05); filter: drop-shadow(0 0 40px rgba(167, 139, 250, 0.8)); }
    </style>
</head>
<body class="min-h-screen bg-gradient">

    <div id="overlay" onclick="document.getElementById('overlay').style.display='none'">
        <div class="text-center">
            <h2 class="text-3xl font-black tracking-widest animate-pulse uppercase">Enter the Vibe</h2>
            <p class="text-gray-500 mt-2 text-sm uppercase italic">Palm trees & Midnight Skies</p>
        </div>
    </div>

    <section class="flex flex-col items-center justify-center text-center pt-20 pb-10 px-4">
        <a href="https://vrchat.com/home/group/grp_e6ecca5a-828b-4706-9c23-db1723469436" target="_blank" class="block mb-6">
            <img src="logo.png" alt="Join Jon Jon and Friends" class="w-64 md:w-80 logo-glow">
        </a>
        
        <h1 class="text-5xl md:text-7xl gradient-text tracking-tighter uppercase leading-tight">THE INNER CIRCLE</h1>
        <p class="text-lg text-gray-400 font-light mt-2 max-w-lg">"Late night melodies, palm trees, and the family that never sleeps."</p>
    </section>

    <main class="max-w-6xl mx-auto px-6 pb-20">
        <div class="grid grid-cols-1 md:grid-cols-2 gap-8">
            
            <div class="glass p-8 flex flex-col justify-center border-t-2 border-pink-500">
                <h3 class="text-xs font-bold text-pink-400 mb-4 uppercase tracking-[0.3em]">Now Streaming</h3>
                <div class="rounded-xl overflow-hidden shadow-2xl">
                    <iframe style="border-radius:12px" src="https://open.spotify.com/embed/playlist/37i9dQZF1EIdZp8n0S7v87?utm_source=generator&theme=0" width="100%" height="352" frameBorder="0" allowfullscreen="" allow="autoplay; clipboard-write; encrypted-media; fullscreen; picture-in-picture" loading="lazy"></iframe>
                </div>
            </div>

            <div class="flex flex-col gap-6">
                <div class="glass p-8 h-full">
                    <h2 class="text-2xl font-bold mb-4 text-purple-300">The 999 / OVO Vibe</h2>
                    <p class="text-gray-400 leading-relaxed italic">
                        "A place for real ones. We don't just world hop; we make memories. Positive energy only. If you're looking for the late-night sound, you found it."
                    </p>
                    <div class="mt-8 grid grid-cols-2 gap-4">
                        <div class="bg-white/5 p-4 rounded-2xl border border-white/10">
                            <p class="text-[10px] text-gray-500 uppercase font-bold">Status</p>
                            <p class="text-green-400 font-bold">ALWAYS LIVE</p>
                        </div>
                        <div class="bg-white/5 p-4 rounded-2xl border border-white/10">
                            <p class="text-[10px] text-gray-500 uppercase font-bold">Vibe Type</p>
                            <p class="text-blue-400 font-bold">MELODIC</p>
                        </div>
                    </div>
                </div>
            </div>

        </div>
    </main>

    <footer class="text-center py-10 opacity-30">
        <p class="text-sm tracking-widest font-bold uppercase">Jon Jon x Friends • Est. 2026</p>
    </footer>

</body>
</html>
