---
layout: default
title: SOC Lab Portfolio
---

# SOC Incident Report: Brute Force Analysis
**Analyst:** [Your Name] | **Status:** RESOLVED

<style>
/* 1. The Lightbox Background (Blur & Dim) */
.modal {
  display: none;
  position: fixed;
  z-index: 9999;
  padding-top: 30px;
  left: 0; top: 0;
  width: 100%; height: 100%;
  background-color: rgba(0,0,0,0.95);
  backdrop-filter: blur(12px);
  -webkit-backdrop-filter: blur(12px);
}

/* 2. The Pop-up Image */
.modal-content {
  margin: auto;
  display: block;
  max-width: 80%;
  max-height: 65vh;
  border: 2px solid #444;
  border-radius: 8px;
}

/* 3. Navigation & Close Buttons */
.close {
  position: absolute;
  top: 15px; right: 35px;
  color: #fff; font-size: 40px; font-weight: bold; cursor: pointer;
}

.prev, .next {
  cursor: pointer;
  position: absolute;
  top: 40%;
  width: auto;
  padding: 16px;
  color: white;
  font-weight: bold;
  font-size: 40px;
  user-select: none;
  text-decoration: none;
  background: rgba(255,255,255,0.1);
  border-radius: 50%;
}

.next { right: 3%; }
.prev { left: 3%; }

/* 4. The Summary Box below the Image */
#caption-container {
  margin: auto;
  width: 70%;
  text-align: center;
  color: white;
  padding: 20px;
  background: rgba(255,255,255,0.05);
  border-radius: 10px;
  margin-top: 15px;
}

#caption-title { font-size: 22px; font-weight: bold; color: #007bff; margin-bottom: 5px; }
#caption-text { font-size: 16px; line-height: 1.5; color: #ddd; }

/* 5. Horizontal Slider Styling */
.gallery-container {
  display: flex;
  overflow-x: auto;
  gap: 15px;
  padding: 20px;
  background: #1e1e1e;
  border-radius: 10px;
}

.gallery-item {
  flex: 0 0 250px;
  height: 150px;
  object-fit: cover;
  cursor: pointer;
  border-radius: 6px;
  opacity: 0.8;
  transition: 0.3s;
}

.gallery-item:hover { opacity: 1; transform: translateY(-5px); }
</style>

## Brute Force Attack Evidence (8 Stages)
*Click a screenshot to analyze the evidence. The background will blur, and a detailed summary will appear below the image.*

<div class="gallery-container">
  <img class="gallery-item" src="BF_1.png" alt="1. Initial Dashboard Alert" onclick="openModal(0)">
  <img class="gallery-item" src="BF_2.png" alt="2. Email Header Analysis" onclick="openModal(1)">
  <img class="gallery-item" src="BF_3.png" alt="3. Source IP Identification" onclick="openModal(2)">
  <img class="gallery-item" src="BF_4.png" alt="4. Rule 5712 Log Breakdown" onclick="openModal(3)">
  <img class="gallery-item" src="BF_5.png" alt="5. Authentication Failure Spikes" onclick="openModal(4)">
  <img class="gallery-item" src="BF_6.png" alt="6. User Account Targeted" onclick="openModal(5)">
  <img class="gallery-item" src="BF_7.png" alt="7. Persistence Mechanism Identified" onclick="openModal(6)">
  <img class="gallery-item" src="BF_8.png" alt="8. Successful Mitigation Log" onclick="openModal(7)">
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

// --- ADD YOUR SUMMARIES HERE ---
const summaries = [
  "Initial spike in failed logins detected on the main Wazuh dashboard. High volume of Rule 5712 alerts observed within a short window.",
  "Detailed analysis of the phishing email headers reveals the true source IP and the spoofing technique used to bypass filters.",
  "Isolated the malicious Source IP: 10.48.156.247. Cross-referencing logs confirms this IP is responsible for 100% of the failed SSH attempts.",
  "Breakdown of Rule ID 5712. This rule triggered 69 times, indicating a sustained brute force attempt against the administrative account.",
  "Visualizing the timeline of failures. The attacker attempted access every 10 minutes to avoid triggering immediate account lockouts.",
  "Identified the specific target username: 'root'. The attacker is attempting to gain the highest level of privilege on the system.",
  "Detection of a successful login followed by a 'useradd' command. The attacker created 'persistence_user' to maintain access.",
  "Final mitigation logs. Shows the blocking of the attacker's IP at the firewall and the manual deletion of the backdoor account."
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

window.onclick = function(event) {
  let modal = document.getElementById("myModal");
  if (event.target == modal) { closeModal(); }
}
</script>
