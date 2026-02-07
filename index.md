---
layout: default
title: Arivazhagan | SOC Analyst L1
---

<style>
/* 1. MERGED CSS FROM GITHUB SOURCE */
body {
    font-family: 'Segoe UI', sans-serif;
    line-height: 1.6;
    color: #e0e0e0; /* Adjusted for dark theme readability */
    /* Using the Pentester background you requested */
    background: #0a0e14 url('Pentester.PNG') no-repeat center center fixed;
    background-size: cover;
    padding: 0; /* Navbar handles padding */
    margin: auto;
}

/* Dark overlay to make the GitHub style text pop against the image */
body::before {
    content: "";
    position: fixed;
    top: 0; left: 0; width: 100%; height: 100%;
    background: rgba(10, 14, 20, 0.85); 
    z-index: -1;
}

.navbar {
    background-color: #007acc; /* The exact blue from the source */
    padding: 1rem;
    text-align: center;
    position: sticky;
    top: 0;
    z-index: 1000;
    box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
}

.navbar a {
    color: white;
    text-decoration: none;
    margin: 0 15px;
    font-weight: bold;
    transition: color 0.3s ease;
}

.navbar a:hover {
    text-decoration: underline;
    color: #cceeff;
}

/* Header & Photo Section (New Layout) */
.header-hero {
    display: flex;
    justify-content: space-between;
    align-items: center;
    max-width: 900px;
    margin: 40px auto;
    padding: 0 20px;
}

.bio-content { flex: 1; text-align: left; }
.bio-content h1 { text-align: left; margin-bottom: 5px; color: #fff; }
.bio-content .role { color: #007acc; font-weight: bold; font-size: 1.2rem; }

.profile-photo-right img {
    width: 180px;
    height: 180px;
    border-radius: 12px;
    border: 3px solid #007acc;
    object-fit: cover;
    margin: 0; /* Overriding default img margin */
}

/* The Project Info Box from the source */
.project-info {
    margin: 40px auto;
    padding: 20px;
    background: rgba(247, 247, 247, 0.05); /* Transparent version of source */
    border-left: 4px solid #4caf50; /* The green border you wanted */
    max-width: 800px;
    font-family: sans-serif;
    backdrop-filter: blur(10px);
}

.project-info h3 {
    margin-top: 0;
    color: #4caf50;
    text-align: left;
}

.project-info p { color: #ccc; }

/* Screenshot Gallery */
.evidence-gallery {
    max-width: 900px;
    margin: auto;
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(140px, 1fr));
    gap: 15px;
    padding: 20px;
}

.evidence-gallery img {
    margin: 0; /* Resetting the 30px margin from source */
    cursor: pointer;
    transition: transform 0.2s;
    border: 1px solid #444;
}

.evidence-gallery img:hover {
    transform: scale(1.05);
    border-color: #007acc;
}

/* Lightbox Styling */
#lightbox {
    display: none;
    position: fixed;
    z-index: 9999;
    top: 0; left: 0; width: 100%; height: 100%;
    background: rgba(0,0,0,0.9);
    padding: 40px;
    box-sizing: border-box;
}

.lightbox-content {
    max-width: 1000px;
    margin: auto;
    background: #1a1a1a;
    border-radius: 8px;
    overflow: hidden;
}

.close-btn { color: white; float: right; font-size: 30px; cursor: pointer; padding: 10px; }
</style>

<nav class="navbar">
    <ul>
        <li><a href="#home">Home</a></li>
        <li><a href="#projects">Incident Report</a></li>
        <li><a href="mailto:arivazhagan@email.com">Contact</a></li>
        <li><a href="https://linkedin.com/in/arivazhagan" target="_blank">LinkedIn</a></li>
    </ul>
</nav>

<header id="home" class="header-hero">
    <div class="bio-content">
        <h1>ARIVAZHAGAN</h1>
        <span class="role">SOC Analyst L1</span>
        <p style="color: #bbb; max-width: 500px; margin-top: 15px;">
            Specializing in SIEM monitoring and incident response. Dedicated to protecting 
            digital assets through vigilant analysis and rapid threat containment.
        </p>
    </div>
    <div class="profile-photo-right">
        <img src="my-photo.jpg" alt="Arivazhagan">
    </div>
</header>

<hr>

<div id="projects" class="project-info">
    <h3>Quick Summary & Verdict</h3>
    <p><strong>Verdict:</strong> Confirmed Malicious SSH Brute Force Attack.</p>
    <p><strong>Action Taken:</strong> Identified source IP 141.98.81.37. Restored SIEM configuration after a system crash and implemented a permanent block via IPTables to stop the credential harvesting attempt.</p>
</div>

<h2 style="color: #fff;">Evidence Gallery</h2>
<div class="evidence-gallery">
    <img src="01.png" alt="Step 1" onclick="openLightbox(0)">
    <img src="02.png" alt="Step 2" onclick="openLightbox(1)">
    <img src="03.png" alt="Step 3" onclick="openLightbox(2)">
    <img src="04.png" alt="Step 4" onclick="openLightbox(3)">
    <img src="05.png" alt="Step 5" onclick="openLightbox(4)">
    <img src="06.png" alt="Step 6" onclick="openLightbox(5)">
    <img src="07.png" alt="Step 7" onclick="openLightbox(6)">
    <img src="08.png" alt="Step 8" onclick="openLightbox(7)">
    <img src="09.png" alt="Step 9" onclick="openLightbox(8)">
    <img src="10.png" alt="Step 10" onclick="openLightbox(9)">
    <img src="11.png" alt="Step 11" onclick="openLightbox(10)">
    <img src="12.png" alt="Step 12" onclick="openLightbox(11)">
    <img src="13.png" alt="Step 13" onclick="openLightbox(12)">
    <img src="14.png" alt="Step 14" onclick="openLightbox(13)">
</div>

<div id="lightbox">
    <span class="close-btn" onclick="closeLightbox()">&times;</span>
    <div class="lightbox-content">
        <img id="activeImg" src="" style="margin:0; width:100%; border-radius:0;">
        <div style="padding: 20px; background: #1a1a1a; border-top: 1px solid #333;">
            <h3 id="detailTitle" style="color:#007acc; text-align:left; margin-bottom:10px;"></h3>
            <p id="detailText" style="color:#ddd; margin-bottom:15px;"></p>
            <div style="background: rgba(76, 175, 80, 0.1); border-left: 4px solid #4caf50; padding: 10px;">
                <strong style="color: #4caf50;">L2 Escalation Reason:</strong>
                <p id="l2Text" style="margin: 5px 0 0; font-size: 0.9em; font-style: italic;"></p>
            </div>
        </div>
    </div>
</div>

<script>
let currentIndex = 0;
const reportData = [
    { title: "Baseline Monitoring", text: "Establishing standard monitoring before the spike.", l2: "Baseline required to identify deviation." },
    { title: "Wazuh Alert Spike", text: "Detection of high-frequency login failures.", l2: "Alert volume indicates automated attack." },
    { title: "Auth Log Isolation", text: "Identifying Rule 5712 triggers.", l2: "Targeting specific brute force signature." },
    { title: "Attack Simulation", text: "Testing detection rules with manual scripts.", l2: "Validating rule response before blocking." },
    { title: "Config Recovery", text: "Repairing corrupted SIEM manager configuration.", l2: "System outage required manual intervention." },
    { title: "Metric Review", text: "Total of 1,379 authentication events analyzed.", l2: "Quantifying scope for incident severity." },
    { title: "User Probing", text: "Attempts to access 'admin' and 'guest' users.", l2: "Confirmed malicious intent via user enumeration." },
    { title: "IP Isolation", text: "Pinpointing 141.98.81.37 as the source.", l2: "Isolating threat actor for mitigation." },
    { title: "Incident Escalation", text: "Alert elevated to Level 12 Severity.", l2: "Threshold reached for active response." },
    { title: "Threat Actor Profile", text: "Determining origin and history of the IP.", l2: "Intelligence gathering for the blocklist." },
    { title: "AbuseIPDB OSINT", text: "Verified 100% confidence abuse score.", l2: "Third-party intel confirms malicious IP." },
    { title: "MITRE ATT&CK Mapping", text: "Categorized as T1110 (Brute Force).", l2: "Standardizing the incident framework." },
    { title: "Active Mitigation", text: "Manual execution of IPTables DROP command.", l2: "Direct intervention to sever actor access." },
    { title: "Final Verification", text: "Confirming zero traffic from blocked IP.", l2: "Post-mitigation audit to ensure safety." }
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
