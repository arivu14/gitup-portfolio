---
layout: null
---
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Arivazhagan | SOC Analyst</title>
    <style>
        /* BASE STYLES */
        * { box-sizing: border-box; }
        html, body { margin: 0; padding: 0; width: 100%; background-color: #0a0e14; color: white; font-family: 'Segoe UI', Arial, sans-serif; }
        
 /* The Blur Effect */
        .main-wrapper.blurred { filter: blur(20px); pointer-events: none; transition: filter 0.4s ease; }

.hero-section {
            width: 100%; min-height: 100vh;
            background: linear-gradient(rgba(0,0,0,0.7), rgba(0,0,0,0.7)), url('cc.jpg');
            background-size: cover; background-position: center; display: flex; align-items: center; justify-content: center;
        }
        .container { width: 85%; max-width: 1200px; display: flex; justify-content: space-between; align-items: center; }
        .text-side h1 { font-size: 5rem; margin: 0; font-weight: 900; }
        .text-side .role { font-size: 2rem; color: #38bdf8; display: block; margin-bottom: 20px; }
        .photo-side img { width: 300px; height: 300px; border-radius: 50%; border: 4px solid #38bdf8; object-fit: cover; }

 /* CENTERED SINGLE THUMBNAIL SECTION */
        .reports-container { background: #0f172a; padding: 100px 0; text-align: center; }
        
.main-evidence-cover {
            max-width: 600px; margin: 0 auto; cursor: pointer; position: relative;
            transition: 0.4s; border-radius: 15px; border: 3px solid #1e293b; overflow: hidden;
        }
.main-evidence-cover:hover { border-color: #38bdf8; transform: scale(1.02); box-shadow: 0 0 30px rgba(56, 189, 248, 0.3); }
        .main-evidence-cover img { width: 100%; display: block; }
        .hover-overlay {
            position: absolute; top: 0; left: 0; width: 100%; height: 100%;
            background: rgba(56, 189, 248, 0.2); display: flex; align-items: center;
            justify-content: center; opacity: 0; transition: 0.3s;
        }
        .main-evidence-cover:hover .hover-overlay { opacity: 1; }
        .hover-overlay span { background: #38bdf8; color: #0a0e14; padding: 10px 20px; font-weight: bold; border-radius: 5px; }

/* Hidden data pool for the 13 images */
        #image-pool { display: none; }

/* MODAL SLIDESHOW */
        .modal {
            display: none; position: fixed; z-index: 9999; left: 0; top: 0;
            width: 100%; height: 100%; background: rgba(0,0,0,0.85);
            align-items: center; justify-content: center;
        }
        .modal-wrapper { position: relative; width: 90%; max-width: 1100px; display: flex; flex-direction: column; align-items: center; }
        .modal-img { max-width: 100%; max-height: 65vh; border: 3px solid #38bdf8; border-radius: 8px; }
        
.prev, .next {
            cursor: pointer; position: absolute; top: 45%; padding: 20px;
            color: #38bdf8; font-weight: bold; font-size: 60px; transition: 0.3s;
        }
        .next { right: -100px; } .prev { left: -100px; }
        .prev:hover, .next:hover { color: white; }

 .details-box {
            background: #1e293b; color: #cbd5e1; padding: 25px; margin-top: 20px;
            border-radius: 10px; border-left: 6px solid #38bdf8; width: 100%; text-align: left;
        }
        .close-x { position: absolute; top: -60px; right: 0; color: white; font-size: 45px; cursor: pointer; }

        @media (max-width: 1200px) { .next { right: 0; } .prev { left: 0; } }
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
        <h2 style="text-transform:uppercase; letter-spacing:3px; margin-bottom:10px;">Incident Report Analysis</h2>
        <p style="color:#94a3b8; margin-bottom:40px;">Click the report below to view the full 13-step investigation evidence.</p>
        
 <div class="main-evidence-cover" onclick="openGallery(0)">
            <img src="s1.png" alt="Investigation Cover">
            <div class="hover-overlay">
                <span>VIEW FULL ANALYSIS (13 STEPS)</span>
            </div>
        </div>
    </div>
</div>

<div id="image-pool">
    <div data-src="01.png" data-cap="<b>Dashboard Overview:</b> Baseline monitoring with 173 total events and 16 Level 12+ critical alerts."></div>
    <div data-src="02.png" data-cap="<b>Metric Analysis:</b> Identifying normal authentication patterns before the brute force anomaly."></div>
    <div data-src="03.png" data-cap="<b>Access Logs:</b> Initial log state showing 8 authentication failures vs 1 success."></div>
    <div data-src="04.png" data-cap="<b>Live Attack:</b> Captured view from the attacker terminal during active brute force execution."></div>
    <div data-src="05.png" data-cap="<b>Incident Spike:</b> Post-attack dashboard showing 1379 events, 129 Level 12 alerts, and 85 failures."></div>
    <div data-src="06.png" data-cap="<b>SIEM Investigation:</b> Filtering Rule ID 5712 to isolate the SSH Brute Force signature."></div>
    <div data-src="07.png" data-cap="<b>Advanced Filtering:</b> Tracking Rule ID 5710 to map all authentication attempts."></div>
    <div data-src="08.png" data-cap="<b>Log Correlation:</b> Final filtering process to confirm the scope of the SSH attack."></div>
    <div data-src="09.png" data-cap="<b>Source Extraction:</b> Deep dive into event 5710 to extract the Source IP and check login status."></div>
    <div data-src="10.png" data-cap="<b>OSINT Pivot:</b> Verifying malicious IP on AbuseIPDB - Confirmed True Positive botnet activity."></div>
    <div data-src="11.png" data-cap="<b>MITRE Mapping:</b> Aligning Rule ID 5712 with Technique T1110 (Brute Force) & Tactic: Credential Access."></div>
    <div data-src="12.png" data-cap="<b>Containment:</b> Locating and identifying the malicious IP via terminal for emergency response."></div>
    <div data-src="13.png" data-cap="<b>Remediation:</b> Final block execution using IPTables to DROP all traffic from the malicious source."></div>
</div>

<div id="galleryModal" class="modal">
    <div class="modal-wrapper">
        <span class="close-x" onclick="closeGallery()">&times;</span>
        <a class="prev" onclick="moveSlide(-1)">&#10094;</a>
        <img id="displayImg" class="modal-img">
        <a class="next" onclick="moveSlide(1)">&#10095;</a>
        
<div class="details-box">
            <h3 style="margin:0 0 10px 0; color:#38bdf8;">Investigation Detail</h3>
            <p id="displayCap" style="margin:0;"></p>
        </div>
    </div>
</div>

<script>
    let currentStep = 0;
    const pool = document.querySelectorAll('#image-pool div');
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

    // Close on click outside
    window.onclick = function(e) { if (e.target == modal) closeGallery(); }
</script>

</body>
</html>
