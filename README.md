<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>Jon Jon and Friends</title>
    <style>
        * { box-sizing: border-box; margin: 0; padding: 0; }
        
        body {
            background-color: #020202;
            color: #666;
            font-family: 'Georgia', serif;
            height: 100vh;
            width: 100vw;
            display: flex;
            justify-content: center;
            align-items: center;
            overflow: hidden;
            text-align: center;
        }

        /* Main Bio Page */
        .bio-container {
            width: 85%;
            max-width: 450px;
        }

        h1 {
            font-family: 'Courier New', Courier, monospace;
            font-size: 0.8rem;
            letter-spacing: 6px;
            color: #222;
            margin-bottom: 30px;
            text-transform: uppercase;
        }

        p { line-height: 1.8; margin-bottom: 20px; font-style: italic; font-size: 1.05rem; }

        .highlight { color: #888; font-weight: bold; }

        /* Secret Trigger (Bottom Right) */
        .trigger {
            position: fixed;
            bottom: 20px;
            right: 20px;
            font-size: 0.7rem;
            color: #1a1a1a;
            cursor: pointer;
            text-transform: uppercase;
            letter-spacing: 2px;
            font-family: 'Courier New', Courier, monospace;
        }

        /* The Death Certificate Pop-up */
        #deathCert {
            display: none; /* Hidden by default */
            position: fixed;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            width: 90%;
            max-width: 400px;
            background-color: #080808;
            border: 1px solid #1a1a1a;
            padding: 30px;
            z-index: 100;
            text-align: left;
            box-shadow: 0 0 50px #000;
        }

        .cert-header {
            text-align: center;
            border-bottom: 1px solid #222;
            padding-bottom: 10px;
            margin-bottom: 20px;
            color: #444;
            font-size: 0.8rem;
            letter-spacing: 3px;
        }

        .cert-row { margin-bottom: 10px; font-size: 0.8rem; font-family: 'Courier New', Courier, monospace; }
        .cert-label { color: #333; }
        .cert-val { color: #777; font-style: italic; }

        .close-btn {
            margin-top: 20px;
            color: #222;
            font-size: 0.6rem;
            text-align: center;
            display: block;
            cursor: pointer;
        }

        @media (max-width: 480px) {
            p { font-size: 0.95rem; }
        }
    </style>
</head>
<body>

    <div class="bio-container">
        <h1>Jon Jon and Friends</h1>
        <p>I built these walls out of love, thinking they would hold us forever. I wired the lights so no one would ever have to sit in the dark. But the only sound left is my own heartbeat.</p>
        <p>I loved you all from the bottom of my heart. <span class="highlight">Galaxia</span>, <span class="highlight">Aubrey</span>, <span class="highlight">Cookies</span>, and <span class="highlight">Xfood</span>—you were the reason I kept the lights on. Aubrey, I know you’re still here, but watching everyone else drift away makes the site I built feel like a graveyard.</p>
        <p>The door is closed. JonnyM85 out.</p>
    </div>

    <div class="trigger" onclick="openCert()">
        TIME OF DEATH: [ CLICK ]
    </div>

    <div id="deathCert">
        <div class="cert-header">CERTIFICATE OF CESSATION</div>
        <div class="cert-row"><span class="cert-label">SUBJECT:</span> <span class="cert-val">JONNYM85</span></div>
        <div class="cert-row"><span class="cert-label">KIN:</span> <span class="cert-val">AUBREY D GRAHAM</span></div>
        <div class="cert-row"><span class="cert-label">CAUSE:</span> <span class="cert-val">CHOKING ON THE SILENCE.</span></div>
        <div class="cert-row" style="margin-top: 20px; border-top: 1px solid #111; padding-top: 10px;">
            <span class="cert-label">TIME OF DEATH:</span><br>
            <span style="color: #555; font-style: italic; font-size: 0.9rem;">He's been dead for years.</span>
        </div>
        <span class="close-btn" onclick="closeCert()">[ CLOSE FILE ]</span>
    </div>

    <script>
        function openCert() {
            document.getElementById('deathCert').style.display = 'block';
        }
        function closeCert() {
            document.getElementById('deathCert').style.display = 'none';
        }
    </script>

</body>
</html>
