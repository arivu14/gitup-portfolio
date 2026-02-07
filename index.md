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
        /* BASE & HERO STYLES */
        * { box-sizing: border-box; }
        html, body { margin: 0; padding: 0; width: 100%; background-color: #0a0e14; color: white; font-family: 'Segoe UI', Arial, sans-serif; }
        
/* Blur class for background when modal is open */
        .blur { filter: blur(8px); pointer-events: none; transition: 0.3s; }
        
.hero-section {
            width: 100%; min-height: 100vh;
            background: linear-gradient(rgba(0,0,0,0.7), rgba(0,0,0,0.7)), url('cc.jpg');
            background-size: cover; background-position: center; display: flex; align-items: center; justify-content: center;
        }

 /* LIGHTBOX MODAL STYLES */
        .modal {
            display: none; position: fixed; z-index: 1000; left: 0; top: 0;
            width: 100%; height: 100%; background-color: rgba(0,0,0,0.9);
            align-items: center; justify-content: center; flex-direction: column;
        }

.modal-content {
            position: relative; max-width: 80%; max-height: 70%;
            display: flex; align-items: center; justify-content: center;
        }

.modal-content img {
            width: 100%; height: auto; border: 2px solid #38bdf8; border-radius: 8px;
        }

.caption-container {
            margin-top: 20px; color: #cbd5e1; text-align: center;
            max-width: 70%; line-height: 1.6; font-size: 1.1rem;
        }

/* NAVIGATION BUTTONS */
        .prev, .next {
            cursor: pointer; position: absolute; top: 50%; width: auto;
            padding: 16px; margin-top: -50px; color: #38bdf8; font-weight: bold;
            font-size: 40px; transition: 0.6s ease; border-radius: 0 3px 3px 0;
            user-select: none; text-decoration: none;
        }
.next { right: -100px; border-radius: 3px 0 0 3px; }
.prev { left: -100px; }
.prev:hover, .next:hover { color: white; }

 .close {
            position: absolute; top: 20px; right: 35px; color: #f1f1f1;
            font-size: 40px; font-weight: bold; cursor: pointer;
        }

/* REPORT THUMBNAILS */
        .reports-container { background: #0f172a; padding: 80px 0; text-align: center; }
        .report-grid {
            display: grid; grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
            gap: 20px; width: 85%; max-width: 1200px; margin: 0 auto;
        }

.thumb {
            cursor: pointer; border-radius: 8px; border: 2px solid transparent;
            transition: 0.3s; width: 100%; height: 150px; object-fit: cover;
        }
.thumb:hover { border-color: #38bdf8; transform: scale(1.05); }

/* HEADER TEXT STYLES (Same as before) */
        .text-side h1 { font-size: 5rem; margin: 0; text-transform: uppercase; font-weight: 900; }
        .text-side .role { font-size: 2rem; color: #38bdf8; display: block; margin: 5px 0 20px 0; }
        .contact-info a { color: #38bdf8; text-decoration: none; font-weight: bold; }
        .photo-side img { width: 320px; height: 320px; border-radius: 50%; border: 5px solid #38bdf8; object-fit: cover; }
    </style>
</head>
<body>

<div id="main-content">
    <div class="hero-section">
        <div class="container" style="display:flex; width:85%; max-width:1200px; justify-content:space-between; align-items:center;">
            <div class="text-side">
                <h1>ARIVAZHAGAN</h1>
                <span class="role">SOC Analyst L1</span>
                <div class="contact-info">
                    <span><strong>C.N:</strong> +91 6379944366</span> | 
                    <span><strong>LinkedIn:</strong> <a href="#" target="_blank">Click Here</a></span>
                </div>
            </div>
            <div class="photo-side">
                <img src="Screenshot_20260103_200618_Gallery.jpg" alt="Arivazhagan">
            </div>
        </div>
    </div>

<div class="reports-container">
        <h1 style="border-bottom: 3px solid #38bdf8; display:inline-block; padding-bottom:10px; margin-bottom:50px;">Incident Report Evidence</h1>
        <div class="report-grid">
            <img class="thumb" src="s1.png" onclick="openModal();currentSlide(1)" alt="Report 1: Initial detection of the malicious transaction via SIEM dashboard.">
            <img class="thumb" src="s2.png" onclick="openModal();currentSlide(2)" alt="Report 2: Full email body text analysis identifying the fake merchant address.">
            </div>
    </div>
</div>

<div id="myModal" class="modal">
    <span class="close" onclick="closeModal()">&times;</span>
    <div class="modal-content">
        <img id="modal-img">
        <a class="prev" onclick="plusSlides(-1)">&#10094;</a>
        <a class="next" onclick="plusSlides(1)">&#10095;</a>
    </div>
    <div class="caption-container">
        <p id="caption"></p>
    </div>
</div>

<script>
    let slideIndex = 1;
    const images = document.getElementsByClassName("thumb");

    function openModal() {
        document.getElementById("myModal").style.display = "flex";
        document.getElementById("main-content").classList.add("blur");
    }

    function closeModal() {
        document.getElementById("myModal").style.display = "none";
        document.getElementById("main-content").classList.remove("blur");
    }

    function currentSlide(n) {
        showSlides(slideIndex = n);
    }

    function plusSlides(n) {
        showSlides(slideIndex += n);
    }

    function showSlides(n) {
        if (n > images.length) {slideIndex = 1}
        if (n < 1) {slideIndex = images.length}
        
        let modalImg = document.getElementById("modal-img");
        let captionText = document.getElementById("caption");
        
        modalImg.src = images[slideIndex-1].src;
        captionText.innerHTML = images[slideIndex-1].alt;
    }
</script>

</body>
</html>
