<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Landslide Monitoring</title>
    <style>
        /* General Styles */
        body {
            background-color: #0d0d0d;
            color: white;
            font-family: 'Poppins', sans-serif;
            margin: 0;
            padding: 0;
            text-align: center;
        }

        /* Header Styles */
        .header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 15px 30px;
            background: rgba(0, 0, 0, 0.8);
            backdrop-filter: blur(10px);
            border-bottom: 1px solid #555;
            position: fixed;
            width: 100%;
            top: 0;
            left: 0;
            z-index: 1000;
        }

        .logo {
            font-size: 24px;
            font-weight: bold;
            text-transform: uppercase;
            letter-spacing: 2px;
            color: #ffcc00;
        }

        /* Navigation Bar */
        .nav a {
            color: white;
            text-decoration: none;
            margin: 0 15px;
            font-size: 18px;
            position: relative;
            transition: color 0.3s ease-in-out;
        }

        .nav a:hover {
            color: #ffcc00;
        }

        .nav a::after {
            content: "";
            display: block;
            height: 2px;
            width: 0;
            background: #ffcc00;
            transition: width 0.3s ease-in-out;
            position: absolute;
            bottom: -5px;
            left: 50%;
            transform: translateX(-50%);
        }

        .nav a:hover::after {
            width: 100%;
        }

        /* Main Title */
        .main-title {
            font-size: 32px;
            font-weight: bold;
            margin-top: 100px;
        }

        /* Section Styling */
        .section {
            display: none;
            padding: 60px 20px;
            max-width: 800px;
            margin: 0 auto;
            opacity: 0;
            transform: translateY(20px);
            transition: opacity 0.5s ease-out, transform 0.5s ease-out;
            text-align: left;
        }

        .visible {
            display: block;
            opacity: 1;
            transform: translateY(0);
        }

        /* Glassmorphism Effect for Sections */
        .content-box {
            background: rgba(255, 255, 255, 0.1);
            padding: 25px;
            border-radius: 15px;
            box-shadow: 0 4px 10px rgba(255, 255, 255, 0.1);
            backdrop-filter: blur(10px);
            border: 1px solid rgba(255, 255, 255, 0.2);
        }

        /* Responsive Design */
        @media (max-width: 768px) {
            .header {
                flex-direction: column;
                padding: 10px;
            }

            .nav {
                margin-top: 10px;
            }

            .nav a {
                font-size: 16px;
                margin: 5px;
            }

            .main-title {
                font-size: 24px;
                margin-top: 80px;
            }

            .section {
                padding: 40px 10px;
            }
        }
    </style>
</head>
<body>

    <!-- Header -->
    <header class="header">
        <div class="logo">MAVERICKS</div>
        <nav class="nav">
            <a onclick="showSection('home')">Home</a>
            <a onclick="showSection('about')">About</a>
            <a onclick="showSection('datas')">Datas</a>
            <a onclick="showSection('gallery')">Gallery</a>
            <a onclick="showSection('contact')">Contact</a>
        </nav>
    </header>

    <!-- Page Title -->
    <div class="main-title">Integrated Landslide Monitoring and Early Warning System</div>

    <!-- Sections -->
    <div id="home" class="section visible">
        <div class="content-box">
            <h2>Welcome to the Landslide Monitoring System</h2>
            <p>This system provides real-time landslide monitoring and early warnings to ensure safety.</p>
        </div>
    </div>

    <div id="about" class="section">
        <div class="content-box">
            <h2>About the Integrated Landslide Monitoring System</h2>
            <p>Landslides are a growing concern in India, particularly in hilly regions where intense rainfall and unstable slopes pose a severe risk to infrastructure and human lives...</p>
            
            <h3>Our Approach</h3>
            <p>Our system integrates sensor-based data collection with geotechnical analysis to predict landslides before they occur. The project focuses on:</p>
            <ul>
                <li>✔ Real-time rainfall and soil moisture monitoring using sensors.</li>
                <li>✔ Slope stability analysis with advanced modeling techniques like <strong>PLAXIS 2D</strong>.</li>
                <li>✔ Database-driven prediction system that correlates real-time data with predefined safety factors.</li>
                <li>✔ Automated early warning alerts when the <strong>Factor of Safety (FoS)</strong> falls below critical levels.</li>
            </ul>

            <h3>Our Vision</h3>
            <p>With this system, we hope to mitigate the risks of landslides, minimize economic losses, and enhance community safety by providing a reliable early warning mechanism.</p>
        </div>
    </div>

    <div id="datas" class="section">
        <div class="content-box">
            <h2>Datas</h2>
            <p>Live data of rainfall levels and factor of safety values will be displayed here.</p>
        </div>
    </div>

    <div id="gallery" class="section">
        <div class="content-box">
            <h2>Gallery</h2>
            <p>Images and diagrams related to landslide monitoring.</p>
        </div>
    </div>

    <div id="contact" class="section">
        <div class="content-box">
            <h2>Contact Details</h2>
            
            <p><strong>Email:</strong></p>
            <p>nirmal.john@saintgits.org</p>
            <p>jithin.cea2125@saintgits.org</p>
            <p>manu.ceb2125@saintgits.org</p>
            <p>mervin.ceb2125@saintgits.org</p>
            <p>noble.ceb2125@saintgits.org</p>

            <p><strong>Phone Numbers:</strong></p>
            <p>+91 95266 08654</p>
            <p>+91 89211 23469</p>
            <p>+91 85908 32820</p>
            <p>+91 75580 69423</p>
        </div>
    </div>

    <script>
        function showSection(sectionId) {
            document.querySelectorAll('.section').forEach(section => {
                section.classList.remove('visible');
            });

            setTimeout(() => {
                document.getElementById(sectionId).classList.add('visible');
            }, 100);
        }
    </script>

</body>
</html>
