---
layout: null
---
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Arivazhagan | SOC Analyst</title>
    <style>
        /* RESET & BASE */
        * { box-sizing: border-box; }
        html, body {
            margin: 0;
            padding: 0;
            width: 100%;
            background-color: #0a0e14;
            color: white;
            font-family: 'Segoe UI', Arial, sans-serif;
        }

 /* THE HERO SECTION */
        .hero-section {
            position: relative;
            width: 100%;
            min-height: 100vh;
            background: linear-gradient(rgba(0,0,0,0.7), rgba(0,0,0,0.7)), url('cc.jpg');
            background-size: cover;
            background-position: center;
            background-attachment: fixed;
            display: flex;
            align-items: center;
            justify-content: center;
        }

 .container {
            width: 85%;
            max-width: 1200px;
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 40px 0;
        }
.text-side { flex: 1; padding-right: 50px; }
        .text-side h1 {
            font-size: 5rem;
            margin: 0;
            text-transform: uppercase;
            font-weight: 900;
            letter-spacing: -2px;
        }

.text-side .role {
           font-size: 2rem;
            color: #38bdf8;
            display: block;
            margin: 5px 0 20px 0;
        }

 .contact-info { font-size: 1.1rem; margin-bottom: 30px; }
        .contact-info span { margin-right: 35px; }
        .contact-info a { color: #38bdf8; text-decoration: none; font-weight: bold; }

 /* NEW: QUICK SUMMARY BOX */
        .quick-summary {
            background: rgba(56, 189, 248, 0.1);
            border-left: 4px solid #38bdf8;
            padding: 20px;
            border-radius: 4px;
            backdrop-filter: blur(10px);
            max-width: 600px;
        }

 .quick-summary h3 {
            margin: 0 0 10px 0;
            font-size: 1.2rem;
            color: #38bdf8;
            text-transform: uppercase;
        }

 .quick-summary p {
            margin: 0;
            font-size: 1rem;
            line-height: 1.5;
            color: #cbd5e1;
        }

.photo-side img {
            width: 320px; 
            height: 320px;
            border-radius: 50%;
            border: 5px solid #38bdf8;
            object-fit: cover;
            box-shadow: 0 0 50px rgba(56, 189, 248, 0.4);
        }

/* INCIDENT REPORTS SECTION */
        .reports-container {
            background: #0f172a;
            padding: 80px 0;
            display: flex;
            flex-direction: column;
            align-items: center;
        }

.report-grid {
            width: 85%;
            max-width: 1200px;
        }

.report-card {
            background: rgba(255, 255, 255, 0.03);
            border: 1px solid rgba(56, 189, 248, 0.2);
            padding: 30px;
            margin-bottom: 40px;
            border-radius: 12px;
        }

.report-card h2 { color: #38bdf8; margin-top: 0; }
.report-card .meta { color: #94a3b8; font-size: 0.9rem; margin-bottom: 15px; display: block; }
.report-card p { line-height: 1.6; color: #cbd5e1; }
        
.report-card img {
            width: 100%;
            max-width: 850px;
            margin-top: 25px;
            border-radius: 8px;
            border: 1px solid #334155;
        }

@media (max-width: 900px) {
            .container { flex-direction: column-reverse; text-align: center; }
            .text-side { padding-right: 0; }
            .text-side h1 { font-size: 3.5rem; }
            .photo-side img { width: 220px; height: 220px; margin-bottom: 30px; }
            .quick-summary { margin: 0 auto; text-align: left; }
        }
    </style>
</head>
<body>

<div class="hero-section">
        <div class="container">
            <div class="text-side">
                <h1>ARIVAZHAGAN</h1>
                <span class="role">SOC Analyst L1</span>
                
 <div class="contact-info">
                    <span><strong>C.N:</strong> +91 6379944366</span>
                    <span><strong>LinkedIn:</strong> <a href="https://linkedin.com/in/arivazhagan" target="_blank">Click Here</a></span>
                </div>

<div class="quick-summary">
                    <h3>Latest Incident Response</h3>
                    <p>
                        Detected and mitigated a <strong>Level 10 Critical SSH Brute Force attack</strong> using Wazuh SIEM. 
                        Identified malicious botnet activity via AbuseIPDB and executed emergency containment 
                        through host-based firewall (IPTables) to secure Ubuntu Agent 004.
                    </p>
                </div>
            </div>

 <div class="photo-side">
                <img src="Screenshot_20260103_200618_Gallery.jpg" alt="Arivazhagan">
            </div>
        </div>
    </div>

 <div class="reports-container">
        <div class="report-grid">
            <h1 style="color:white; border-bottom: 3px solid #38bdf8; padding-bottom: 10px; margin-bottom: 50px;">Incident Report Analysis</h1>
            
<div class="report-card">
                <span class="meta">February 06, 2026 | Target: Ubuntu Linux</span>
                <h2>SSH Brute Force Detection & Response</h2>
                <p>
                    <strong>The Attack:</strong> Malicious source IP (141.98.81.37) attempted to gain access to the system via brute force, triggering Wazuh Rule 5712. <br><br>
                    <strong>Analysis:</strong> Verified 0 successful logins via SIEM dashboards. PIVOTED to AbuseIPDB which confirmed 100% abuse confidence for the source IP.<br><br>
                    <strong>The Fix:</strong> Executed emergency containment via IPTables (DROP) and verified Ground Truth via Linux CLI. 
                    Successfully mapped to <i>MITRE ATT&CK: Brute Force (T1110)</i>.
                </p>
                <img src="brute-force-screenshot.jpg" alt="Wazuh Brute Force Alert">
            </div>

 </div>
 </div>

</body>
</html>
