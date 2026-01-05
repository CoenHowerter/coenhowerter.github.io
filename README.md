<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Astrobiology Portfolio</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            line-height: 1.6;
            color: #e0e0e0;
            background: linear-gradient(135deg, #0a0e27 0%, #1a1f3a 50%, #0f1419 100%);
            min-height: 100vh;
        }

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

        nav {
            background: rgba(26, 31, 58, 0.9);
            backdrop-filter: blur(10px);
            padding: 1rem 0;
            position: relative;
            z-index: 100;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.5);
        }

        nav ul {
            list-style: none;
            display: flex;
            justify-content: center;
            align-items: baseline;
            flex-wrap: wrap;
            gap: 2rem;
        }

        nav a {
            color: #64c8ff;
            text-decoration: none;
            font-weight: 500;
            transition: all 0.3s;
            padding: 0.5rem 1rem;
            border-radius: 5px;
        }

        nav a:hover {
            background: rgba(100, 200, 255, 0.2);
            transform: translateY(-2px);
        }

        .container {
            max-width: 1200px;
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
        }

        h2 {
            color: #64c8ff;
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

        .research-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 1.5rem;
            margin-top: 1.5rem;
        }

        .research-card {
            background: rgba(15, 20, 40, 0.6);
            padding: 1.5rem;
            border-radius: 8px;
            border: 1px solid rgba(100, 200, 255, 0.2);
            transition: all 0.3s;
        }

        .research-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 8px 25px rgba(100, 200, 255, 0.2);
            border-color: #64c8ff;
        }

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
        }

        ul {
            margin-left: 2rem;
            margin-top: 1rem;
        }

        li {
            margin: 0.5rem 0;
            color: #c0d8e8;
        }

        li a {
            color: #64c8ff;
            text-decoration: none;
            transition: color 0.3s;
            border-bottom: 1px solid rgba(100, 200, 255, 0.3);
        }

        li a:hover {
            color: #a0d8ff;
            border-bottom-color: #a0d8ff;
        }

        @media (max-width: 768px) {
            header h1 {
                font-size: 2rem;
            }
            
            nav ul {
                flex-direction: column;
                gap: 0.5rem;
            }
            
            .container {
                padding: 1rem;
            }
        }
    </style>
</head>
<body>
    <div class="stars" id="stars"></div>

    <header>
        <h1>Coen Howerter</h1>
        <p>Astrobiology | Astrophysics</p>
    </header>

    <nav>
        <ul>
            <li><a href="#about">About</a></li>
            <li><a href="#research">Research</a></li>
            <li><a href="#projects">Projects</a></li>
            <li><a href="#skills">Skills</a></li>
            <li><a href="#contact">Contact</a></li>
        </ul>
    </nav>

    <div class="container">
        <section id="about">
            <h2>About Me</h2>
            <div style="display: flex; gap: 2rem; align-items: flex-start; flex-wrap: wrap;">
                <div style="flex: 1; min-width: 300px;">
                    <p>CHANGE ME (About Me Paragraph 1) - Write about your background, what drew you to astrobiology, and your academic interests.</p>
                    <p>CHANGE ME (About Me Paragraph 2) - Describe your career goals and what excites you most about studying life in the universe.</p>
                </div>
                <div style="flex: 0 0 250px;">
                    <img src="CHANGE ME (URL to your headshot image)" alt="Professional Headshot" style="width: 100%; border-radius: 10px; box-shadow: 0 8px 20px rgba(100, 200, 255, 0.3); border: 3px solid #64c8ff;">
                    <p style="text-align: center; margin-top: 0.5rem; font-size: 0.9rem; color: #a0d8ff;">Coen Howerter</p>
                </div>
            </div>
        </section>

        <section id="research">
            <h2>Research Interests</h2>
            <div class="research-grid">
                <div class="research-card">
                    <h3>CHANGE ME (Research Interest 1 Title)</h3>
                    <p>CHANGE ME (Research Interest 1 Description)</p>
                </div>
                <div class="research-card">
                    <h3>CHANGE ME (Research Interest 2 Title)</h3>
                    <p>CHANGE ME (Research Interest 2 Description)</p>
                </div>
                <div class="research-card">
                    <h3>CHANGE ME (Research Interest 3 Title)</h3>
                    <p>CHANGE ME (Research Interest 3 Description)</p>
                </div>
                <div class="research-card">
                    <h3>CHANGE ME (Research Interest 4 Title)</h3>
                    <p>CHANGE ME (Research Interest 4 Description)</p>
                </div>
            </div>
        </section>

        <section id="projects">
            <h2>Projects</h2>
            <h3>Biology & Chemistry</h3>
            <ul>
                <li><a href="CHANGE ME (Project 1 URL)" target="_blank">CHANGE ME (Project 1)</a></li>
                <li><a href="CHANGE ME (Project 2 URL)" target="_blank">CHANGE ME (Project 2)</a></li>
                <li><a href="CHANGE ME (Project 3 URL)" target="_blank">CHANGE ME (Project 3)</a></li>
                <li><a href="CHANGE ME (Project 4 URL)" target="_blank">CHANGE ME (Project 4)</a></li>
            </ul>
            
            <h3>Physics & Astronomy</h3>
            <ul>
                <li><a href="CHANGE ME (Project 1 URL)" target="_blank">CHANGE ME (Project 1)</a></li>
                <li><a href="CHANGE ME (Project 2 URL)" target="_blank">CHANGE ME (Project 2)</a></li>
                <li><a href="CHANGE ME (Project 3 URL)" target="_blank">CHANGE ME (Project 3)</a></li>
                <li><a href="CHANGE ME (Project 4 URL)" target="_blank">CHANGE ME (Project 4)</a></li>
            </ul>
            
            <h3>Python</h3>
            <ul>
                <li><a href="https://github.com/coenhowerter/LibraryPy" target="_blank">LibraryPy</a></li>
                <li><a href="CHANGE ME (Project 2 URL)" target="_blank">CHANGE ME (Project 2)</a></li>
                <li><a href="CHANGE ME (Project 3 URL)" target="_blank">CHANGE ME (Project 3)</a></li>
            </ul>
        </section>

        <section id="skills">
            <h2>Skills & Techniques</h2>
            <div class="skills">
                <span class="skill-tag">CHANGE ME (Skill 1)</span>
                <span class="skill-tag">CHANGE ME (Skill 2)</span>
                <span class="skill-tag">CHANGE ME (Skill 3)</span>
                <span class="skill-tag">CHANGE ME (Skill 4)</span>
                <span class="skill-tag">CHANGE ME (Skill 5)</span>
                <span class="skill-tag">CHANGE ME (Skill 6)</span>
                <span class="skill-tag">CHANGE ME (Skill 7)</span>
                <span class="skill-tag">CHANGE ME (Skill 8)</span>
                <span class="skill-tag">CHANGE ME (Skill 9)</span>
                <span class="skill-tag">CHANGE ME (Skill 10)</span>
            </div>
        </section>

        <section id="contact">
            <h2>Contact</h2>
            <div class="contact-info">
                <div class="contact-item">
                    <strong>Email:</strong>
                    <a href="mailto:coenhowerter@gmail.com">coenhowerter@gmail.com</a>
                </div>
                <div class="contact-item">
                    <strong>LinkedIn:</strong>
                    <a href="https://www.linkedin.com/in/coen-howerter/" target="_blank">LinkedIn</a>
                </div>
                <div class="contact-item">
                    <strong>GitHub:</strong>
                    <a href="https://github.com/coenhowerter" target="_blank">GitHub</a>
                </div>
                <div class="contact-item">
                    <strong>University:</strong>
                    <span>Florida Institute of Technology</span>
                </div>
            </div>
        </section>
    </div>

    <footer>
        <p>&copy; 2025 Coen Howerter | Astrobiology Student | Exploring Life in the Universe</p>
    </footer>

    <script>
        // Create animated stars
        const starsContainer = document.getElementById('stars');
        for (let i = 0; i < 100; i++) {
            const star = document.createElement('div');
            star.className = 'star';
            star.style.left = Math.random() * 100 + '%';
            star.style.top = Math.random() * 100 + '%';
            star.style.width = Math.random() * 2 + 1 + 'px';
            star.style.height = star.style.width;
            star.style.animationDelay = Math.random() * 3 + 's';
            starsContainer.appendChild(star);
        }

        // Smooth scrolling for navigation links
        document.querySelectorAll('nav a').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                const target = document.querySelector(this.getAttribute('href'));
                target.scrollIntoView({ behavior: 'smooth', block: 'start' });
            });
        });
    </script>
</body>
</html>
