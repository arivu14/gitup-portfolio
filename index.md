---
layout: default
title: SOC Lab Portfolio
---

<style>
/* 1. The Horizontal Evidence Strip */
.evidence-container {
  display: flex;
  flex-wrap: nowrap;
  overflow-x: auto;
  gap: 20px;
  padding: 20px;
  background: #121212;
  border-radius: 12px;
}

.evidence-item {
  flex: 0 0 250px;
  text-align: center;
  transition: 0.3s;
}

.evidence-item img {
  width: 100%;
  border-radius: 8px;
  border: 2px solid #333;
  cursor: pointer;
  transition: transform 0.3s ease;
}

/* When active, the image highlights */
.evidence-item.active img {
  border-color: #007bff;
  transform: scale(1.05);
}

/* 2. The Pop-Up Summary Box (Appears directly below the clicked image) */
.detail-popup {
  display: none;
  margin-top: 15px;
  padding: 15px;
  background: rgba(30, 30, 30, 0.95);
  border: 1px solid #007bff;
  border-radius: 8px;
  color: #ddd;
  text-align: left;
  font-size: 14px;
  box-shadow: 0 4px 15px rgba(0,0,0,0.5);
  animation: slideDown 0.3s ease-out;
}

@keyframes slideDown {
  from { opacity: 0; transform: translateY(-10px); }
  to { opacity: 1; transform: translateY(0); }
}

/* Blur effect for the rest of the section when clicking */
.blurred { filter: blur(4px); pointer-events: none; }
</style>

# SOC Incident Report: Brute Force Analysis
*Scroll horizontally to view the 14 stages. Click any image to reveal the analyst notes.*

<div id="master-container" class="evidence-container">

  <div class="evidence-item" id="item-1">
    <img src="01.png" onclick="toggleDetails(1)">
    <div id="detail-1" class="detail-popup">
      <strong style="color:#007bff;">1. Security Overview</strong><br>
      Initial dashboard view displaying high-level threat metrics and the current security posture of Agent 004.
    </div>
  </div>

  <div class="evidence-item" id="item-4">
    <img src="04.png" onclick="toggleDetails(4)">
    <div id="detail-4" class="detail-popup">
      <strong style="color:#007bff;">4. The Struggle: VM Crash</strong><br>
      Following a VMware crash, the ossec.conf was corrupted (0 bytes). Documenting the manual recovery of the Wazuh Agent connection.
    </div>
  </div>

  <div class="evidence-item" id="item-6">
    <img src="06.png" onclick="toggleDetails(6)">
    <div id="detail-6" class="detail-popup">
      <strong style="color:#007bff;">6. 24-Hour Metrics</strong><br>
      Dashboard stats: 1,379 events detected, including 129 Level 12+ alerts, 85 auth failures, and 13 successful logins.
    </div>
  </div>

  <div class="evidence-item" id="item-9">
    <img src="09.png" onclick="toggleDetails(9)">
    <div id="detail-9" class="detail-popup">
      <strong style="color:#007bff;">9. Rule 5712: Brute Force</strong><br>
      Wazuh detection of multiple authentication failures meeting the high-frequency brute force threshold.
    </div>
  </div>

  <div class="evidence-item" id="item-11">
    <img src="011.png" onclick="toggleDetails(11)">
    <div id="detail-11" class="detail-popup">
      <strong style="color:#007bff;">11. OSINT: AbuseIPDB</strong><br>
      Intelligence verification showing 141.98.81.37 as a 100% Abuse Confidence malicious bot.
    </div>
  </div>

  <div class="evidence-item" id="item-13">
    <img src="013.png" onclick="toggleDetails(13)">
    <div id="detail-13" class="detail-popup">
      <strong style="color:#007bff;">13. Mitigation: IP Block</strong><br>
      Containment action: Manually implemented a DROP rule via IPTables to terminate the attacker's access.
    </div>
  </div>

  </div>

<script>
function toggleDetails(id) {
  // Hide all other open popups first
  const allPopups = document.querySelectorAll('.detail-popup');
  const allItems = document.querySelectorAll('.evidence-item');
  
  allPopups.forEach(p => p.style.display = 'none');
  allItems.forEach(i => i.classList.remove('active'));

  // Show the specific detail for the clicked image
  const targetDetail = document.getElementById('detail-' + id);
  const targetItem = document.getElementById('item-' + id);
  
  targetDetail.style.display = 'block';
  targetItem.classList.add('active');
}
</script>
