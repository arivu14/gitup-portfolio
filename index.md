---
layout: default
title: SOC Lab Portfolio
---

<style>
/* Grid Layout for Evidence */
.evidence-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  gap: 25px;
  margin-top: 30px;
}

/* Individual Card Styling */
.evidence-card {
  background: #1e1e1e;
  border: 1px solid #333;
  border-radius: 12px;
  overflow: hidden;
  transition: transform 0.3s ease, border-color 0.3s ease;
  cursor: pointer;
  position: relative;
}

.evidence-card:hover {
  transform: translateY(-5px);
  border-color: #007bff;
}

.evidence-card img {
  width: 100%;
  height: 200px;
  object-fit: cover;
  border-bottom: 1px solid #333;
}

/* The Summary Box (Hidden by default) */
.evidence-summary {
  padding: 15px;
  background: #252525;
  color: #ddd;
  font-size: 14px;
  line-height: 1.6;
  display: none; /* This is the key - it pops up on click */
  border-top: 2px solid #007bff;
  animation: fadeIn 0.4s ease forwards;
}

.evidence-title {
  padding: 12px;
  font-weight: bold;
  color: #007bff;
  text-align: center;
  background: #1a1a1a;
}

@keyframes fadeIn {
  from { opacity: 0; transform: translateY(10px); }
  to { opacity: 1; transform: translateY(0); }
}

/* Active State for clicked cards */
.evidence-card.active {
  border-color: #28a745;
}

.evidence-card.active .evidence-summary {
  display: block;
}
</style>

# SOC Incident Report: Brute Force Analysis
*Click any screenshot below to reveal the analyst notes and investigation details.*

<div class="evidence-grid">

  <div class="evidence-card" onclick="this.classList.toggle('active')">
    <img src="01.png" alt="Threat Dashboard">
    <div class="evidence-title">1. Security Posture Overview</div>
    <div class="evidence-summary">
      <b>Analyst Note:</b> Initial monitoring of the Wazuh Dashboard. This screen captures the baseline security posture before the attack began, showing general system health and agent status.
    </div>
  </div>

  <div class="evidence-card" onclick="this.classList.toggle('active')">
    <img src="04.png" alt="Terminal Attack">
    <div class="evidence-title">4. Manual Attack Simulation</div>
    <div class="evidence-summary">
      <b>The Struggle:</b> During this phase, the VMware environment crashed, corrupting the <i>ossec.conf</i> file (0 bytes). I had to manually recover the agent configuration and re-establish the manager handshake before the attack could be logged.
    </div>
  </div>

  <div class="evidence-card" onclick="this.classList.toggle('active')">
    <img src="06.png" alt="24hr Dashboard">
    <div class="evidence-title">6. 24-Hour Event Aggregation</div>
    <div class="evidence-summary">
      <b>Findings:</b> A total of 1,379 events were captured. Statistics show 129 Level 12+ alerts, 85 authentication failures, and 13 successful logins (authorized). This volume confirms a persistent brute-force attempt.
    </div>
  </div>

  <div class="evidence-card" onclick="this.classList.toggle('active')">
    <img src="09.png" alt="Rule 5712">
    <div class="evidence-title">9. Rule 5712: Brute Force Trigger</div>
    <div class="evidence-summary">
      <b>Detection:</b> Wazuh Rule 5712 fired after detecting multiple failed SSH attempts in a short window. This confirms the system successfully identified the automated nature of the attack.
    </div>
  </div>

  <div class="evidence-card" onclick="this.classList.toggle('active')">
    <img src="011.png" alt="AbuseIPDB">
    <div class="evidence-title">11. AbuseIPDB Intelligence</div>
    <div class="evidence-summary">
      <b>OSINT:</b> Cross-referenced the attacker's IP with AbuseIPDB. The IP was flagged with a 100% Abuse Confidence Score, confirming it as a known malicious bot scanning for open SSH ports.
    </div>
  </div>

  <div class="evidence-card" onclick="this.classList.toggle('active')">
    <img src="013.png" alt="IP Block">
    <div class="evidence-title">13. Containment: IP Block</div>
    <div class="evidence-summary">
      <b>Mitigation:</b> To stop the attack, I manually executed <code>sudo iptables -I INPUT -s [IP] -j DROP</code>. This immediately severed the connection between the attacker and the target server.
    </div>
  </div>

</div>

<script>
// Logic to ensure only one card is expanded at a time (Optional)
const cards = document.querySelectorAll('.evidence-card');
cards.forEach(card => {
  card.addEventListener('click', () => {
    cards.forEach(c => { if(c !== card) c.classList.remove('active'); });
  });
});
</script>
