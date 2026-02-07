---
layout: default
title: Arivazhagan | SOC Analyst Portfolio
---

<style>
/* 1. GLOBAL PROFESSIONAL STYLING */
body {
    background: #0a0e14 url('Pentester.jpg') no-repeat center center fixed;
    background-size: cover;
    color: #e0e0e0;
    /* Clean, non-messy professional font */
    font-family: 'Inter', 'Segoe UI', Roboto, Helvetica, Arial, sans-serif;
    margin: 0;
    line-height: 1.6;
}

body::before {
    content: "";
    position: fixed;
    top: 0; left: 0; width: 100%; height: 100%;
    background: rgba(10, 14, 20, 0.88); 
    z-index: -1;
}

/* 2. NEW BIO HEADER (Replaces old SOC Lab Portfolio text) */
.hero-container {
    max-width: 1200px;
    margin: 40px auto;
    padding: 40px;
    background: rgba(15, 23, 42, 0.4);
    border: 1px solid rgba(56, 189, 248, 0.2);
    border-radius: 20px;
    display: flex;
    justify-content: space-between;
    align-items: center;
    backdrop-filter: blur(10px);
}

.bio-text { flex: 2; }

.bio-text h1 {
    font-size: 3rem;
    margin: 0;
    color: #fff;
    letter-spacing: -1px;
}

.bio-text .role {
    font-size: 1.2rem;
    color: #38bdf8;
    font-weight: 600;
    margin-bottom: 20px;
    display: block;
}

.bio-summary {
    font-size: 1.1rem;
    color: #94a3b8;
    max-width: 600px;
    margin-bottom: 25px;
}

/* Contact & LinkedIn Styling */
.contact-links {
    display: flex;
    gap: 20px;
    font-size: 0.9rem;
}

.contact-links a {
    color: #fff;
    text-decoration: none;
    background: rgba(56, 189, 248, 0.1);
    padding: 8px 16px;
    border-radius: 6px;
    border: 1px solid rgba(56, 189, 248, 0.3);
    transition: 0.3s;
}

.contact-links a:hover {
    background: #38bdf8;
    color: #0a0e14;
}

/* PROFILE PHOTO ON THE RIGHT */
.profile-photo-right {
    flex: 1;
    display: flex;
    justify-content: flex-end;
}

.profile-photo-right img {
    width: 200px;
    height: 200px;
    border-radius: 20%; /* Modern soft-square look */
    border: 2px solid #38bdf8;
    object-fit: cover;
    box-shadow: 0 0 30px rgba(56, 189, 248, 0.2);
}

/* 3. INCIDENT REPORT AREA (Cleaned) */
.report-section {
    max-width: 1200px;
    margin: auto;
    padding: 20px;
}

.section-title {
    font-size: 1.8rem;
    color: #fff;
    margin-bottom: 20px;
    border-bottom: 2px solid #38bdf8;
    display: inline-block;
    padding-bottom: 5px;
}

.verdict-box {
    background: rgba(30, 41, 59, 0.5);
    padding: 25px;
    border-radius: 12px;
    margin-bottom: 40px;
}

/* Remove slashes from headlines */
h3 { color: #38bdf8; margin-top: 0; }

/* 4. GALLERY STRIP */
.evidence-strip {
    display: flex;
    overflow-x: auto;
    gap: 15px;
    padding: 10px 0;
}

.thumb {
    height: 120px;
    border-radius: 8px;
    cursor: pointer;
    opacity: 0.7;
    transition: 0.3s;
}

.thumb:hover { opacity: 1; transform: scale(1.05); }

/* LIGHTBOX (Pop-up) Styles remain similar but cleaned */
.lightbox-overlay {
    display: none;
    position: fixed;
    z-index: 9999;
    left: 0; top: 0; width: 100%; height: 100%;
    background: rgba(2, 6, 23, 0.98);
    backdrop-filter: blur(10px);
}
.lightbox-container {
    position: relative;
    margin: 5% auto;
    width: 80%;
    background: #0f172a;
    border-radius: 15px;
    overflow: hidden;
}
#activeImg { width: 100%; max-height: 50vh; object-fit: contain; background: #000; }
.details-content { padding: 30px; }
.close-btn { position: absolute; top: 20px; right: 30px; color: #fff; font-size: 30px; cursor: pointer; }
</style>

<header class="hero-container">
    <div class="bio-text">
        <h1>ARIVAZHAGAN</h1>
        <span class="role">SOC Analyst L1</span>
        <p class="bio-summary">
            Dedicated Security Operations Center Analyst focused on threat detection, 
            incident response, and SIEM optimization. I specialize in identifying 
            malicious patterns and defending infrastructure from automated brute-force 
            and credential-harvesting attacks.
        </p>
        <div class="contact-links">
            <a href="mailto:your.email@example.com">Email Me</a>
            <a href="https://linkedin.com/in/yourprofile" target="_blank">LinkedIn Profile</a>
        </div>
    </div>
    <div class="profile-photo-right">
        <img src="my-photo.jpg" alt="Arivazhagan">
    </div>
</header>

<div class="report-section">
    <h2 class="section-title">Incident Analysis: SSH Brute Force</h2>
    
<div class="verdict-box">
        <h3>Final Verdict</h3>
        <p><strong>Status:</strong> Resolved</p>
        <p><strong>Summary:</strong> Identified a persistent brute force attempt from IP 141.98.81.37. Implemented an immediate IP Tables block to mitigate the threat and secured the system configuration.</p>
    </div>

<h3>Evidence Gallery</h3>
<div class="evidence-strip">
        <img class="thumb" src="01.png" onclick="openLightbox(0)">
        <img class="thumb" src="02.png" onclick="openLightbox(1)">
        <img class="thumb" src="03.png" onclick="openLightbox(2)">
        <img class="thumb" src="04.png" onclick="openLightbox(3)">
        <img class="thumb" src="05.png" onclick="openLightbox(4)">
        <img class="thumb" src="06.png" onclick="openLightbox(5)">
        <img class="thumb" src="07.png" onclick="openLightbox(6)">
        <img class="thumb" src="08.png" onclick="openLightbox(7)">
        <img class="thumb" src="09.png" onclick="openLightbox(8)">
        <img class="thumb" src="10.png" onclick="openLightbox(9)">
        <img class="thumb" src="11.png" onclick="openLightbox(10)">
        <img class="thumb" src="12.png" onclick="openLightbox(11)">
        <img class="thumb" src="13.png" onclick="openLightbox(12)">
        <img class="thumb" src="14.png" onclick="openLightbox(13)">
    </div>
</div>

<div id="lightbox" class="lightbox-overlay">
    <span class="close-btn" onclick="closeLightbox()">&times;</span>
    <div class="lightbox-container">
        <img id="activeImg" src="">
        <div class="details-content">
            <h2 id="detailTitle" style="color:#38bdf8;"></h2>
            <p id="detailText" style="color:#94a3b8;"></p>
        </div>
    </div>
</div>

<script>
let currentIndex = 0;
const reportData = [
    { title: "Dashboard Baseline", text: "Establishing standard monitoring before the spike." },
    { title: "Severity Spike", text: "Wazuh alerts showing high-frequency login failures." },
    { title: "Auth Failures", text: "Isolating Rule 5712 (SSHD Brute Force) events." },
    { title: "Attack Simulation", text: "Verifying the detection threshold for automated scripts." },
    { title: "Config Recovery", text: "Manually repairing the OSSEC configuration post-crash." },
    { title: "Metric Aggregation", text: "Quantifying 1,379 total events over a 24-hour window." },
    { title: "User Probing", text: "Detection of attempts on non-existent users (Admin/Guest)." },
    { title: "Log Deep-Dive", text: "Identifying source IP 141.98.81.37 from raw system logs." },
    { title: "Incident Escalation", text: "Elevating the event to a Level 12 Critical Incident." },
    { title: "Actor Identification", text: "Isolating the malicious source for attribution." },
    { title: "OSINT Verification", text: "Confirmed 100% abuse score on AbuseIPDB." },
    { title: "MITRE Mapping", text: "Mapping to T1110 (Brute Force) framework." },
    { title: "Mitigation", text: "Executing IPTables DROP command to block the attacker." },
    { title: "Verification", text: "Confirming zero further traffic from the blocked source." }
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
}
</script>
