<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>OFFLINE</title>
    <style>
        /* The most basic, stable CSS possible to prevent freezing */
        body {
            background-color: #000;
            color: #444;
            font-family: 'Courier New', Courier, monospace;
            margin: 0;
            padding: 40px 20px;
            display: block; /* Removed Flexbox to prevent layout freezing */
            text-align: center;
        }

        .tombstone {
            margin-bottom: 50px;
            color: #111;
        }

        .tombstone h1 { font-size: 1.2rem; margin: 0; letter-spacing: 5px; }
        .tombstone h2 { font-size: 3rem; margin: 10px 0; color: #0a0a0a; }

        .status-line {
            color: #600; /* Dark red */
            font-size: 0.8rem;
            letter-spacing: 3px;
            margin-bottom: 40px;
        }

        .data-block {
            max-width: 400px;
            margin: 0 auto;
            text-align: left;
            border-top: 1px solid #111;
            padding-top: 20px;
        }

        .row {
            margin-bottom: 15px;
            font-size: 0.85rem;
        }

        .label { color: #222; font-weight: bold; }
        .value { color: #666; font-style: italic; }

        .message {
            max-width: 450px;
            margin: 40px auto;
            text-align: left;
            color: #555;
            line-height: 1.6;
            font-size: 0.95rem;
            border-bottom: 1px solid #111;
            padding-bottom: 30px;
        }

        .stamp {
            text-align: right;
            max-width: 450px;
            margin: 20px auto;
            font-size: 0.7rem;
            color: #1a1a1a;
        }

        .final {
            margin-top: 60px;
            color: #0f0f0f;
            font-size: 0.7rem;
            letter-spacing: 2px;
        }
    </style>
</head>
<body>

    <div class="tombstone">
        <h1>MEMORIAL</h1>
        <h2>RIP</h2>
        <h1>JONNYM85 — VRC</h1>
    </div>

    <div class="status-line">TERMINATION COMPLETE</div>

    <div class="data-block">
        <div class="row"><span class="label">ID:</span> <span class="value">JONNYM85</span></div>
        <div class="row"><span class="label">LOC:</span> <span class="value">VRChat World Index</span></div>
        <div class="row"><span class="label">LOG:</span> <span class="value">Permanently Inactive</span></div>
    </div>

    <div class="message">
        This instance has been terminated. The battle to sustain a world where everyone else has already moved on has come to an end. We can no longer be the target of the silence, and we can no longer maintain a sanctuary that everyone has already left. 
        <br><br>
        A world built out of love, where the creator wired the lights so no one would ever sit in the dark, is too heavy to carry alone. The lights are flickering out, and the door is closed. We are walking away while there is still a memory left to save. 
    </div>

    <div class="stamp">
        VOID ENTRY #000<br>
        FILED & CLOSED<br><br>
        <span style="color: #333;">TIME OF DEATH:</span><br>
        <span style="color: #555; font-style: italic; font-size: 0.85rem;">View Death Certificate.</span>
    </div>

    <div class="final">
        JONNYM85 IS DEAD. LONG LIVE THE VOID.
    </div>

</body>
</html>
