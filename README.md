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

        /* STAR BACKGROUND */
        .stars {
            position: fixed;
            inset: 0;
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
            text-shadow: 0 0 20px rgba(100, 200, 255, 0.5);
        }

        header p {
            font-size: 1.2rem;
            color: #a0d8ff;
        }

        nav {
            background: rgba(26, 31, 58, 0.9);
            padding: 1rem 0;
            position: sticky;
            top: 0;
            z-index: 100;
        }

        nav ul {
            list-style: none;
            display: flex;
            justify-content: center;
            gap: 2rem;
            flex-wrap: wrap;
        }

        nav a {
            color: #64c8ff;
            text-decoration: none;
            padding: 0.5rem 1rem;
            border-radius: 5px;
            transition: 0.3s;
        }

        nav a:hover {
            background: rgba(100, 200, 255, 0.2);
        }

        .container {
            max-width: 1200px;
            margin: auto;
            padding: 2rem;
            position: relative;
            z-index: 1;
        }

        section {
            background: rgba(26, 31, 58, 0.7);
            padding: 2rem;
            margin: 2rem 0;
            border-radius: 10px;
            border: 1px solid rgba(100, 200, 255, 0.2);
        }

        h2 {
            color: #64c8ff;
            margin-bottom: 1.5rem;
            border-bottom: 2px solid rgba(100, 200, 255, 0.3);
        }

        h3 {
            color: #a0d8ff;
            margin: 1rem 0 0.5rem;
        }

        /* ABOUT SECTION FIX */
        .about-layout {
            display: flex;
            gap: 2rem;
            align-items: center;
            flex-wrap: wrap;
        }

        .about-layout img {
            width: 250px;
            border-radius: 10px;
            border: 3px solid #64c8ff;
            box-shadow: 0 8px 20px rgba(100, 200, 255, 0.3);
            aspect-ratio: 1 / 1;
            object-fit: cover;
        }

        .research-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 1.5rem;
        }

        .research-card {
            background: rgba(15, 20, 40, 0.6);
            padding: 1.5rem;
            border-radius: 8px;
            transition: 0.3s;
        }

        .research-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 8px 25px rgba(100, 200, 255, 0.2);
        }

        ul {
            margin-left: 1.5rem;
        }

        li {
            margin: 0.5rem 0;
        }

        li a {
            color: #64c8ff;
            text-decoration: none;
        }

        .skills {
            display: flex;
            flex-wrap: wrap;
            gap: 1rem;
        }

        .skill-tag {
            background: rgba(100, 200, 255, 0.2);
            padding: 0.5rem 1rem;
            border-radius: 20px;
            font-size: 0.9rem;
        }

        .contact-info {
            display: flex;
            flex-direction: column;
            gap: 1rem;
        }

        footer {
            text-align: center;
            padding: 2rem;
            color: #a0d8ff;
        }

        @media (max-width: 768px) {
            header h1 { font-size: 2rem; }
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
    <div class="about-layout">
        <div>
            <p>
                I am an undergraduate student with strong interests in astrobiology and astrophysics, particularly
                in observational and experimental approaches to studying life in extreme environments.
            </p>
            <p>
                My long-term goal is to contribute to space missions and research efforts that investigate planetary
                habitability, biosignatures, and the origins of life beyond Earth.
            </p>
        </div>

        <img src="assets/images/headshot.jpg" alt="Professional Headshot">
    </div>
</section>

<section id="research">
    <h2>Research Interests</h2>
    <div class="research-grid">
        <div class="research-card">
            <h3>Planetary Habitability</h3>
            <p>Studying environmental constraints on life in extreme planetary conditions.</p>
        </div>
        <div class="research-card">
            <h3>Astrobiological Instrumentation</h3>
            <p>Development and analysis of tools for detecting biosignatures.</p>
        </div>
        <div class="research-card">
            <h3>Observational Astronomy</h3>
            <p>Telescope-based data acquisition and image processing.</p>
        </div>
        <div class="research-card">
            <h3>Origins of Life</h3>
            <p>Chemical and physical pathways toward prebiotic chemistry.</p>
        </div>
    </div>
</section>

<section id="projects">
    <h2>Projects</h2>

    <h3>Python</h3>
    <ul>
        <li><a href="https://github.com/coenhowerter/LibraryPy" target="_blank">LibraryPy</a></li>
    </ul>
</section>

<section id="skills">
    <h2>Skills & Techniques</h2>
    <div class="skills">
        <span class="skill-tag">Python</span>
        <span class="skill-tag">Data Analysis</span>
        <span class="skill-tag">Astronomical Imaging</span>
        <span class="skill-tag">Linux</span>
        <span class="skill-tag">Git & GitHub</span>
        <span class="skill-tag">Scientific Writing</span>
    </div>
</section>

<section id="contact">
    <h2>Contact</h2>
    <div class="contact-info">
        <div><strong>Email:</strong> <a href="mailto:coenhowerter@gmail.com">coenhowerter@gmail.com</a></div>
        <div><strong>Phone:</strong> <a href="tel:+1XXXXXXXXXX">+1 (XXX) XXX-XXXX</a></div>
        <div><strong>LinkedIn:</strong> <a href="https://www.linkedin.com/in/coen-howerter/" target="_blank">LinkedIn</a></div>
        <div><strong>GitHub:</strong> <a href="https://github.com/coenhowerter" target="_blank">GitHub</a></div>
        <div><strong>University:</strong> Florida Institute of Technology</div>
    </div>
</section>

</div>

<footer>
    &copy; 2025 Coen Howerter — Astrobiology Portfolio
</footer>

<script>
    const stars = document.getElementById('stars');
    for (let i = 0; i < 100; i++) {
        const s = document.createElement('div');
        s.className = 'star';
        s.style.left = Math.random() * 100 + '%';
        s.style.top = Math.random() * 100 + '%';
        s.style.width = s.style.height = Math.random() * 2 + 1 + 'px';
        s.style.animationDelay = Math.random() * 3 + 's';
        stars.appendChild(s);
    }

    document.querySelectorAll('nav a').forEach(link => {
        link.addEventListener('click', e => {
            e.preventDefault();
            document.querySelector(link.getAttribute('href'))
                .scrollIntoView({ behavior: 'smooth' });
        });
    });
</script>
</body>
</html>
