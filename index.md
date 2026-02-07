---
layout: default
title: SOC Lab Portfolio
---

<style>
/* 1. Integrated Cybersecurity Background */
body {
    background: #0a0e14 url('Pentester.jpg') no-repeat center center fixed;
    background-size: cover;
    color: #e0e0e0;
    font-family: 'Segoe UI', Roboto, Helvetica, Arial, sans-serif;
    margin: 0;
    padding: 0;
}

/* Overlay to ensure text readability over the background image */
body::before {
    content: "";
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background: rgba(10, 14, 20, 0.85); /* Adjust opacity to make background clearer or darker */
    z-index: -1;
}

/* 2. Layout Containers */
.main-wrapper {
    display: flex;
    flex-wrap: wrap;
    gap: 30px;
    padding: 40px 20px;
    max-width: 1200px;
    margin: auto;
}

/* 3. Profile Sidebar */
.profile-sidebar {
    flex: 1 1 300px;
    background: rgba(15, 23, 42, 0.6);
    border: 1px solid rgba(0, 123, 255, 0.3);
    border-radius: 15px;
    padding: 25px;
    text-align: center;
    backdrop-filter: blur(8px);
    height: fit-content;
}

.profile-pic {
    width: 150px;
    height: 150px;
    border-radius: 50%;
    border: 3px solid #007bff;
    object-fit: cover;
    margin-bottom: 15px;
    box-shadow: 0 0 20px rgba(0, 123, 255, 0.4);
}

.profile-sidebar h2 { 
    color: #ffffff; 
    margin-bottom: 5px; 
    text-transform: uppercase;
    letter-spacing: 2px;
}
.profile-sidebar p.title { 
    color: #38bdf8; 
    font-weight: bold; 
    margin-bottom: 15px; 
    font-size: 1.1em;
}

/* 4. Incident Report Content */
.report-content {
    flex: 3 1 700px;
}

.verdict-box {
    background: rgba(0, 123, 255, 0.1);
    border-left: 5px solid #007bff;
    padding: 20px;
    margin-bottom: 30px;
    border-radius: 0 10px 10px 0;
    backdrop-filter: blur(5px);
}

/* 5. Horizontal Evidence Strip */
.evidence-strip {
    display: flex;
    overflow-x: auto;
    gap: 15px;
    padding: 20px 0;
    scrollbar-width: thin;
    scrollbar-color: #007bff #0f172a;
}

.thumb {
    height: 140px;
    border: 2px solid rgba(51, 65, 85, 0.5);
    border-radius: 8px;
    cursor: pointer;
    transition: 0.3s ease;
}

.thumb:hover {
    border-color: #007bff;
    transform: translateY(-5px);
    box-shadow: 0 5px 15px rgba(0, 123, 255, 0.5);
}

/* 6. The Interactive Lightbox (Pop-up) */
.lightbox-overlay {
    display: none;
    position: fixed;
    z-index: 99999;
    left: 0; top: 0;
    width: 100%; height: 100%;
    background: rgba(2, 6, 23, 0.95);
    backdrop-filter: blur(15px);
}

.lightbox-container {
    position: relative;
    margin: 2% auto;
    width: 90%;
    max-width: 1100px;
    background: #0f172a;
    border-radius: 12px;
    overflow: hidden;
    border: 1px solid #1e293b;
}

#activeImg {
    display: block;
    width: 100%;
    max-height: 65vh;
    object-fit: contain;
    background: #000;
}

.details-content { padding: 30px; background: #0f172a; }

.close-btn { position: absolute; top: 15px; right: 25px; color: #64748b; font-size: 40px; cursor: pointer; }
.close-btn:hover { color: #fff; }

.nav-btn {
    cursor: pointer;
    position: absolute;
    top: 40%;
    padding: 20px;
    color: #64748b;
    font-size: 50px;
    transition: 0.3s;
    text-decoration: none;
}
.nav-btn:hover { color: #007bff; transform: scale(1.2); }
.next { right: 1%; } .prev { left: 1%; }

.l2-box {
    background: rgba(30, 41, 59, 0.5);
    border-left: 4px solid #38bdf8;
    padding: 15px;
    margin-top: 15px;
    border-radius: 4px;
}
</style>

<div class="main-wrapper">
    <aside class="profile-sidebar">
        <img src="my-photo.jpg" alt="Arivazhagan" class="profile-pic">
        <h2>Arivazhagan</h2>
        <p class="title">SOC Analyst L1</p>
        <p>Specializing in SIEM monitoring, incident response, and threat hunting. Passionate about securing cloud environments and defending against credential-based attacks.</p>
        <div style="margin-top: 20px; border-top: 1px solid rgba(51, 65, 85, 0.5); padding-top: 15px;">
            <p><strong>Certifications:</strong> Security+, BTL1 (In Progress)</p>
            <p><strong>Tools:</strong> Wazuh, Splunk, Wireshark, Nmap</p>
        </div>
    </aside>

    <main class="report-content">
        <h1 style="color: #ffffff; margin-bottom: 10px; text-shadow: 2px 2px 4px rgba(0,0,0,0.5);">Incident Report: SSH Brute Force Analysis</h1>
        <p style="margin-bottom: 25px;"><strong>Status:</strong> <span style="color: #10b981; text-transform: uppercase;">● Resolved</span></p>

        <div class="verdict-box">
            <h3 style="margin-top: 0; color: #38bdf8;">/// Quick Summary & Verdict</h3>
            <p><strong>Verdict:</strong> Confirmed Malicious Brute Force Attack via automated script.</p>
            <p><strong>Action Taken:</strong> After identifying a persistent credential harvesting attempt from IP 141.98.81.37, I bypassed a system-level configuration crash to implement a host-based firewall block (IPTables), successfully terminating the threat actor's access.</p>
        </div>

        <h3 style="color: #94a3b8; font-size: 1em; letter-spacing: 1px;">EVIDENCE GALLERY (Click to Investigate)</h3>
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
    </main>
</div>

<div id="lightbox" class="lightbox-overlay">
    <span class="close-btn" onclick="closeLightbox()">&times;</span>
    <a class="nav-btn prev" onclick="changeSlide(-1)">&#10094;</a>
    <a class="nav-btn next" onclick="changeSlide(1)">&#10095;</a>

    <div class="lightbox-container">
        <img id="activeImg" src="" alt="Incident Evidence">
        <div class="details-content">
            <h2 id="detailTitle" style="color: #38bdf8; margin-top: 0;"></h2>
            <p id="detailText" style="color: #94a3b8; font-size: 1.1em; line-height: 1.6;"></p>
            <div class="l2-box">
                <strong style="color: #38bdf8;">L2 Escalation Logic:</strong>
                <p id="l2Text" style="margin-top: 8px; font-style: italic; color: #cbd5e1;"></p>
            </div>
        </div>
    </div>
</div>

<script>
let currentIndex = 0;
const reportData = [
    { title: "01: Dashboard Baseline", text: "Overview of the security posture before the attack began.", l2: "Initial monitoring showed low noise; established baseline for behavioral detection." },
    { title: "02: Alert Severity Spikes", text: "Wazuh dashboard showing multiple Level 10 Critical alerts appearing in a short time frame.", l2: "Automated alerts alone aren't enough; moved to L2 phase to correlate logs with external threat intel." },
    { title: "03: Authentication Failures", text: "Heavy volume of Rule 5712 (SSHD Brute Force) events isolated in the SIEM.", l2: "High-frequency failures indicated a scripted attack rather than a human typo." },
    { title: "04: Attack Simulation", text: "Validating detection rules by simulating a multi-attempt SSH login via terminal.", l2: "Simulation confirmed that Rule 5712 triggers correctly at the 8th failed attempt." },
    { title: "05: Recovery: Fixing Corrupted Config", text: "VMware crash caused 'ossec.conf' to wipe. Manually rebuilt the manager-agent handshake.", l2: "Escalated to system recovery; restored visibility before the attacker could exploit the blind spot." },
    { title: "06: 24-Hour Metric Aggregation", text: "Stats show 1379 total events, with 85 critical authentication failures.", l2: "Quantified the scope of the attack to determine if it was a targeted campaign or opportunistic bot." },
    { title: "07: Rule 5710 Analysis", text: "Detection of SSH attempts for users that do not exist (e.g., 'admin', 'guest').", l2: "User probing confirmed the attacker was scanning for common misconfigurations." },
    { title: "08: SSHD Log Deep-Dive", text: "Reviewing raw syslogs to identify the specific source IP and timestamp patterns.", l2: "L2 Analysis: Identified 141.98.81.37 as the persistent offender." },
    { title: "09: Brute Force Escalation", text: "The SIEM successfully aggregated Level 6 events into a high-severity Level 12 incident.", l2: "Escalated from 'noise' to 'active incident' based on sustained attack duration." },
    { title: "10: Threat Actor Identification", text: "Isolating the source IP 141.98.81.37 for cross-referencing.", l2: "L2 investigation focused on attribution and determining attacker location/intent." },
    { title: "11: OSINT Verification", text: "Querying AbuseIPDB results in a 100% Abuse Confidence Score for the identified IP.", l2: "Intelligence pivot: Verified the IP belongs to a known malicious botnet." },
    { title: "12: MITRE ATT&CK Mapping", text: "Categorizing activity under T1110 (Brute Force) for formal reporting.", l2: "Standardized the incident to communicate risk to stakeholders using industry frameworks." },
    { title: "13: Mitigation (IP Tables)", text: "Manual execution of 'DROP' command on the malicious IP to sever access.", l2: "Active Defense: Proactive containment used to prevent potential credential compromise." },
    { title: "14: Post-Mitigation Check", text: "Final status check showing zero further logs from the blocked IP address.", l2: "Verification: Confirmed the block is holding and the system is secured." }
];

function openLightbox(index) {
    currentIndex = index;
    document.getElementById("lightbox").style.display = "block";
    updateContent();
}

function closeLightbox() { document.getElementById("lightbox").style.display = "none"; }

function changeSlide(n) {
    currentIndex += n;
    if (currentIndex >= 14) currentIndex = 0;
    if (currentIndex < 0) currentIndex = 13;
    updateContent();
}

function updateContent() {
    const imgElement = document.getElementById("activeImg");
    let fileNumber = currentIndex + 1;
    let fileName = (fileNumber < 10) ? "0" + fileNumber + ".png" : fileNumber + ".png";
    imgElement.src = fileName;
    
    document.getElementById("detailTitle").innerText = reportData[currentIndex].title;
    document.getElementById("detailText").innerText = reportData[currentIndex].text;
    document.getElementById("l2Text").innerText = reportData[currentIndex].l2;
}
</script>
