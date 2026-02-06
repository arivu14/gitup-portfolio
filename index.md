---
layout: default
title: SOC Lab Portfolio
---

<div style="background: #1a1a1a; padding: 20px; border-radius: 10px; border-left: 5px solid #007bff; margin-bottom: 30px;">
    <h1 style="margin:0; color:#007bff;">Incident Report: SSH Brute Force Analysis</h1>
    <p style="margin: 5px 0;"><strong>Analyst:</strong> [Your Name] | <strong>Status:</strong> <span style="color:#28a745;">RESOLVED</span></p>
    <p style="color:#bbb;"><strong>Summary:</strong> Identified and mitigated a persistent brute force attack originating from IP 141.98.81.37 targeting administrative credentials. Recovery included manual restoration of corrupted Agent 004 configurations following a system crash.</p>
</div>

<h3 style="color:#eee;">Evidence Gallery (14 Stages)</h3>
<div class="evidence-strip">
    <img class="thumb" src="01.png" onclick="openLightbox(0)">
    <img class="thumb" src="02.png" onclick="openLightbox(1)">
    <img class="thumb" src="03.png" onclick="openLightbox(2)">
    <img class="thumb" src="04.png" onclick="openLightbox(3)">
    <img class="thumb" src="06.png" onclick="openLightbox(5)">
    <img class="thumb" src="07.png" onclick="openLightbox(6)">
    <img class="thumb" src="08.png" onclick="openLightbox(7)">
    <img class="thumb" src="09.png" onclick="openLightbox(8)">
    <img class="thumb" src="010.png" onclick="openLightbox(9)">
    <img class="thumb" src="011.png" onclick="openLightbox(10)">
    <img class="thumb" src="012.png" onclick="openLightbox(11)">
    <img class="thumb" src="013.png" onclick="openLightbox(12)">
    <img class="thumb" src="014.png" onclick="openLightbox(13)">
</div>

<div id="lightbox" class="lightbox">
    <span class="close" onclick="closeLightbox()">&times;</span>
    
  <a class="prev" onclick="changeSlide(-1)">&#10094;</a>
    <a class="next" onclick="changeSlide(1)">&#10095;</a>

  <div class="lightbox-content">
        <img id="activeImg" src="" style="width:100%; border-radius: 8px;">
        <div class="details-box">
            <h2 id="detailTitle" style="color:#007bff; margin-top:0;"></h2>
            <p id="detailText" style="font-size:16px; line-height:1.6;"></p>
        </div>
    </div>
</div>

<style>
/* Styling for the Horizontal Strip */
.evidence-strip {
    display: flex;
    overflow-x: auto;
    gap: 15px;
    padding: 15px;
    background: #111;
    border-radius: 8px;
    white-space: nowrap;
}
.thumb {
    height: 120px;
    border: 2px solid #333;
    border-radius: 5px;
    cursor: pointer;
    transition: 0.3s;
}
.thumb:hover { border-color: #007bff; transform: scale(1.05); }

/* Lightbox & Blur Effect */
.lightbox {
    display: none;
    position: fixed;
    z-index: 10000;
    left: 0; top: 0;
    width: 100%; height: 100%;
    background: rgba(0,0,0,0.9);
    backdrop-filter: blur(10px); /* Background Blur */
}

.lightbox-content {
    position: relative;
    margin: 5% auto;
    width: 70%;
    max-width: 1000px;
}

.details-box {
    background: #1e1e1e;
    padding: 20px;
    margin-top: -5px;
    border-radius: 0 0 8px 8px;
    border-top: 3px solid #007bff;
    color: #ddd;
}

/* Close & Nav Buttons */
.close { position: absolute; top: 20px; right: 40px; color: white; font-size: 50px; cursor: pointer; z-index: 10001; }
.prev, .next {
    cursor: pointer;
    position: absolute;
    top: 40%;
    padding: 16px;
    color: white;
    font-weight: bold;
    font-size: 40px;
    background: rgba(0,123,255,0.2);
    border-radius: 50%;
    text-decoration: none;
}
.next { right: 5%; }
.prev { left: 5%; }
.prev:hover, .next:hover { background: #007bff; }
</style>

<script>
let currentIndex = 0;
const summaries = [
    { title: "Stage 1: Alert Detection", text: "Initial dashboard entry showing a spike in high-severity alerts. Status: Investigating." },
    { title: "Stage 2: Severity Distribution", text: "Breakdown of authentication alerts. High concentration of Level 10 triggers identified." },
    { title: "Stage 3: Auth Success/Failure", text: "Comparison graph showing thousands of failed logins vs zero successes for the targeted IP." },
    { title: "Stage 4: Attack Simulation", text: "STRESS TEST: Running the brute force script from the attacker terminal to verify SIEM logging." },
    { title: "Stage 5: Configuration Recovery", text: "THE STRUGGLE: Recovering 'ossec.conf' after a VM crash. Successfully restored Agent 004 connectivity." },
    { title: "Stage 6: 24-Hour Dashboard", text: "Comprehensive view: 1,379 total events. 129 Critical alerts and 85 specific SSH failures." },
    { title: "Stage 7: Rule 5710 Analysis", text: "Detailed log for 'Attempt to login using a non-existent user.' Target account: root." },
    { title: "Stage 8: SSHD Log Details", text: "Raw syslog data from /var/log/auth.log showing the specific connection attempts." },
    { title: "Stage 9: Rule 5712: Brute Force", text: "The SIEM confirms a sustained attack, triggering the high-frequency brute force rule." },
    { title: "Stage 10: Attacker IP Isolation", text: "Source IP 141.98.81.37 identified as the malicious actor." },
    { title: "Stage 11: AbuseIPDB Verification", text: "OSINT check: IP 141.98.81.37 confirmed as a 100% confidence malicious bot." },
    { title: "Stage 12: MITRE Mapping", text: "Tactic: Credential Access (TA0006). Technique: Brute Force (T1110)." },
    { title: "Stage 13: Mitigation (IPTables)", text: "CONTAINMENT: Executing the DROP rule to permanently block the attacker IP." },
    { title: "Stage 14: Resolution Check", text: "FINAL VERIFICATION: Firewall logs confirm 0 packets accepted from the malicious source. Status: RESOLVED." }
];

function openLightbox(index) {
    currentIndex = index;
    document.getElementById("lightbox").style.display = "block";
    updateLightbox();
}

function closeLightbox() {
    document.getElementById("lightbox").style.display = "none";
}

function changeSlide(n) {
    currentIndex += n;
    if (currentIndex >= 14) currentIndex = 0;
    if (currentIndex < 0) currentIndex = 13;
    updateLightbox();
}

function updateLightbox() {
    document.getElementById("activeImg").src = "BF_" + (currentIndex + 1) + ".png";
    document.getElementById("detailTitle").innerText = summaries[currentIndex].title;
    document.getElementById("detailText").innerText = summaries[currentIndex].text;
}
</script>
