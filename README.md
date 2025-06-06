<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Portofolio Digital - Nama Anda</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Arial', sans-serif;
            line-height: 1.6;
            color: #333;
            background-color: #f8f9fa;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        /* Navigation */
        nav {
            background: #fff;
            box-shadow: 0 2px 5px rgba(0,0,0,0.1);
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
        }

        nav .container {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 1rem 20px;
        }

        .logo {
            font-size: 1.5rem;
            font-weight: bold;
            color: #2c3e50;
        }

        .nav-links {
            display: flex;
            list-style: none;
            gap: 2rem;
        }

        .nav-links a {
            text-decoration: none;
            color: #333;
            font-weight: 500;
            transition: color 0.3s;
        }

        .nav-links a:hover {
            color: #3498db;
        }

        /* Hero Section */
        .hero {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            padding: 10rem 0 5rem;
            text-align: center;
            margin-top: 70px;
        }

        .hero h1 {
            font-size: 3rem;
            margin-bottom: 1rem;
            animation: fadeInUp 1s ease;
        }

        .hero p {
            font-size: 1.2rem;
            margin-bottom: 2rem;
            animation: fadeInUp 1s ease 0.3s both;
        }

        .hero-img {
            width: 200px;
            height: 200px;
            border-radius: 50%;
            margin: 2rem auto;
            background: #ddd;
            border: 5px solid white;
            animation: fadeInUp 1s ease 0.6s both;
        }

        /* Section Styles */
        section {
            padding: 5rem 0;
        }

        .section-title {
            text-align: center;
            font-size: 2.5rem;
            margin-bottom: 3rem;
            color: #2c3e50;
        }

        /* About Section */
        .about {
            background: white;
        }

        .about-content {
            display: grid;
            grid-template-columns: 1fr 2fr;
            gap: 3rem;
            align-items: center;
        }

        .about-text {
            font-size: 1.1rem;
            line-height: 1.8;
        }

        .skills {
            display: flex;
            flex-wrap: wrap;
            gap: 1rem;
            margin-top: 2rem;
        }

        .skill-tag {
            background: #3498db;
            color: white;
            padding: 0.5rem 1rem;
            border-radius: 25px;
            font-size: 0.9rem;
        }

        /* Projects Section */
        .projects-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
            margin-top: 3rem;
        }

        .project-card {
            background: white;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
            transition: transform 0.3s;
        }

        .project-card:hover {
            transform: translateY(-5px);
        }

        .project-img {
            width: 100%;
            height: 200px;
            background: #ddd;
            position: relative;
        }

        .project-info {
            padding: 1.5rem;
        }

        .project-title {
            font-size: 1.3rem;
            margin-bottom: 0.5rem;
            color: #2c3e50;
        }

        .project-desc {
            color: #666;
            margin-bottom: 1rem;
        }

        .project-links {
            display: flex;
            gap: 1rem;
        }

        .btn {
            display: inline-block;
            padding: 0.5rem 1rem;
            background: #3498db;
            color: white;
            text-decoration: none;
            border-radius: 5px;
            transition: background 0.3s;
        }

        .btn:hover {
            background: #2980b9;
        }

        .btn-secondary {
            background: #95a5a6;
        }

        .btn-secondary:hover {
            background: #7f8c8d;
        }

        /* Contact Section */
        .contact {
            background: #2c3e50;
            color: white;
        }

        .contact-content {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 3rem;
        }

        .contact-info h3 {
            margin-bottom: 1rem;
        }

        .contact-item {
            margin-bottom: 1rem;
            display: flex;
            align-items: center;
            gap: 0.5rem;
        }

        .contact-form {
            background: rgba(255,255,255,0.1);
            padding: 2rem;
            border-radius: 10px;
        }

        .form-group {
            margin-bottom: 1rem;
        }

        .form-group label {
            display: block;
            margin-bottom: 0.5rem;
        }

        .form-group input,
        .form-group textarea {
            width: 100%;
            padding: 0.75rem;
            border: none;
            border-radius: 5px;
            background: rgba(255,255,255,0.9);
        }

        textarea {
            height: 120px;
            resize: vertical;
        }

        /* Footer */
        footer {
            background: #1a1a1a;
            color: white;
            text-align: center;
            padding: 2rem 0;
        }

        .social-links {
            display: flex;
            justify-content: center;
            gap: 1rem;
            margin-bottom: 1rem;
        }

        .social-links a {
            display: inline-block;
            width: 40px;
            height: 40px;
            background: #3498db;
            color: white;
            text-decoration: none;
            border-radius: 50%;
            line-height: 40px;
            text-align: center;
            transition: background 0.3s;
        }

        .social-links a:hover {
            background: #2980b9;
        }

        /* Animations */
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

        /* Responsive Design */
        @media (max-width: 768px) {
            .nav-links {
                display: none;
            }

            .hero h1 {
                font-size: 2rem;
            }

            .about-content,
            .contact-content {
                grid-template-columns: 1fr;
            }

            .projects-grid {
                grid-template-columns: 1fr;
            }
        }

        /* Smooth Scrolling */
        html {
            scroll-behavior: smooth;
        }

        /* Loading Animation */
        .loading {
            opacity: 0;
            animation: fadeInUp 1s ease forwards;
        }
    </style>
</head>
<body>
    <!-- Navigation -->
    <nav>
        <div class="container">
            <div class="logo">Portfolio</div>
            <ul class="nav-links">
                <li><a href="#home">Home</a></li>
                <li><a href="#about">Tentang</a></li>
                <li><a href="#projects">Projects</a></li>
                <li><a href="#contact">Kontak</a></li>
            </ul>
        </div>
    </nav>

    <!-- Hero Section -->
    <section id="home" class="hero">
        <div class="container">
            <img src="/api/placeholder/200/200" alt="Profile Picture" class="hero-img">
            <h1>Nama Anda</h1>
            <p>Web Developer | UI/UX Designer | Creative Problem Solver</p>
        </div>
    </section>

    <!-- About Section -->
    <section id="about" class="about">
        <div class="container">
            <h2 class="section-title">Tentang Saya</h2>
            <div class="about-content">
                <div>
                    <img src="/api/placeholder/400/300" alt="About Image" style="width: 100%; border-radius: 10px;">
                </div>
                <div class="about-text">
                    <p>Halo! Saya adalah seorang developer yang passionate dalam menciptakan pengalaman digital yang menarik dan fungsional. Dengan pengalaman lebih dari 3 tahun di bidang web development, saya telah mengerjakan berbagai project mulai dari website company profile hingga aplikasi web kompleks.</p>
                    
                    <p>Saya selalu tertarik untuk belajar teknologi baru dan mencari solusi inovatif untuk setiap tantangan yang dihadapi. Mari berkolaborasi untuk mewujudkan ide digital Anda!</p>
                    
                    <div class="skills">
                        <span class="skill-tag">HTML/CSS</span>
                        <span class="skill-tag">JavaScript</span>
                        <span class="skill-tag">React</span>
                        <span class="skill-tag">Node.js</span>
                        <span class="skill-tag">Python</span>
                        <span class="skill-tag">UI/UX Design</span>
                        <span class="skill-tag">Figma</span>
                        <span class="skill-tag">Photoshop</span>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Projects Section -->
    <section id="projects" class="projects">
        <div class="container">
            <h2 class="section-title">Projects Terbaru</h2>
            <div class="projects-grid">
                <div class="project-card loading">
                    <div class="project-img">
                        <img src="/api/placeholder/300/200" alt="Project 1" style="width: 100%; height: 100%; object-fit: cover;">
                    </div>
                    <div class="project-info">
                        <h3 class="project-title">E-Commerce Website</h3>
                        <p class="project-desc">Website e-commerce modern dengan fitur pembayaran terintegrasi, dashboard admin, dan responsive design.</p>
                        <div class="project-links">
                            <a href="#" class="btn">Live Demo</a>
                            <a href="#" class="btn btn-secondary">GitHub</a>
                        </div>
                    </div>
                </div>

                <div class="project-card loading">
                    <div class="project-img">
                        <img src="/api/placeholder/300/200" alt="Project 2" style="width: 100%; height: 100%; object-fit: cover;">
                    </div>
                    <div class="project-info">
                        <h3 class="project-title">Mobile App UI Design</h3>
                        <p class="project-desc">Desain UI/UX untuk aplikasi mobile dengan fokus pada user experience yang intuitif dan modern.</p>
                        <div class="project-links">
                            <a href="#" class="btn">Lihat Design</a>
                            <a href="#" class="btn btn-secondary">Figma</a>
                        </div>
                    </div>
                </div>

                <div class="project-card loading">
                    <div class="project-img">
                        <img src="/api/placeholder/300/200" alt="Project 3" style="width: 100%; height: 100%; object-fit: cover;">
                    </div>
                    <div class="project-info">
                        <h3 class="project-title">Task Management App</h3>
                        <p class="project-desc">Aplikasi manajemen tugas dengan fitur collaboration real-time, built with React dan Node.js.</p>
                        <div class="project-links">
                            <a href="#" class="btn">Live Demo</a>
                            <a href="#" class="btn btn-secondary">GitHub</a>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section id="contact" class="contact">
        <div class="container">
            <h2 class="section-title" style="color: white;">Hubungi Saya</h2>
            <div class="contact-content">
                <div class="contact-info">
                    <h3>Mari Berkolaborasi!</h3>
                    <p>Saya terbuka untuk project freelance, pekerjaan full-time, atau sekadar diskusi tentang teknologi. Jangan ragu untuk menghubungi saya!</p>
                    
                    <div class="contact-item">
                        <span>📧</span>
                        <span>email@domain.com</span>
                    </div>
                    <div class="contact-item">
                        <span>📱</span>
                        <span>+62 812-3456-7890</span>
                    </div>
                    <div class="contact-item">
                        <span>📍</span>
                        <span>Jakarta, Indonesia</span>
                    </div>
                </div>

                <form class="contact-form">
                    <div class="form-group">
                        <label for="name">Nama</label>
                        <input type="text" id="name" name="name" required>
                    </div>
                    <div class="form-group">
                        <label for="email">Email</label>
                        <input type="email" id="email" name="email" required>
                    </div>
                    <div class="form-group">
                        <label for="message">Pesan</label>
                        <textarea id="message" name="message" required></textarea>
                    </div>
                    <button type="submit" class="btn" style="width: 100%;">Kirim Pesan</button>
                </form>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="container">
            <div class="social-links">
                <a href="#" title="LinkedIn">💼</a>
                <a href="#" title="GitHub">📂</a>
                <a href="#" title="Instagram">📷</a>
                <a href="#" title="Twitter">🐦</a>
            </div>
            <p>&copy; 2025 Nama Anda. All rights reserved.</p>
        </div>
    </footer>

    <script>
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

        // Form submission
        document.querySelector('.contact-form').addEventListener('submit', function(e) {
            e.preventDefault();
            alert('Terima kasih! Pesan Anda telah dikirim. Saya akan segera menghubungi Anda kembali.');
            this.reset();
        });

        // Loading animation for project cards
        const observerOptions = {
            threshold: 0.1,
            rootMargin: '0px 0px -50px 0px'
        };

        const observer = new IntersectionObserver(function(entries) {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.style.opacity = '1';
                    entry.target.style.transform = 'translateY(0)';
                }
            });
        }, observerOptions);

        document.querySelectorAll('.loading').forEach(el => {
            el.style.opacity = '0';
            el.style.transform = 'translateY(30px)';
            el.style.transition = 'opacity 0.6s ease, transform 0.6s ease';
            observer.observe(el);
        });

        // Active navigation link
        window.addEventListener('scroll', function() {
            const sections = document.querySelectorAll('section');
            const navLinks = document.querySelectorAll('.nav-links a');
            
            let current = '';
            sections.forEach(section => {
                const sectionTop = section.offsetTop;
                const sectionHeight = section.clientHeight;
                if (pageYOffset >= sectionTop - 200) {
                    current = section.getAttribute('id');
                }
            });

            navLinks.forEach(link => {
                link.classList.remove('active');
                if (link.getAttribute('href') === '#' + current) {
                    link.classList.add('active');
                }
            });
        });
    </script>

    <style>
        .nav-links a.active {
            color: #3498db;
            border-bottom: 2px solid #3498db;
        }
    </style>
</body>
</html>
