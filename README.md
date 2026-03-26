<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>CERTIFICATE OF CESSATION</title>
    <style>
        /* Forces the entire page to be a fixed, dark container */
        html, body {
            height: 100%;
            width: 100%;
            margin: 0;
            padding: 0;
            background-color: #030303; /* Deep black background */
            display: flex;
            justify-content: center;
            align-items: center;
            font-family: 'Courier New', Courier, monospace;
            overflow: hidden; /* No scrolling allowed */
        }

        /* The 'document' container that centers everything on screen */
        .document-box {
            width: 90%;
            max-width: 500px;
            background-color: #0c0c0c; /* Slightly lighter document paper color */
            padding: 30px;
            color: #777;
            position: relative;
            box-shadow: 0 0 20px rgba(0,0,0,0.8);
            border: 1px solid #1a1a1a;
            box-sizing: border-box;
        }

        /* Header formatting */
        .doc-header {
            text-align: center;
            margin-bottom: 30px;
            border-bottom: 1px solid #222;
            padding-bottom: 15px;
        }

        .doc-title {
            color: #d1d1d1;
            font-size: 1.1rem;
            letter-spacing: 5px;
            text-transform: uppercase;
        }

        /* Data fields (Label: Value) */
        .field {
            margin-bottom: 12px;
            display: flex;
            font-size: 0.9rem;
        }

        .label {
            width: 35%;
            color: #444;
            font-weight: bold;
            text-transform: uppercase;
        }

        .value {
            width: 65%;
            color: #999;
            font-style: italic;
        }

        /* Cause of Death formatting */
        .cause-box {
            margin-top: 30px;
            padding-top: 20px;
            border-top: 1px solid #222;
        }

        .cause-title {
            color: #444;
            text-transform: uppercase;
            font-size: 0.8rem;
            margin-bottom: 10px;
            display: block;
        }

        .cause-text {
            color: #999;
            font-style: italic;
            line-height: 1.6;
            font-size: 0.95rem;
        }

        /* The requested bureaucratic stamp in the bottom right */
        .stamp-box {
            position: absolute;
            bottom: 20px;
            right: 20px;
            text-align: right;
            max-width: 200px;
        }

        .stamp-line {
            color: #333; /* Dark, faded stamp ink color */
            font-size: 0.75rem;
            letter-spacing: 1.5px;
            text-transform: uppercase;
            font-weight: bold;
        }

        /* Responsive adjustments for very small phones */
        @media (max-width: 480px) {
            .document-box { padding: 20px; }
            .label { width: 40%; }
            .value { width: 60%; font-size: 0.85rem; }
            .stamp-box { bottom: 10px; right: 10px; max-width: 150px; }
            .stamp-line { font-size: 0.65rem; }
        }
    </style>
</head>
<body>

    <div class="document-box">
        
        <div class="doc-header">
            <span class="doc-title">CERTIFICATE OF CESSATION</span>
        </div>

        <div class="field">
            <span class="label">ALIAS:</span>
            <span class="value">JONNYM85</span>
        </div>

        <div class="field">
            <span class="label">GROUP ID:</span>
            <span class="value">JON JON AND FRIENDS (DEFUNCT)</span>
        </div>

        <div class="field">
            <span class="label">SITE DOMAIN:</span>
            <span class="value">JONJON.GITHUB.IO</span>
        </div>

        <div class="field">
            <span class="label">RELATIONS:</span>
            <span class="value">GALAXIA, COOKIES, XFOOD</span>
        </div>

        <div class="field">
            <span class="label">STATUS (AUBREY D GRAHAM):</span>
            <span class="value">INACTIVE FRIEND / KIN (NOT LEAVING)</span>
        </div>

        <div class="cause-box">
            <span class="cause-title">PRIMARY CAUSE:</span>
            <p class="cause-text">
                The high finally wore off, and the house was still empty. I bled into these lines of code until I was a ghost in my own logs, chasing a chemical numbness just to drown out the silence.
            </p>
        </div>

        <p class="cause-text">
            I built a sanctuary for people who only needed a place to leave behind. It’s too heavy to stay in a graveyard I built myself. The door is closed.
        </p>

        <div class="stamp-box">
            <div class="stamp-line">FILED & CLOSED</div>
            <div class="stamp-line">VOID ENTRY #000</div>
            <div class="stamp-line" style="color: #444; border-top: 1px solid #222; padding-top: 5px; margin-top: 5px;">TIME OF DEATH:</div>
            <div class="stamp-line" style="color: #666; font-style: italic;">He's been dead for years.</div>
        </div>

    </div>

</body>
</html>

