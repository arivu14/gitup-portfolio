---
layout: default
title: SOC Lab Portfolio
---

# SOC Incident Report: Brute Force Analysis
**Analyst:** [Arivazhagan] | **Status:** RESOLVED

<style>
/* 1. The Lightbox Background (Blur & Dim) */
.modal {
  display: none;
  position: fixed;
  z-index: 9999;
  padding-top: 50px;
  left: 0; top: 0;
  width: 100%; height: 100%;
  background-color: rgba(0,0,0,0.9);
  backdrop-filter: blur(10px);
  -webkit-backdrop-filter: blur(10px);
}

/* 2. The Pop-up Image */
.modal-content {
  margin: auto;
  display: block;
  max-width: 85%;
  max-height: 80vh;
  border: 3px solid #fff;
  border-radius: 5px;
  box-shadow: 0px 0px 20px rgba(255,255,255,0.2);
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
  top: 50%;
  width: auto;
  padding: 16px;
  margin-top: -50px;
  color: white;
  font-weight: bold;
  font-size: 40px;
  transition: 0.6s ease;
  user-select: none;
  text-decoration: none;
}

.next { right: 5%; }
.prev { left: 5%; }

/* 4. Horizontal Slider Styling */
.gallery-container {
  display: flex;
  overflow-x: auto;
  gap: 15px;
  padding: 20px;
  background: #1e1e1e;
  border-radius: 10px;
  border: 1px solid #333;
}

.gallery-item {
  flex: 0 0 280px;
  height: 180px;
  object-fit: cover;
  cursor: pointer;
  border-radius: 6px;
  border: 2px solid transparent;
  transition: 0.3s;
}

.gallery-item:hover {
  border-color: #007bff;
  transform: scale(1.02);
}

#caption {
  text-align: center;
  color: #ccc;
  margin-top: 20px;
  font-size: 20px;
}
</style>

## Brute Force Attack Evidence (8 Stages)
*Click any screenshot to open the Interactive Lightbox. Use the arrows to navigate through the 8 stages of the attack.*

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
  <div id="caption"></div>
</div>

<script>
let currentSlideIndex = 0;
const images = document.getElementsByClassName("gallery-item");

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
  const captionText = document.getElementById("caption");
  modalImg.src = images[currentSlideIndex].src;
  captionText.innerHTML = images[currentSlideIndex].alt;
}

// Close if user clicks background
window.onclick = function(event) {
  let modal = document.getElementById("myModal");
  if (event.target == modal) { closeModal(); }
}
</script>
