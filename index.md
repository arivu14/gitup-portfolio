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
            background: linear-gradient(rgba(10, 14, 20, 0.9), rgba(10, 14, 20, 0.9)), url('cc.jpg');
            background-size: cover; background-position: center; background-attachment: fixed;
            color: white; font-family: 'Consolas', 'Monaco', 'Courier New', monospace; 
            overflow-x: hidden; 
        }
        
.page-wrap.is-blurred { filter: blur(20px); pointer-events: none; transition: 0.4s ease; }

/* TAB NAVIGATION */
        .tab-nav {
            display: flex; justify-content: center; background: rgba(15, 23, 42, 0.98);
            border-bottom: 2px solid #38bdf8; position: sticky; top: 0; z-index: 100;
        }
        .tab-btn {
            padding: 20px 30px; border: none; background: none; color: #94a3b8;
            cursor: pointer; font-weight: bold; transition: 0.3s; font-family: inherit;
        }
        .tab-btn.active { color: #38bdf8; border-bottom: 3px solid #38bdf8; background: rgba(56,189,248,0.1); }
        .tab-content { display: none; padding-top: 20px; animation: fadeIn 0.4s; }
        @keyframes fadeIn { from { opacity: 0; } to { opacity: 1; } }
        .tab-content.active { display: block; }

/* HERO SECTION */
        .hero { width: 100%; padding: 50px 0; display: flex; align-items: center; justify-content: center; }
        .hero-container { width: 90%; max-width: 1200px; display: flex; justify-content: space-between; align-items: center; }
        .text-side h1 { font-size: 3.5rem; margin: 0; font-weight: 900; letter-spacing: -1px; color: #fff; }
        .text-side .role { font-size: 1.6rem; color: #38bdf8; display: block; margin: 5px 0 10px 0; }
        .contact-info { font-size: 0.9rem; line-height: 1.6; color: #cbd5e1; font-family: sans-serif; }
        .pfp { width: 200px; height: 200px; border-radius: 50%; border: 3px solid #38bdf8; object-fit: cover; box-shadow: 0 0 30px rgba(56, 189, 248, 0.3); }

 /* INVESTIGATION LAYOUT */
        .investigation-section { width: 90%; max-width: 1200px; margin: 0 auto; padding-bottom: 80px; text-align: left; }
        .mission-summary { max-width: 800px; margin-bottom: 30px; font-family: sans-serif; line-height: 1.6; color: #38bdf8; font-weight: bold; font-size: 1.1rem; text-transform: uppercase; }

 /* TERMINAL & CARDS */
        .grid { display: grid; grid-template-columns: 1fr 1fr; gap: 20px; margin-top: 20px; }
        .card { background: rgba(15, 23, 42, 0.95); border: 1px solid #334155; padding: 25px; border-radius: 8px; position: relative; }
        .terminal { background: #000; color: #10b981; padding: 15px; border-radius: 5px; font-size: 0.85rem; line-height: 1.5; white-space: pre-wrap; border: 1px solid #1e293b; min-height: 150px; }

.trigger-box { max-width: 450px; cursor: pointer; border-radius: 12px; border: 2px solid #334155; overflow: hidden; transition: 0.3s ease; box-shadow: 0 15px 35px rgba(0,0,0,0.6); margin-bottom: 30px; }
        .trigger-box:hover { border-color: #38bdf8; transform: translateY(-5px); }
        .trigger-box img { width: 100%; display: block; height: auto; }
        .trigger-footer { padding: 15px; background: #1e293b; color: #38bdf8; font-weight: bold; font-size: 0.8rem; text-align: center; font-family: sans-serif; }

 /* MODAL */
        .modal-overlay { display: none; position: fixed; z-index: 9999; left: 0; top: 0; width: 100%; height: 100%; background: rgba(0,0,0,0.95); align-items: center; justify-content: center; }
        .modal-content { position: relative; width: 90%; max-width: 1100px; display: flex; flex-direction: column; align-items: center; }
        .modal-img { max-width: 100%; max-height: 70vh; border: 2px solid #38bdf8; border-radius: 8px; box-shadow: 0 0 50px rgba(56,189,248,0.2); }
        .nav-btn { cursor: pointer; position: absolute; top: 45%; color: #38bdf8; font-size: 50px; transition: 0.3s; user-select: none; text-decoration: none; background: rgba(0,0,0,0.3); padding: 10px; border-radius: 50%; }
        .btn-prev { left: -80px; } .btn-next { right: -80px; }
        .details-panel { background: #1e293b; padding: 25px; margin-top: 20px; border-radius: 8px; width: 100%; border-left: 5px solid #38bdf8; font-family: sans-serif; }
        .close-btn { position: absolute; top: -60px; right: 0; color: white; font-size: 40px; cursor: pointer; }

 #data-store-ssh, #data-store-agent, #data-store-malware { display: none; }
        
 @media (max-width: 1100px) {
            .hero-container { flex-direction: column-reverse; text-align: center; }
            .grid { grid-template-columns: 1fr; }
            .btn-prev, .btn-next { display: none; }
        }
</style>
</head>
<body>

<div class="page-wrap" id="main-site">
    <div class="hero">
        <div class="hero-container">
            <div class="text-side">
                <h1>ARIVAZHAGAN</h1>
                <span class="role">SOC Analyst L1 | Security Automation</span>
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
        <button class="tab-btn active" onclick="openTab(event, 'detection')">1. INCIDENT INVESTIGATION</button>
        <button class="tab-btn" onclick="openTab(event, 'ai-agent')">2. CYPHER-SENTINEL (AI AGENT)</button>
        <button class="tab-btn" onclick="openTab(event, 'malware-triage')">3. MALWARE AI TRIAGE</button>
    </nav>

 <div class="investigation-section">
    
<div id="detection" class="tab-content active">
            <div class="mission-summary">CASE-001: SSH BRUTE FORCE DETECTION & RESPONSE [WAZUH SIEM]</div>
            <div class="trigger-box" onclick="launchGallery('ssh', 0)">
                <img src="01.png" alt="SOC Investigation">
                <div class="trigger-footer">OPEN 13-STEP INVESTIGATION GALLERY ➔</div>
            </div>
<div class="grid">
                <div class="card" style="border-left: 4px solid #f87171;">
                    <h3 style="color:#f87171; margin-top:0; font-size:1.1rem;">IMMEDIATE MITIGATION (L1)</h3>
                    <p style="font-family: sans-serif; line-height:1.6; font-size: 0.9rem;">
                        <b>ACTION:</b> IPTables DROP rule applied to Source IP 141.98.81.37.<br>
                        <b>RATIONALE:</b> 100% abuse confidence score on OSINT enrichment. 145+ failed attempts within 5 minutes.
                    </p>
                </div>
<div class="card" style="border-left: 4px solid #10b981;">
                    <h3 style="color:#10b981; margin-top:0; font-size:1.1rem;">PREVENTION & HARDENING</h3>
                    <p style="font-family: sans-serif; line-height:1.6; font-size: 0.9rem;">
                        <b>RECOMMENDATION:</b> Move to SSH Key-based authentication and disable password logins in <code>sshd_config</code>. Implement Fail2Ban for automated temporary null-routing.
                    </p>
                </div>
            </div>
        </div>

 <div id="ai-agent" class="tab-content">
            <div class="mission-summary">AUTOMATING TIER-1 TRIAGE WITH LLM REASONING</div>
            <div class="card" style="margin-bottom: 30px; border-left: 5px solid #10b981; background: rgba(16, 185, 129, 0.05);">
                <h4 style="margin-top:0; color:#10b981;">🚀 AGENT ARCHITECTURE: "CYPHER-SENTINEL"</h4>
                <p style="font-family: sans-serif; color:#cbd5e1; font-size: 0.9rem; line-height:1.6;">
                    Built on Google Colab using <b>Gemini 2.5-Flash</b>. This agent automates the "Pivot" phase of an investigation. It takes raw Wazuh JSON data and outputs a human-readable verdict to reduce MTTR.
                </p>
                </div>
<div class="trigger-box" onclick="launchGallery('agent', 0)">
                <img src="Soc_agent_1.png" alt="AI Agent Execution">
                <div class="trigger-footer">VIEW AGENT LOGIC & EXECUTION ➔</div>
            </div>
 <div class="grid">
                <div class="card">
                    <h4>📥 RAW SIEM INPUT</h4>
                    <div class="terminal" style="color:#38bdf8">{ "target_ip": "172.16.17.207", "log_source": "Wazuh_Manager", "event_type": "Internal_Audit" }</div>
                </div>
                <div class="card">
                    <h4>🧠 AI ANALYST VERDICT</h4>
                    <div class="terminal">🕵️ INVESTIGATION REPORT
IP: 172.16.17.207 (Private)
VERDICT: BENIGN. Asset identified as internal management server.</div>
                </div>
            </div>
        </div>

 <div id="malware-triage" class="tab-content">
            <div class="mission-summary">CASE-002: AUTOMATED MALWARE TRIAGE & AI FORENSICS</div>
            

<div class="card" style="margin-bottom: 30px; border-left: 5px solid #38bdf8; background: rgba(56, 189, 248, 0.05);">
                <h4 style="margin-top:0; color:#38bdf8;">🔬 THE PROJECT: AUTOMATED REASONING</h4>
                <p style="font-family: sans-serif; color:#cbd5e1; font-size: 0.9rem; line-height:1.6;">
                    This system automates the analysis of suspicious scripts by calculating <b>Shannon Entropy</b> (detecting hidden/encrypted code) and <b>Shell Funnel Execution</b> logic. It interprets raw forensic math through an AI Agent to provide instant SOC Tier-2 insights.
                </p>
            </div>

 <div class="trigger-box" onclick="launchGallery('malware', 0)">
                <img src="malware_thumb.png" alt="Malware Analysis Pipeline">
                <div class="trigger-footer">OPEN 8-STEP FORENSIC GALLERY ➔</div>
            </div>

<div class="grid">
                <div class="card">
                    <h4>📥 FORENSIC SCRIPT OUTPUT</h4>
                    <div class="terminal" style="color:#10b981">$ ./triage.sh elite_malware.sh
[!] ALERT: High Entropy Detected (7.84)
[!] ALERT: Execution Funnel detected (| sh)
[+] Result: Potential Obfuscated Shellcode</div>
                </div>
                <div class="card">
                    <h4>🤖 AI SENIOR ANALYST VERDICT</h4>
                    <div class="terminal" style="color:#38bdf8">🕵️ VERDICT: MALICIOUS
TYPE: Encrypted Reverse Shell
RISK: Critical. Attempting to bypass file-based detection via hex-encoding and direct piping.</div>
                </div>
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
    <div data-img="01.png" data-text="<b>Step 1: Baseline</b> - Monitoring SIEM state before alert."></div>
    <div data-img="02.png" data-text="<b>Step 2: Metrics</b> - Establishing normal traffic flow."></div>
    <div data-img="03.png" data-text="<b>Step 3: Log State</b> - Initial monitoring of auth logs."></div>
    <div data-img="04.png" data-text="<b>Step 4: Active Attack</b> - Attacker terminal during attempt."></div>
    <div data-img="05.png" data-text="<b>Step 5: Alert Spike</b> - Wazuh triggering critical Lvl 12 alerts."></div>
    <div data-img="06.png" data-text="<b>Step 6: Rule Filter</b> - Isolating Brute Force signatures."></div>
    <div data-img="07.png" data-text="<b>Step 7: Timeline</b> - Analyzing login attempt frequency."></div>
    <div data-img="08.png" data-text="<b>Step 8: Deep Dive</b> - Investigating auth.log details."></div>
    <div data-img="09.png" data-text="<b>Step 9: IP Extraction</b> - Identifying malicious source IP."></div>
    <div data-img="10.png" data-text="<b>Step 10: OSINT</b> - Verifying IP reputation on AbuseIPDB."></div>
    <div data-img="11.png" data-text="<b>Step 11: MITRE</b> - Mapping activity to T1110 (Brute Force)."></div>
    <div data-img="12.png" data-text="<b>Step 12: Preparation</b> - Drafting containment commands."></div>
    <div data-img="13.png" data-text="<b>Step 13: Mitigation</b> - Applying IPTables DROP to block attacker."></div>
</div>

<div id="data-store-agent">
    <div data-img="Soc_agent_1.png" data-text="<b>Agent Initialization:</b> Script loading Gemini 2.5-Flash and SOC context."></div>
    <div data-img="Soc_agent_2.png" data-text="<b>Log Processing:</b> Parsing raw SIEM JSON into structured analysis blocks."></div>
    <div data-img="Soc_agent_3.png" data-text="<b>Final Triage:</b> Generating automated investigation report and verdict."></div>
</div>

<div id="data-store-malware">
    <div data-img="malware_1.png" data-text="<b>Step 1: Initial Detection</b> - Wazuh FIM (File Integrity Monitoring) identifies new suspicious script."></div>
    <div data-img="malware_2.png" data-text="<b>Step 2: Forensic Execution</b> - Triggering the custom triage.sh bash script."></div>
    <div data-img="malware_3.png" data-text="<b>Step 3: Entropy Check</b> - Calculating Shannon Entropy to identify obfuscation levels."></div>
    <div data-img="malware_4.png" data-text="<b>Step 4: Funnel Analysis</b> - Scanning for direct pipes to shell interpreters (| bash, | sh)."></div>
    <div data-img="malware_5.png" data-text="<b>Step 5: Data Dispatch</b> - Python agent formatting forensic results into JSON for AI analysis."></div>
    <div data-img="malware_6.png" data-text="<b>Step 6: AI Reasoning</b> - Gemini API processing the entropy and funnel alerts."></div>
    <div data-img="malware_7.png" data-text="<b>Step 7: Threat Verdict</b> - AI confirms malicious intent and identifies the attack type."></div>
    <div data-img="malware_8.png" data-text="<b>Step 8: Remediation</b> - Automated output of containment steps for the SOC team."></div>
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
