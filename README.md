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
        }
        .glass {
            background: rgba(255, 255, 255, 0.03);
            backdrop-filter: blur(10px);
            border: 1px solid rgba(255, 255, 255, 0.1);
            transition: all 0.3s ease;
        }
        .glass:hover {
            background: rgba(255, 255, 255, 0.07);
            border-color: rgba(255, 255, 255, 0.3);
            transform: translateY(-5px);
        }
        .gradient-text {
            background: linear-gradient(90deg, #a78bfa, #f472b6, #fb923c);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            font-weight: 900;
        }
        .glow-button {
            box-shadow: 0 0 15px rgba(167, 139, 250, 0.4);
        }
        .glow-button:hover {
            box-shadow: 0 0 25px rgba(167, 139, 250, 0.7);
        }
    </style>
</head>
<body class="min-h-screen">

    <section class="flex flex-col items-center justify-center text-center py-24 px-4">
        <h1 class="text-6xl md:text-8xl gradient-text mb-4 tracking-tighter">JON JON & FRIENDS</h1>
        <p class="text-xl md:text-2xl text-gray-400 font-light mb-8 italic">"Welcome to the party, we don't want it to end."</p>
        
        <a href="https://vrchat.com/home/group/grp_e6ecca5a-828b-4706-9c23-db1723469436" 
           class="glow-button bg-white text-black px-10 py-4 rounded-full font-bold text-lg hover:scale-105 transition-transform">
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
            </div>

            <div class="glass p-8 rounded-3xl flex flex-col justify-center">
                <span class="text-5xl mb-2">🎶</span>
                <h3 class="text-xl font-bold">100% Chill</h3>
                <p class="text-gray-400">Melodic tracks & memories.</p>
            </div>

            <div class="glass p-8 rounded-3xl border-l-4 border-purple-500">
                <h3 class="text-2xl font-bold mb-2">999 Energy</h3>
                <p class="text-gray-400">Turning negativity into something positive. Music that hits the soul.</p>
            </div>

            <div class="glass p-8 rounded-3xl border-l-4 border-blue-500">
                <h3 class="text-2xl font-bold mb-2">The 6 Side</h3>
                <p class="text-gray-400">Late-night energy. Melodic flows. We stay focused.</p>
            </div>

            <div class="glass p-8 rounded-3xl flex items-center justify-center text-center">
                <p class="text-2xl font-black uppercase tracking-widest opacity-50">Vibe Check: Passed</p>
            </div>

        </div>
    </main>

    <footer class="text-center py-10 border-t border-white/10">
        <p class="text-gray-500 text-sm">Jon Jon and Friends • VRChat Community • 2026</p>
    </footer>

</body>
</html>
