---
layout: null
---
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Arivazhagan | SOC Analyst</title>
    <style>
        html, body {
            margin: 0;
            padding: 0;
            width: 100%;
            height: 100%;
            background-color: #0a0e14;
        }

.hero-section {
            position: relative;
            width: 100%;
            height: 100vh;
            /* Using your file name: cyber-bg.jpg */
            background-image: linear-gradient(rgba(0,0,0,0.6), rgba(0,0,0,0.6)), url('cyber-bg.jpg');
            background-size: cover;
            background-position: center;
            background-repeat: no-repeat;
            display: flex;
            align-items: center;
            justify-content: center;
            font-family: 'Segoe UI', Arial, sans-serif;
            color: white;
        }

.container {
            width: 85%;
            max-width: 1200px;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

 .text-side {
            flex: 1;
        }

.text-side h1 {
            font-size: 5.5rem;
            margin: 0;
            text-transform: uppercase;
            font-weight: 900;
            letter-spacing: -2px;
        }

.text-side .role {
            font-size: 2.2rem;
            color: #38bdf8;
            display: block;
            margin: 5px 0 30px 0;
        }

.contact-info {
            font-size: 1.2rem;
        }

.contact-info span { 
            margin-right: 35px; 
        }

.contact-info a { 
            color: #38bdf8; 
            text-decoration: none; 
            font-weight: bold; 
        }

/* BIG PROFILE PHOTO */
        .photo-side img {
            width: 320px; 
            height: 320px;
            border-radius: 50%;
            border: 5px solid #38bdf8;
            object-fit: cover;
            box-shadow: 0 0 50px rgba(56, 189, 248, 0.4);
        }

@media (max-width: 900px) {
    .container { flex-direction: column-reverse; text-align: center; }
            .text-side h1 { font-size: 3.5rem; }
            .photo-side img { width: 200px; height: 200px; margin-bottom: 20px; }
            .contact-info span { display: block; margin: 10px 0; }
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
            </div>
 <div class="photo-side">
                <img src="Screenshot_20260103_200618_Gallery.jpg" alt="Arivazhagan">
            </div>
        </div>
    </div>

</body>
</html>
