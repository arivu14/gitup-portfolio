<div class="gallery-container">
  <img class="gallery-item" src="01.png" alt="Overview: High-Level Threat Dashboard" onclick="openModal(0)">
  <img class="gallery-item" src="02.png" alt="Security Posture: Severity & Auth Trends" onclick="openModal(1)">
  <img class="gallery-item" src="03.png" alt="The Success/Failure Narrative" onclick="openModal(2)">
  <img class="gallery-item" src="04.png" alt="Simulation: Initiating Terminal Attack" onclick="openModal(3)">
  <img class="gallery-item" src="06.png" alt="Recovery: Fixing Corrupted ossec.conf" onclick="openModal(4)">
  <img class="gallery-item" src="07.png" alt="24-Hour Metrics: 1379 Security Events" onclick="openModal(5)">
  <img class="gallery-item" src="08.png" alt="Rule 5710: Non-Existing User Probing" onclick="openModal(6)">
  <img class="gallery-item" src="09.png" alt="Rule 5712: Brute Force Threshold Trigger" onclick="openModal(8)">
  <img class="gallery-item" src="010.png" alt="Attacker Identification: Source IP 141.98.81.37" onclick="openModal(9)">
  <img class="gallery-item" src="011.png" alt="OSINT: AbuseIPDB Intelligence Check" onclick="openModal(10)">
  <img class="gallery-item" src="012.png" alt="Mapping: MITRE ATT&CK Framework" onclick="openModal(11)">
  <img class="gallery-item" src="013.png" alt="Containment: Manual IPTables DROP Rule" onclick="openModal(12)">
  <img class="gallery-item" src="014.png" alt="Verification: Confirming Blocked Traffic" onclick="openModal(13)">
</div>

<div id="myModal" class="modal">
  <span class="close" onclick="closeModal()">&times;</span>
  <a class="prev" onclick="changeSlide(-1)">&#10094;</a>
  <a class="next" onclick="changeSlide(1)">&#10095;</a>
  
  <img class="modal-content" id="img01">
  
  <div id="caption-container">
    <div id="caption-title"></div>
    <div id="caption-text"></div>
  </div>
</div>

<script>
let currentSlideIndex = 0;
const images = document.getElementsByClassName("gallery-item");

// This array maps exactly to your 14 screenshots
const summaries = [
  "STAGE 1: Dashboard overview displaying active security threats and severity levels across the environment.",
  "STAGE 2: Analyzing the distribution of high-level alerts. This view highlights critical authentication anomalies.",
  "STAGE 3: The 'Success vs. Failure' story. Note the massive spike in failures compared to zero successful logins.",
  "STAGE 4: Executing a manual brute force attack from the attacker terminal to verify SIEM detection logic.",
  "STAGE 5: PROJECT STRUGGLE: Following a VM crash, the ossec.conf was corrupted (0 bytes). This shows the manual restoration of the Wazuh Agent connection.",
  "STAGE 6: 24-Hour Review: 1,379 total events captured. This includes 129 Level 12+ alerts and 13 successful (authorized) logins.",
  "STAGE 7: Rule 5710 Analysis. The SIEM detects a scanner attempting to guess usernames that do not exist on the Ubuntu system.",
  "STAGE 8: Deeper look at Rule 5710. The logs show the sshd service correctly identifying 'Invalid User' attempts.",
  "STAGE 9: Rule 5712 Alert. The high frequency of failed attempts triggered the 'Brute Force' threshold, escalating to Level 10.",
  "STAGE 10: Identifying the Adversary. Source IP 141.98.81.37 is flagged as the primary threat actor behind the brute force.",
  "STAGE 11: OSINT Investigation. AbuseIPDB results confirm the source IP is a known malicious bot with 100% abuse confidence.",
  "STAGE 12: Tactical Mapping. Applying the MITRE ATT&CK framework: Tactic TA0006 (Credential Access) & Technique T1110 (Brute Force).",
  "STAGE 13: MITIGATION. Manually implementing a DROP rule in IPTables to sever the attacker's connection to the server.",
  "STAGE 14: SUCCESS. Final verification in the terminal showing 0 packets reaching the server from the malicious source IP."
];

function openModal(index) {
  currentSlideIndex = index;
  document.getElementById("myModal").style.display = "block";
  updateModal();
}

function closeModal() {
  document.getElementById("myModal").style.display = "none";
}

function changeSlide(n) {
  currentSlideIndex += n;
  if (currentSlideIndex >= images.length) {currentSlideIndex = 0}
  if (currentSlideIndex < 0) {currentSlideIndex = images.length - 1}
  updateModal();
}

function updateModal() {
  const modalImg = document.getElementById("img01");
  const captionTitle = document.getElementById("caption-title");
  const captionText = document.getElementById("caption-text");
  
  modalImg.src = images[currentSlideIndex].src;
  captionTitle.innerHTML = images[currentSlideIndex].alt;
  captionText.innerHTML = summaries[currentSlideIndex];
}

// Close modal when clicking outside the image
window.onclick = function(event) {
  let modal = document.getElementById("myModal");
  if (event.target == modal) { closeModal(); }
}
</script>
