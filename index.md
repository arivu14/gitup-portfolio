---
layout: null
---
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Arivazhagan | SOC Portfolio</title>
    <style>
        /* BASE THEME & BACKGROUND */
        * { box-sizing: border-box; }
        html, body { 
            margin: 0; padding: 0; width: 100%; 
            background: linear-gradient(rgba(10, 14, 20, 0.8), rgba(10, 14, 20, 0.8)), url('cc.jpg');
            background-size: cover; background-position: center; background-attachment: fixed;
            color: white; font-family: 'Consolas', 'Monaco', 'Courier New', monospace; 
            overflow-x: hidden; 
        }
        
 /* BLUR EFFECT */
        .page-wrap.is-blurred { filter: blur(20px); pointer-events: none; transition: 0.4s ease; }

 /* HERO SECTION */
        .hero { width: 100%; padding: 60px 0; display: flex; align-items: center; justify-content: center; }
        .hero-container { width: 90%; max-width: 1200px; display: flex; justify-content: space-between; align-items: center; }
        .text-side h1 { font-size: 4rem; margin: 0; font-weight: 900; letter-spacing: -2px; color: #fff; }
        .text-side .role { font-size: 1.8rem; color: #38bdf8; display: block; margin: 5px 0 15px 0; }
        .contact-info { font-size: 0.95rem; line-height: 1.6; color: #cbd5e1; }
        .pfp { width: 220px; height: 220px; border-radius: 50%; border: 4px solid #38bdf8; object-fit: cover; box-shadow: 0 0 30px rgba(56, 189, 248, 0.3); }

/* LEFT-ALIGNED INVESTIGATION SECTION */
        .investigation-section { width: 90%; max-width: 1200px; margin: 0 auto; padding-bottom: 80px; text-align: left; }
        
.report-summary { 
            background: rgba(15, 23, 42, 0.9); 
            border: 1px solid #334155; 
            padding: 20px; 
            border-radius: 8px; 
            margin-bottom: 30px; 
            font-size: 0.85rem; 
            line-height: 1.4; 
            white-space: pre-wrap;
            color: #94a3b8;
        }

.trigger-box {
            max-width: 400px; /* Medium-small rectangle */
            cursor: pointer; 
            border-radius: 12px; 
            border: 2px solid #334155; 
            overflow: hidden;
            transition: 0.3s ease;
            box-shadow: 0 15px 35px rgba(0,0,0,0.6);
            margin-bottom: 30px;
        }
        .trigger-box:hover { border-color: #38bdf8; transform: translateY(-5px); }
        .trigger-box img { width: 100%; display: block; }
        .trigger-footer { padding: 15px; background: #1e293b; color: #38bdf8; font-weight: bold; font-size: 0.8rem; text-align: center; }

.escalation-brief {
            background: rgba(56, 189, 248, 0.05);
            border-left: 4px solid #38bdf8;
            padding: 20px;
            max-width: 600px;
            border-radius: 4px;
        }
        .escalation-brief h3 { color: #38bdf8; margin-top: 0; font-size: 1.1rem; }
        .escalation-brief ul { list-style: none; padding: 0; margin: 0; }
        .escalation-brief li { margin-bottom: 8px; font-size: 0.9rem; }
        .escalation-brief b { color: #fff; }

 /* MODAL SLIDESHOW */
        .modal-overlay {
            display: none; position: fixed; z-index: 9999; left: 0; top: 0;
            width: 100%; height: 100%; background: rgba(0,0,0,0.9);
            align-items: center; justify-content: center;
        }
        .modal-content { position: relative; width: 90%; max-width: 1000px; display: flex; flex-direction: column; align-items: center; }
        .modal-img { max-width: 100%; max-height: 65vh; border: 2px solid #38bdf8; border-radius: 8px; }
        .nav-btn { cursor: pointer; position: absolute; top: 40%; color: #38bdf8; font-size: 60px; transition: 0.3s; user-select: none; }
        .btn-prev { left: -100px; } .btn-next { right: -100px; }
        .details-panel { background: #1e293b; padding: 20px; margin-top: 20px; border-radius: 8px; width: 100%; border-left: 5px solid #38bdf8; }
        .close-btn { position: absolute; top: -60px; right: 0; color: white; font-size: 45px; cursor: pointer; }

        #data-store { display: none; }

 @media (max-width: 1100px) {
            .hero-container { flex-direction: column-reverse; text-align: center; }
            .investigation-section { text-align: center; }
            .trigger-box { margin: 0 auto 30px auto; }
            .escalation-brief { margin: 0 auto; text-align: left; }
            .btn-prev { left: 10px; } .btn-next { right: 10px; }
        }
    </style>
</head>
<body>

<div class="page-wrap" id="main-site">
    <div class="hero">
        <div class="hero-container">
            <div class="text-side">
                <h1>ARIVAZHAGAN</h1>
                <span class="role">SOC Analyst L1</span>
                <div class="contact-info">
                    <strong>C.N:</strong> +91 6379944366<br>
                    <strong>Email:</strong> arivazhagans1411@gmail.com<br>
                    <strong>LinkedIn:</strong> <a href="https://linkedin.com/in/arivazhagan" target="_blank" style="color:#38bdf8;">Profile</a>
                </div>
            </div>
            <img src="Screenshot_20260103_200618_Gallery.jpg" class="pfp" alt="Arivazhagan">
        </div>
    </div>

<div class="investigation-section">
        <div class="report-summary">================================================================================
PROJECT REPORT: SSH BRUTE FORCE DETECTION & INCIDENT RESPONSE
================================================================================

DATE:         February 06, 2026
ANALYST:      Arivazhagan
TARGET SYSTEM: Ubuntu Linux (Agent 004)
TOOLS USED:   Wazuh SIEM, Linux CLI, IPTables, AbuseIPDB (OSINT)

--------------------------------------------------------------------------------
1. INITIAL PHASE: AGENT DEPLOYMENT & RECOVERY
--------------------------------------------------------------------------------
* STATUS: Manual recovery of corrupted 'ossec.conf' after network crash.
* FIX: Restored agent handshake with Manager IP (10.48.90.166).

--------------------------------------------------------------------------------
2. DETECTION & ANALYSIS
--------------------------------------------------------------------------------
* ALERT: Rule 5712 - SSH Brute Force attempt detected (Level 10).
* ATTACKER: Source IP 141.98.81.37 targeting "Administrators".
* OSINT: AbuseIPDB confirmed malicious botnet with 100% confidence score.

--------------------------------------------------------------------------------
3. RESPONSE & MITIGATION
--------------------------------------------------------------------------------
* ACTION: Emergency containment via IPTables Host Firewall.
* COMMAND: sudo iptables -I INPUT -s 141.98.81.37 -j DROP
* MITRE: Credential Access (TA0006) | Brute Force (T1110)
================================================================================</div>

  <div class="trigger-box" onclick="launchGallery(0)">
            <img src="01.png" alt="Investigation Snapshot">
            <div class="trigger-footer">VIEW 13-STEP EVIDENCE SLIDESHOW ➔</div>
        </div>

  <div class="escalation-brief">
            <h3>Tier 2 Escalation Brief (5 W's)</h3>
            <ul>
                <li><b>WHO:</b> Malicious Source IP 141.98.81.37 (Confirmed Botnet).</li>
                <li><b>WHAT:</b> High-frequency SSH Brute Force attack targeting Ubuntu Agent 004.</li>
                <li><b>WHERE:</b> Target System /var/log/auth.log via Wazuh SIEM monitoring.</li>
                <li><b>WHEN:</b> Incident identified and mitigated on Feb 06, 2026.</li>
                <li><b>WHY:</b> Attempted unauthorized credential access (TA0006). L1 mitigated via IPTables.</li>
            </ul>
        </div>
    </div>
</div>

<div id="modalBox" class="modal-overlay">
    <div class="modal-content">
        <span class="close-btn" onclick="exitGallery()">&times;</span>
        <a class="nav-btn btn-prev" onclick="stepSlide(-1)">&#10094;</a>
        <img id="mainViewer" class="modal-img">
        <a class="nav-btn btn-next" onclick="stepSlide(1)">&#10095;</a>
        <div class="details-panel">
            <p id="viewerCap" style="margin:0;"></p>
        </div>
    </div>
</div>

<div id="data-store">
    <div data-img="01.png" data-text="<b>Step 1: Dashboard Overview</b> - Initial monitoring setup."></div>
    <div data-img="02.png" data-text="<b>Step 2: Metric Analysis</b> - Tracking event volume."></div>
    <div data-img="03.png" data-text="<b>Step 3: Log Review</b> - Identifying baseline failures."></div>
    <div data-img="04.png" data-text="<b>Step 4: Attack Capture</b> - Attacker terminal during execution."></div>
    <div data-img="05.png" data-text="<b>Step 5: Alert Spike</b> - Rapid increase in Level 12 alerts."></div>
    <div data-img="06.png" data-text="<b>Step 6: Filtering Rule 5712</b> - Isolating Brute Force attempts."></div>
    <div data-img="07.png" data-text="<b>Step 7: Rule 5710 Correlation</b> - Investigating auth logs."></div>
    <div data-img="08.png" data-text="<b>Step 8: Incident Confirmation</b> - Confirming attack scope."></div>
    <div data-img="09.png" data-text="<b>Step 9: Source IP Extraction</b> - Pinpointing 141.98.81.37."></div>
    <div data-img="10.png" data-text="<b>Step 10: OSINT Pivot</b> - 100% Abuse Confidence on AbuseIPDB."></div>
    <div data-img="11.png" data-text="<b>Step 11: MITRE Mapping</b> - Technique T1110 classification."></div>
    <div data-img="12.png" data-text="<b>Step 12: Active Containment</b> - Terminal isolation commands."></div>
    <div data-img="13.png" data-text="<b>Step 13: Mitigation Verified</b> - IPTables DROP policy active."></div>
</div>

<script>
    let activeStep = 0;
    const slides = document.querySelectorAll('#data-store div');
    const modal = document.getElementById('modalBox');
    const bgWrap = document.getElementById('main-site');

    function launchGallery(n) {
        activeStep = n;
        modal.style.display = "flex";
        bgWrap.classList.add('is-blurred');
        render();
    }

    function exitGallery() {
        modal.style.display = "none";
        bgWrap.classList.remove('is-blurred');
    }

    function stepSlide(n) {
        activeStep += n;
        if (activeStep >= slides.length) activeStep = 0;
        if (activeStep < 0) activeStep = slides.length - 1;
        render();
    }

    function render() {
        const item = slides[activeStep];
        document.getElementById('mainViewer').src = item.getAttribute('data-img');
        document.getElementById('viewerCap').innerHTML = item.getAttribute('data-text');
    }

    window.onclick = function(e) { if (e.target == modal) exitGallery(); }
</script>

</body>
</html>
