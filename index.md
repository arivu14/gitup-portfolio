---
layout: null
---
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Arivazhagan | SOC Portfolio</title>
    <style>
        /* BASE THEME & BACKGROUND */
        * { box-sizing: border-box; }
        html, body { 
            margin: 0; padding: 0; width: 100%; 
            background: linear-gradient(rgba(10, 14, 20, 0.85), rgba(10, 14, 20, 0.85)), url('cc.jpg');
            background-size: cover; background-position: center; background-attachment: fixed;
            color: white; font-family: 'Consolas', 'Monaco', 'Courier New', monospace; 
            overflow-x: hidden; 
        }
        
.page-wrap.is-blurred { filter: blur(20px); pointer-events: none; transition: 0.4s ease; }
        
  /* TAB NAVIGATION */
        .tab-nav {
            display: flex; justify-content: center; background: rgba(15, 23, 42, 0.95);
            border-bottom: 2px solid #38bdf8; position: sticky; top: 0; z-index: 100;
        }
        .tab-btn {
            padding: 20px 30px; border: none; background: none; color: #94a3b8;
            cursor: pointer; font-weight: bold; transition: 0.3s; font-family: inherit;
        }
        .tab-btn.active { color: #38bdf8; border-bottom: 3px solid #38bdf8; background: rgba(56,189,248,0.1); }
        .tab-content { display: none; padding-top: 20px; }
        .tab-content.active { display: block; }

/* HERO SECTION */
        .hero { width: 100%; padding: 50px 0; display: flex; align-items: center; justify-content: center; }
        .hero-container { width: 90%; max-width: 1200px; display: flex; justify-content: space-between; align-items: center; }
        .text-side h1 { font-size: 3.5rem; margin: 0; font-weight: 900; letter-spacing: -1px; color: #fff; }
        .text-side .role { font-size: 1.6rem; color: #38bdf8; display: block; margin: 5px 0 10px 0; }
        .contact-info { font-size: 0.9rem; line-height: 1.6; color: #cbd5e1; font-family: sans-serif; }
        .pfp { width: 200px; height: 200px; border-radius: 50%; border: 3px solid #38bdf8; object-fit: cover; box-shadow: 0 0 30px rgba(56, 189, 248, 0.3); }

/* LAYOUTS */
        .investigation-section { width: 90%; max-width: 1200px; margin: 0 auto; padding-bottom: 80px; text-align: left; }
        .mission-summary { max-width: 800px; margin-bottom: 30px; font-family: sans-serif; line-height: 1.6; color: #38bdf8; font-weight: bold; font-size: 1.1rem; }

/* TERMINAL & CARDS */
        .grid { display: grid; grid-template-columns: 1fr 1fr; gap: 20px; margin-top: 20px; }
        .card { background: rgba(15, 23, 42, 0.95); border: 1px solid #334155; padding: 25px; border-radius: 8px; }
        .terminal { background: #000; color: #10b981; padding: 15px; border-radius: 5px; font-size: 0.85rem; line-height: 1.5; white-space: pre-wrap; border: 1px solid #1e293b; }

.trigger-box { max-width: 400px; cursor: pointer; border-radius: 12px; border: 2px solid #334155; overflow: hidden; transition: 0.3s ease; box-shadow: 0 15px 35px rgba(0,0,0,0.6); margin-bottom: 40px; }
        .trigger-box:hover { border-color: #38bdf8; transform: translateY(-5px); }
        .trigger-box img { width: 100%; display: block; height: auto; }
        .trigger-footer { padding: 15px; background: #1e293b; color: #38bdf8; font-weight: bold; font-size: 0.8rem; text-align: center; font-family: sans-serif; }

/* ROADMAP */
        .roadmap-item { display: flex; align-items: center; margin-bottom: 15px; padding: 15px; border-radius: 5px; background: rgba(15, 23, 42, 0.8); border: 1px solid #1e293b; }
        .status-done { color: #10b981; margin-right: 15px; font-weight: bold; }
        .status-pending { color: #f59e0b; margin-right: 15px; font-weight: bold; }

 /* MODAL */
        .modal-overlay { display: none; position: fixed; z-index: 9999; left: 0; top: 0; width: 100%; height: 100%; background: rgba(0,0,0,0.92); align-items: center; justify-content: center; }
        .modal-content { position: relative; width: 90%; max-width: 1000px; display: flex; flex-direction: column; align-items: center; }
        .modal-img { max-width: 100%; max-height: 65vh; border: 2px solid #38bdf8; border-radius: 8px; }
        .nav-btn { cursor: pointer; position: absolute; top: 40%; color: #38bdf8; font-size: 60px; transition: 0.3s; user-select: none; text-decoration: none; }
        .btn-prev { left: -100px; } .btn-next { right: -100px; }
        .details-panel { background: #1e293b; padding: 25px; margin-top: 20px; border-radius: 8px; width: 100%; border-left: 5px solid #38bdf8; font-family: sans-serif; }
        .close-btn { position: absolute; top: -70px; right: 0; color: white; font-size: 50px; cursor: pointer; }

 #data-store-ssh, #data-store-agent { display: none; }

@media (max-width: 1100px) {
            .hero-container { flex-direction: column-reverse; text-align: center; }
            .grid { grid-template-columns: 1fr; }
            .btn-prev { left: 10px; } .btn-next { right: 10px; }
        }
    </style>
</head>
<body>

<div class="page-wrap" id="main-site">
    <div class="hero">
        <div class="hero-container">
            <div class="text-side">
                <h1>ARIVAZHAGAN</h1>
                <span class="role">SOC Analyst L1</span>
                <div class="contact-info">
                    <strong>Contact:</strong> +91 6379944366<br>
                    <strong>Email:</strong> arivazhagans1411@gmail.com<br>
                    <strong>LinkedIn:</strong> <a href="https://www.linkedin.com/in/arivazhagan11/" target="_blank" style="color:#38bdf8; text-decoration:none;">Profile Page</a>
                </div>
            </div>
            <img src="Screenshot_20260103_200618_Gallery.jpg" class="pfp" alt="Arivazhagan">
        </div>
    </div>

<nav class="tab-nav">
        <button class="tab-btn active" onclick="openTab(event, 'detection')">1. LIVE DETECTION</button>
        <button class="tab-btn" onclick="openTab(event, 'ai-agent')">2. SENTINEL AI AGENT</button>
        <button class="tab-btn" onclick="openTab(event, 'roadmap')">3. PROJECT ROADMAP</button>
    </nav>

<div class="investigation-section">
        
<div id="detection" class="tab-content active">
            <div class="mission-summary">
                DETECTED AND CONTAINED A HIGH-SEVERITY SSH BRUTE FORCE ATTACK ORIGINATING FROM A KNOWN MALICIOUS BOTNET.
            </div>
 <div class="trigger-box" onclick="launchGallery('ssh', 0)">
                <img src="01.png" alt="SOC Investigation">
                <div class="trigger-footer">OPEN 13-STEP EVIDENCE SLIDESHOW ➔</div>
            </div>
<div class="card" style="margin-bottom:20px; border-left: 4px solid #38bdf8;">
                <h3 style="color:#38bdf8; margin-top:0;">Tier 2 Escalation Rationale</h3>
                <p style="font-family: sans-serif; line-height:1.6;"><b>TECHNICAL JUSTIFICATION:</b> L1 containment (IPTables DROP) applied. Escalation required for source IP 141.98.81.37 due to 100% abuse score. Need cross-network correlation for lateral movement detection.</p>
            </div>
        </div>

 <div id="ai-agent" class="tab-content">
            <div class="mission-summary">AUTOMATED TRIAGE ENGINE USING GEMINI 2.5-FLASH FOR INSTANT LOG ANALYSIS.</div>
            
<div class="card" style="margin-bottom: 30px; border-left: 5px solid #10b981;">
                <h4 style="margin-top:0; color:#10b981;">🛡️ AGENT CORE LOGIC</h4>
                <p style="font-family: sans-serif; color:#cbd5e1; font-size: 0.9rem;">
                    The Sentinel Agent acts as an autonomous Tier-1 Analyst. It performs <b>automated parsing</b> of raw logs, <b>API-based enrichment</b> (VirusTotal/AbuseIPDB), and generates an <b>executive verdict</b> to reduce Mean Time to Respond (MTTR).
                </p>
            </div>


<div class="trigger-box" onclick="launchGallery('agent', 0)">
                <img src="Soc_agent_1.png" alt="AI Agent Execution">
                <div class="trigger-footer">VIEW AGENT LOGIC SLIDESHOW ➔</div>
            </div>

 <div class="grid">
                <div class="card">
                    <h4>📥 Raw Log Input</h4>
                    <div class="terminal" style="color:#38bdf8">{
  "target_ip": "172.16.17.207",
  "engine": "Wazuh-Sentinel-Link",
  "scan_type": "Internal_Asset_Audit"
}</div>
                </div>
                <div class="card">
                    <h4>🧠 Sentinel AI Report</h4>
                    <div class="terminal">🕵️ INVESTIGATION REPORT
Target IP: 172.16.17.207
VT Malicious Score: 0

FINAL DECISION: Internal private IP. No publicly known threats. Vigilance required for zero-day internal activity.</div>
                </div>
            </div>
        </div>

 <div id="roadmap" class="tab-content">
            <div class="mission-summary">CONTINUOUS UPSKILLING & TOOL INTEGRATION PIPELINE.</div>
            <div class="roadmap-item">
                <span class="status-done">✔</span>
                <div><b>SSH Brute Force Suite:</b> Live monitoring and IPTables response.</div>
            </div>
 <div class="roadmap-item">
                <span class="status-done">✔</span>
                <div><b>Sentinel AI Agent:</b> Gemini 2.5-Flash integration for log triage.</div>
            </div>
 <div class="roadmap-item">
                <span class="status-pending">⚡</span>
                <div><b>AbuseIPDB API:</b> Real-time automated reputation scoring.</div>
            </div>
 <div class="roadmap-item">
                <span class="status-pending">⚡</span>
                <div><b>Parent-Process Audit:</b> Process tree analysis for LotL detection.</div>
            </div>
        </div>

    </div>
</div>

<div id="modalBox" class="modal-overlay">
    <div class="modal-content">
        <span class="close-btn" onclick="exitGallery()">&times;</span>
        <a class="nav-btn btn-prev" onclick="stepSlide(-1)">&#10094;</a>
        <img id="mainViewer" class="modal-img">
        <a class="nav-btn btn-next" onclick="stepSlide(1)">&#10095;</a>
        <div class="details-panel">
            <p id="viewerCap" style="margin:0; font-size: 1.1rem; line-height:1.5;"></p>
        </div>
    </div>
</div>

<div id="data-store-ssh">
    <div data-img="01.png" data-text="<b>Step 1: Baseline Dashboard</b> - Monitoring SIEM state."></div>
    <div data-img="02.png" data-text="<b>Step 2: Metric Monitoring</b> - Normal traffic flow."></div>
    <div data-img="03.png" data-text="<b>Step 3: Initial Log State</b> - Auth failures recorded."></div>
    <div data-img="04.png" data-text="<b>Step 4: Active Attack</b> - Attacker terminal during attempt."></div>
    <div data-img="05.png" data-text="<b>Step 5: Alert Spike</b> - Wazuh Level 12 critical alerts."></div>
    <div data-img="06.png" data-text="<b>Step 6: Rule 5712 Filter</b> - Isolating Brute Force signatures."></div>
    <div data-img="07.png" data-text="<b>Step 7: Timeline Correlation</b> - Sequence analysis."></div>
    <div data-img="08.png" data-text="<b>Step 8: Deep Dive</b> - Scope verification."></div>
    <div data-img="09.png" data-text="<b>Step 9: IP Extraction</b> - ID source 141.98.81.37."></div>
    <div data-img="10.png" data-text="<b>Step 10: OSINT Pivot</b> - 100% Abuse score confirmed."></div>
    <div data-img="11.png" data-text="<b>Step 11: MITRE Mapping</b> - Mapping to T1110."></div>
    <div data-img="12.png" data-text="<b>Step 12: Terminal Response</b> - Containment prep."></div>
    <div data-img="13.png" data-text="<b>Step 13: Final Remediation</b> - IPTables DROP policy applied."></div>
</div>

<div id="data-store-agent">
    <div data-img="Soc_agent_1.png" data-text="<b>Agent Step 1: Initialization</b> - Gemini 2.5-Flash loading security context."></div>
    <div data-img="Soc_agent_2.png" data-text="<b>Agent Step 2: Enrichment</b> - Querying threat intel for IP reputation."></div>
    <div data-img="Soc_agent_3.png" data-text="<b>Agent Step 3: Final Triage</b> - Generating autonomous verdict and summary."></div>
</div>

<script>
    let activeStep = 0;
    let currentStore = [];
    const modal = document.getElementById('modalBox');
    const bgWrap = document.getElementById('main-site');

    function openTab(evt, tabName) {
        var i, tabcontent, tablinks;
        tabcontent = document.getElementsByClassName("tab-content");
        for (i = 0; i < tabcontent.length; i++) { tabcontent[i].style.display = "none"; }
        tablinks = document.getElementsByClassName("tab-btn");
        for (i = 0; i < tablinks.length; i++) { tablinks[i].className = tablinks[i].className.replace(" active", ""); }
        document.getElementById(tabName).style.display = "block";
        evt.currentTarget.className += " active";
    }

    function launchGallery(type, n) {
        currentStore = document.querySelectorAll('#data-store-' + type + ' div');
        activeStep = n;
        modal.style.display = "flex";
        bgWrap.classList.add('is-blurred');
        render();
    }

    function exitGallery() {
        modal.style.display = "none";
        bgWrap.classList.remove('is-blurred');
    }

    function stepSlide(n) {
        activeStep += n;
        if (activeStep >= currentStore.length) activeStep = 0;
        if (activeStep < 0) activeStep = currentStore.length - 1;
        render();
    }

    function render() {
        const item = currentStore[activeStep];
        document.getElementById('mainViewer').src = item.getAttribute('data-img');
        document.getElementById('viewerCap').innerHTML = item.getAttribute('data-text');
    }

    window.onclick = function(e) { if (e.target == modal) exitGallery(); }
</script>

</body>
</html>
