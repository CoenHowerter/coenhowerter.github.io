<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Your Name - Portfolio</title>
    <style>
        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            line-height: 1.6;
            color: #e0e0e0;
            background: linear-gradient(135deg, #0a0e27 0%, #1a1f3a 50%, #0f1419 100%);
            min-height: 100vh;
        }

        /* Star Animation Background */
        .stars {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            pointer-events: none;
            z-index: 0;
        }

        .star {
            position: absolute;
            background: white;
            border-radius: 50%;
            animation: twinkle 3s infinite;
        }

        @keyframes twinkle {
            0%, 100% { opacity: 0.3; }
            50% { opacity: 1; }
        }

        /* Header */
        header {
            background: rgba(10, 14, 39, 0.8);
            backdrop-filter: blur(10px);
            padding: 2rem 0;
            text-align: center;
            border-bottom: 2px solid rgba(100, 200, 255, 0.3);
            position: relative;
            z-index: 1;
        }

        header h1 {
            font-size: 2.5rem;
            color: #64c8ff;
            margin-bottom: 0.5rem;
            text-shadow: 0 0 20px rgba(100, 200, 255, 0.5);
        }

        header p {
            font-size: 1.2rem;
            color: #a0d8ff;
        }

        /* Navigation */
        nav {
            background: rgba(26, 31, 58, 0.9);
            backdrop-filter: blur(10px);
            padding: 1rem 0;
            position: sticky; /* FIX: sticky keeps nav visible while scrolling */
            top: 0;
            z-index: 100;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.5);
        }

        nav ul {
            list-style: none;
            display: flex;
            justify-content: center;
            flex-wrap: wrap;
            gap: 2rem;
        }

        nav a {
            color: #64c8ff;
            text-decoration: none;
            font-weight: 500;
            padding: 0.5rem 1rem;
            border-radius: 5px;
            transition: all 0.3s;
            display: inline-block; /* FIX: moved here so transform works consistently */
        }

        nav a:hover {
            background: rgba(100, 200, 255, 0.2);
            transform: translateY(-2px);
            /* FIX: removed "display: inline-block" from here — it belongs on the base rule */
        }

        /* Main Content */
        .container {
            max-width: 1000px;
            margin: 0 auto;
            padding: 2rem;
            position: relative;
            z-index: 1;
        }

        section {
            background: rgba(26, 31, 58, 0.7);
            backdrop-filter: blur(10px);
            margin: 2rem 0;
            padding: 2rem;
            border-radius: 10px;
            border: 1px solid rgba(100, 200, 255, 0.2);
            box-shadow: 0 4px 20px rgba(0, 0, 0, 0.3);
            scroll-margin-top: 70px; /* FIX: prevents sticky nav from covering section headings on anchor jump */
        }

        h2 {
            color: #64c8ff;
            margin-top: 0;
            margin-bottom: 1.5rem;
            font-size: 2rem;
            border-bottom: 2px solid rgba(100, 200, 255, 0.3);
            padding-bottom: 0.5rem;
        }

        h3 {
            color: #a0d8ff;
            margin-top: 1.5rem;
            margin-bottom: 1rem;
        }

        p {
            margin-bottom: 1rem;
        }

        /* Project Cards */
        .project-card {
            background: rgba(15, 20, 40, 0.6);
            padding: 2rem;
            border-radius: 8px;
            border: 1px solid rgba(100, 200, 255, 0.2);
            transition: all 0.3s;
            margin-top: 1.5rem;
        }

        .project-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 8px 25px rgba(100, 200, 255, 0.2);
            border-color: #64c8ff;
        }

        .project-card a {
            color: #64c8ff;
            text-decoration: none;
            font-weight: bold;
            border-bottom: 1px solid rgba(100, 200, 255, 0.3);
            transition: all 0.3s;
        }

        .project-card a:hover {
            color: #a0d8ff;
            border-bottom-color: #a0d8ff;
        }

        /* Skills */
        .skills {
            display: flex;
            flex-wrap: wrap;
            gap: 1rem;
            margin-top: 1rem;
        }

        .skill-tag {
            background: rgba(100, 200, 255, 0.2);
            color: #64c8ff;
            padding: 0.5rem 1rem;
            border-radius: 20px;
            font-size: 0.9rem;
            border: 1px solid rgba(100, 200, 255, 0.3);
        }

        /* Contact */
        .contact-info {
            display: flex;
            flex-direction: column;
            gap: 1rem;
            margin-top: 1rem;
        }

        .contact-item {
            display: flex;
            align-items: center;
            gap: 1rem;
        }

        .contact-item a {
            color: #64c8ff;
            text-decoration: none;
            transition: color 0.3s;
        }

        .contact-item a:hover {
            color: #a0d8ff;
        }

        /* Footer */
        footer {
            background: rgba(10, 14, 39, 0.9);
            text-align: center;
            padding: 2rem;
            margin-top: 3rem;
            border-top: 2px solid rgba(100, 200, 255, 0.3);
            position: relative;
            z-index: 1;
        }

        footer p {
            color: #a0d8ff;
            margin-bottom: 0; /* FIX: removes extra bottom margin inside footer */
        }

        /* Mobile */
        @media (max-width: 768px) {
            header h1 { font-size: 2rem; }
            nav ul { flex-direction: column; align-items: center; gap: 0.5rem; } /* FIX: added align-items center for proper centering on mobile */
            .container { padding: 1rem; }
        }
    </style>
</head>
<body>

    <div class="stars" id="stars"></div>

    <header>
        <h1>Your Name</h1>
        <p>Software Developer &amp; Space Enthusiast</p>
    </header>

    <nav>
        <ul>
            <li><a href="#about">About</a></li>
            <li><a href="#projects">Projects</a></li>
            <li><a href="#skills">Skills</a></li>
            <li><a href="#contact">Contact</a></li>
        </ul>
    </nav>

    <div class="container">

        <section id="about">
            <h2>About Me</h2>
            <p>Welcome to my portfolio! I'm a passionate software developer with a love for exploring the intersection of technology and the cosmos. I build clean, efficient, and creative solutions.</p>
            <p>When I'm not coding, you'll find me stargazing or tinkering with new ideas.</p>
        </section>

        <section id="projects">
            <h2>Projects</h2>
            <div class="project-card">
                <h3>Project Alpha</h3>
                <p>A full-stack web application that does something amazing. Built with modern technologies and a focus on user experience.</p>
                <p><a href="https://github.com/yourusername/project-alpha" target="_blank" rel="noopener noreferrer">View on GitHub →</a></p>
                <!-- FIX: added target="_blank" + rel="noopener noreferrer" for security on external links -->
            </div>
            <div class="project-card">
                <h3>Project Beta</h3>
                <p>An open-source tool that solves a real-world problem. Contributions welcome!</p>
                <p><a href="https://github.com/yourusername/project-beta" target="_blank" rel="noopener noreferrer">View on GitHub →</a></p>
            </div>
        </section>

        <section id="skills">
            <h2>Skills</h2>
            <div class="skills">
                <span class="skill-tag">JavaScript</span>
                <span class="skill-tag">Python</span>
                <span class="skill-tag">React</span>
                <span class="skill-tag">Node.js</span>
                <span class="skill-tag">HTML &amp; CSS</span>
                <span class="skill-tag">Git</span>
                <span class="skill-tag">SQL</span>
                <span class="skill-tag">REST APIs</span>
            </div>
        </section>

        <section id="contact">
            <h2>Contact</h2>
            <div class="contact-info">
                <div class="contact-item">
                    <span>✉</span>
                    <a href="mailto:you@example.com">you@example.com</a>
                </div>
                <div class="contact-item">
                    <span>🐙</span>
                    <a href="https://github.com/yourusername" target="_blank" rel="noopener noreferrer">github.com/yourusername</a>
                </div>
                <div class="contact-item">
                    <span>💼</span>
                    <a href="https://linkedin.com/in/yourusername" target="_blank" rel="noopener noreferrer">linkedin.com/in/yourusername</a>
                </div>
            </div>
        </section>

    </div>

    <footer>
        <p>&copy; 2026 Your Name. Built with ☕ and curiosity.</p>
    </footer>

    <script>
        // Star background
        const starsContainer = document.getElementById('stars');
        for (let i = 0; i < 120; i++) {
            const star = document.createElement('div');
            star.className = 'star';
            const size = Math.random() * 3 + 1;
            star.style.cssText = `width:${size}px; height:${size}px; top:${Math.random() * 100}%; left:${Math.random() * 100}%; animation-delay:${Math.random() * 3}s; animation-duration:${2 + Math.random() * 3}s;`;
            starsContainer.appendChild(star);
        }

        // FIX: smooth scrolling for nav anchor links
        document.querySelectorAll('nav a[href^="#"]').forEach(link => {
            link.addEventListener('click', function (e) {
                e.preventDefault();
                const target = document.querySelector(this.getAttribute('href'));
                if (target) target.scrollIntoView({ behavior: 'smooth' });
            });
        });
    </script>

</body>
</html>
