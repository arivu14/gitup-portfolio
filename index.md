---
layout: null
---
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Arivazhagan | SOC Analyst Portfolio</title>
    <style>
        /* FULL BACKGROUND SETUP */
        body {
            /* This MUST match your file name: cyber-bg.jpg */
            background: #0a0e14 url('cyber-bg.jpg') no-repeat center center fixed;
            background-size: cover;
            margin: 0;
            padding: 0;
            height: 100vh;
            display: flex;
            align-items: center;
            font-family: 'Segoe UI', Arial, sans-serif;
            color: white;
            overflow: hidden;
        }

/* Dark professional overlay */
        body::before {
            content: "";
            position: fixed;
            top: 0; left: 0; width: 100%; height: 100%;
            background: rgba(0, 0, 0, 0.7); 
            z-index: -1;
        }

.container {
            width: 85%;
            max-width: 1200px;
            margin: auto;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

/* Left side: Text Details */
        .text-content {
            flex: 1;
        }

 .text-content h1 {
            font-size: 5rem;
            margin: 0;
            font-weight: 800;
            text-transform: uppercase;
            letter-spacing: -2px;
        }

.text-content .role {
            font-size: 2.2rem;
            color: #38bdf8; 
            display: block;
            margin-bottom: 30px;
        }

.contact-line {
            font-size: 1.2rem;
        }

.contact-line span {
            margin-right: 40px;
        }

.contact-line a {
            color: #38bdf8;
            text-decoration: none;
            font-weight: bold;
        }

/* Right side: LARGE Profile Photo */
        .photo-side {
            flex: 0 0 300px; 
        }

.photo-side img {
            width: 300px; /* Big size as requested */
            height: 300px;
            border-radius: 50%;
            border: 4px solid #38bdf8;
            object-fit: cover;
            box-shadow: 0 0 50px rgba(56, 189, 248, 0.5);
        }

/* Mobile responsiveness */
        @media (max-width: 900px) {
            .container { flex-direction: column-reverse; text-align: center; }
            .text-content h1 { font-size: 3.5rem; }
            .photo-side { margin-bottom: 40px; }
            .contact-line span { display: block; margin: 10px 0; }
        }
    </style>
</head>
<body>

<div class="container">
        <div class="text-content">
            <h1>Arivazhagan</h1>
            <span class="role">SOC Analyst L1</span>
            
<div class="contact-line">
                <span><strong>C.N:</strong> +91 6379944366</span>
                <span><strong>LinkedIn:</strong> <a href="https://linkedin.com/in/arivazhagan" target="_blank">Click Here</a></span>
            </div>
        </div>

 <div class="photo-side">
            <img src="my-photo.jpg" alt="Arivazhagan Profile">
        </div>
    </div>

</body>
</html>
