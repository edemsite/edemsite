```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Edem Victor | Professional Video Editor</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        :root {
            --primary-color: #3498db;
            --secondary-color: #2c3e50;
            --accent-color: #e74c3c;
            --text-color: #333;
            --light-color: #ecf0f1;
            --dark-color: #2c3e50;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }

        body {
            background-color: var(--light-color);
            color: var(--text-color);
            line-height: 1.6;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        header {
            background-color: var(--secondary-color);
            color: white;
            padding: 20px 0;
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 100;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
        }

        .header-container {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            font-size: 24px;
            font-weight: bold;
        }

        .logo span {
            color: var(--primary-color);
        }

        nav ul {
            display: flex;
            list-style: none;
        }

        nav ul li {
            margin-left: 20px;
        }

        nav ul li a {
            color: white;
            text-decoration: none;
            transition: color 0.3s;
        }

        nav ul li a:hover {
            color: var(--primary-color);
        }

        .hero {
            height: 100vh;
            display: flex;
            align-items: center;
            background: linear-gradient(rgba(0, 0, 0, 0.7), rgba(0, 0, 0, 0.7)), url('https://images.unsplash.com/photo-1626785774573-4b799315345d?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1471&q=80') no-repeat center center/cover;
            color: white;
            text-align: center;
            padding-top: 80px;
        }

        .hero-content {
            max-width: 800px;
            margin: 0 auto;
        }

        .hero h1 {
            font-size: 48px;
            margin-bottom: 20px;
        }

        .hero p {
            font-size: 20px;
            margin-bottom: 30px;
        }

        .btn {
            display: inline-block;
            background-color: var(--primary-color);
            color: white;
            padding: 12px 30px;
            border-radius: 5px;
            text-decoration: none;
            font-weight: bold;
            transition: background-color 0.3s;
            border: none;
            cursor: pointer;
        }

        .btn:hover {
            background-color: #2980b9;
        }

        .btn-outline {
            background-color: transparent;
            border: 2px solid white;
            margin-left: 15px;
        }

        .btn-outline:hover {
            background-color: white;
            color: var(--text-color);
        }

        section {
            padding: 80px 0;
        }

        .section-title {
            text-align: center;
            margin-bottom: 50px;
        }

        .section-title h2 {
            font-size: 36px;
            color: var(--secondary-color);
            position: relative;
            display: inline-block;
            padding-bottom: 15px;
        }

        .section-title h2::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 50%;
            transform: translateX(-50%);
            width: 80px;
            height: 3px;
            background-color: var(--primary-color);
        }

        .about-content {
            display: flex;
            align-items: center;
            gap: 50px;
        }

        .about-img {
            flex: 1;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
        }

        .about-img img {
            width: 100%;
            height: auto;
            display: block;
        }

        .about-text {
            flex: 1;
        }

        .about-text h3 {
            font-size: 28px;
            margin-bottom: 20px;
            color: var(--secondary-color);
        }

        .about-text p {
            margin-bottom: 15px;
        }

        .skills {
            background-color: var(--secondary-color);
            color: white;
        }

        .skills-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
        }

        .skill-card {
            background-color: rgba(255, 255, 255, 0.1);
            padding: 30px;
            border-radius: 10px;
            transition: transform 0.3s;
        }

        .skill-card:hover {
            transform: translateY(-10px);
        }

        .skill-card i {
            font-size: 50px;
            margin-bottom: 20px;
            color: var(--primary-color);
        }

        .skill-card h3 {
            font-size: 24px;
            margin-bottom: 15px;
        }

        .portfolio-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 30px;
        }

        .portfolio-item {
            position: relative;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
        }

        .portfolio-item img {
            width: 100%;
            height: 300px;
            object-fit: cover;
            display: block;
            transition: transform 0.5s;
        }

        .portfolio-item:hover img {
            transform: scale(1.1);
        }

        .portfolio-overlay {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0, 0, 0, 0.7);
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            opacity: 0;
            transition: opacity 0.5s;
            color: white;
            padding: 20px;
            text-align: center;
        }

        .portfolio-item:hover .portfolio-overlay {
            opacity: 1;
        }

        .portfolio-overlay h3 {
            font-size: 24px;
            margin-bottom: 10px;
        }

        .contact-form {
            max-width: 600px;
            margin: 0 auto;
            background-color: white;
            padding: 40px;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
        }

        .form-group {
            margin-bottom: 20px;
        }

        .form-group label {
            display: block;
            margin-bottom: 5px;
            font-weight: bold;
        }

        .form-group input,
        .form-group textarea {
            width: 100%;
            padding: 12px;
            border: 1px solid #ddd;
            border-radius: 5px;
            font-size: 16px;
        }

        .form-group textarea {
            height: 150px;
            resize: vertical;
        }

        footer {
            background-color: var(--secondary-color);
            color: white;
            padding: 30px 0;
            text-align: center;
        }

        .social-links {
            margin-bottom: 20px;
        }

        .social-links a {
            display: inline-block;
            margin: 0 10px;
            color: white;
            font-size: 24px;
            transition: color 0.3s;
        }

        .social-links a:hover {
            color: var(--primary-color);
        }

        .editor-controls {
            position: fixed;
            right: 20px;
            top: 50%;
            transform: translateY(-50%);
            background-color: white;
            padding: 15px;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
            z-index: 1000;
        }

        .editor-controls h3 {
            margin-bottom: 10px;
            font-size: 16px;
            color: var(--secondary-color);
        }

        .color-options {
            display: flex;
            gap: 10px;
            margin-bottom: 15px;
        }

        .color-option {
            width: 30px;
            height: 30px;
            border-radius: 50%;
            cursor: pointer;
            border: 2px solid white;
        }

        .color-option:hover {
            transform: scale(1.1);
        }

        .reset-btn {
            background-color: var(--accent-color);
            color: white;
            border: none;
            padding: 8px 15px;
            border-radius: 5px;
            cursor: pointer;
            font-size: 14px;
            transition: background-color 0.3s;
        }

        .reset-btn:hover {
            background-color: #c0392b;
        }

        @media (max-width: 768px) {
            .header-container {
                flex-direction: column;
            }

            nav ul {
                margin-top: 20px;
            }

            .about-content {
                flex-direction: column;
            }

            .hero h1 {
                font-size: 36px;
            }

            .hero p {
                font-size: 18px;
            }

            .editor-controls {
                top: auto;
                bottom: 20px;
                right: 20px;
                transform: none;
            }
        }
    </style>
</head>
<body>
    <header>
        <div class="container header-container">
            <div class="logo">Edem <span>Victor</span></div>
            <nav>
                <ul>
                    <li><a href="#home">Home</a></li>
                    <li><a href="#about">About</a></li>
                    <li><a href="#skills">Skills</a></li>
                    <li><a href="#portfolio">Portfolio</a></li>
                    <li><a href="#contact">Contact</a></li>
                </ul>
            </nav>
        </div>
    </header>

    <section class="hero" id="home">
        <div class="container hero-content">
            <h1>Professional Video Editor</h1>
            <p>Specializing in Adobe Premiere Pro, After Effects, and CapCut to create stunning visual content that tells your story.</p>
            <div>
                <a href="#portfolio" class="btn">View My Work</a>
                <a href="#contact" class="btn btn-outline">Hire Me</a>
            </div>
        </div>
    </section>

    <section id="about">
        <div class="container">
            <div class="section-title">
                <h2>About Me</h2>
            </div>
            <div class="about-content">
                <div class="about-img">
                    <img src="https://images.unsplash.com/photo-1507003211169-0a1dd7228f2d?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=687&q=80" alt="Edem Victor">
                </div>
                <div class="about-text">
                    <h3>Hi, I'm Edem Victor</h3>
                    <p>I'm a professional video editor with over 5 years of experience creating compelling visual content for clients worldwide. My expertise lies in Adobe Creative Suite (Premiere Pro, After Effects) and CapCut, where I combine technical skills with creative vision to produce engaging videos.</p>
                    <p>I specialize in cinematic edits, social media content, promotional videos, and music videos. My approach combines storytelling with technical precision to deliver videos that resonate with audiences and achieve my clients' goals.</p>
                    <p>Whether you need a sleek corporate video, an engaging social media clip, or a cinematic masterpiece, I have the skills and creativity to bring your vision to life.</p>
                    <a href="#contact" class="btn">Get In Touch</a>
                </div>
            </div>
        </div>
    </section>

    <section class="skills" id="skills">
        <div class="container">
            <div class="section-title">
                <h2>My Skills</h2>
            </div>
            <div class="skills-container">
                <div class="skill-card">
                    <i class="fas fa-film"></i>
                    <h3>Video Editing</h3>
                    <p>Expert in Adobe Premiere Pro with advanced skills in timeline editing, color correction, audio syncing, and multi-cam editing.</p>
                </div>
                <div class="skill-card">
                    <i class="fas fa-magic"></i>
                    <h3>Motion Graphics</h3>
                    <p>Proficient in Adobe After Effects for creating stunning motion graphics, visual effects, and animated titles.</p>
                </div>
                <div class="skill-card">
                    <i class="fas fa-mobile-alt"></i>
                    <h3>CapCut Editing</h3>
                    <p>Skilled in CapCut for creating trendy, fast-paced social media content with smooth transitions and effects.</p>
                </div>
                <div class="skill-card">
                    <i class="fas fa-paint-brush"></i>
                    <h3>Color Grading</h3>
                    <p>Advanced color grading skills using Lumetri Color in Premiere Pro and DaVinci Resolve for cinematic looks.</p>
                </div>
                <div class="skill-card">
                    <i class="fas fa-music"></i>
                    <h3>Audio Editing</h3>
                    <p>Professional audio editing and mixing to ensure perfect sound quality that complements the visual experience.</p>
                </div>
                <div class="skill-card">
                    <i class="fas fa-lightbulb"></i>
                    <h3>Creative Storytelling</h3>
                    <p>Ability to craft compelling narratives through visual storytelling techniques that engage audiences.</p>
                </div>
            </div>
        </div>
    </section>

    <section id="portfolio">
        <div class="container">
            <div class="section-title">
                <h2>My Portfolio</h2>
            </div>
            <div class="portfolio-grid">
                <div class="portfolio-item">
                    <img src="https://images.unsplash.com/photo-1551269901-5c5e14c25df7?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1469&q=80" alt="Project 1">
                    <div class="portfolio-overlay">
                        <h3>Cinematic Travel Video</h3>
                        <p>4K travel video edited in Premiere Pro with color grading in DaVinci Resolve</p>
                        <a href="#" class="btn btn-outline">View Project</a>
                    </div>
                </div>
                <div class="portfolio-item">
                    <img src="https://images.unsplash.com/photo-1485846234645-a62644f84728?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1459&q=80" alt="Project 2">
                    <div class="portfolio-overlay">
                        <h3>Music Video</h3>
                        <p>High-energy music video edited in Premiere Pro with effects created in After Effects</p>
                        <a href="#" class="btn btn-outline">View Project</a>
                    </div>
                </div>
                <div class="portfolio-item">
                    <img src="https://images.unsplash.com/photo-1542744173-8e7e53415bb0?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1470&q=80" alt="Project 3">
                    <div class="portfolio-overlay">
                        <h3>Corporate Promo</h3>
                        <p>Corporate promotional video with motion graphics and animated infographics</p>
                        <a href="#" class="btn btn-outline">View Project</a>
                    </div>
                </div>
                <div class="portfolio-item">
                    <img src="https://images.unsplash.com/photo-1560169897-fc0cdbdfa4d5?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1472&q=80" alt="Project 4">
                    <div class="portfolio-overlay">
                        <h3>Social Media Content</h3>
                        <p>TikTok/Instagram Reels edited in CapCut with trendy transitions and effects</p>
                        <a href="#" class="btn btn-outline">View Project</a>
                    </div>
                </div>
                <div class="portfolio-item">
                    <img src="https://images.unsplash.com/photo-1511671782779-c97d3d27a1d4?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1470&q=80" alt="Project 5">
                    <div class="portfolio-overlay">
                        <h3>Product Commercial</h3>
                        <p>30-second product commercial with cinematic shots and dynamic editing</p>
                        <a href="#" class="btn btn-outline">View Project</a>
                    </div>
                </div>
                <div class="portfolio-item">
                    <img src="https://images.unsplash.com/photo-1551818255-e6e10975bc17?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1459&q=80" alt="Project 6">
                    <div class="portfolio-overlay">
                        <h3>Event Highlights</h3>
                        <p>Conference event highlights video with multi-cam editing and speaker overlays</p>
                        <a href="#" class="btn btn-outline">View Project</a>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <section id="contact">
        <div class="container">
            <div class="section-title">
                <h2>Contact Me</h2>
            </div>
            <div class="contact-form">
                <form id="contactForm">
                    <div class="form-group">
                        <label for="name">Your Name</label>
                        <input type="text" id="name" name="name" required>
                    </div>
                    <div class="form-group">
                        <label for="email">Your Email</label>
                        <input type="email" id="email" name="email" required>
                    </div>
                    <div class="form-group">
                        <label for="subject">Subject</label>
                        <input type="text" id="subject" name="subject" required>
                    </div>
                    <div class="form-group">
                        <label for="message">Your Message</label>
                        <textarea id="message" name="message" required></textarea>
                    </div>
                    <button type="submit" class="btn">Send Message</button>
                </form>
            </div>
        </div>
    </section>

    <footer>
        <div class="container">
            <div class="social-links">
                <a href="https://www.instagram.com/yourprofile" target="_blank"><i class="fab fa-instagram"></i></a>
                <a href="https://www.youtube.com/yourchannel" target="_blank"><i class="fab fa-youtube"></i></a>
                <a href="https://www.twitter.com/yourprofile" target="_blank"><i class="fab fa-twitter"></i></a>
                <a href=```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Edem Victor | Professional Video Editor</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        :root {
            --primary-color: #3498db;
            --secondary-color: #2c3e50;
            --accent-color: #e74c3c;
            --text-color: #333;
            --light-color: #ecf0f1;
            --dark-color: #2c3e50;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }

        body {
            background-color: var(--light-color);
            color: var(--text-color);
            line-height: 1.6;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        header {
            background-color: var(--secondary-color);
            color: white;
            padding: 20px 0;
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 100;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
        }

        .header-container {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            font-size: 24px;
            font-weight: bold;
        }

        .logo span {
            color: var(--primary-color);
        }

        nav ul {
            display: flex;
            list-style: none;
        }

        nav ul li {
            margin-left: 20px;
        }

        nav ul li a {
            color: white;
            text-decoration: none;
            transition: color 0.3s;
        }

        nav ul li a:hover {
            color: var(--primary-color);
        }

        .hero {
            height: 100vh;
            display: flex;
            align-items: center;
            background: linear-gradient(rgba(0, 0, 0, 0.7), rgba(0, 0, 0, 0.7)), url('https://images.unsplash.com/photo-1626785774573-4b799315345d?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1471&q=80') no-repeat center center/cover;
            color: white;
            text-align: center;
            padding-top: 80px;
        }

        .hero-content {
            max-width: 800px;
            margin: 0 auto;
        }

        .hero h1 {
            font-size: 48px;
            margin-bottom: 20px;
        }

        .hero p {
            font-size: 20px;
            margin-bottom: 30px;
        }

        .btn {
            display: inline-block;
            background-color: var(--primary-color);
            color: white;
            padding: 12px 30px;
            border-radius: 5px;
            text-decoration: none;
            font-weight: bold;
            transition: background-color 0.3s;
            border: none;
            cursor: pointer;
        }

        .btn:hover {
            background-color: #2980b9;
        }

        .btn-outline {
            background-color: transparent;
            border: 2px solid white;
            margin-left: 15px;
        }

        .btn-outline:hover {
            background-color: white;
            color: var(--text-color);
        }

        section {
            padding: 80px 0;
        }

        .section-title {
            text-align: center;
            margin-bottom: 50px;
        }

        .section-title h2 {
            font-size: 36px;
            color: var(--secondary-color);
            position: relative;
            display: inline-block;
            padding-bottom: 15px;
        }

        .section-title h2::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 50%;
            transform: translateX(-50%);
            width: 80px;
            height: 3px;
            background-color: var(--primary-color);
        }

        .about-content {
            display: flex;
            align-items: center;
            gap: 50px;
        }

        .about-img {
            flex: 1;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
        }

        .about-img img {
            width: 100%;
            height: auto;
            display: block;
        }

        .about-text {
            flex: 1;
        }

        .about-text h3 {
            font-size: 28px;
            margin-bottom: 20px;
            color: var(--secondary-color);
        }

        .about-text p {
            margin-bottom: 15px;
        }

        .skills {
            background-color: var(--secondary-color);
            color: white;
        }

        .skills-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
        }

        .skill-card {
            background-color: rgba(255, 255, 255, 0.1);
            padding: 30px;
            border-radius: 10px;
            transition: transform 0.3s;
        }

        .skill-card:hover {
            transform: translateY(-10px);
        }

        .skill-card i {
            font-size: 50px;
            margin-bottom: 20px;
            color: var(--primary-color);
        }

        .skill-card h3 {
            font-size: 24px;
            margin-bottom: 15px;
        }

        .portfolio-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 30px;
        }

        .portfolio-item {
            position: relative;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
        }

        .portfolio-item img {
            width: 100%;
            height: 300px;
            object-fit: cover;
            display: block;
            transition: transform 0.5s;
        }

        .portfolio-item:hover img {
            transform: scale(1.1);
        }

        .portfolio-overlay {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0, 0, 0, 0.7);
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            opacity: 0;
            transition: opacity 0.5s;
            color: white;
            padding: 20px;
            text-align: center;
        }

        .portfolio-item:hover .portfolio-overlay {
            opacity: 1;
        }

        .portfolio-overlay h3 {
            font-size: 24px;
            margin-bottom: 10px;
        }

        .contact-form {
            max-width: 600px;
            margin: 0 auto;
            background-color: white;
            padding: 40px;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
        }

        .form-group {
            margin-bottom: 20px;
        }

        .form-group label {
            display: block;
            margin-bottom: 5px;
            font-weight: bold;
        }

        .form-group input,
        .form-group textarea {
            width: 100%;
            padding: 12px;
            border: 1px solid #ddd;
            border-radius: 5px;
            font-size: 16px;
        }

        .form-group textarea {
            height: 150px;
            resize: vertical;
        }

        footer {
            background-color: var(--secondary-color);
            color: white;
            padding: 30px 0;
            text-align: center;
        }

        .social-links {
            margin-bottom: 20px;
        }

        .social-links a {
            display: inline-block;
            margin: 0 10px;
            color: white;
            font-size: 24px;
            transition: color 0.3s;
        }

        .social-links a:hover {
            color: var(--primary-color);
        }

        .editor-controls {
            position: fixed;
            right: 20px;
            top: 50%;
            transform: translateY(-50%);
            background-color: white;
            padding: 15px;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
            z-index: 1000;
        }

        .editor-controls h3 {
            margin-bottom: 10px;
            font-size: 16px;
            color: var(--secondary-color);
        }

        .color-options {
            display: flex;
            gap: 10px;
            margin-bottom: 15px;
        }

        .color-option {
            width: 30px;
            height: 30px;
            border-radius: 50%;
            cursor: pointer;
            border: 2px solid white;
        }

        .color-option:hover {
            transform: scale(1.1);
        }

        .reset-btn {
            background-color: var(--accent-color);
            color: white;
            border: none;
            padding: 8px 15px;
            border-radius: 5px;
            cursor: pointer;
            font-size: 14px;
            transition: background-color 0.3s;
        }

        .reset-btn:hover {
            background-color: #c0392b;
        }

        @media (max-width: 768px) {
            .header-container {
                flex-direction: column;
            }

            nav ul {
                margin-top: 20px;
            }

            .about-content {
                flex-direction: column;
            }

            .hero h1 {
                font-size: 36px;
            }

            .hero p {
                font-size: 18px;
            }

            .editor-controls {
                top: auto;
                bottom: 20px;
                right: 20px;
                transform: none;
            }
        }
    </style>
</head>
<body>
    <header>
        <div class="container header-container">
            <div class="logo">Edem <span>Victor</span></div>
            <nav>
                <ul>
                    <li><a href="#home">Home</a></li>
                    <li><a href="#about">About</a></li>
                    <li><a href="#skills">Skills</a></li>
                    <li><a href="#portfolio">Portfolio</a></li>
                    <li><a href="#contact">Contact</a></li>
                </ul>
            </nav>
        </div>
    </header>

    <section class="hero" id="home">
        <div class="container hero-content">
            <h1>Professional Video Editor</h1>
            <p>Specializing in Adobe Premiere Pro, After Effects, and CapCut to create stunning visual content that tells your story.</p>
            <div>
                <a href="#portfolio" class="btn">View My Work</a>
                <a href="#contact" class="btn btn-outline">Hire Me</a>
            </div>
        </div>
    </section>

    <section id="about">
        <div class="container">
            <div class="section-title">
                <h2>About Me</h2>
            </div>
            <div class="about-content">
                <div class="about-img">
                    <img src="https://images.unsplash.com/photo-1507003211169-0a1dd7228f2d?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=687&q=80" alt="Edem Victor">
                </div>
                <div class="about-text">
                    <h3>Hi, I'm Edem Victor</h3>
                    <p>I'm a professional video editor with over 5 years of experience creating compelling visual content for clients worldwide. My expertise lies in Adobe Creative Suite (Premiere Pro, After Effects) and CapCut, where I combine technical skills with creative vision to produce engaging videos.</p>
                    <p>I specialize in cinematic edits, social media content, promotional videos, and music videos. My approach combines storytelling with technical precision to deliver videos that resonate with audiences and achieve my clients' goals.</p>
                    <p>Whether you need a sleek corporate video, an engaging social media clip, or a cinematic masterpiece, I have the skills and creativity to bring your vision to life.</p>
                    <a href="#contact" class="btn">Get In Touch</a>
                </div>
            </div>
        </div>
    </section>

    <section class="skills" id="skills">
        <div class="container">
            <div class="section-title">
                <h2>My Skills</h2>
            </div>
            <div class="skills-container">
                <div class="skill-card">
                    <i class="fas fa-film"></i>
                    <h3>Video Editing</h3>
                    <p>Expert in Adobe Premiere Pro with advanced skills in timeline editing, color correction, audio syncing, and multi-cam editing.</p>
                </div>
                <div class="skill-card">
                    <i class="fas fa-magic"></i>
                    <h3>Motion Graphics</h3>
                    <p>Proficient in Adobe After Effects for creating stunning motion graphics, visual effects, and animated titles.</p>
                </div>
                <div class="skill-card">
                    <i class="fas fa-mobile-alt"></i>
                    <h3>CapCut Editing</h3>
                    <p>Skilled in CapCut for creating trendy, fast-paced social media content with smooth transitions and effects.</p>
                </div>
                <div class="skill-card">
                    <i class="fas fa-paint-brush"></i>
                    <h3>Color Grading</h3>
                    <p>Advanced color grading skills using Lumetri Color in Premiere Pro and DaVinci Resolve for cinematic looks.</p>
                </div>
                <div class="skill-card">
                    <i class="fas fa-music"></i>
                    <h3>Audio Editing</h3>
                    <p>Professional audio editing and mixing to ensure perfect sound quality that complements the visual experience.</p>
                </div>
                <div class="skill-card">
                    <i class="fas fa-lightbulb"></i>
                    <h3>Creative Storytelling</h3>
                    <p>Ability to craft compelling narratives through visual storytelling techniques that engage audiences.</p>
                </div>
            </div>
        </div>
    </section>

    <section id="portfolio">
        <div class="container">
            <div class="section-title">
                <h2>My Portfolio</h2>
            </div>
            <div class="portfolio-grid">
                <div class="portfolio-item">
                    <img src="https://images.unsplash.com/photo-1551269901-5c5e14c25df7?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1469&q=80" alt="Project 1">
                    <div class="portfolio-overlay">
                        <h3>Cinematic Travel Video</h3>
                        <p>4K travel video edited in Premiere Pro with color grading in DaVinci Resolve</p>
                        <a href="#" class="btn btn-outline">View Project</a>
                    </div>
                </div>
                <div class="portfolio-item">
                    <img src="https://images.unsplash.com/photo-1485846234645-a62644f84728?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1459&q=80" alt="Project 2">
                    <div class="portfolio-overlay">
                        <h3>Music Video</h3>
                        <p>High-energy music video edited in Premiere Pro with effects created in After Effects</p>
                        <a href="#" class="btn btn-outline">View Project</a>
                    </div>
                </div>
                <div class="portfolio-item">
                    <img src="https://images.unsplash.com/photo-1542744173-8e7e53415bb0?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1470&q=80" alt="Project 3">
                    <div class="portfolio-overlay">
                        <h3>Corporate Promo</h3>
                        <p>Corporate promotional video with motion graphics and animated infographics</p>
                        <a href="#" class="btn btn-outline">View Project</a>
                    </div>
                </div>
                <div class="portfolio-item">
                    <img src="https://images.unsplash.com/photo-1560169897-fc0cdbdfa4d5?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1472&q=80" alt="Project 4">
                    <div class="portfolio-overlay">
                        <h3>Social Media Content</h3>
                        <p>TikTok/Instagram Reels edited in CapCut with trendy transitions and effects</p>
                        <a href="#" class="btn btn-outline">View Project</a>
                    </div>
                </div>
                <div class="portfolio-item">
                    <img src="https://images.unsplash.com/photo-1511671782779-c97d3d27a1d4?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1470&q=80" alt="Project 5">
                    <div class="portfolio-overlay">
                        <h3>Product Commercial</h3>
                        <p>30-second product commercial with cinematic shots and dynamic editing</p>
                        <a href="#" class="btn btn-outline">View Project</a>
                    </div>
                </div>
                <div class="portfolio-item">
                    <img src="https://images.unsplash.com/photo-1551818255-e6e10975bc17?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1459&q=80" alt="Project 6">
                    <div class="portfolio-overlay">
                        <h3>Event Highlights</h3>
                        <p>Conference event highlights video with multi-cam editing and speaker overlays</p>
                        <a href="#" class="btn btn-outline">View Project</a>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <section id="contact">
        <div class="container">
            <div class="section-title">
                <h2>Contact Me</h2>
            </div>
            <div class="contact-form">
                <form id="contactForm">
                    <div class="form-group">
                        <label for="name">Your Name</label>
                        <input type="text" id="name" name="name" required>
                    </div>
                    <div class="form-group">
                        <label for="email">Your Email</label>
                        <input type="email" id="email" name="email" required>
                    </div>
                    <div class="form-group">
                        <label for="subject">Subject</label>
                        <input type="text" id="subject" name="subject" required>
                    </div>
                    <div class="form-group">
                        <label for="message">Your Message</label>
                        <textarea id="message" name="message" required></textarea>
                    </div>
                    <button type="submit" class="btn">Send Message</button>
                </form>
            </div>
        </div>
    </section>

    <footer>
        <div class="container">
            <div class="social-links">
                <a href="https://www.instagram.com/yourprofile" target="_blank"><i class="fab fa-instagram"></i></a>
                <a href="https://www.youtube.com/yourchannel" target="_blank"><i class="fab fa-youtube"></i></a>
                <a href="https://www.twitter.com/yourprofile" target="_blank"><i class="fab fa-twitter"></i></a>
                <a href=
