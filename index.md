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
            background: linear-gradient(rgba(10, 14, 20, 0.85), rgba(10, 14, 20, 0.85)), url('cc.jpg');
            background-size: cover; background-position: center; background-attachment: fixed;
            color: white; font-family: 'Consolas', 'Monaco', 'Courier New', monospace; 
            overflow-x: hidden; 
        }
        
 /* BLUR EFFECT */
        .page-wrap.is-blurred { filter: blur(20px); pointer-events: none; transition: 0.4s ease; }

   /* HERO SECTION */
        .hero { width: 100%; padding: 50px 0; display: flex; align-items: center; justify-content: center; }
        .hero-container { width: 90%; max-width: 1200px; display: flex; justify-content: space-between; align-items: center; }
        .text-side h1 { font-size: 3.5rem; margin: 0; font-weight: 900; letter-spacing: -1px; color: #fff; }
        .text-side .role { font-size: 1.6rem; color: #38bdf8; display: block; margin: 5px 0 10px 0; }
        .contact-info { font-size: 0.9rem; line-height: 1.6; color: #cbd5e1; font-family: sans-serif; }
        .pfp { width: 200px; height: 200px; border-radius: 50%; border: 3px solid #38bdf8; object-fit: cover; box-shadow: 0 0 30px rgba(56, 189, 248, 0.3); }

        /* LEFT-ALIGNED INVESTIGATION LAYOUT */
        .investigation-section { width: 90%; max-width: 1200px; margin: 0 auto; padding-bottom: 80px; text-align: left; }
        
 /* SHORT MISSION SUMMARY */
        .mission-summary {
            max-width: 800px;
            margin-bottom: 30px;
            font-family: sans-serif;
            line-height: 1.6;
            color: #38bdf8;
            font-weight: bold;
            font-size: 1.1rem;
        }

 /* THE TERMINAL PROJECT REPORT */
        .report-summary { 
            background: rgba(15, 23, 42, 0.95); 
            border: 1px solid #334155; 
            padding: 25px; 
            border-radius: 8px; 
            margin-bottom: 40px; 
            font-size: 0.9rem; 
            line-height: 1.4; 
            white-space: pre-wrap;
            color: #d1d5db;
            box-shadow: 0 10px 30px rgba(0,0,0,0.5);
        }
  /* THE TRIGGER BOX (REDUCED & LEFT) */
        .trigger-box {
            max-width: 400px; 
            cursor: pointer; 
            border-radius: 12px; 
            border: 2px solid #334155; 
            overflow: hidden;
            transition: 0.3s ease;
            box-shadow: 0 15px 35px rgba(0,0,0,0.6);
            margin-bottom: 40px;
        }
        .trigger-box:hover { border-color: #38bdf8; transform: translateY(-5px); }
        .trigger-box img { width: 100%; display: block; height: auto; }
        .trigger-footer { padding: 15px; background: #1e293b; color: #38bdf8; font-weight: bold; font-size: 0.8rem; text-align: center; font-family: sans-serif; }

 /* ESCALATION RATIONALE */
        .escalation-brief {
            background: rgba(56, 189, 248, 0.05);
            border-left: 4px solid #38bdf8;
            padding: 25px;
            max-width: 800px;
            border-radius: 4px;
            font-family: sans-serif;
        }
        .escalation-brief h3 { color: #38bdf8; margin-top: 0; font-size: 1.2rem; text-transform: uppercase; letter-spacing: 1px; }
        .escalation-brief p { font-size: 1rem; line-height: 1.6; color: #cbd5e1; margin: 0; }
        .escalation-brief b { color: #fff; }

 /* MODAL / SLIDESHOW OVERLAY */
        .modal-overlay {
            display: none; position: fixed; z-index: 9999; left: 0; top: 0;
            width: 100%; height: 100%; background: rgba(0,0,0,0.92);
            align-items: center; justify-content: center;
        }
.modal-content { position: relative; width: 90%; max-width: 1000px; display: flex; flex-direction: column; align-items: center; }
        .modal-img { max-width: 100%; max-height: 65vh; border: 2px solid #38bdf8; border-radius: 8px; }
        .nav-btn { cursor: pointer; position: absolute; top: 40%; color: #38bdf8; font-size: 60px; transition: 0.3s; user-select: none; text-decoration: none; }
        .btn-prev { left: -100px; } .btn-next { right: -100px; }
        .details-panel { background: #1e293b; padding: 25px; margin-top: 20px; border-radius: 8px; width: 100%; border-left: 5px solid #38bdf8; font-family: sans-serif; }
        .close-btn { position: absolute; top: -70px; right: 0; color: white; font-size: 50px; cursor: pointer; }

        #data-store { display: none; }

 @media (max-width: 1100px) {
            .hero-container { flex-direction: column-reverse; text-align: center; }
            .investigation-section { text-align: center; }
            .report-summary { text-align: left; overflow-x: auto; }
            .trigger-box { margin: 0 auto 40px auto; }
            .escalation-brief { margin: 0 auto; text-align: left; }
            .btn-prev { left: 10px; background: rgba(0,0,0,0.5); } 
            .btn-next { right: 10px; background: rgba(0,0,0,0.5); }
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
                    <strong>Contact:</strong> +91 6379944366<br>
                    <strong>Email:</strong> arivazhagans1411@gmail.com<br>
                    <strong>LinkedIn:</strong> <a href="https://www.linkedin.com/in/arivazhagan11/" target="_blank" style="color:#38bdf8; text-decoration:none;">Profile Page</a>
                </div>
            </div>
            <img src="Screenshot_20260103_200618_Gallery.jpg" class="pfp" alt="Arivazhagan">
        </div>
    </div>

<div class="investigation-section">
        
<div class="mission-summary">
            DETECTED AND CONTAINED A HIGH-SEVERITY SSH BRUTE FORCE ATTACK ORIGINATING FROM A KNOWN MALICIOUS BOTNET. UTILIZED WAZUH SIEM FOR DETECTION, OSINT FOR THREAT INTELLIGENCE, AND IPTABLES FOR IMMEDIATE FIREWALL CONTAINMENT.
        </div>

 
<div class="trigger-box" onclick="launchGallery(0)">
            <img src="01.png" alt="SOC Investigation">
            <div class="trigger-footer">OPEN 13-STEP EVIDENCE SLIDESHOW ➔</div>
        </div>

<div class="escalation-brief">
            <h3>Tier 2 Escalation Rationale</h3>
            <p>
                <b>TECHNICAL JUSTIFICATION:</b> While L1 containment (IPTables DROP) successfully mitigated the immediate threat to Agent 004, this incident requires L2 escalation due to the <b>100% abuse confidence score</b> of Source IP 141.98.81.37. Escalation is necessary to perform a <b>cross-network correlation</b> to ensure this botnet has not attempted lateral movement across other internal assets. Additionally, L2 review is requested for permanent IP blacklisting at the edge firewall/perimeter level.
            </p>
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
            <p id="viewerCap" style="margin:0; font-size: 1.1rem; line-height:1.5;"></p>
        </div>
    </div>
</div>

<div id="data-store">
    <div data-img="01.png" data-text="<b>Step 1: Baseline Dashboard</b> - Monitoring initial SIEM state."></div>
    <div data-img="02.png" data-text="<b>Step 2: Metric Monitoring</b> - Establishing normal traffic flow."></div>
    <div data-img="03.png" data-text="<b>Step 3: Initial Log State</b> - Recording baseline auth failures."></div>
    <div data-img="04.png" data-text="<b>Step 4: Active Attack</b> - Attacker terminal during the brute force attempt."></div>
    <div data-img="05.png" data-text="<b>Step 5: Alert Spike</b> - Wazuh triggering Level 12 critical alerts."></div>
    <div data-img="06.png" data-text="<b>Step 6: Rule 5712 Filter</b> - Isolating specific Brute Force signatures."></div>
    <div data-img="07.png" data-text="<b>Step 7: Timeline Correlation</b> - Analyzing auth log sequences."></div>
    <div data-img="08.png" data-text="<b>Step 8: Deep Dive</b> - Verifying the scope of the SSH attack."></div>
    <div data-img="09.png" data-text="<b>Step 9: IP Extraction</b> - Identifying malicious source 141.98.81.37."></div>
    <div data-img="10.png" data-text="<b>Step 10: OSINT Pivot</b> - 100% Abuse score confirmed on AbuseIPDB."></div>
    <div data-img="11.png" data-text="<b>Step 11: MITRE Mapping</b> - Mapping to Technique T1110 (Brute Force)."></div>
    <div data-img="12.png" data-text="<b>Step 12: Terminal Response</b> - Locating IP for immediate containment."></div>
    <div data-img="13.png" data-text="<b>Step 13: Final Remediation</b> - Applying IPTables DROP policy to block actor."></div>
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
