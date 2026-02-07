<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Arivazhagan | SOC Analyst Portfolio</title>
    <style>
        /* STEP 1: Full Background with Pentester.png */
        body {
            /* Ensure the file name is exactly Pentester.png in your folder */
            background: #0a0e14 url('Pentester.PNG') no-repeat center center fixed;
            background-size: cover;
            margin: 0;
            padding: 0;
            height: 100vh;
            display: flex;
            align-items: center; 
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            color: white;
            overflow: hidden; /* Keeps the page simple and non-scrolling */
        }

 /* Dark overlay for text readability */
        body::before {
            content: "";
            position: fixed;
            top: 0; left: 0; width: 100%; height: 100%;
            background: rgba(0, 0, 0, 0.5); 
            z-index: -1;
        }

 /* Main layout container */
        .container {
            width: 85%;
            max-width: 1100px;
            margin: auto;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

 /* STEP 2: Left Side Details */
        .bio-info {
            flex: 1;
        }

.bio-info h1 {
            font-size: 4rem;
            margin: 0;
            text-transform: uppercase;
            letter-spacing: 3px;
        }

.bio-info .role {
            font-size: 1.8rem;
            color: #38bdf8; /* Professional blue highlight */
            margin-bottom: 25px;
            display: block;
        }

/* Single line contact details */
        .contact-links {
            font-size: 1rem;
            color: #d1d5db;
        }

.contact-links span {
            margin-right: 30px;
        }

.contact-links a {
            color: #38bdf8;
            text-decoration: none;
            font-weight: bold;
        }

.contact-links a:hover {
            text-decoration: underline;
        }

/* STEP 2: Right Side Small Profile Photo */
        .profile-pic {
            flex: 0 0 140px; /* Controls the size of the photo section */
        }

.profile-pic img {
            width: 140px; /* Small size as requested */
            height: 140px;
            border-radius: 50%;
            border: 2px solid #38bdf8;
            object-fit: cover;
            box-shadow: 0 0 20px rgba(56, 189, 248, 0.3);
        }
    </style>
</head>
<body>

<div class="container">
        <div class="bio-info">
            <h1>Arivazhagan</h1>
            <span class="role">SOC Analyst L1</span>
            
<div class="contact-links">
                <span><strong>C.N:</strong> +91 6379944366</span>
                <span><strong>LinkedIn:</strong> <a href="#">Click Here</a></span>
            </div>
        </div>

<div class="profile-pic">
            <img src="my-photo.jpg" alt="Arivazhagan">
        </div>
    </div>

</body>
</html>
