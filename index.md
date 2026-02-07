---
layout: default
title: Arivazhagan | SOC Analyst L1
---

<style>
/* 1. THEME FOUNDATION (Matching virg736 style) */
body {
    background: #0a0c10 url('Pentester.jpg') no-repeat center center fixed;
    background-size: cover;
    color: #c9d1d9; /* GitHub Dark text color */
    font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Helvetica, Arial, sans-serif;
    margin: 0;
    line-height: 1.6;
}

/* Glassmorphism Overlay */
body::before {
    content: "";
    position: fixed;
    top: 0; left: 0; width: 100%; height: 100%;
    background: rgba(13, 17, 23, 0.85); /* Deep dark overlay */
    z-index: -1;
}

/* 2. CUSTOM HEADER (Name & Role + Photo on Right) */
.header-container {
    max-width: 1000px;
    margin: 60px auto 30px;
    padding: 0 20px;
    display: flex;
    justify-content: space-between;
    align-items: center;
}

.header-content h1 {
    font-size: 2.5rem;
    color: #f0f6fc;
    margin: 0;
    font-weight: 600;
}

.header-content .role {
    font-size: 1.2rem;
    color: #58a6ff; /* GitHub Blue */
    font-weight: 500;
}

.profile-img-container img {
    width: 160px;
    height: 160px;
    border-radius: 12px; /* Soft square like virg736 style */
    border: 2px solid #30363d;
    object-fit: cover;
    box-shadow: 0 8px 24px rgba(0,0,0,0.5);
}

/* 3. SUMMARY & CONTACT BOX */
.summary-section {
    max-width: 1000px;
    margin: 0 auto 40px;
    padding: 30px;
    background: rgba(22, 27, 34, 0.6);
    border: 1px solid #30363d;
    border-radius: 12px;
    backdrop-filter: blur(10px);
}

.contact-bar {
    margin-top: 15px;
    display: flex;
    gap: 15px;
}

.contact-bar a {
    color: #8b949e;
    text-decoration: none;
    font-size: 0.9rem;
    padding: 5px 12px;
    border: 1px solid #30363d;
    border-radius: 6px;
    background: #21262d;
    transition: 0.2s;
}

.contact-bar a:hover {
    background: #30363d;
    color: #58a6ff;
}

/* 4. INCIDENT DETAILS (Cleaned - No Slashes) */
.report-body {
    max-width: 1000px;
    margin: auto;
    padding: 0 20px 60px;
}

.report-body h2 {
    font-size: 1.5rem;
    color: #f0f6fc;
    border-bottom: 1px solid #30363d;
    padding-bottom: 10px;
    margin-top: 40px;
}

/* Quick Summary Box */
.verdict-card {
    background: rgba(88, 166, 255, 0.1);
    border-left: 4px solid #58a6ff;
    padding: 20px;
    border-radius: 0 8px 8px 0;
    margin: 20px 0;
}

/* 5. EVIDENCE GRID (Modern Grid) */
.evidence-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(180px, 1fr));
    gap: 15px;
    margin-top: 20px;
}

.thumb-item {
    width: 100%;
    aspect-ratio: 16/9;
    object-fit: cover;
    border-radius: 6px;
    border: 1px solid #30363d;
    cursor: pointer;
    transition: 0.3s;
}

.thumb-item:hover {
    border-color: #58a6ff;
    transform: scale(1.03);
}

/* 6. LIGHTBOX POPUP */
.lightbox-overlay {
    display: none;
    position: fixed;
    z-index: 10000;
    top: 0; left: 0; width: 100%; height: 100%;
    background: rgba(1, 4, 9, 0.95);
    backdrop-filter: blur(5px);
}

.lightbox-content {
    position: relative;
    max-width: 900px;
    margin: 5% auto;
    background: #0d1117;
    border: 1px solid #30363d;
    border-radius: 12px;
    overflow: hidden;
}

#activeImg { width: 100%; display: block; background: #000; }
.info-pane { padding: 25px; }
.close-x { position: absolute; top: 15px; right: 20px; color: #8b949e; font-size: 28px; cursor: pointer; }
</style>

<div class="header-container">
    <div class="header-content">
        <h1>ARIVAZHAGAN</h1>
        <div class="role">SOC Analyst L1</div>
        <div class="contact-bar">
            <a href="mailto:your-email@example.com">Email</a>
            <a href="https://linkedin.com/in/yourprofile" target="_blank">LinkedIn</a>
        </div>
    </div>
    <div class="profile-img-container">
        <img src="my-photo.jpg" alt="Arivazhagan">
    </div>
</div>

<div class="summary-section">
    <h2>Professional Summary</h2>
    <p>
        I am a Junior SOC Analyst specializing in real-time monitoring, incident triaging, and 
        threat mitigation. My core focus is on securing network endpoints and identifying 
        unauthorized access patterns using SIEM tools like Wazuh and ELK.
    </p>
</div>

<div class="report-body">
    <h2>Incident Analysis: SSH Brute Force Mitigation</h2>
    
<div class="verdict-card">
        <h3 style="margin-top:0; color:#58a6ff;">Attack Verdict</h3>
        <p><strong>Status:</strong> RESOLVED</p>
        <p><strong>Analysis:</strong> Confirmed a high-velocity automated brute force attempt from IP 141.98.81.37. The actor attempted to harvest credentials for 'admin' and 'root' users. I successfully executed an IPTables block and verified system integrity.</p>
    </div>

    <h2>Evidence & Investigation</h2>
<div class="evidence-grid">
        <img class="thumb-item" src="01.png" onclick="openLightbox(0)">
        <img class="thumb-item" src="02.png" onclick="openLightbox(1)">
        <img class="thumb-item" src="03.png" onclick="openLightbox(2)">
        <img class="thumb-item" src="04.png" onclick="openLightbox(3)">
        <img class="thumb-item" src="05.png" onclick="openLightbox(4)">
        <img class="thumb-item" src="06.png" onclick="openLightbox(5)">
        <img class="thumb-item" src="07.png" onclick="openLightbox(6)">
        <img class="thumb-item" src="08.png" onclick="openLightbox(7)">
        <img class="thumb-item" src="09.png" onclick="openLightbox(8)">
        <img class="thumb-item" src="10.png" onclick="openLightbox(9)">
        <img class="thumb-item" src="11.png" onclick="openLightbox(10)">
        <img class="thumb-item" src="12.png" onclick="openLightbox(11)">
        <img class="thumb-item" src="13.png" onclick="openLightbox(12)">
        <img class="thumb-item" src="14.png" onclick="openLightbox(13)">
    </div>
</div>

<div id="lightbox" class="lightbox-overlay">
    <div class="lightbox-content">
        <span class="close-x" onclick="closeLightbox()">&times;</span>
        <img id="activeImg" src="">
        <div class="info-pane">
            <h3 id="detailTitle" style="color:#58a6ff; margin-top:0;"></h3>
            <p id="detailText"></p>
            <div style="background:#161b22; padding:10px; border-radius:6px; border-left:3px solid #f85149; margin-top:15px;">
                <strong style="color:#f85149;">L2 Escalation:</strong>
                <p id="l2Text" style="margin:5px 0 0; font-size:0.9rem; font-style:italic;"></p>
            </div>
        </div>
    </div>
</div>

<script>
let currentIndex = 0;
const reportData = [
    { title: "Baseline Monitoring", text: "Dashboard status before the incident began.", l2: "Baseline established to detect anomalies." },
    { title: "Alert Spike", text: "Wazuh detecting high-frequency Rule 5712 triggers.", l2: "Escalated due to volume exceeding automated thresholds." },
    { title: "Auth Failures", text: "Log isolation showing focused brute force attempts.", l2: "Moving to L2 for deep packet/log inspection." },
    { title: "Attack Simulation", text: "Validating SIEM rules via manual attack scripts.", l2: "Confirmed rule integrity for automated blocking." },
    { title: "System Recovery", text: "Restoring manager-agent communication after a crash.", l2: "L2 intervention required for system-level repair." },
    { title: "Metric Review", text: "Analysis of 1,379 total security events.", l2: "Quantifying risk for executive reporting." },
    { title: "Probing Detection", text: "Attempts to access non-existent administrative users.", l2: "Confirmed intent: Credential Harvesting." },
    { title: "Source Identification", text: "Pinpointing IP 141.98.81.37 as the primary threat.", l2: "IP isolation for external threat intelligence check." },
    { title: "Incident Escalation", text: "Event promoted to Level 12 Severity.", l2: "Mandatory L2 review for high-severity alerts." },
    { title: "Actor Profiling", text: "Profiling the source IP location and history.", l2: "Attribution phase: identifying actor origin." },
    { title: "OSINT Check", text: "AbuseIPDB confirms 100% malicious reputation score.", l2: "Verified threat via global intelligence databases." },
    { title: "MITRE Mapping", text: "Activity categorized as T1110 (Brute Force).", l2: "Alignment with industry-standard frameworks." },
    { title: "Containment", text: "Blocking the IP via manual IPTables command.", l2: "Active mitigation performed by L2 analyst." },
    { title: "Final Verification", text: "Monitoring logs to ensure no further activity.", l2: "Post-incident audit to confirm security posture." }
];

function openLightbox(index) {
    currentIndex = index;
    document.getElementById("lightbox").style.display = "block";
    updateContent();
}
function closeLightbox() { document.getElementById("lightbox").style.display = "none"; }
function updateContent() {
    let file = (currentIndex + 1 < 10) ? "0" + (currentIndex + 1) : (currentIndex + 1);
    document.getElementById("activeImg").src = file + ".png";
    document.getElementById("detailTitle").innerText = reportData[currentIndex].title;
    document.getElementById("detailText").innerText = reportData[currentIndex].text;
    document.getElementById("l2Text").innerText = reportData[currentIndex].l2;
}
</script>
