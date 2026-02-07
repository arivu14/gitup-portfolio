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
        /* STEP 1: Background and Overlay */
        body {
            /* Replace 'cyber-bg.jpg' with your chosen background image filename */
            background: #0a0e14 url('background.jpg') no-repeat center center fixed;
            background-size: cover;
            margin: 0;
            padding: 0;
            height: 100vh;
            display: flex;
            align-items: center;
            font-family: 'Segoe UI', Roboto, Helvetica, Arial, sans-serif;
            color: white;
            overflow: hidden;
        }

 /* Dark overlay to keep text professional and readable */
        body::before {
            content: "";
            position: fixed;
            top: 0; left: 0; width: 100%; height: 100%;
            background: rgba(0, 0, 0, 0.65); 
            z-index: -1;
        }

 /* STEP 2: The Two-Step Layout */
        .portfolio-wrapper {
            width: 85%;
            max-width: 1100px;
            margin: auto;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

 /* Left Side: Identity & Contact */
        .bio-info {
            flex: 1;
        }

.bio-info h1 {
            font-size: 4.5rem;
            margin: 0;
            font-weight: 700;
            letter-spacing: -1px;
            text-transform: uppercase;
        }

.bio-info .role {
            font-size: 1.8rem;
            color: #38bdf8; /* Sleek cyber blue */
            display: block;
            margin-bottom: 30px;
            font-weight: 400;
        }

.contact-row {
            font-size: 1.1rem;
            color: #e2e8f0;
        }

.contact-row span {
            margin-right: 40px;
        }

.contact-row a {
            color: #38bdf8;
            text-decoration: none;
            font-weight: 600;
            transition: 0.3s;
        }

.contact-row a:hover {
            color: white;
            text-decoration: underline;
        }

/* Right Side: Small Profile Photo */
        .profile-container {
            flex: 0 0 150px;
        }

.profile-container img {
            width: 150px; /* Small profile photo as requested */
            height: 150px;
            border-radius: 50%;
            border: 2px solid rgba(255, 255, 255, 0.2);
            object-fit: cover;
            box-shadow: 0 0 30px rgba(0, 0, 0, 0.5);
        }

 /* Mobile Responsiveness */
        @media (max-width: 768px) {
            .portfolio-wrapper {
                flex-direction: column-reverse;
                text-align: center;
            }
            .bio-info h1 { font-size: 3rem; }
            .profile-container { margin-bottom: 20px; }
            .contact-row span { display: block; margin: 10px 0; }
        }
    </style>
</head>
<body>

<div class="portfolio-wrapper">
        <div class="bio-info">
            <h1>Arivazhagan</h1>
            <span class="role">SOC Analyst L1</span>
            
<div class="contact-row">
                <span><strong>C.N:</strong> +91 6379944366</span>
                <span><strong>LinkedIn:</strong> <a href="https://linkedin.com/in/yourprofile" target="_blank">Click Here</a></span>
            </div>
        </div>

  <div class="profile-container">
            <img src="my-photo.jpg" alt="Arivazhagan">
        </div>
    </div>

</body>
</html>
