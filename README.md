<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>TERMINATION COMPLETE | JONNYM85</title>
    <style>
        * { box-sizing: border-box; margin: 0; padding: 0; }
        
        /* Forces the page to occupy the full screen height and width */
        html, body {
            height: 100%;
            width: 100%;
            margin: 0;
            padding: 0;
            background-color: #030303; /* Deep black background */
            font-family: 'Courier New', Courier, monospace;
            display: flex;
            justify-content: center;
            align-items: center;
            overflow: hidden; /* No scrolling allowed */
            position: fixed; /* Locked centering for mobile */
            color: #444; /* Dark gray text */
        }

        /* The main container - modeled after Omegle's flat text layout */
        .memorial-container {
            width: 90%;
            max-width: 500px;
            text-align: left;
            padding: 20px;
        }

        /* The Tombstone Header (Omegle Style) */
        .tombstone {
            text-align: center;
            margin-bottom: 30px;
            color: #1a1a1a;
            letter-spacing: 2px;
            text-transform: uppercase;
        }

        .tombstone h1 { font-size: 1.1rem; line-height: 1; margin-bottom: 5px; }
        .tombstone h2 { font-size: 2.2rem; line-height: 1; color: #111; }

        /* General site status */
        .status-header {
            color: #d11c1c; /* Blood red text for 'Shutdown' status */
            font-weight: bold;
            font-size: 0.95rem;
            text-transform: uppercase;
            text-align: center;
            letter-spacing: 3px;
            margin-bottom: 30px;
            border-top: 1px solid #111;
            padding-top: 10px;
        }

        /* Standard data rows (Status: Offline) */
        .field {
            margin-bottom: 15px;
            display: flex;
            border-bottom: 1px solid #111;
            padding-bottom: 8px;
        }

        .label {
            width: 40%;
            color: #2a2a2a;
            font-weight: bold;
            text-transform: uppercase;
            font-size: 0.8rem;
        }

        .value {
            width: 60%;
            color: #777;
            font-style: italic;
            font-size: 0.85rem;
        }

        /* The System Message (Cause of Termination) */
        .bureau-text {
            color: #666;
            line-height: 1.7;
            margin-top: 30px;
            border-top: 1px solid #111;
            padding-top: 20px;
            font-size: 1rem;
            text-align: left;
            font-family: 'Georgia', serif; /* Poetic font for the system letter */
            font-style: italic;
        }

        /* The Bureaucratic Stamp (Bottom Right) */
        .stamp-box {
            position: fixed;
            bottom: 20px;
            right: 20px;
            text-align: right;
            max-width: 180px;
            font-family: 'Courier New', Courier, monospace;
        }

        .stamp-line {
            color: #111; /* Very faint, faded stamp color */
            font-size: 0.75rem;
            letter-spacing: 1.5px;
            text-transform: uppercase;
            display: block;
        }

        /* Responsive adjustments for mobile */
        @media (max-width: 480px) {
            .tombstone h2 { font-size: 1.8rem; }
            .value { font-size: 0.8rem; }
            .bureau-text { font-size: 0.95rem; }
            .stamp-box { bottom: 10px; right: 10px; }
        }
    </style>
</head>
<body>

    <div class="memorial-container">
        
        <div class="tombstone">
            <h1>MEMORIAL</h1>
            <h2>RIP</h2>
            <h1>JONNYM85 — VRC</h1>
        </div>

        <div class="status-header">SYSTEM SHUTDOWN</div>

        <div class="field">
            <span class="label">ALIAS ID:</span>
            <span class="value">JONNYM85</span>
        </div>

        <div class="field">
            <span class="label">INSTANCE:</span>
            <span class="value">VRChat World Index (OFFLINE)</span>
        </div>

        <div class="field">
            <span class="label">STATUS:</span>
            <span class="value">Permanently Inactive.</span>
        </div>

        <div class="field">
            <span class="label">DISPOSITION:</span>
            <span class="value">Deleted from Public Server Logs.</span>
        </div>

        <div class="bureau-text">
            This instance has been terminated. The battle to sustain a world where everyone else has already moved on has come to an end. We can no longer be the target of the silence, and we can no longer maintain a sanctuary that everyone has already left. 
            <br><br>
            A world built out of love, where the creator wired the lights so no one would ever sit in the dark, is too heavy to carry alone. The lights are flickering out, and the door is closed. We are walking away while there is still a memory left to save. 
        </div>

        <div class="stamp-box">
            <span class="stamp-line">VOID ENTRY #000</span>
            <span class="stamp-line">FILED & CLOSED</span>
            <span class="stamp-line" style="color: #222; border-top: 1px solid #111; padding-top: 5px; margin-top: 5px;">TIME OF DEATH:</span>
            <span class="stamp-line" style="color: #666; font-style: italic;">He's been dead for years.</span>
        </div>

        <p style="color: #111; font-size: 0.7rem; text-align: center; margin-top: 50px;">
            JONNYM85 IS DEAD. LONG LIVE THE VOID.
        </p>

    </div>

</body>
</html>


