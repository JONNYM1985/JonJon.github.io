<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Cold Reality</title>
    <style>
        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
        }
        body {
            background-color: #020202;
            color: #555;
            font-family: 'Courier New', Courier, monospace;
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
            width: 100vw;
            overflow: hidden;
            text-align: center;
        }

        .content-box {
            width: 85%;
            max-width: 480px;
            animation: flicker 4s linear infinite;
        }

        h1 {
            font-weight: 100;
            font-size: 0.9rem;
            letter-spacing: 8px;
            color: #222;
            margin-bottom: 40px;
            text-transform: uppercase;
        }

        p {
            line-height: 1.6;
            margin-bottom: 25px;
            font-size: 1rem;
            color: #666;
        }

        .names {
            color: #333;
            font-style: italic;
            font-size: 0.85rem;
        }

        .heavy {
            color: #888;
        }

        @keyframes flicker {
            0%, 18%, 22%, 25%, 53%, 57%, 100% { opacity: 1; }
            20%, 24%, 55% { opacity: 0.3; }
        }

        @media (max-width: 480px) {
            p { font-size: 0.9rem; }
        }
    </style>
</head>
<body>

    <div class="content-box">
        <h1>Jon Jon and Friends</h1>
        
        <p>
            I tried to build a paradise, but I ended up just building a cage. 
            Now I’m sitting in the back of the world, chasing a high just to forget how quiet it’s become. 
            The pills don't fix the silence, they just make it feel farther away.
        </p>
        
        <p class="heavy">
            Watching everyone leave while I’m still here holding the bottle. 
            I gave my soul to this site, and now I’m just drowning in the code. 
            I’m so far gone I don’t even recognize the person who built these walls.
        </p>

        <p class="names">
            Galaxia. Aubrey. Cookies. Xfood. <br>
            I loved you all, but the ghosts are too loud now.
        </p>

        <p style="color: #444; font-size: 0.8rem; margin-top: 50px;">
            The lights are flickering out. <br>
            JONNYM85 — FADED.
        </p>
    </div>

</body>
</html>

