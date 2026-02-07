---
layout: null
---
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Arivazhagan | SOC Analyst</title>
    <style>
        /* This forces the background to cover the screen even if GitHub is being slow */
        html, body {
            margin: 0;
            padding: 0;
            width: 100%;
            height: 100%;
            background-color: #0a0e14; /* Fallback color */
        }

 .hero-section {
            position: relative;
            width: 100%;
            height: 100vh;
            /* We are using a direct link here to prove the code works */
            background-image: linear-gradient(rgba(0,0,0,0.7), rgba(0,0,0,0.7)), url('https://images.unsplash.com/photo-1550751827-4bd374c3f58b?auto=format&fit=crop&w=1920&q=80');
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
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

.text-side h1 {
            font-size: 5rem;
            margin: 0;
            text-transform: uppercase;
        }

.text-side .role {
            font-size: 2rem;
            color: #00d4ff;
            display: block;
            margin-bottom: 20px;
        }

.contact-info {
            font-size: 1.1rem;
        }

.contact-info span { margin-right: 30px; }

.photo-side img {
            width: 300px; /* Big photo */
            height: 300px;
            border-radius: 50%;
            border: 4px solid #00d4ff;
            object-fit: cover;
        }

@media (max-width: 800px) {
            .container { flex-direction: column-reverse; text-align: center; }
            .text-side h1 { font-size: 3rem; }
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
                    <span><strong>LinkedIn:</strong> <a href="https://linkedin.com/in/arivazhagan" style="color:#00d4ff;">Click Here</a></span>
                </div>
            </div>
            <div class="photo-side">
                <img src="my-photo.jpg" alt="Profile Photo">
            </div>
        </div>
    </div>

</body>
</html>
