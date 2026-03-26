<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>JONNYM85 | OFFLINE</title>
    <style>
        /* Base setup to prevent zoom/scroll lag */
        * { box-sizing: border-box; margin: 0; padding: 0; }
        html, body {
            height: 100%;
            width: 100%;
            background-color: #050505;
            color: #555;
            font-family: 'Georgia', serif;
            display: flex;
            justify-content: center;
            align-items: center;
            overflow: hidden;
        }

        /* Main Bio Page */
        .main-page {
            width: 85%;
            max-width: 450px;
            text-align: center;
        }

        .rip-header {
            font-family: 'Courier New', Courier, monospace;
            margin-bottom: 20px;
        }

        .rip-header h2 {
            font-size: 3.5rem;
            color: #4a0000; /* Deep Blood Red */
            letter-spacing: 10px;
            margin: 0;
        }

        .rip-header p {
            font-size: 0.8rem;
            color: #222;
            letter-spacing: 5px;
            text-transform: uppercase;
        }

        .bio-text {
            line-height: 1.8;
            font-style: italic;
            font-size: 1.05rem;
            margin-bottom: 40px;
        }

        /* Click Trigger */
        .cert-trigger {
            font-family: 'Courier New', Courier, monospace;
            font-size: 0.75rem;
            color: #888;
            cursor: pointer;
            text-decoration: underline;
            letter-spacing: 2px;
            text-transform: uppercase;
        }

        /* THE DEATH CERTIFICATE (Hidden Pop-up) */
        #deathCertOverlay {
            display: none; /* Starts hidden */
            position: fixed;
            top: 0; left: 0; width: 100%; height: 100%;
            background-color: #000;
            z-index: 1000;
            padding: 30px 15px;
            overflow-y: auto;
        }

        .official-cert {
            border: 1px solid #1a1a1a;
            padding: 25px;
            max-width: 500px;
            margin: 0 auto;
            background: #080808;
            font-family: 'Courier New', Courier, monospace;
            color: #777;
        }

        .cert-top {
            text-align: center;
            border-bottom: 2px solid #222;
            padding-bottom: 15px;
            margin-bottom: 25px;
        }

        .cert-top h3 { color: #444; font-size: 1rem; letter-spacing: 3px; }

        .cert-row {
            display: flex;
            border-bottom: 1px solid #111;
            padding: 10px 0;
            font-size: 0.75rem;
        }

        .c-label { width: 40%; color: #333; font-weight: bold; }
        .c-val { width: 60%; color: #999; font-style: italic; }

        .c-cause {
            margin-top: 25px;
            font-size: 0.85rem;
            line-height: 1.6;
        }

        .c-stamp {
            margin-top: 40px;
            text-align: right;
            border-top: 1px solid #222;
            padding-top: 15px;
        }

        .close-btn {
            display: block;
            margin-top: 30px;
            text-align: center;
            color: #333;
            font-size: 0.65rem;
            cursor: pointer;
        }
    </style>
</head>
<body>

    <div class="main-page">
        <div class="rip-header">
            <h2>RIP</h2>
            <p>JONNYM85 — VRC</p>
        </div>

        <div class="bio-text">
            This instance has been terminated. The battle to sustain a world where everyone else has already moved on has come to an end. We can no longer be the target of the silence, and we can no longer maintain a sanctuary that everyone has already left.
        </div>

        <div class="cert-trigger" onclick="showCert()">
            VIEW THE DEATH CERTIFICATE
        </div>
    </div>

    <div id="deathCertOverlay">
        <div class="official-cert">
            <div class="cert-top">
                <h3>CERTIFICATE OF DEATH</h3>
                <p style="font-size: 0.5rem; color: #222; margin-top: 5px;">DEPARTMENT OF VIRTUAL CESSATION</p>
            </div>

            <div class="cert-row"><span class="c-label">DECEASED:</span> <span class="c-val">JONNYM85</span></div>
            <div class="cert-row"><span class="c-label">WORLD ID:</span> <span class="c-val">JON JON AND FRIENDS</span></div>
            <div class="cert-row"><span class="c-label">FILE NO:</span> <span class="c-val">000-VOID-85</span></div>

            <div class="c-cause">
                <span style="color:#333; font-size: 0.7rem;">[ PRIMARY CAUSE ]</span><br>
                Systemic collapse of the digital sanctuary. Subject reported chronic emotional exhaustion from attempting to maintain light in a space that had been abandoned. 
            </div>

            <div class="c-cause">
                <span style="color:#333; font-size: 0.7rem;">[ DISPOSITION ]</span><br>
                The door is officially closed. Memory retention only.
            </div>

            <div class="c-stamp">
                <span style="display:block; font-size: 0.6rem; color: #222;">FILED & VERIFIED</span>
                <span style="display:block; color: #444; margin-top: 5px; font-weight: bold;">TIME OF DEATH:</span>
                <span style="color: #666; font-style: italic;">TUESDAY, MARCH 24TH, 2026.</span>
            </div>

            <div class="close-btn" onclick="hideCert()">[ CLOSE FILE ]</div>
        </div>
    </div>

    <script>
        function showCert() {
            document.getElementById('deathCertOverlay').style.display = 'block';
        }
        function hideCert() {
            document.getElementById('deathCertOverlay').style.display = 'none';
        }
    </script>

</body>
</html>

