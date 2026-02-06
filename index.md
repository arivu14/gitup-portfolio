---
layout: default
title: SOC Lab Portfolio
---

<div style="padding: 10px 0; margin-bottom: 20px; font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;">
    <h1 style="color: #007bff; margin-bottom: 5px;">Incident Report: SSH Brute Force Analysis</h1>
    <p style="font-size: 1.1em; margin: 0;"><strong>Analyst:</strong> [Your Name] | <strong>Status:</strong> <span style="color: #28a745; font-weight: bold;">RESOLVED</span></p>
</div>

<div style="margin-bottom: 30px; border-left: 4px solid #007bff; padding-left: 15px;">
    <h3 style="margin-top: 0; color: #eee;">Quick Summary & Verdict</h3>
    <p style="color: #bbb; line-height: 1.6; max-width: 900px;">
        <strong>Verdict:</strong> Confirmed Malicious Brute Force Attack. <br>
        <strong>Action Taken:</strong> After identifying a persistent credential harvesting attempt from IP 141.98.81.37, I manually bypassed a system-level configuration crash to implement a host-based firewall block (IPTables), successfully terminating the threat actor's access.
    </p>
</div>

<h3 style="color: #eee; margin-left: 5px; font-size: 1.2em;">/// Evidence Gallery (Click to Investigate)</h3>
<div class="evidence-strip">
    <img class="thumb" src="01.png" alt="Dashboard Overview" onclick="openLightbox(0)">
    <img class="thumb" src="02.png" alt="Severity Levels" onclick="openLightbox(1)">
    <img class="thumb" src="03.png" alt="Auth Patterns" onclick="openLightbox(2)">
    <img class="thumb" src="04.png" alt="Attack Simulation" onclick="openLightbox(3)">
    <img class="thumb" src="05.png" alt="Recovery Process" onclick="openLightbox(4)">
    <img class="thumb" src="06.png" alt="24hr Metrics" onclick="openLightbox(5)">
    <img class="thumb" src="07.png" alt="User Probing" onclick="openLightbox(6)">
    <img class="thumb" src="08.png" alt="Log Details" onclick="openLightbox(7)">
    <img class="thumb" src="09.png" alt="Rule 5712" onclick="openLightbox(8)">
    <img class="thumb" src="10.png" alt="IP Identification" onclick="openLightbox(9)">
    <img class="thumb" src="11.png" alt="AbuseIPDB" onclick="openLightbox(10)">
    <img class="thumb" src="12.png" alt="MITRE Mapping" onclick="openLightbox(11)">
    <img class="thumb" src="13.png" alt="IP Block" onclick="openLightbox(12)">
    <img class="thumb" src="14.png" alt="Verification" onclick="openLightbox(13)">
</div>

<div id="lightbox" class="lightbox-overlay">
    <span class="close-btn" onclick="closeLightbox()">&times;</span>
    <a class="nav-btn prev" onclick="changeSlide(-1)">&#10094;</a>
    <a class="nav-btn next" onclick="changeSlide(1)">&#10095;</a>

<div class="lightbox-container">
        <div style="width: 100%; background: #000; display: flex; justify-content: center; min-height: 400px; border-bottom: 1px solid #333;">
            <img id="activeImg" src="" alt="Incident Evidence" style="max-width: 100%; height: auto; display: block;">
        </div>
        
<div class="details-content">
            <h2 id="detailTitle" style="color: #007bff; margin-top: 0; margin-bottom: 10px;"></h2>
            <div id="analystNotes" style="margin-bottom: 15px;">
                <strong style="color: #eee;">Analyst Notes:</strong>
                <p id="detailText" style="font-size: 15px; color: #ccc; margin-top: 5px; line-height: 1.5;"></p>
            </div>
            <div id="l2Section" style="background: rgba(0, 123, 255, 0.1); padding: 12px; border-radius: 6px; border-left: 3px solid #007bff;">
                <strong style="color: #007bff;">L2 Escalation Logic:</strong>
                <p id="l2Text" style="font-size: 14px; color: #ddd; margin-top: 5px; margin-bottom: 0; font-style: italic;"></p>
            </div>
        </div>
    </div>
</div>

<style>
.evidence-strip { display: flex; overflow-x: auto; gap: 15px; padding: 15px 5px; scrollbar-width: thin; scrollbar-color: #007bff #222; }
.thumb { height: 140px; border: 2px solid #333; border-radius: 8px; cursor: pointer; transition: 0.3s; }
.thumb:hover { border-color: #007bff; transform: translateY(-3px); }

.lightbox-overlay { display: none; position: fixed; z-index: 99999; left: 0; top: 0; width: 100%; height: 100%; background: rgba(0,0,0,0.95); backdrop-filter: blur(12px); -webkit-backdrop-filter: blur(12px); }
.lightbox-container { position: relative; margin: 2% auto; width: 85%; max-width: 1000px; background: #181818; border-radius: 12px; overflow: hidden; box-shadow: 0 0 50px rgba(0,0,0,1); border: 1px solid #333; }
.details-content { padding: 25px; background: #181818; }
.close-btn { position: absolute; top: 20px; right: 40px; color: #fff; font-size: 60px; cursor: pointer; text-shadow: 0 0 10px #000; }
.nav-btn { cursor: pointer; position: absolute; top: 45%; padding: 20px; color: white; font-size: 50px; text-decoration: none; user-select: none; }
.next { right: 1%; } .prev { left: 1%; }
</style>

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
