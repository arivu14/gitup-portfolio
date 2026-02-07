---
layout: null
---
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Arivazhagan | SOC Analyst Portfolio</title>
    <style>
        /* BASE STYLES */
        * { box-sizing: border-box; }
        html, body { margin: 0; padding: 0; width: 100%; background-color: #0a0e14; color: white; font-family: 'Segoe UI', Arial, sans-serif; overflow-x: hidden; }
        
 /* Blur effect for modal */
        .blur-target { transition: filter 0.3s ease; }
        .modal-active .blur-target { filter: blur(12px); pointer-events: none; }

 /* HERO SECTION */
        .hero-section {
            width: 100%; min-height: 100vh;
            background: linear-gradient(rgba(0,0,0,0.7), rgba(0,0,0,0.7)), url('cc.jpg');
            background-size: cover; background-position: center; display: flex; align-items: center; justify-content: center;
        }
        .container { width: 85%; max-width: 1200px; display: flex; justify-content: space-between; align-items: center; }
        .text-side h1 { font-size: 5rem; margin: 0; font-weight: 900; }
        .text-side .role { font-size: 2rem; color: #38bdf8; display: block; margin-bottom: 20px; }
        .photo-side img { width: 300px; height: 300px; border-radius: 50%; border: 4px solid #38bdf8; object-fit: cover; }

 /* GALLERY GRID */
        .reports-container { background: #0f172a; padding: 80px 0; text-align: center; }
        .report-grid {
            display: grid; grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));
            gap: 25px; width: 85%; max-width: 1200px; margin: 0 auto;
        }
        .thumb-wrapper { position: relative; overflow: hidden; border-radius: 8px; border: 2px solid #1e293b; transition: 0.3s; }
        .thumb-wrapper:hover { border-color: #38bdf8; transform: translateY(-5px); }
        .thumb { width: 100%; height: 200px; object-fit: cover; cursor: pointer; }
        .thumb-label { padding: 10px; background: #1e293b; font-size: 0.9rem; color: #38bdf8; font-weight: bold; }

 /* MODAL / LIGHTBOX */
        .modal {
            display: none; position: fixed; z-index: 9999; left: 0; top: 0;
            width: 100%; height: 100%; background: rgba(0,0,0,0.85);
            align-items: center; justify-content: center; flex-direction: column;
        }
        .modal-content { position: relative; width: 80%; max-height: 80vh; display: flex; justify-content: center; }
        .modal-content img { max-width: 100%; max-height: 70vh; border: 2px solid #38bdf8; border-radius: 5px; box-shadow: 0 0 30px rgba(56, 189, 248, 0.3); }
        
.caption-box { width: 80%; background: rgba(15, 23, 42, 0.9); padding: 20px; border-radius: 8px; margin-top: 20px; border-top: 3px solid #38bdf8; text-align: center; }
        .caption-box p { margin: 0; font-size: 1.1rem; line-height: 1.6; color: #f1f5f9; }

 /* SLIDER BUTTONS */
        .prev, .next {
            cursor: pointer; position: absolute; top: 50%; width: auto; padding: 20px;
            color: #38bdf8; font-weight: bold; font-size: 50px; transition: 0.3s;
            user-select: none; text-decoration: none;
        }
 .next { right: -80px; } .prev { left: -80px; }
        .prev:hover, .next:hover { color: white; }
        .close { position: absolute; top: 30px; right: 40px; color: white; font-size: 40px; cursor: pointer; }

@media (max-width: 1000px) {
            .next { right: 10px; } .prev { left: 10px; }
            .container { flex-direction: column-reverse; text-align: center; }
            .modal-content { width: 95%; }
        }
    </style>
</head>
<body id="body-tag">

<div class="blur-target">
    <div class="hero-section">
        <div class="container">
            <div class="text-side">
                <h1>ARIVAZHAGAN</h1>
                <span class="role">SOC Analyst L1</span>
                <div style="font-size:1.2rem;">
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
        <h1 style="margin-bottom:50px; text-transform:uppercase; letter-spacing:2px;">Incident Analysis Workflow</h1>
        <div class="report-grid">
<div class="thumb-wrapper"><img class="thumb" src="01.png" onclick="openModal();currentSlide(1)" alt="Baseline Security Posture: Initial Wazuh Dashboard showing 173 total events with 16 Level 12+ alerts and 8 authentication failures."><div class="thumb-label">Baseline Dashboard</div></div>
            <div class="thumb-wrapper"><img class="thumb" src="02.png" onclick="openModal();currentSlide(2)" alt="Pre-Attack Metrics: Monitoring standard event flow and baseline authentication success/failure ratios."><div class="thumb-label">Metric Overview</div></div>
            <div class="thumb-wrapper"><img class="thumb" src="03.png" onclick="openModal();currentSlide(3)" alt="Pre-Attack State: Detailed view of the single successful login vs failure alerts before the brute force attempt."><div class="thumb-label">Security State</div></div>
            
<div class="thumb-wrapper"><img class="thumb" src="04.png" onclick="openModal();currentSlide(4)" alt="Threat Actor Perspective: Active brute force attack initiated from the attacker's terminal targeting the Ubuntu agent."><div class="thumb-label">Attacker Activity</div></div>
            
 <div class="thumb-wrapper"><img class="thumb" src="05.png" onclick="openModal();currentSlide(5)" alt="Incident Impact: Wazuh Dashboard spike to 1379 total events, 129 Level 12 alerts, and 85 failures following the attack."><div class="thumb-label">Post-Attack Spike</div></div>
            
 <div class="thumb-wrapper"><img class="thumb" src="06.png" onclick="openModal();currentSlide(6)" alt="Log Analysis: Filtering for Rule ID 5712 to isolate and identify the SSH Brute Force signature."><div class="thumb-label">Rule 5712 Filter</div></div>
<div class="thumb-wrapper"><img class="thumb" src="07.png" onclick="openModal();currentSlide(7)" alt="Investigation: Filtering for Rule ID 5710 to monitor specific authentication attempts across the network."><div class="thumb-label">Rule 5710 Tracking</div></div>
<div class="thumb-wrapper"><img class="thumb" src="08.png" onclick="openModal();currentSlide(8)" alt="Advanced Filtering: Correlating SSH attack patterns to confirm the scope of the brute force attempt."><div class="thumb-label">Pattern Correlation</div></div>
            
<div class="thumb-wrapper"><img class="thumb" src="09.png" onclick="openModal();currentSlide(9)" alt="Event Forensics: Deep dive into Rule 5710 details to extract the source IP and verify login success/failure status."><div class="thumb-label">Source IP Extraction</div></div>
            
<div class="thumb-wrapper"><img class="thumb" src="10.png" onclick="openModal();currentSlide(10)" alt="OSINT Verification: Cross-referencing source IP with AbuseIPDB, confirming a True Positive malicious botnet."><div class="thumb-label">OSINT Verification</div></div>
            
<div class="thumb-wrapper"><img class="thumb" src="11.png" onclick="openModal();currentSlide(11)" alt="MITRE Mapping: Aligning Rule 5712 with Technique T1110 (Brute Force) and Tactics for Credential Access."><div class="thumb-label">MITRE ATT&CK Mapping</div></div>
            
<div class="thumb-wrapper"><img class="thumb" src="12.png" onclick="openModal();currentSlide(12)" alt="Containment: Identifying and isolating the malicious IP via Linux CLI for immediate firewall response."><div class="thumb-label">Threat Isolation</div></div>
            <div class="thumb-wrapper"><img class="thumb" src="s13.png" onclick="openModal();currentSlide(13)" alt="Remediation: Successful implementation of IPTables block to drop all traffic from the verified malicious source."><div class="thumb-label">Final Remediation</div></div>
        </div>
    </div>
</div>

<div id="myModal" class="modal">
    <span class="close" onclick="closeModal()">&times;</span>
    <div class="modal-content">
        <a class="prev" onclick="plusSlides(-1)">&#10094;</a>
        <img id="modal-img">
        <a class="next" onclick="plusSlides(1)">&#10095;</a>
    </div>
    <div class="caption-box"><p id="caption-text"></p></div>
</div>

<script>
    let slideIndex = 1;
    const thumbs = document.getElementsByClassName("thumb");

    function openModal() {
        document.getElementById("myModal").style.display = "flex";
        document.getElementById("body-tag").classList.add("modal-active");
    }

    function closeModal() {
        document.getElementById("myModal").style.display = "none";
        document.getElementById("body-tag").classList.remove("modal-active");
    }

    function currentSlide(n) { showSlides(slideIndex = n); }
    function plusSlides(n) { showSlides(slideIndex += n); }

    function showSlides(n) {
        if (n > thumbs.length) {slideIndex = 1}
        if (n < 1) {slideIndex = thumbs.length}
        document.getElementById("modal-img").src = thumbs[slideIndex-1].src;
        document.getElementById("caption-text").innerHTML = thumbs[slideIndex-1].alt;
    }

    // Close on background click
    window.onclick = function(event) {
        if (event.target == document.getElementById("myModal")) { closeModal(); }
    }
</script>

</body>
</html>
