---
layout: default
title: SOC Lab Portfolio
---

<div style="background: #1a1a1a; padding: 25px; border-radius: 12px; border-left: 5px solid #007bff; margin-bottom: 30px; box-shadow: 0 4px 15px rgba(0,0,0,0.3);">
    <h1 style="margin:0; color:#007bff; font-family: 'Segoe UI', sans-serif;">Incident Report: SSH Brute Force Analysis</h1>
    <p style="margin: 10px 0; font-size: 1.1em;"><strong>Analyst:</strong> [Your Name] | <strong>Status:</strong> <span style="color:#28a745; font-weight:bold;">RESOLVED</span></p>
    <p style="color:#bbb; line-height:1.5;"><strong>Executive Summary:</strong> Detected a high-severity brute force attack from IP 141.98.81.37. Despite a VMware system crash that corrupted agent configurations, I successfully recovered the environment and implemented a permanent firewall block to secure the endpoint.</p>
</div>

<h3 style="color:#eee; margin-left: 10px;">Evidence Gallery (Click to Investigate)</h3>
<div class="evidence-strip">
    <img class="thumb" src="01.png" onclick="openLightbox(0)">
    <img class="thumb" src="02.png" onclick="openLightbox(1)">
    <img class="thumb" src="03.png" onclick="openLightbox(2)">
    <img class="thumb" src="04.png" onclick="openLightbox(3)">
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

<div id="lightbox" class="lightbox-overlay">
    <span class="close-btn" onclick="closeLightbox()">&times;</span>
    
<a class="nav-btn prev" onclick="changeSlide(-1)">&#10094;</a>
    <a class="nav-btn next" onclick="changeSlide(1)">&#10095;</a>

<div class="lightbox-container">
        <div style="width:100%; background:#000; display:flex; justify-content:center; min-height: 400px;">
            <img id="activeImg" src="" alt="Incident Evidence" style="max-width:100%; height:auto; display:block;">
        </div>
        
<div class="details-content">
            <h2 id="detailTitle" style="color:#007bff; margin-top:0; border-bottom: 1px solid #333; padding-bottom: 10px;"></h2>
            <p id="detailText" style="font-size:16px; color:#ddd; line-height:1.6;"></p>
        </div>
    </div>
</div>

<style>
.evidence-strip {
    display: flex;
    overflow-x: auto;
    gap: 15px;
    padding: 20px;
    background: #111;
    border-radius: 10px;
}
.thumb {
    height: 140px;
    border: 2px solid #333;
    border-radius: 8px;
    cursor: pointer;
}
.thumb:hover { border-color: #007bff; }

.lightbox-overlay {
    display: none;
    position: fixed;
    z-index: 99999;
    left: 0; top: 0;
    width: 100%; height: 100%;
    background: rgba(0,0,0,0.95);
    backdrop-filter: blur(12px);
    -webkit-backdrop-filter: blur(12px);
}

.lightbox-container {
    position: relative;
    margin: 2% auto;
    width: 85%;
    max-width: 1000px;
    background: #181818;
    border-radius: 12px;
    overflow: hidden;
    box-shadow: 0 0 50px rgba(0,0,0,1);
}

.details-content { padding: 25px; background: #181818; }
.close-btn { position: absolute; top: 20px; right: 40px; color: #fff; font-size: 60px; cursor: pointer; }
.nav-btn { cursor: pointer; position: absolute; top: 45%; padding: 20px; color: white; font-size: 50px; text-decoration: none; }
.next { right: 2%; } .prev { left: 2%; }
</style>

<script>
let currentIndex = 0;
const reportData = [
    { title: "Dashboard Entry", text: "Baseline security monitoring view. Captured moments before the automated brute force attack spiked in volume." },
    { title: "Critical Severity Alerts", text: "Analysis of the Wazuh alert levels. Multiple Level 10 triggers indicate a sustained attempt to bypass SSH security." },
    { title: "Authentication Story", text: "Clear evidence of malicious activity: The graph displays a vertical spike in failures with zero successful logins." },
    { title: "Attack Simulation", text: "Manual testing phase. Executing SSH brute force scripts from the attacker machine to confirm real-time SIEM logging." },
    { title: "The Struggle: Recovery", text: "After a system crash, Agent 004's config was destroyed. I manually restored the handshake and ossec.conf file." },
    { title: "24-Hour Dashboard", text: "Comprehensive event log: 1,379 events total, 129 critical level alerts, and 85 specific authentication failures." },
    { title: "Rule 5710 Trigger", text: "Detection of attempts to access non-existent usernames. This is common 'probing' behavior from automated bots." },
    { title: "Log Analysis (sshd)", text: "Diving into raw syslog data. Confirmed the attacker is attempting to guess passwords for the 'root' account." },
    { title: "Rule 5712 Escalation", text: "Brute force rule fired. The SIEM correctly aggregated multiple Level 6 failures into a Level 10 Critical Incident." },
    { title: "Adversary Identification", text: "Isolated Source IP 141.98.81.37. This IP is responsible for 100% of the unauthorized traffic in this window." },
    { title: "OSINT Intelligence", text: "Cross-referencing 141.98.81.37 on AbuseIPDB confirms a 100% confidence malicious score for SSH scanning." },
    { title: "MITRE ATT&CK Mapping", text: "Tactic: Credential Access (TA0006). Technique: Brute Force (T1110). Visualizing the attack vector." },
    { title: "L2 Response: IP Block", text: "Containment: Implementing a DROP rule via IPTables to permanently terminate the attacker's connection." },
    { title: "Final Resolution", text: "Verification check. Firewall logs show zero packets accepted from the malicious source. Incident successfully closed." }
];

function openLightbox(index) {
    currentIndex = index;
    document.getElementById("lightbox").style.display = "block";
    updateContent();
}

function closeLightbox() {
    document.getElementById("lightbox").style.display = "none";
}

function changeSlide(n) {
    currentIndex += n;
    if (currentIndex >= 14) currentIndex = 0;
    if (currentIndex < 0) currentIndex = 13;
    updateContent();
}

function updateContent() {
    const imgElement = document.getElementById("activeImg");
    
    // logic to handle 01, 02... 09 vs 10, 11... 14
    let fileNumber = currentIndex + 1;
    let fileName = (fileNumber < 10) ? "0" + fileNumber + ".png" : fileNumber + ".png";
    
    imgElement.src = fileName;
    
    // Debugging check: Open your browser console (F12) to see if it's hitting the right path
    console.log("Attempting to load: " + fileName);

    document.getElementById("detailTitle").innerText = reportData[currentIndex].title;
    document.getElementById("detailText").innerText = reportData[currentIndex].text;
}
</script>
