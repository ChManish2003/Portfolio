# Portfolio
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Chintakayala Manish Kumar - Portfolio</title>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800;900&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.2/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        html {
            scroll-behavior: smooth;
        }

        body {
            font-family: 'Inter', sans-serif;
            background: linear-gradient(135deg, #0f172a 0%, #581c87 50%, #0f172a 100%);
            color: white;
            line-height: 1.6;
            overflow-x: hidden;
        }

        /* Custom Scrollbar */
        ::-webkit-scrollbar {
            width: 8px;
        }

        ::-webkit-scrollbar-track {
            background: #1e293b;
        }

        ::-webkit-scrollbar-thumb {
            background: linear-gradient(to bottom, #3b82f6, #8b5cf6);
            border-radius: 4px;
        }

        ::-webkit-scrollbar-thumb:hover {
            background: linear-gradient(to bottom, #2563eb, #7c3aed);
        }

        /* Navigation */
        .navbar {
            position: fixed;
            top: 0;
            width: 100%;
            z-index: 1000;
            padding: 1rem 2rem;
            transition: all 0.3s ease;
            backdrop-filter: blur(10px);
        }

        .navbar.scrolled {
            background: rgba(15, 23, 42, 0.95);
            box-shadow: 0 4px 20px rgba(0, 0, 0, 0.3);
        }

        .nav-container {
            max-width: 1200px;
            margin: 0 auto;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            font-size: 1.5rem;
            font-weight: 800;
            color: white;
        }

        .nav-menu {
            display: flex;
            list-style: none;
            gap: 2rem;
        }

        .nav-menu a {
            color: #d1d5db;
            text-decoration: none;
            transition: color 0.3s ease;
            font-weight: 500;
        }

        .nav-menu a:hover {
            color: #3b82f6;
        }

        .hamburger {
            display: none;
            flex-direction: column;
            cursor: pointer;
        }

        .hamburger span {
            width: 25px;
            height: 3px;
            background: white;
            margin: 3px 0;
            transition: 0.3s;
        }

        /* Hero Section */
        .hero {
            min-height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            position: relative;
            overflow: hidden;
            padding: 0 2rem;
        }

        .hero::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: 
                radial-gradient(circle at 25% 25%, rgba(59, 130, 246, 0.1) 0%, transparent 50%),
                radial-gradient(circle at 75% 75%, rgba(139, 92, 246, 0.1) 0%, transparent 50%);
            animation: float 6s ease-in-out infinite;
        }

        @keyframes float {
            0%, 100% { transform: translateY(0px); }
            50% { transform: translateY(-20px); }
        }

        .hero-content {
            text-align: center;
            z-index: 2;
            max-width: 800px;
        }

        .hero h1 {
            font-size: clamp(2.5rem, 8vw, 4.5rem);
            font-weight: 800;
            margin-bottom: 1rem;
            opacity: 0;
            animation: fadeInUp 1s ease forwards;
        }

        .hero .name-highlight {
            background: linear-gradient(135deg, #3b82f6, #8b5cf6);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        .hero .subtitle {
            font-size: clamp(1.2rem, 4vw, 2rem);
            color: #d1d5db;
            margin-bottom: 2rem;
            height: 80px;
            display: flex;
            align-items: center;
            justify-content: center;
            opacity: 0;
            animation: fadeInUp 1s ease 0.3s forwards;
        }

        .hero-buttons {
            display: flex;
            gap: 1rem;
            justify-content: center;
            flex-wrap: wrap;
            opacity: 0;
            animation: fadeInUp 1s ease 0.6s forwards;
        }

        .btn {
            padding: 1rem 2rem;
            border-radius: 50px;
            text-decoration: none;
            font-weight: 600;
            transition: all 0.3s ease;
            display: inline-flex;
            align-items: center;
            gap: 0.5rem;
            border: none;
            cursor: pointer;
            font-size: 1rem;
        }

        .btn-primary {
            background: linear-gradient(135deg, #3b82f6, #8b5cf6);
            color: white;
        }

        .btn-primary:hover {
            transform: scale(1.05);
            box-shadow: 0 10px 30px rgba(59, 130, 246, 0.3);
        }

        .btn-outline {
            border: 2px solid #3b82f6;
            color: #3b82f6;
            background: transparent;
        }

        .btn-outline:hover {
            background: #3b82f6;
            color: white;
            transform: scale(1.05);
        }

        @keyframes fadeInUp {
            from {
                opacity: 0;
                transform: translateY(30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        /* Section Styles */
        .section {
            padding: 5rem 2rem;
            max-width: 1200px;
            margin: 0 auto;
        }

        .section-alt {
            background: rgba(30, 41, 59, 0.3);
        }

        .section-title {
            text-align: center;
            font-size: clamp(2rem, 5vw, 3rem);
            font-weight: 800;
            margin-bottom: 1rem;
        }

        .section-title .highlight {
            color: #3b82f6;
        }

        .section-divider {
            width: 100px;
            height: 4px;
            background: linear-gradient(135deg, #3b82f6, #8b5cf6);
            margin: 0 auto 3rem;
            border-radius: 2px;
        }

        /* About Section */
        .about-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 3rem;
            align-items: center;
        }

        .about-text {
            font-size: 1.1rem;
            color: #d1d5db;
            line-height: 1.8;
        }

        .skills-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
            gap: 1.5rem;
        }

        .skill-card {
            background: rgba(30, 41, 59, 0.5);
            padding: 1.5rem;
            border-radius: 15px;
            text-align: center;
            border: 1px solid rgba(71, 85, 105, 0.5);
            transition: all 0.3s ease;
            backdrop-filter: blur(10px);
        }

        .skill-card:hover {
            transform: translateY(-5px);
            border-color: #3b82f6;
            box-shadow: 0 10px 30px rgba(59, 130, 246, 0.2);
        }

        .skill-card i {
            font-size: 2rem;
            margin-bottom: 1rem;
            color: #3b82f6;
        }

        /* Education Timeline */
        .timeline {
            position: relative;
            max-width: 800px;
            margin: 0 auto;
        }

        .timeline::before {
            content: '';
            position: absolute;
            left: 50%;
            top: 0;
            bottom: 0;
            width: 2px;
            background: linear-gradient(to bottom, #3b82f6, #8b5cf6);
            transform: translateX(-50%);
        }

        .timeline-item {
            position: relative;
            margin: 3rem 0;
            display: flex;
            align-items: center;
        }

        .timeline-item:nth-child(odd) {
            flex-direction: row-reverse;
        }

        .timeline-content {
            background: rgba(30, 41, 59, 0.5);
            padding: 2rem;
            border-radius: 15px;
            width: 45%;
            border: 1px solid rgba(71, 85, 105, 0.5);
            backdrop-filter: blur(10px);
            transition: all 0.3s ease;
        }

        .timeline-content:hover {
            transform: scale(1.05);
            border-color: #3b82f6;
        }

        .timeline-dot {
            position: absolute;
            left: 50%;
            width: 20px;
            height: 20px;
            background: linear-gradient(135deg, #3b82f6, #8b5cf6);
            border-radius: 50%;
            transform: translateX(-50%);
            border: 4px solid #0f172a;
        }

        /* Projects Grid */
        .projects-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(400px, 1fr));
            gap: 2rem;
        }

        .project-card {
            background: rgba(30, 41, 59, 0.5);
            border-radius: 20px;
            padding: 2rem;
            border: 1px solid rgba(71, 85, 105, 0.5);
            transition: all 0.3s ease;
            backdrop-filter: blur(10px);
        }

        .project-card:hover {
            transform: translateY(-10px);
            border-color: #3b82f6;
            box-shadow: 0 20px 40px rgba(59, 130, 246, 0.2);
        }

        .project-header {
            display: flex;
            align-items: center;
            margin-bottom: 1.5rem;
        }

        .project-icon {
            width: 60px;
            height: 60px;
            border-radius: 15px;
            display: flex;
            align-items: center;
            justify-content: center;
            margin-right: 1rem;
            font-size: 1.5rem;
            color: white;
        }

        .stock-icon {
            background: linear-gradient(135deg, #10b981, #3b82f6);
        }

        .pill-icon {
            background: linear-gradient(135deg, #f472b6, #a855f7);
        }

        .project-title {
            font-size: 1.3rem;
            font-weight: 700;
            margin-bottom: 0.5rem;
        }

        .project-year {
            color: #3b82f6;
            font-weight: 600;
        }

        .project-description {
            color: #d1d5db;
            margin-bottom: 1.5rem;
            line-height: 1.6;
        }

        .project-highlights {
            margin-bottom: 1.5rem;
        }

        .project-highlights h4 {
            font-size: 0.9rem;
            margin-bottom: 0.5rem;
            color: white;
        }

        .project-highlights ul {
            list-style: none;
            padding: 0;
        }

        .project-highlights li {
            color: #9ca3af;
            font-size: 0.85rem;
            margin-bottom: 0.3rem;
            padding-left: 1rem;
            position: relative;
        }

        .project-highlights li::before {
            content: "•";
            color: #3b82f6;
            position: absolute;
            left: 0;
        }

        .tech-badges {
            display: flex;
            flex-wrap: wrap;
            gap: 0.5rem;
            margin-bottom: 2rem;
        }

        .tech-badge {
            background: rgba(71, 85, 105, 0.5);
            color: #3b82f6;
            padding: 0.4rem 0.8rem;
            border-radius: 20px;
            font-size: 0.8rem;
            border: 1px solid rgba(59, 130, 246, 0.3);
        }

        /* Certificates Carousel */
        .certificates-carousel {
            position: relative;
            max-width: 600px;
            margin: 0 auto;
        }

        .certificate-card {
            background: rgba(30, 41, 59, 0.5);
            padding: 3rem;
            border-radius: 20px;
            text-align: center;
            border: 1px solid rgba(71, 85, 105, 0.5);
            backdrop-filter: blur(10px);
        }

        .certificate-icon {
            width: 80px;
            height: 80px;
            margin: 0 auto 1.5rem;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 2rem;
            color: white;
        }

        .ibm-cert {
            background: linear-gradient(135deg, #3b82f6, #06b6d4);
        }

        .duke-cert {
            background: linear-gradient(135deg, #10b981, #059669);
        }

        .carousel-nav {
            display: flex;
            justify-content: center;
            gap: 0.5rem;
            margin-top: 2rem;
        }

        .carousel-dot {
            width: 12px;
            height: 12px;
            border-radius: 50%;
            background: rgba(71, 85, 105, 0.5);
            cursor: pointer;
            transition: all 0.3s ease;
        }

        .carousel-dot.active {
            background: #3b82f6;
        }

        /* Technologies Grid */
        .tech-section {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 3rem;
        }

        .tech-category h3 {
            font-size: 1.5rem;
            margin-bottom: 2rem;
            text-align: center;
        }

        .tech-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(120px, 1fr));
            gap: 1rem;
        }

        .soft-skills {
            display: flex;
            flex-direction: column;
            gap: 1.5rem;
        }

        .soft-skill {
            background: rgba(30, 41, 59, 0.5);
            padding: 1.5rem;
            border-radius: 15px;
            display: flex;
            align-items: center;
            gap: 1rem;
            border: 1px solid rgba(71, 85, 105, 0.5);
            transition: all 0.3s ease;
        }

        .soft-skill:hover {
            transform: scale(1.05);
            border-color: #8b5cf6;
        }

        .soft-skill-icon {
            width: 50px;
            height: 50px;
            border-radius: 10px;
            background: linear-gradient(135deg, #8b5cf6, #f472b6);
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
        }

        .progress-bar {
            width: 100%;
            height: 8px;
            background: rgba(71, 85, 105, 0.5);
            border-radius: 4px;
            overflow: hidden;
            margin-top: 0.5rem;
        }

        .progress-fill {
            height: 100%;
            background: linear-gradient(135deg, #8b5cf6, #f472b6);
            width: 90%;
            border-radius: 4px;
            animation: fillProgress 2s ease-in-out;
        }

        @keyframes fillProgress {
            from { width: 0; }
            to { width: 90%; }
        }

        /* Contact Section */
        .contact-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 3rem;
        }

        .contact-info {
            display: flex;
            flex-direction: column;
            gap: 1.5rem;
        }

        .contact-item {
            display: flex;
            align-items: center;
            gap: 1rem;
            padding: 1.5rem;
            background: rgba(30, 41, 59, 0.5);
            border-radius: 15px;
            border: 1px solid rgba(71, 85, 105, 0.5);
            transition: all 0.3s ease;
            text-decoration: none;
            color: inherit;
        }

        .contact-item:hover {
            transform: scale(1.05);
            border-color: #3b82f6;
        }

        .contact-icon {
            width: 50px;
            height: 50px;
            border-radius: 10px;
            background: linear-gradient(135deg, #3b82f6, #8b5cf6);
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
        }

        .contact-form {
            background: rgba(30, 41, 59, 0.5);
            padding: 2rem;
            border-radius: 20px;
            border: 1px solid rgba(71, 85, 105, 0.5);
            backdrop-filter: blur(10px);
        }

        .form-group {
            margin-bottom: 1.5rem;
        }

        .form-control {
            width: 100%;
            padding: 1rem;
            background: rgba(71, 85, 105, 0.5);
            border: 1px solid rgba(71, 85, 105, 0.5);
            border-radius: 10px;
            color: white;
            font-size: 1rem;
            transition: all 0.3s ease;
        }

        .form-control:focus {
            outline: none;
            border-color: #3b82f6;
            box-shadow: 0 0 0 3px rgba(59, 130, 246, 0.1);
        }

        .form-control::placeholder {
            color: #9ca3af;
        }

        textarea.form-control {
            resize: vertical;
            min-height: 120px;
        }

        /* Footer */
        .footer {
            background: rgba(15, 23, 42, 0.5);
            padding: 2rem;
            text-align: center;
            border-top: 1px solid rgba(71, 85, 105, 0.5);
            backdrop-filter: blur(10px);
        }

        .footer-links {
            display: flex;
            justify-content: center;
            gap: 2rem;
            margin-top: 1rem;
        }

        .footer-links a {
            color: #9ca3af;
            text-decoration: none;
            transition: color 0.3s ease;
        }

        .footer-links a:hover {
            color: #3b82f6;
        }

        /* Responsive Design */
        @media (max-width: 768px) {
            .nav-menu {
                display: none;
            }

            .hamburger {
                display: flex;
            }

            .about-grid,
            .contact-grid,
            .tech-section {
                grid-template-columns: 1fr;
            }

            .timeline::before {
                left: 20px;
            }

            .timeline-item {
                flex-direction: row !important;
                padding-left: 50px;
            }

            .timeline-content {
                width: 100%;
            }

            .timeline-dot {
                left: 20px;
            }

            .projects-grid {
                grid-template-columns: 1fr;
            }

            .hero-buttons {
                flex-direction: column;
                align-items: center;
            }
        }

        /* Typing Animation */
        .typing-text {
            border-right: 2px solid #3b82f6;
            animation: blink 1s infinite;
        }

        @keyframes blink {
            0%, 50% { border-color: transparent; }
            51%, 100% { border-color: #3b82f6; }
        }

        /* Scroll Reveal Animation */
        .reveal {
            opacity: 0;
            transform: translateY(50px);
            transition: all 0.8s ease;
        }

        .reveal.active {
            opacity: 1;
            transform: translateY(0);
        }
    </style>
</head>
<script>
  function downloadResume() {
    // This opens your resume in a new tab or triggers a download
    window.open('MANISH_DEVELOPER_RESUME.pdf', '_blank');
  }
</script>

<body>
    <!-- Navigation -->
    <nav class="navbar" id="navbar">
        <div class="nav-container">
            <div class="logo">MK</div>
            <ul class="nav-menu">
                <li><a href="#home">Home</a></li>
                <li><a href="#about">About</a></li>
                <li><a href="#education">Education</a></li>
                <li><a href="#projects">Projects</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
            <div class="hamburger">
                <span></span>
                <span></span>
                <span></span>
            </div>
        </div>
    </nav>

 <!-- Hero Section -->
<section id="home" class="hero">
    <div class="hero-content">
        <h1>
            Chintakayala <span class="name-highlight">Manish Kumar</span>
        </h1>
        <div class="subtitle">
            <span id="typing-text" class="typing-text">Aspiring Full Stack Developer</span>
        </div>
        <div class="hero-buttons">
            <!-- Correct Resume Link -->
<a href="Resume/MANISH_DEVELOPER_RESUME.pdf" 
   download="MANISH_KUMAR_Resume.pdf" 
   target="_blank" 
   class="btn btn-primary">
    <i class="fas fa-download"></i>
    Download Resume
</a>
               
            </a>
            <a href="#contact" class="btn btn-outline">
                <i class="fas fa-envelope"></i>
                Contact Me
            </a>
        </div>
    </div>
</section>



    <!-- About Section -->
    <section id="about" class="section reveal">
        <h2 class="section-title">About <span class="highlight">Me</span></h2>
        <div class="section-divider"></div>
        <div class="about-grid">
            <div class="about-text">
                <p>Highly organized and detail-oriented individual with strong problem-solving skills. Passionate about building scalable and user-focused applications. Seeking opportunities to grow as a developer and contribute to real-world tech solutions.</p>
                <p>Currently pursuing B.Tech in Computer Science Engineering at Gitam University, I'm constantly learning and exploring new technologies to enhance my development skills.</p>
            </div>
            <div class="skills-grid">
                <div class="skill-card">
                    <i class="fab fa-java"></i>
                    <h3>Java</h3>
                </div>
                <div class="skill-card">
                    <i class="fab fa-python"></i>
                    <h3>Python</h3>
                </div>
                <div class="skill-card">
                    <i class="fas fa-database"></i>
                    <h3>SQL</h3>
                </div>
                <div class="skill-card">
                    <i class="fab fa-js"></i>
                    <h3>JavaScript</h3>
                </div>
                <div class="skill-card">
                    <i class="fab fa-git-alt"></i>
                    <h3>Git</h3>
                </div>
                <div class="skill-card">
                    <i class="fas fa-code"></i>
                    <h3>VS Code</h3>
                </div>
            </div>
        </div>
    </section>

    <!-- Education Section -->
    <section id="education" class="section section-alt reveal">
        <h2 class="section-title">Education <span class="highlight">Timeline</span></h2>
        <div class="section-divider"></div>
        <div class="timeline">
            <div class="timeline-item">
                <div class="timeline-content">
                    <div style="display: flex; align-items: center; margin-bottom: 1rem;">
                        <i class="fas fa-graduation-cap" style="color: #3b82f6; margin-right: 0.5rem;"></i>
                        <span style="color: #3b82f6; font-weight: 600;">2021 - 2025</span>
                    </div>
                    <h3>Gitam University</h3>
                    <p style="color: #8b5cf6; font-weight: 600;">B.Tech Computer Science Engineering</p>
                    <p style="color: #10b981; font-weight: 600;">GPA: 7.42</p>
                    <p style="color: #d1d5db; font-size: 0.9rem;">Currently pursuing Bachelor of Technology in Computer Science Engineering</p>
                </div>
                <div class="timeline-dot"></div>
            </div>
            <div class="timeline-item">
                <div class="timeline-content">
                    <div style="display: flex; align-items: center; margin-bottom: 1rem;">
                        <i class="fas fa-graduation-cap" style="color: #3b82f6; margin-right: 0.5rem;"></i>
                        <span style="color: #3b82f6; font-weight: 600;">2019 - 2021</span>
                    </div>
                    <h3>Narayana Junior College</h3>
                    <p style="color: #8b5cf6; font-weight: 600;">Intermediate (12th)</p>
                    <p style="color: #10b981; font-weight: 600;">93%</p>
                    <p style="color: #d1d5db; font-size: 0.9rem;">Completed Intermediate education with excellent academic performance</p>
                </div>
                <div class="timeline-dot"></div>
            </div>
            <div class="timeline-item">
                <div class="timeline-content">
                    <div style="display: flex; align-items: center; margin-bottom: 1rem;">
                        <i class="fas fa-graduation-cap" style="color: #3b82f6; margin-right: 0.5rem;"></i>
                        <span style="color: #3b82f6; font-weight: 600;">2018 - 2019</span>
                    </div>
                    <h3>Sri Chaitanya School</h3>
                    <p style="color: #8b5cf6; font-weight: 600;">SSC (10th)</p>
                    <p style="color: #10b981; font-weight: 600;">GPA: 9.0</p>
                    <p style="color: #d1d5db; font-size: 0.9rem;">Completed Secondary School Certificate with outstanding results</p>
                </div>
                <div class="timeline-dot"></div>
            </div>
        </div>
    </section>

    <!-- Projects Section -->
    <section id="projects" class="section reveal">
        <h2 class="section-title">Featured <span class="highlight">Projects</span></h2>
        <div class="section-divider"></div>
        <div class="projects-grid">
            <div class="project-card">
                <div class="project-header">
                    <div class="project-icon stock-icon">
                        <i class="fas fa-chart-line"></i>
                    </div>
                    <div>
                        <h3 class="project-title">Stock Market Prediction (Major Project)</h3>
                        <p class="project-year">2024</p>
                    </div>
                </div>
                <p class="project-description">
                    Developed a comprehensive Stock Market Prediction application using Python and machine learning techniques to analyze historical stock data and predict future trends. The project incorporates data preprocessing, feature extraction, and model training using a hybrid combination of LSTM and Random Forest algorithms to provide insights into stock price movements. Features a user-friendly interface to visualize predictions and offers tools to assist users in making informed investment decisions.
                </p>
                <div class="project-highlights">
                    <h4>Key Features:</h4>
                    <ul>
                        <li>Hybrid ML model combining LSTM and Random Forest</li>
                        <li>Historical data analysis and preprocessing</li>
                        <li>Interactive visualization dashboard</li>
                        <li>Investment decision support tools</li>
                    </ul>
                </div>
                <div class="tech-badges">
                    <span class="tech-badge">Python</span>
                    <span class="tech-badge">SQL</span>
                    <span class="tech-badge">Machine Learning</span>
                    <span class="tech-badge">LSTM</span>
                    <span class="tech-badge">Random Forest</span>
                    <span class="tech-badge">Databases</span>
                </div>
                <a href="https://github.com/ChManish2003/Stock-Market-Predection" target="_blank" class="btn btn-primary">
                    <i class="fab fa-github"></i>
                    View on GitHub
                </a>
            </div>

            <div class="project-card">
                <div class="project-header">
                    <div class="project-icon pill-icon">
                        <i class="fas fa-pills"></i>
                    </div>
                    <div>
                        <h3 class="project-title">Pill Reminder Application</h3>
                        <p class="project-year">2023</p>
                    </div>
                </div>
                <p class="project-description">
                    A comprehensive web-based application designed to help users track their medication schedules, monitor pill consumption, and receive timely reminders for taking medication. The app automatically updates pill count as doses are taken and alerts users when refills are needed. Provides a practical solution to healthcare challenges, particularly benefiting users managing multiple medications or chronic conditions.
                </p>
                <div class="project-highlights">
                    <h4>Key Features:</h4>
                    <ul>
                        <li>Automated medication tracking system</li>
                        <li>SMS and pop-up notification alerts</li>
                        <li>Refill reminder functionality</li>
                        <li>Multi-medication management support</li>
                    </ul>
                </div>
                <div class="tech-badges">
                    <span class="tech-badge">Python</span>
                    <span class="tech-badge">JavaScript</span>
                    <span class="tech-badge">UI Design</span>
                    <span class="tech-badge">Database</span>
                    <span class="tech-badge">SMS Notifications</span>
                </div>
                <a href="https://github.com/ChManish2003/Pill-Reminder-Application" target="_blank" class="btn btn-primary">
                    <i class="fab fa-github"></i>
                    View on GitHub
                </a>
            </div>
        </div>
    </section>

    <!-- Internship Section -->
    <section class="section section-alt reveal">
        <h2 class="section-title">Internship <span class="highlight" style="color: #10b981;">Experience</span></h2>
        <div class="section-divider"></div>
        <div style="max-width: 800px; margin: 0 auto;">
            <div class="project-card">
                <div class="project-header">
                    <div class="project-icon" style="background: linear-gradient(135deg, #10b981, #3b82f6);">
                        <i class="fas fa-briefcase"></i>
                    </div>
                    <div>
                        <h3 class="project-title">DSA Intern (Java)</h3>
                        <p class="project-year">Innovate - 2024</p>
                    </div>
                </div>
                <div style="display: grid; grid-template-columns: 1fr 1fr; gap: 2rem;">
                    <div>
                        <h4 style="color: white; margin-bottom: 1rem; display: flex; align-items: center;">
                            <i class="fas fa-code" style="color: #3b82f6; margin-right: 0.5rem;"></i>
                            Key Highlights
                        </h4>
                        <ul style="list-style: none; padding: 0;">
                            <li style="color: #d1d5db; margin-bottom: 0.8rem; display: flex; align-items: start;">
                                <i class="fas fa-check-circle" style="color: #10b981; margin-right: 0.5rem; margin-top: 0.2rem;"></i>
                                Solved real-world problems using arrays and data structures
                            </li>
                            <li style="color: #d1d5db; margin-bottom: 0.8rem; display: flex; align-items: start;">
                                <i class="fas fa-check-circle" style="color: #10b981; margin-right: 0.5rem; margin-top: 0.2rem;"></i>
                                Implemented efficient searching and sorting algorithms
                            </li>
                            <li style="color: #d1d5db; margin-bottom: 0.8rem; display: flex; align-items: start;">
                                <i class="fas fa-check-circle" style="color: #10b981; margin-right: 0.5rem; margin-top: 0.2rem;"></i>
                                Worked with stacks and queues for complex problem solving
                            </li>
                            <li style="color: #d1d5db; margin-bottom: 0.8rem; display: flex; align-items: start;">
                                <i class="fas fa-check-circle" style="color: #10b981; margin-right: 0.5rem; margin-top: 0.2rem;"></i>
                                Gained hands-on experience with Java programming
                            </li>
                        </ul>
                    </div>
                    <div style="background: rgba(71, 85, 105, 0.3); border-radius: 15px; padding: 1.5rem;">
                        <h4 style="color: white; margin-bottom: 1rem;">Skills Developed</h4>
                        <div style="display: flex; flex-wrap: wrap; gap: 0.5rem;">
                            <span style="padding: 0.3rem 0.8rem; background: rgba(16, 185, 129, 0.2); color: #10b981; border-radius: 20px; font-size: 0.8rem; border: 1px solid rgba(16, 185, 129, 0.3);">Java</span>
                            <span style="padding: 0.3rem 0.8rem; background: rgba(16, 185, 129, 0.2); color: #10b981; border-radius: 20px; font-size: 0.8rem; border: 1px solid rgba(16, 185, 129, 0.3);">Data Structures</span>
                            <span style="padding: 0.3rem 0.8rem; background: rgba(16, 185, 129, 0.2); color: #10b981; border-radius: 20px; font-size: 0.8rem; border: 1px solid rgba(16, 185, 129, 0.3);">Algorithms</span>
                            <span style="padding: 0.3rem 0.8rem; background: rgba(16, 185, 129, 0.2); color: #10b981; border-radius: 20px; font-size: 0.8rem; border: 1px solid rgba(16, 185, 129, 0.3);">Problem Solving</span>
                            <span style="padding: 0.3rem 0.8rem; background: rgba(16, 185, 129, 0.2); color: #10b981; border-radius: 20px; font-size: 0.8rem; border: 1px solid rgba(16, 185, 129, 0.3);">Code Optimization</span>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Certificates Section -->
    <section class="section reveal">
        <h2 class="section-title"><span class="highlight" style="color: #fbbf24;">Certificates</span> & Achievements</h2>
        <div class="section-divider"></div>
        <div class="certificates-carousel">
            <div class="certificate-card" id="certificate-0">
                <div class="certificate-icon ibm-cert">
                    <i class="fas fa-award"></i>
                </div>
                <h3>Structured Query Language</h3>
                <p style="color: #3b82f6; font-weight: 600; font-size: 1.1rem;">IBM</p>
                <p style="color: #d1d5db; margin-top: 1rem;">Comprehensive SQL certification covering database design, queries, and optimization</p>
            </div>
            <div class="certificate-card" id="certificate-1" style="display: none;">
                <div class="certificate-icon ibm-cert">
                    <i class="fas fa-award"></i>
                </div>
                <h3>Data Structures</h3>
                <p style="color: #3b82f6; font-weight: 600; font-size: 1.1rem;">IBM</p>
                <p style="color: #d1d5db; margin-top: 1rem;">Advanced data structures and algorithms certification with practical implementations</p>
            </div>
            <div class="certificate-card" id="certificate-2" style="display: none;">
                <div class="certificate-icon duke-cert">
                    <i class="fas fa-award"></i>
                </div>
                <h3>Machine Learning</h3>
                <p style="color: #10b981; font-weight: 600; font-size: 1.1rem;">Duke University</p>
                <p style="color: #d1d5db; margin-top: 1rem;">Machine learning fundamentals, algorithms, and real-world applications</p>
            </div>
            <div class="carousel-nav">
                <div class="carousel-dot active" onclick="showCertificate(0)"></div>
                <div class="carousel-dot" onclick="showCertificate(1)"></div>
                <div class="carousel-dot" onclick="showCertificate(2)"></div>
            </div>
        </div>
    </section>

    <!-- Technologies Section -->
    <section class="section section-alt reveal">
        <h2 class="section-title">Technologies & <span class="highlight" style="color: #8b5cf6;">Skills</span></h2>
        <div class="section-divider"></div>
        <div class="tech-section">
            <div class="tech-category">
                <h3>Technical Skills</h3>
                <div class="tech-grid">
                    <div class="skill-card">
                        <i class="fab fa-java" style="color: #f97316;"></i>
                        <h4>Java</h4>
                        <p style="color: #9ca3af; font-size: 0.8rem;">Programming</p>
                    </div>
                    <div class="skill-card">
                        <i class="fab fa-python" style="color: #3b82f6;"></i>
                        <h4>Python</h4>
                        <p style="color: #9ca3af; font-size: 0.8rem;">Programming</p>
                    </div>
                    <div class="skill-card">
                        <i class="fas fa-database" style="color: #10b981;"></i>
                        <h4>SQL</h4>
                        <p style="color: #9ca3af; font-size: 0.8rem;">Database</p>
                    </div>
                    <div class="skill-card">
                        <i class="fab fa-github" style="color: #8b5cf6;"></i>
                        <h4>GitHub</h4>
                        <p style="color: #9ca3af; font-size: 0.8rem;">Version Control</p>
                    </div>
                    <div class="skill-card">
                        <i class="fas fa-server" style="color: #ef4444;"></i>
                        <h4>SQL Server</h4>
                        <p style="color: #9ca3af; font-size: 0.8rem;">Database</p>
                    </div>
                    <div class="skill-card">
                        <i class="fas fa-code" style="color: #3b82f6;"></i>
                        <h4>VS Code</h4>
                        <p style="color: #9ca3af; font-size: 0.8rem;">Tools</p>
                    </div>
                </div>
            </div>
            <div class="tech-category">
                <h3>Soft Skills</h3>
                <div class="soft-skills">
                    <div class="soft-skill">
                        <div class="soft-skill-icon">
                            <i class="fas fa-lightbulb"></i>
                        </div>
                        <div style="flex: 1;">
                            <h4>Problem Solving</h4>
                            <div class="progress-bar">
                                <div class="progress-fill"></div>
                            </div>
                        </div>
                    </div>
                    <div class="soft-skill">
                        <div class="soft-skill-icon">
                            <i class="fas fa-bullseye"></i>
                        </div>
                        <div style="flex: 1;">
                            <h4>Critical Thinking</h4>
                            <div class="progress-bar">
                                <div class="progress-fill"></div>
                            </div>
                        </div>
                    </div>
                    <div class="soft-skill">
                        <div class="soft-skill-icon">
                            <i class="fas fa-users"></i>
                        </div>
                        <div style="flex: 1;">
                            <h4>Teamwork</h4>
                            <div class="progress-bar">
                                <div class="progress-fill"></div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section id="contact" class="section reveal">
        <h2 class="section-title">Get In <span class="highlight">Touch</span></h2>
        <div class="section-divider"></div>
        <p style="text-align: center; color: #d1d5db; font-size: 1.1rem; margin-bottom: 3rem; max-width: 600px; margin-left: auto; margin-right: auto;">
            I'm always open to discussing new opportunities and interesting projects. Let's connect and create something amazing together!
        </p>
        <div class="contact-grid">
            <div class="contact-info">
                <h3 style="margin-bottom: 2rem;">Contact Information</h3>
                <a href="mailto:ch.manishkumar2003@gmail.com" class="contact-item">
                    <div class="contact-icon">
                        <i class="fas fa-envelope"></i>
                    </div>
                    <div>
                        <p style="color: #9ca3af; font-size: 0.9rem;">Email</p>
                        <p style="color: #3b82f6; font-weight: 600;">ch.manishkumar2003@gmail.com</p>
                    </div>
                </a>
                <a href="tel:+917989992982" class="contact-item">
                    <div class="contact-icon">
                        <i class="fas fa-phone"></i>
                    </div>
                    <div>
                        <p style="color: #9ca3af; font-size: 0.9rem;">Phone</p>
                        <p style="color: #10b981; font-weight: 600;">+91 7989992982</p>
                    </div>
                </a>
                <a href="https://www.linkedin.com/in/manish-kumar7989/" target="_blank" class="contact-item">
                    <div class="contact-icon">
                        <i class="fab fa-linkedin"></i>
                    </div>
                    <div>
                        <p style="color: #9ca3af; font-size: 0.9rem;">LinkedIn</p>
                        <p style="color: #0ea5e9; font-weight: 600;">linkedin.com/in/manish-kumar7989</p>
                    </div>
                </a>
                <a href="https://github.com/ChManish2003" target="_blank" class="contact-item">
                    <div class="contact-icon">
                        <i class="fab fa-github"></i>
                    </div>
                    <div>
                        <p style="color: #9ca3af; font-size: 0.9rem;">GitHub</p>
                        <p style="color: #8b5cf6; font-weight: 600;">github.com/ChManish2003</p>
                    </div>
                </a>
            </div>
            <div class="contact-form">
                <h3 style="margin-bottom: 2rem;">Send a Message</h3>
                <form>
                    <div class="form-group">
                        <input type="text" class="form-control" placeholder="Your Name" required>
                    </div>
                    <div class="form-group">
                        <input type="email" class="form-control" placeholder="Your Email" required>
                    </div>
                    <div class="form-group">
                        <textarea class="form-control" placeholder="Your Message" required></textarea>
                    </div>
                    <button type="submit" class="btn btn-primary" style="width: 100%;">
                        <i class="fas fa-paper-plane"></i>
                        Send Message
                    </button>
                </form>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="footer">
        <p>Copyright © 2024 Chintakayala Manish Kumar. All rights reserved.</p>
        <p style="margin-top: 0.5rem; display: flex; align-items: center; justify-content: center; gap: 0.5rem;">
            Built with <i class="fas fa-heart" style="color: #ef4444;"></i> by Manish Kumar
        </p>
        <div class="footer-links">
            <a href="https://www.linkedin.com/in/manish-kumar7989/" target="_blank">LinkedIn</a>
            <a href="https://github.com/ChManish2003" target="_blank">GitHub</a>
            <a href="mailto:ch.manishkumar2003@gmail.com">Email</a>
        </div>
    </footer>

    <script>
        // Typing Animation
        const texts = [
            "Aspiring Front End Developer",
            "Core Java Specalist", 
            "Problem Solver",
            "Tech Innovator"
        ];
        let textIndex = 0;
        let charIndex = 0;
        let isDeleting = false;
        const typingElement = document.getElementById('typing-text');

        function typeText() {
            const currentText = texts[textIndex];
            
            if (isDeleting) {
                typingElement.textContent = currentText.substring(0, charIndex - 1);
                charIndex--;
            } else {
                typingElement.textContent = currentText.substring(0, charIndex + 1);
                charIndex++;
            }

            let typeSpeed = isDeleting ? 50 : 100;

            if (!isDeleting && charIndex === currentText.length) {
                typeSpeed = 2000;
                isDeleting = true;
            } else if (isDeleting && charIndex === 0) {
                isDeleting = false;
                textIndex = (textIndex + 1) % texts.length;
                typeSpeed = 500;
            }

            setTimeout(typeText, typeSpeed);
        }

        // Start typing animation
        typeText();

        // Navbar scroll effect
        window.addEventListener('scroll', () => {
            const navbar = document.getElementById('navbar');
            if (window.scrollY > 50) {
                navbar.classList.add('scrolled');
            } else {
                navbar.classList.remove('scrolled');
            }
        });

        // Scroll reveal animation
        const observerOptions = {
            threshold: 0.1,
            rootMargin: '0px 0px -50px 0px'
        };

        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.classList.add('active');
                }
            });
        }, observerOptions);

        document.querySelectorAll('.reveal').forEach(el => {
            observer.observe(el);
        });

        // Certificate carousel
        let currentCertificate = 0;
        const certificates = document.querySelectorAll('[id^="certificate-"]');
        const dots = document.querySelectorAll('.carousel-dot');

        function showCertificate(index) {
            certificates.forEach(cert => cert.style.display = 'none');
            dots.forEach(dot => dot.classList.remove('active'));
            
            certificates[index].style.display = 'block';
            dots[index].classList.add('active');
            currentCertificate = index;
        }

        // Auto-rotate certificates
        setInterval(() => {
            currentCertificate = (currentCertificate + 1) % certificates.length;
            showCertificate(currentCertificate);
        }, 4000);

        // Smooth scrolling for navigation links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                const target = document.querySelector(this.getAttribute('href'));
                if (target) {
                    target.scrollIntoView({
                        behavior: 'smooth',
                        block: 'start'
                    });
                }
            });
        });

        // Resume download function
        function downloadResume() {
            const resumeContent = `CHINTAKAYALA MANISH KUMAR
Nizamabad | ch.manishkumar2003@gmail.com | +91 7989992982
https://www.linkedin.com/in/manish-kumar7989/ | https://github.com/ChManish2003

ABOUT ME
• Highly organized and detail-oriented worker, with a drive to exceed expectations. Ability to analyze data, develop strategies, and provide solutions to complex problems. Seeking to leverage skills and knowledge to contribute to team success.

EDUCATION
SSC, Sri Chaitanya School                                                    June 2018 – June 2019
• GPA: 9.0

TSBIE, Narayana Junior College                                               July 2019 – June 2021
• Percentage: 93%

Gitam University, B.Tech Computer Science and Engineering                    June 2021 – June 2025
• GPA: 7.42

PROJECTS
Stock Market Prediction (Major)                                             2024
• Developed a Stock Market Prediction application using Python and machine learning techniques to analyze historical stock data and predict future trends. The project incorporates data preprocessing, feature extraction, and model training to provide insight into stock price movements. It includes a user-friendly interface to visualize predictions and offers tools to assist users in making informed investment decisions. It is a combination of hybrid model of machine learning algorithms LSTM and Random Forest.
• Tools used: Python, SQL, Machine Learning, Databases.

Pill Reminder Application                                                    2023
• The Pill Reminder Project is a web-based application designed to help users track their medication schedules, monitor pill consumption, and receive timely reminders for taking their medication. The app will automatically update the pill count as doses are taken and alert users when a refill is needed. This application provides a practical solution to a common healthcare challenge, particularly benefiting users managing multiple medications or chronic conditions.
• Tools Used: Python, UI (User Interface), JavaScript, Database, SMS or Pop-up Notifications.

INTERNSHIP
Innovate Intern (DSA using Java)                                           2024
• During my internship, I applied my knowledge of Data Structures and Algorithms in Java to solve real-world problems efficiently. I worked with arrays, linked lists, stacks, and queues to manage data, and implemented algorithms like searching and sorting to optimize application performance. This hands-on experience helped me improve my coding skills and contributed to building scalable features in the projects I was involved in.

TECHNOLOGIES
Languages: Java, SQL, Python
Technologies: SQL Server, GitHub, VS Code
Soft Skills: Problem Solving, Teamwork, Critical Thinking

CERTIFICATES
• Structured Query Language - IBM
• Machine Learning - Duke University
• Data Structures - IBM`;

            const blob = new Blob([resumeContent], { type: 'text/plain' });
            const url = URL.createObjectURL(blob);
            const link = document.createElement('a');
            link.href = url;
            link.download = 'Chintakayala_Manish_Kumar_Resume.txt';
            document.body.appendChild(link);
            link.click();
            document.body.removeChild(link);
            URL.revokeObjectURL(url);
        }

        // Mobile menu toggle (if needed)
        const hamburger = document.querySelector('.hamburger');
        const navMenu = document.querySelector('.nav-menu');

        if (hamburger && navMenu) {
            hamburger.addEventListener('click', () => {
                hamburger.classList.toggle('active');
                navMenu.classList.toggle('active');
            });
        }
    </script>
</body>
</html>
