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
        html, body { margin: 0; padding: 0; width: 100%; background-color: #0a0e14; color: white; font-family: 'Segoe UI', Arial, sans-serif; overflow-x: hidden; }
        
/* Blur trigger - hides background noise when investigating a report */
        .main-wrapper.blurred { filter: blur(15px); pointer-events: none; transition: filter 0.3s ease; }

 /* HERO SECTION */
        .hero-section {
            width: 100%; min-height: 100vh;
            background: linear-gradient(rgba(0,0,0,0.7), rgba(0,0,0,0.7)), url('cc.jpg');
            background-size: cover; background-position: center; display: flex; align-items: center; justify-content: center;
        }
        .container { width: 85%; max-width: 1200px; display: flex; justify-content: space-between; align-items: center; }
        .text-side h1 { font-size: 5rem; margin: 0; font-weight: 900; letter-spacing: -2px; }
        .text-side .role { font-size: 2rem; color: #38bdf8; display: block; margin: 5px 0 20px 0; }
        .photo-side img { width: 320px; height: 320px; border-radius: 50%; border: 5px solid #38bdf8; object-fit: cover; box-shadow: 0 0 50px rgba(56,189,248,0.4); }

 /* REPORT GRID */
        .reports-container { background: #0f172a; padding: 80px 0; text-align: center; }
        .report-grid {
            display: grid; grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));
            gap: 25px; width: 85%; max-width: 1200px; margin: 0 auto;
        }
        .thumb { 
            width: 100%; height: 180px; object-fit: cover; cursor: pointer; 
            border-radius: 12px; border: 2px solid #1e293b; transition: 0.3s;
        }
        .thumb:hover { border-color: #38bdf8; transform: translateY(-5px); }

 /* SLIDESHOW MODAL */
        .modal {
            display: none; position: fixed; z-index: 9999; left: 0; top: 0;
            width: 100%; height: 100%; background: rgba(0,0,0,0.85);
            align-items: center; justify-content: center; flex-direction: column;
        }
        .modal-content-wrapper { position: relative; width: 85%; max-width: 1100px; display: flex; flex-direction: column; align-items: center; }
        .modal-img { max-width: 100%; max-height: 65vh; border: 3px solid #38bdf8; border-radius: 8px; }
        
 /* Navigation Arrows */
        .prev, .next {
            cursor: pointer; position: absolute; top: 40%; width: auto; padding: 25px;
            color: #38bdf8; font-weight: bold; font-size: 60px; transition: 0.3s;
            user-select: none; text-decoration: none;
        }
        .next { right: -120px; } .prev { left: -120px; }
        .prev:hover, .next:hover { color: white; transform: scale(1.1); }

/* Detail/Summary Box */
        .details-box {
            background: #1e293b; color: #cbd5e1; padding: 25px;
            margin-top: 25px; border-radius: 12px; border-top: 4px solid #38bdf8;
            width: 100%; text-align: left; font-size: 1.1rem; line-height: 1.6;
        }
        .close-btn { position: absolute; top: -70px; right: 0; color: white; font-size: 50px; cursor: pointer; }

@media (max-width: 1200px) {
            .next { right: 0; } .prev { left: 0; }
            .modal-content-wrapper { width: 95%; }
            .text-side h1 { font-size: 3.5rem; }
        }
    </style>
</head>
<body>

<div class="main-wrapper" id="content">
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
        <h1 style="margin-bottom:50px; text-transform:uppercase; letter-spacing:2px;">Incident Report Analysis</h1>
        <div class="report-grid">
            <img class="thumb" src="01.png" onclick="openSlide(1)" alt="<b>Dashboard Overview:</b> Baseline monitoring with 173 total events and 16 Level 12+ critical alerts.">
            <img class="thumb" src="02.png" onclick="openSlide(2)" alt="<b>Metric Analysis:</b> Identifying normal authentication patterns before the brute force anomaly.">
            <img class="thumb" src="03.png" onclick="openSlide(3)" alt="<b>Access Logs:</b> Initial log state showing 8 authentication failures vs 1 success.">
            <img class="thumb" src="04.png" onclick="openSlide(4)" alt="<b>Live Attack:</b> Captured view from the attacker terminal during active brute force execution.">
            <img class="thumb" src="05.png" onclick="openSlide(5)" alt="<b>Incident Spike:</b> Post-attack dashboard showing 1379 events, 129 Level 12 alerts, and 85 failures.">
            <img class="thumb" src="06.png" onclick="openSlide(6)" alt="<b>SIEM Investigation:</b> Filtering Rule ID 5712 to isolate the SSH Brute Force signature.">
            <img class="thumb" src="07.png" onclick="openSlide(7)" alt="<b>Advanced Filtering:</b> Tracking Rule ID 5710 to map all authentication attempts.">
            <img class="thumb" src="08.png" onclick="openSlide(8)" alt="<b>Log Correlation:</b> Final filtering process to confirm the scope of the SSH attack.">
            <img class="thumb" src="09.png" onclick="openSlide(9)" alt="<b>Source Extraction:</b> Deep dive into event 5710 to extract the Source IP and check login status.">
            <img class="thumb" src="10.png" onclick="openSlide(10)" alt="<b>OSINT Pivot:</b> Verifying malicious IP on AbuseIPDB - Confirmed True Positive botnet activity.">
            <img class="thumb" src="11.png" onclick="openSlide(11)" alt="<b>MITRE Mapping:</b> Aligning Rule ID 5712 with Technique T1110 (Brute Force) & Tactic: Credential Access.">
            <img class="thumb" src="12.png" onclick="openSlide(12)" alt="<b>Containment:</b> Locating and identifying the malicious IP via terminal for emergency response.">
            <img class="thumb" src="13.png" onclick="openSlide(13)" alt="<b>Remediation:</b> Final block execution using IPTables to DROP all traffic from the malicious source.">
        </div>
    </div>
</div>

<div id="slideModal" class="modal">
    <div class="modal-content-wrapper">
        <span class="close-btn" onclick="closeSlide()">&times;</span>
        <a class="prev" onclick="changeSlide(-1)">&#10094;</a>
        <img class="modal-img" id="modalImg">
        <a class="next" onclick="changeSlide(1)">&#10095;</a>
        <div class="details-box">
            <h3 style="margin-top:0; color:#38bdf8;">Technical Investigation Detail</h3>
            <p id="modalCaption"></p>
        </div>
    </div>
</div>

<script>
    let currentIdx = 0;
    const thumbs = document.getElementsByClassName("thumb");
    const modal = document.getElementById("slideModal");
    const content = document.getElementById("content");

    function openSlide(n) {
        currentIdx = n - 1;
        modal.style.display = "flex";
        content.classList.add("blurred");
        updateModal();
    }

    function closeSlide() {
        modal.style.display = "none";
        content.classList.remove("blurred");
    }

    function changeSlide(n) {
        currentIdx += n;
        if (currentIdx >= thumbs.length) { currentIdx = 0; }
        if (currentIdx < 0) { currentIdx = thumbs.length - 1; }
        updateModal();
    }

    function updateModal() {
        document.getElementById("modalImg").src = thumbs[currentIdx].src;
        document.getElementById("modalCaption").innerHTML = thumbs[currentIdx].alt;
    }

    window.onclick = function(event) { if (event.target == modal) { closeSlide(); } }
</script>

</body>
</html>
