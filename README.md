<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>The Void</title>
    <style>
        /* Forces the entire page to be a non-scrollable, centered container */
        html, body {
            height: 100%;
            margin: 0;
            padding: 0;
            background-color: #030303;
            overflow: hidden; /* Prevents accidental scrolling */
            display: grid;
            place-items: center; /* The ultimate centering trick */
        }

        .content-box {
            width: 85%;
            max-width: 420px;
            text-align: center;
            animation: glitch-fade 6s ease-in-out infinite;
        }

        h1 {
            font-family: 'Courier New', Courier, monospace;
            font-weight: 100;
            font-size: 0.8rem;
            letter-spacing: 10px;
            color: #222;
            margin-bottom: 40px;
            text-transform: uppercase;
        }

        p {
            font-family: 'Georgia', serif;
            line-height: 1.8;
            margin-bottom: 20px;
            font-size: 1.05rem;
            color: #666;
            font-style: italic;
        }

        .names {
            font-family: 'Courier New', Courier, monospace;
            color: #3a3a3a;
            font-size: 0.8rem;
            letter-spacing: 2px;
            margin-top: 30px;
        }

        .drug-context {
            color: #444;
            font-size: 0.9rem;
            border-top: 1px solid #111;
            padding-top: 20px;
            margin-top: 20px;
        }

        @keyframes glitch-fade {
            0%, 100% { opacity: 0.2; filter: blur(2px); }
            50% { opacity: 1; filter: blur(0px); }
        }

        /* Mobile specific font sizing */
        @media (max-width: 480px) {
            p { font-size: 0.95rem; }
            h1 { font-size: 0.75rem; letter-spacing: 6px; }
        }
    </style>
</head>
<body>

    <div class="content-box">
        <h1>Jon Jon and Friends</h1>
        
        <p>
            I bled into these lines of code until I had nothing left in my veins. 
            I built a sanctuary for people who only wanted a place to leave behind.
        </p>
        
        <p>
            Now I’m just staring at the wall, chasing a chemical numbness because the silence is a debt I can't pay. 
            The pills don't bring the noise back; they just turn the ghosts into shadows. 
            I’m drowning in a bottle of my own making.
        </p>

        <div class="drug-context">
            The lights are flickering, but nobody's home. <br>
            I loved you all, but the high is finally wearing off.
        </div>

        <div class="names">
            GALAXIA • AUBREY • COOKIES • XFOOD
        </div>

        <p style="color: #1a1a1a; font-size: 0.7rem; margin-top: 40px; text-transform: uppercase; letter-spacing: 4px;">
            JONNYM85 OFFICIALLY LOGS OFF FOR NOW.
        </p>
    </div>

</body>
</html>
