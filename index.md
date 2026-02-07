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
        body {
            /* TEST IMAGE: Using an external URL to verify the background logic works */
            background: #0a0e14 url('https://images.unsplash.com/photo-1550751827-4bd374c3f58b?auto=format&fit=crop&w=1920&q=80') no-repeat center center fixed;
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

 body::before {
            content: "";
            position: fixed;
            top: 0; left: 0; width: 100%; height: 100%;
            background: rgba(0, 0, 0, 0.7); 
            z-index: -1;
        }

.main-container {
            width: 85%;
            max-width: 1200px;
            margin: auto;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

 .info-box {
            flex: 1;
        }

.info-box h1 {
            font-size: 5.5rem;
            margin: 0;
            font-weight: 900;
            text-transform: uppercase;
            letter-spacing: -3px;
            line-height: 1;
        }

.info-box .role {
            font-size: 2.2rem;
            color: #00d4ff; 
            display: block;
            margin: 10px 0 40px 0;
            font-weight: 300;
        }

.contact-details {
            font-size: 1.2rem;
            background: rgba(255, 255, 255, 0.1);
            padding: 15px 25px;
            border-radius: 50px;
            display: inline-block;
            backdrop-filter: blur(5px);
        }

.contact-details span { margin-right: 30px; }
.contact-details a { color: #00d4ff; text-decoration: none; font-weight: bold; }

/* LARGE PHOTO SECTION */
        .photo-box {
            flex: 0 0 320px; 
        }

.photo-box img {
            width: 320px; 
            height: 320px;
            border-radius: 50%;
            border: 4px solid #00d4ff;
            object-fit: cover;
            box-shadow: 0 0 60px rgba(0, 212, 255, 0.3);
        }

 @media (max-width: 900px) {
            .main-container { flex-direction: column-reverse; text-align: center; }
            .info-box h1 { font-size: 3.5rem; }
            .photo-box { margin-bottom: 40px; }
            .contact-details { border-radius: 20px; }
            .contact-details span { display: block; margin: 10px 0; }
        }
    </style>
</head>
<body>

<div class="main-container">
        <div class="info-box">
            <h1>ARIVAZHAGAN</h1>
            <span class="role">SOC Analyst L1</span>
            
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
