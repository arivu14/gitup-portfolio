---
layout: null
---
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Arivazhagan | SOC Portfolio</title>
    <style>
        /* BASE STYLES */
        * { box-sizing: border-box; }
        html, body { margin: 0; padding: 0; width: 100%; background-color: #0a0e14; color: white; font-family: 'Segoe UI', Arial, sans-serif; }
        
 /* The Blur Effect for the background */
        .main-wrapper.blurred { filter: blur(15px); pointer-events: none; transition: 0.4s ease; }

 .hero-section {
            width: 100%; min-height: 80vh;
            background: linear-gradient(rgba(0,0,0,0.7), rgba(0,0,0,0.7)), url('cc.jpg');
            background-size: cover; background-position: center; display: flex; align-items: center; justify-content: center;
        }
        .container { width: 85%; max-width: 1200px; display: flex; justify-content: space-between; align-items: center; }
        .text-side h1 { font-size: 5rem; margin: 0; font-weight: 900; }
        .text-side .role { font-size: 2rem; color: #38bdf8; display: block; margin-bottom: 20px; }
        .photo-side img { width: 280px; height: 280px; border-radius: 50%; border: 4px solid #38bdf8; object-fit: cover; }

 /* MEDIUM RECTANGLE TRIGGER (The Change You Requested) */
        .reports-container { background: #0f172a; padding: 60px 0; text-align: center; }
        
.trigger-box {
            max-width: 550px; /* Controlled medium size */
            margin: 0 auto; 
            cursor: pointer; 
            position: relative;
            border-radius: 12px; 
            border: 2px solid #334155; 
            overflow: hidden;
            transition: 0.3s ease;
            box-shadow: 0 10px 30px rgba(0,0,0,0.5);
        }
        .trigger-box:hover { border-color: #38bdf8; transform: translateY(-5px); }
        .trigger-box img { width: 100%; height: auto; display: block; }

/* Label under the rectangle */
        .trigger-label { 
            padding: 15px; 
            background: #1e293b; 
            color: #38bdf8; 
            font-weight: bold; 
            text-transform: uppercase;
            letter-spacing: 1px;
            font-size: 0.9rem;
        }

 /* MODAL SLIDESHOW STYLES */
        .modal {
            display: none; position: fixed; z-index: 9999; left: 0; top: 0;
            width: 100%; height: 100%; background: rgba(0,0,0,0.92);
            align-items: center; justify-content: center;
        }
        .modal-wrapper { position: relative; width: 90%; max-width: 1000px; display: flex; flex-direction: column; align-items: center; }
        .modal-img { max-width: 100%; max-height: 65vh; border: 2px solid #38bdf8; border-radius: 8px; }
        
.prev, .next {
            cursor: pointer; position: absolute; top: 40%; padding: 20px;
            color: #38bdf8; font-weight: bold; font-size: 50px; transition: 0.3s;
            user-select: none; text-decoration: none;
        }
        .next { right: -100px; } .prev { left: -100px; }
        .prev:hover, .next:hover { color: white; transform: scale(1.2); }

.details-box {
            background: #1e293b; color: #cbd5e1; padding: 20px; margin-top: 15px;
            border-radius: 8px; border-left: 5px solid #38bdf8; width: 100%; text-align: left;
        }
        .close-x { position: absolute; top: -60px; right: 0; color: white; font-size: 45px; cursor: pointer; }

 /* Hidden Pool for JS to pull from */
        #data-pool { display: none; }

 @media (max-width: 1100px) { 
            .next { right: 10px; background: rgba(0,0,0,0.5); } 
            .prev { left: 10px; background: rgba(0,0,0,0.5); } 
            .trigger-box { width: 90%; }
        }
    </style>
</head>
<body>

<div class="main-wrapper" id="page-content">
    <div class="hero-section">
        <div class="container">
            <div class="text-side">
                <h1>ARIVAZHAGAN</h1>
                <span class="role">SOC Analyst L1</span>
                <div>
                    <span><strong>C.N:</strong> +91 6379944366</span> | 
                    <span><strong>LinkedIn:</strong> <a href="https://linkedin.com/in/arivazhagan" target="_blank" style="color:#38bdf8; text-decoration:none;">Click Here</a></span>
                </div>
            </div>
            <div class="photo-side">
                <img src="Screenshot_20260103_200618_Gallery.jpg" alt="Arivazhagan">
            </div>
        </div>
    </div>

 <div class="reports-container">
    <h2 style="margin-bottom:35px; text-transform:uppercase; letter-spacing:2px;">Incident Investigation Analysis</h2>
        
 <div class="trigger-box" onclick="openGallery(0)">
            <img src="s1.png" alt="Investigation Start">
            <div class="trigger-label">Click to Open 13-Step Analysis Evidence</div>
        </div>
    </div>
</div>

<div id="data-pool">
    <div data-src="01.png" data-cap="<b>Step 1: Dashboard Overview</b> - Baseline monitoring with 173 total events and 16 Level 12+ critical alerts."></div>
    <div data-src="02.png" data-cap="<b>Step 2: Metric Analysis</b> - Observing normal authentication patterns before the attack signature was detected."></div>
    <div data-src="03.png" data-cap="<b>Step 3: Baseline Logs</b> - Analysis of 8 authentication failures and 1 success recorded in baseline logs."></div>
    <div data-src="04.png" data-cap="<b>Step 4: Active Attack</b> - Capture from the attacker terminal during active brute force execution targeting the Ubuntu Agent."></div>
    <div data-src="05.png" data-cap="<b>Step 5: Incident Spike</b> - Dashboard spike showing 1379 events, 129 Level 12 alerts, and 85 failures post-attack."></div>
    <div data-src="06.png" data-cap="<b>Step 6: SIEM Filtering</b> - Isolating Rule ID 5712 to track specific SSH brute force signatures."></div>
    <div data-src="07.png" data-cap="<b>Step 7: Threat Tracking</b> - Correlating Rule ID 5710 logs to determine the timeline of the attack."></div>
    <div data-src="08.png" data-cap="<b>Step 8: Deep Dive</b> - Final filtering process to confirm the scope of the brute force attempt."></div>
    <div data-src="09.png" data-cap="<b>Step 9: Event Forensics</b> - Extracting Source IP from Rule 5710 to verify successful vs failed attempts."></div>
    <div data-src="10.png" data-cap="<b>Step 10: OSINT Pivot</b> - Verifying Source IP on AbuseIPDB; confirmed True Positive malicious botnet."></div>
    <div data-src="11.png" data-cap="<b>Step 11: MITRE Mapping</b> - Mapping Rule 5712 to Tactic: Credential Access and Technique: T1110 (Brute Force)."></div>
    <div data-src="12.png" data-cap="<b>Step 12: Containment Phase</b> - Identifying the malicious IP in the terminal to prepare for firewall blocking."></div>
    <div data-src="13.png" data-cap="<b>Step 13: Final Remediation</b> - Successful implementation of IPTables block to DROP all traffic from the malicious source."></div>
</div>

<div id="galleryModal" class="modal">
    <div class="modal-wrapper">
        <span class="close-x" onclick="closeGallery()">&times;</span>
        <a class="prev" onclick="moveSlide(-1)">&#10094;</a>
        <img id="displayImg" class="modal-img">
        <a class="next" onclick="moveSlide(1)">&#10095;</a>
        
<div class="details-box">
            <h3 style="margin:0 0 10px 0; color:#38bdf8; font-size:1.1rem;">Technical Evidence Summary</h3>
            <p id="displayCap" style="margin:0;"></p>
        </div>
    </div>
</div>

<script>
    let currentStep = 0;
    const pool = document.querySelectorAll('#data-pool div');
    const modal = document.getElementById('galleryModal');
    const mainWrapper = document.getElementById('page-content');

    function openGallery(index) {
        currentStep = index;
        modal.style.display = "flex";
        mainWrapper.classList.add('blurred');
        updateDisplay();
    }

    function closeGallery() {
        modal.style.display = "none";
        mainWrapper.classList.remove('blurred');
    }

    function moveSlide(direction) {
        currentStep += direction;
        if (currentStep >= pool.length) currentStep = 0;
        if (currentStep < 0) currentStep = pool.length - 1;
        updateDisplay();
    }

    function updateDisplay() {
        const data = pool[currentStep];
        document.getElementById('displayImg').src = data.getAttribute('data-src');
        document.getElementById('displayCap').innerHTML = data.getAttribute('data-cap');
    }

    window.onclick = function(e) { if (e.target == modal) closeGallery(); }
</script>

</body>
</html>
