---
layout: null
---
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Arivazhagan | SOC Portfolio</title>
    <style>
        /* BASE THEME */
        * { box-sizing: border-box; }
        html, body { margin: 0; padding: 0; width: 100%; background-color: #0a0e14; color: white; font-family: 'Segoe UI', Arial, sans-serif; overflow-x: hidden; }
        
/* THE BLUR EFFECT: Blurs the main page when the modal is active */
        .page-wrap.is-blurred { 
            filter: blur(20px); 
            pointer-events: none; 
            transition: filter 0.4s ease; 
        }

 /* HERO SECTION */
        .hero {
            width: 100%; min-height: 70vh;
            background: linear-gradient(rgba(0,0,0,0.7), rgba(0,0,0,0.7)), url('cc.jpg');
            background-size: cover; background-position: center; display: flex; align-items: center; justify-content: center;
        }
        .hero-container { width: 85%; max-width: 1100px; display: flex; justify-content: space-between; align-items: center; }
        .text-side h1 { font-size: 4.5rem; margin: 0; font-weight: 900; letter-spacing: -2px; }
        .text-side .role { font-size: 2rem; color: #38bdf8; display: block; margin: 10px 0 25px 0; }
        .pfp { width: 280px; height: 280px; border-radius: 50%; border: 4px solid #38bdf8; object-fit: cover; box-shadow: 0 0 40px rgba(56, 189, 248, 0.3); }

 /* CENTERED RECTANGLE TRIGGER (400px) */
        .evidence-section { background: #0f172a; padding: 80px 0; text-align: center; }
        
 .trigger-box {
            max-width: 400px; /* Reduced Size */
            width: 90%;
            margin: 0 auto; 
            cursor: pointer; 
            border-radius: 12px; 
            border: 2px solid #334155; 
            overflow: hidden;
            transition: 0.3s ease;
            box-shadow: 0 15px 35px rgba(0,0,0,0.6);
        }
        .trigger-box:hover { border-color: #38bdf8; transform: translateY(-8px); }
        .trigger-box img { width: 100%; display: block; height: auto; }
        .trigger-footer { padding: 18px; background: #1e293b; color: #38bdf8; font-weight: bold; font-size: 0.85rem; letter-spacing: 1px; }

 /* MODAL OVERLAY */
        .modal-overlay {
            display: none; position: fixed; z-index: 9999; left: 0; top: 0;
            width: 100%; height: 100%; background: rgba(0,0,0,0.9);
            align-items: center; justify-content: center;
        }
        .modal-content { position: relative; width: 90%; max-width: 1000px; display: flex; flex-direction: column; align-items: center; }
        .modal-img { max-width: 100%; max-height: 65vh; border: 2px solid #38bdf8; border-radius: 8px; }
        
/* NAVIGATION */
        .nav-btn {
            cursor: pointer; position: absolute; top: 40%; padding: 25px;
            color: #38bdf8; font-size: 65px; font-weight: bold; transition: 0.3s;
            user-select: none; text-decoration: none;
        }
        .btn-prev { left: -120px; } .btn-next { right: -120px; }
        .nav-btn:hover { color: white; transform: scale(1.1); }

/* CAPTION PANEL */
        .details-panel {
            background: #1e293b; color: #f1f5f9; padding: 25px; margin-top: 25px;
            border-radius: 12px; border-left: 6px solid #38bdf8; width: 100%; text-align: left;
        }
        .close-btn { position: absolute; top: -70px; right: 0; color: white; font-size: 50px; cursor: pointer; }

#data-store { display: none; }

  @media (max-width: 1200px) {
            .btn-prev { left: 0; background: rgba(0,0,0,0.5); }
            .btn-next { right: 0; background: rgba(0,0,0,0.5); }
            .hero-container { flex-direction: column-reverse; text-align: center; }
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
                <div style="font-size:1.1rem; opacity: 0.9;">
                    <span><strong>Contact:</strong> +91 6379944366</span> | 
                    <span><strong>LinkedIn:</strong> <a href="#" style="color:#38bdf8; text-decoration:none;">Profile</a></span>
                </div>
            </div>
            <img src="Screenshot_20260103_200618_Gallery.jpg" class="pfp" alt="Arivazhagan">
        </div>
    </div>

<div class="evidence-section">
        <h2 style="text-transform:uppercase; letter-spacing:3px; margin-bottom:45px;">Incident Investigation Analysis</h2>
        
<div class="trigger-box" onclick="launchGallery(0)">
            <img src="01.png" alt="Investigation Snapshot">
            <div class="trigger-footer">OPEN 13-STEP EVIDENCE SLIDESHOW &#10148;</div>
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
            <h4 style="margin:0 0 10px 0; color:#38bdf8; text-transform:uppercase; font-size: 0.8rem;">Investigation Evidence Summary</h4>
            <p id="viewerCap" style="margin:0; font-size:1.1rem; line-height:1.6;"></p>
        </div>
    </div>
</div>

<div id="data-store">
    <div data-img="01.png" data-text="<b>Step 1: Dashboard Overview</b> - Initial view showing 173 events and 16 critical alerts."></div>
    <div data-img="02.png" data-text="<b>Step 2: Metric Analysis</b> - Monitoring baseline patterns before the attack."></div>
    <div data-img="03.png" data-text="<b>Step 3: Baseline Logs</b> - Log state identifying 8 failures and 1 success."></div>
    <div data-img="04.png" data-text="<b>Step 4: Active Attack</b> - Capture from the attacker terminal during brute force execution."></div>
    <div data-img="05.png" data-text="<b>Step 5: Impact Dashboard</b> - Spike to 1379 events and 129 critical alerts post-attack."></div>
    <div data-img="06.png" data-text="<b>Step 6: Rule 5712</b> - Isolating SSH brute force signatures via specific SIEM rules."></div>
    <div data-img="07.png" data-text="<b>Step 7: Rule 5710</b> - Filtering authentication logs to correlate the attack timeline."></div>
    <div data-img="08.png" data-text="<b>Step 8: Deep Correlation</b> - Final filtering to confirm the full scope of the incident."></div>
    <div data-img="09.png" data-text="<b>Step 9: IP Extraction</b> - Extracting Source IP from logs to check login attempts."></div>
    <div data-img="10.png" data-text="<b>Step 10: OSINT Verification</b> - IP confirmed malicious on AbuseIPDB; True Positive botnet."></div>
    <div data-img="11.png" data-text="<b>Step 11: MITRE Mapping</b> - Linking Rule 5712 to Technique T1110 (Brute Force)."></div>
    <div data-img="12.png" data-text="<b>Step 12: Containment</b> - Identifying malicious IP in terminal for immediate response."></div>
    <div data-img="13.png" data-text="<b>Step 13: Remediation</b> - Applying IPTables block to drop all traffic from the malicious source."></div>
</div>

<script>
    let activeStep = 0;
    const slides = document.querySelectorAll('#data-store div');
    const modal = document.getElementById('modalBox');
    const bgWrap = document.getElementById('main-site');

    function launchGallery(n) {
        activeStep = n;
        modal.style.display = "flex";
        bgWrap.classList.add('is-blurred'); // Activates blur
        render();
    }

    function exitGallery() {
        modal.style.display = "none";
        bgWrap.classList.remove('is-blurred'); // Removes blur
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
