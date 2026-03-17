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
        #overlay {
            position: fixed;
            inset: 0;
            background: black;
            z-index: 100;
            display: flex;
            align-items: center;
            justify-content: center;
            cursor: pointer;
            transition: opacity 0.8s ease;
        }
        /* Hidden YouTube Container */
        #yt-wrapper {
            position: absolute;
            width: 1px;
            height: 1px;
            overflow: hidden;
            opacity: 0;
            pointer-events: none;
        }
    </style>
</head>
<body class="min-h-screen">

    <div id="overlay" onclick="startVibe()">
        <div class="text-center">
            <h2 class="text-2xl font-black tracking-widest animate-pulse">CLICK TO ENTER THE PARTY</h2>
            <p class="text-gray-500 mt-2 text-sm">999 Energy Only • Turn Volume Up</p>
        </div>
    </div>

    <section class="flex flex-col items-center justify-center text-center py-24 px-4">
        <h1 class="text-6xl md:text-8xl gradient-text mb-4 tracking-tighter uppercase">Jon Jon & Friends</h1>
        <p class="text-xl md:text-2xl text-gray-400 font-light mb-8 italic">"Welcome to the party, we don't want it to end."</p>
        
        <a href="https://vrchat.com/home/group/grp_e6ecca5a-828b-4706-9c23-db1723469436" 
           class="bg-white text-black px-10 py-4 rounded-full font-bold text-lg hover:scale-110 transition-transform shadow-[0_0_30px_rgba(167,139,250,0.4)]">
            JOIN VRCHAT GROUP
        </a>
    </section>

    <main class="max-w-6xl mx-auto px-6 pb-20">
        <div class="grid grid-cols-1 md:grid-cols-3 gap-6">
            <div class="glass p-8 rounded-3xl md:col-span-2">
                <h2 class="text-3xl font-bold mb-4">The Community</h2>
                <p class="text-gray-400 leading-relaxed text-lg">A place for real ones. Late-night world hopping and genuine vibes. Legends never die.</p>
            </div>
            <div class="glass p-8 rounded-3xl flex flex-col justify-center border-t-2 border-purple-500">
                <div id="player-status" class="text-xs font-mono text-purple-400 mb-2 uppercase tracking-widest">Player Offline</div>
                <h3 id="track-name" class="text-xl font-bold truncate">Waiting for input...</h3>
                <p class="text-gray-500 text-sm">Now Shuffling Hits</p>
            </div>
        </div>
    </main>

    <div id="yt-wrapper">
        <div id="player"></div>
    </div>

    <script>
        var tag = document.createElement('script');
        tag.src = "https://www.youtube.com/iframe_api";
        var firstScriptTag = document.getElementsByTagName('script')[0];
        firstScriptTag.parentNode.insertBefore(tag, firstScriptTag);

        var player;
        // List of IDs: Drake & Juice WRLD
        var playlist = ['r5SInY60oDM', '0Ir4p7D_9E8', 'fX8W_yT4MvI', '7E6S_mI6Q5Y', 'JMcEb_N_zEw'];

        function onYouTubeIframeAPIReady() {
            player = new YT.Player('player', {
                height: '0',
                width: '0',
                videoId: playlist[Math.floor(Math.random() * playlist.length)],
                playerVars: {
                    'autoplay': 0,
                    'controls': 0,
                    'disablekb': 1,
                    'enablejsapi': 1
                },
                events: {
                    'onReady': onPlayerReady,
                    'onStateChange': onPlayerStateChange
                }
            });
        }

        function onPlayerReady(event) {
            console.log("Player Ready");
        }

        function onPlayerStateChange(event) {
            if (event.data == YT.PlayerState.PLAYING) {
                document.getElementById('player-status').innerText = "LIVE VIBES";
                document.getElementById('track-name').innerText = "Streaming Juice/Drake";
            }
            if (event.data == YT.PlayerState.ENDED) {
                var nextId = playlist[Math.floor(Math.random() * playlist.length)];
                player.loadVideoById(nextId);
            }
        }

        function startVibe() {
            // Hide overlay
            document.getElementById('overlay').style.opacity = '0';
            setTimeout(() => { document.getElementById('overlay').style.display = 'none'; }, 800);

            // Play and Unmute
            if (player) {
                player.unMute();
                player.setVolume(100);
                player.playVideo();
                document.getElementById('player-status').innerText = "BUFFERING...";
            }
        }
    </script>
</body>
</html>
