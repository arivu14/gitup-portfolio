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
        /* STEP 1: FIXED FULL BACKGROUND */
        body {
            /* Make sure the image file in your GitHub is exactly named 'cyber-bg.jpg' */
            background: #0a0e14 url('cyber-bg.jpg') no-repeat center center fixed;
            background-size: cover;
            margin: 0;
            padding: 0;
            height: 100vh;
            display: flex;
            align-items: center;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            color: white;
            overflow: hidden;
        }

 /* Darkening overlay for professional contrast */
        body::before {
            content: "";
            position: fixed;
            top: 0; left: 0; width: 100%; height: 100%;
            background: rgba(0, 0, 0, 0.7); 
            z-index: -1;
        }

/* STEP 2: TWO-STEP LAYOUT */
        .main-wrapper {
            width: 85%;
            max-width: 1200px;
            margin: auto;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

/* Left Content: Identity */
        .bio-section {
            flex: 1;
        }

.bio-section h1 {
            font-size: 4.8rem;
            margin: 0;
            font-weight: 800;
            text-transform: uppercase;
            letter-spacing: -2px;
        }

.bio-section .role-title {
            font-size: 2rem;
            color: #38bdf8; /* Cyber Blue */
            display: block;
            margin-bottom: 35px;
            font-weight: 500;
        }

/* Single Line Contact Info */
        .contact-details {
            font-size: 1.2rem;
            color: #f1f5f9;
        }

.contact-details span {
            margin-right: 40px;
        }

.contact-details a {
            color: #38bdf8;
            text-decoration: none;
            font-weight: bold;
            border-bottom: 2px solid transparent;
            transition: 0.3s;
        }

.contact-details a:hover {
            border-bottom: 2px solid #38bdf8;
        }

/* Right Content: Profile Picture (Increased Size) */
        .photo-box {
            flex: 0 0 220px; /* Bigger container */
        }

.photo-box img {
            width: 220px; /* Larger size as requested */
            height: 220px;
            border-radius: 50%;
            border: 3px solid #38bdf8;
            object-fit: cover;
            box-shadow: 0 0 40px rgba(56, 189, 248, 0.4);
        }

/* Responsive Fix for Mobile */
        @media (max-width: 850px) {
            .main-wrapper {
                flex-direction: column-reverse;
                text-align: center;
            }
.bio-section h1 { font-size: 3.5rem; }
            .photo-box { margin-bottom: 30px; }
            .contact-details span { display: block; margin: 15px 0; }
        }
    </style>
</head>
<body>

<div class="main-wrapper">
        <div class="bio-section">
            <h1>Arivazhagan</h1>
            <span class="role-title">SOC Analyst L1</span>
            
<div class="contact-details">
                <span><strong>C.N:</strong> +91 6379944366</span>
                <span><strong>LinkedIn:</strong> <a href="https://linkedin.com/in/arivazhagan" target="_blank">Click Here</a></span>
            </div>
        </div>

<div class="photo-box">
            <img src="my-photo.jpg" alt="Arivazhagan">
        </div>
    </div>

</body>
</html>
