<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>JonnyM85 | Final Entry</title>
    <style>
        * { box-sizing: border-box; margin: 0; padding: 0; }
        
        /* The Absolute Centering Fix */
        html, body {
            height: 100%;
            width: 100%;
            background-color: #020202;
            color: #555;
            font-family: 'Georgia', serif;
            display: flex;
            justify-content: center;
            align-items: center;
            overflow: hidden; 
            position: fixed; /* Prevents mobile scroll-bounce */
        }

        /* Main Bio Page */
        .bio-container {
            width: 85%;
            max-width: 450px;
            text-align: center;
        }

        h1 {
            font-family: 'Courier New', Courier, monospace;
            font-size: 0.8rem;
            letter-spacing: 6px;
            color: #1a1a1a;
            margin-bottom: 30px;
            text-transform: uppercase;
        }

        p { line-height: 1.8; margin-bottom: 20px; font-style: italic; font-size: 1.05rem; }

        .trigger {
            position: fixed;
            bottom: 20px;
            right: 20px;
            font-size: 0.7rem;
            color: #111;
            cursor: pointer;
            text-transform: uppercase;
            letter-spacing: 2px;
            font-family: 'Courier New', Courier, monospace;
            border-bottom: 1px solid #111;
        }

        /* The Death Certificate - Full Screen Mobile */
        #deathCert {
            display: none;
            position: fixed;
            top: 0; left: 0; width: 100%; height: 100%;
            background-color: #080808;
            z-index: 1000;
            padding: 40px 20px;
            color: #777;
            font-family: 'Courier New', Courier, monospace;
            overflow-y: auto; /* Allows reading if it's long on small phones */
        }

        .cert-border {
            border: 2px solid #1a1a1a;
            padding: 20px;
            height: auto;
            max-width: 500px;
            margin: 0 auto;
        }

        .cert-header {
            text-align: center;
            border-bottom: 2px solid #222;
            padding-bottom: 10px;
            margin-bottom: 25px;
        }

        .cert-header h2 { font-size: 1rem; color: #444; letter-spacing: 4px; }

        .row { display: flex; border-bottom: 1px solid #111; padding: 8px 0; font-size: 0.75rem; }
        .label { width: 40%; color: #333; font-weight: bold; text-transform: uppercase; }
        .val { width: 60%; color: #999; font-style: italic; }

        .cause-section { margin-top: 25px; }
        .cause-title { font-size: 0.7rem; color: #333; text-decoration: underline; margin-bottom: 10px; display: block; }
        .cause-desc { font-size: 0.85rem; line-height: 1.5; color: #888; }

        .stamp {
            margin-top: 40px;
            text-align: right;
            border-top: 1px solid #222;
            padding-top: 10px;
        }

        .close-btn {
            display: block;
            text-align: center;
            margin-top: 30px;
            color: #222;
            font-size: 0.6rem;
            text-decoration: none;
            cursor: pointer;
        }
    </style>
</head>
<body>

    <div class="bio-container">
        <h1>Jon Jon and Friends</h1>
        <p>I built these walls out of love, thinking they would hold us forever. I wired the lights so no one would ever have to sit in the dark. But the only sound left is my own heartbeat.</p>
        <p>I loved you all from the bottom of my heart. <strong>Galaxia</strong>, <strong>Aubrey</strong>, <strong>Cookies</strong>, and <strong>Xfood</strong>—you were the reason I kept the lights on. Aubrey, I know you’re still here, but watching everyone else drift away makes the site I built feel like a graveyard.</p>
        <p>The door is closed. JonnyM85 out.</p>
    </div>

    <div class="trigger" onclick="openCert()">
        OFFICIAL RECORD: [ VIEW ]
    </div>

    <div id="deathCert">
        <div class="cert-border">
            <div class="cert-header">
                <h2>STATE OF SILENCE</h2>
                <p style="font-size: 0.6rem; color: #222;">DEPARTMENT OF VIRTUAL CESSATION</p>
            </div>

            <div class="row"><span class="label">FILE NUMBER:</span> <span class="val">#000-JM85-VOID</span></div>
            <div class="row"><span class="label">NAME:</span> <span class="val">JONNYM85</span></div>
            <div class="row"><span class="label">PLACE:</span> <span class="val">VRC / JON JON & FRIENDS</span></div>
            <div class="row"><span class="label">NEXT OF KIN:</span> <span class="val">AUBREY D GRAHAM</span></div>
            <div class="row"><span class="label">WITNESSES:</span> <span class="val">GALAXIA, COOKIES, XFOOD</span></div>

            <div class="cause-section">
                <span class="cause-title">PART I: IMMEDIATE CAUSE OF DEATH</span>
                <p class="cause-desc">Complete emotional exhaustion following the systemic collapse of a social sanctuary. Subject reported "choking on the silence" while attempting to maintain power in an empty home world.</p>
            </div>

            <div class="cause-section">
                <span class="cause-title">PART II: CONTRIBUTING FACTORS</span>
                <p class="cause-desc">Prolonged exposure to betrayal, chemical numbness via pills and bottles, and the realization that a creator cannot live inside a graveyard of their own making.</p>
            </div>

            <div class="stamp">
                <span style="display:block; color:#333; font-size:0.7rem;">STATUS: PERMANENTLY INACTIVE</span>
                <span style="display:block; color:#444; margin-top:5px;">TIME OF DEATH:</span>
                <span style="color:#888; font-style:italic; font-size:0.9rem;">He's been dead for years.</span>
            </div>

            <span class="close-btn" onclick="closeCert()">[ CLOSE FILE ]</span>
        </div>
    </div>

    <script>
        function openCert() { document.getElementById('deathCert').style.display = 'block'; }
        function closeCert() { document.getElementById('deathCert').style.display = 'none'; }
    </script>

</body>
</html>

