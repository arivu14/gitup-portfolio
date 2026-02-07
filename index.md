---
layout: null
---
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Arivazhagan | SOC Portfolio</title>
    <style>
        /* BASE STYLES */
        * { box-sizing: border-box; }
        html, body { margin: 0; padding: 0; width: 100%; background-color: #0a0e14; color: white; font-family: 'Segoe UI', Arial, sans-serif; }
        
/* Blur Effect for background */
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

 /* MEDIUM RECTANGLE TRIGGER */
        .reports-container { background: #0f172a; padding: 60px 0; text-align: center; }
        
 .trigger-box {
            max-width: 500px; /* Medium Rectangle Width */
            margin: 0 auto; 
            cursor: pointer; 
            position: relative;
            border-radius: 10px; 
            border: 2px solid #1e293b; 
            overflow: hidden;
            transition: 0.3s ease;
        }
        .trigger-box:hover { border-color: #38bdf8; transform: translateY(-5px); box-shadow: 0 10px 30px rgba(56, 189, 248, 0.2); }
        .trigger-box img { width: 100%; height: auto; display: block; }

 /* "Click to View" Hint */
        .trigger-hint { padding: 15px; background: #1e293b; color: #38bdf8; font-weight: bold; font-size: 0.9rem; }

/* MODAL SLIDESHOW */
        .modal {
            display: none; position: fixed; z-index: 9999; left: 0; top: 0;
            width: 100%; height: 100%; background: rgba(0,0,0,0.9);
            align-items: center; justify-content: center;
        }
        .modal-wrapper { position: relative; width: 90%; max-width: 1000px; display: flex; flex-direction: column; align-items: center; }
        .modal-img { max-width: 100%; max-height: 65vh; border: 2px solid #38bdf8; border-radius: 5px; }
        
.prev, .next {
            cursor: pointer; position: absolute; top: 40%; padding: 15px;
            color: #38bdf8; font-weight: bold; font-size: 50px; transition: 0.3s;
            user-select: none;
        }
        .next { right: -90px; } .prev { left: -90px; }
        .prev:hover, .next:hover { color: white; }

.details-box {
            background: #1e293b; color: #cbd5e1; padding: 20px; margin-top: 15px;
            border-radius: 8px; border-left: 5px solid #38bdf8; width: 100%; text-align: left;
        }
        .close-x { position: absolute; top: -50px; right: 0; color: white; font-size: 40px; cursor: pointer; }

/* Hidden Pool */
        #data-pool { display: none; }

 @media (max-width: 1100px) { .next { right: 0; } .prev { left: 0; } .trigger-box { width: 90%; } }
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
        <h2 style="margin-bottom:30px; text-transform:uppercase;">Incident Analysis</h2>
        
 <div class="trigger-box" onclick="openGallery(0)">
            <img src="s1.png" alt="First Screenshot">
            <div class="trigger-hint">VIEW FULL 13-STEP INVESTIGATION &#10148;</div>
        </div>
    </div>
</div>

<div id="data-pool">
    <div data-src="01.png" data-cap="<b>Dashboard Overview:</b> Baseline monitoring showing 173 total events with 16 Level 12+ critical alerts."></div>
    <div data-src="02.png" data-cap="<b>Baseline Metrics:</b> Monitoring standard event flow and authentication patterns."></div>
    <div data-src="03.png" data-cap="<b>Auth Logs:</b> Initial security state showing 8 authentication failures and 1 success."></div>
    <div data-src="04.png" data-cap="<b>Live Attack:</b> Execution of the brute force attempt captured from the attacker's terminal."></div>
    <div data-src="05.png" data-cap="<b>Impact Dashboard:</b> Spikes to 1379 events, 129 Level 12 alerts, and 85 failures post-attack."></div>
    <div data-src="06.png" data-cap="<b>SIEM Investigation:</b> Isolating Rule ID 5712 for SSH Brute Force signature analysis."></div>
    <div data-src="07.png" data-cap="<b>Filtering:</b> Tracking Rule ID 5710 to monitor specific authentication attempts."></div>
    <div data-src="08.png" data-cap="<b>Correlating Logs:</b> Confirming the scope and duration of the brute force attempt."></div>
    <div data-src="09.png" data-cap="<b>Source Extraction:</b> Deep dive into event 5710 to extract the Source IP and verify success status."></div>
    <div data-src="10.png" data-cap="<b>OSINT Verification:</b> Validating the Source IP on AbuseIPDB; confirmed True Positive botnet."></div>
    <div data-src="11.png" data-cap="<b>MITRE Mapping:</b> Aligning Rule 5712 with Technique T1110 (Brute Force) & Tactic: Credential Access."></div>
    <div data-src="12.png" data-cap="<b>Threat Isolation:</b> Identifying the malicious IP via Linux CLI for emergency containment."></div>
    <div data-src="13.png" data-cap="<b>Remediation:</b> Final implementation of IPTables block to DROP all traffic from the malicious source."></div>
</div>

<div id="galleryModal" class="modal">
    <div class="modal-wrapper">
        <span class="close-x" onclick="closeGallery()">&times;</span>
        <a class="prev" onclick="moveSlide(-1)">&#10094;</a>
        <img id="displayImg" class="modal-img">
        <a class="next" onclick="moveSlide(1)">&#10095;</a>
        
<div class="details-box">
            <h3 style="margin:0 0 10px 0; color:#38bdf8; font-size:1.1rem;">Technical Evidence</h3>
            <p id="displayCap" style="margin:0;"></p>
        </div>
    </div>
</div>

<script>
    let currentStep = 0;
    const pool = document.querySelectorAll('#data-pool div');
    const modal = document.getElementById('galleryModal');
    const page = document.getElementById('page-content');

    function openGallery(idx) {
        currentStep = idx;
        modal.style.display = "flex";
        page.classList.add('blurred'); // Applies the background blur
        updateDisplay();
    }

    function closeGallery() {
        modal.style.display = "none";
        page.classList.remove('blurred'); // Removes the background blur
    }

    function moveSlide(dir) {
        currentStep += dir;
        if (currentStep >= pool.length) currentStep = 0;
        if (currentStep < 0) currentStep = pool.length - 1;
        updateDisplay();
    }

    function updateDisplay() {
        const item = pool[currentStep];
        document.getElementById('displayImg').src = item.getAttribute('data-src');
        document.getElementById('displayCap').innerHTML = item.getAttribute('data-cap');
    }

    window.onclick = function(e) { if (e.target == modal) closeGallery(); }
</script>

</body>
</html>
