<html></html>
body {
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    line-height: 1.6;
    color: #e0e0e0;
    background: linear-gradient(135deg, #0a0e27 0%, #1a1f3a 50%, #0f1419 100%);
    min-height: 100vh;
    margin: 0;
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

/* Header & Navigation */
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
    margin-top: 0;
}

header p {
    font-size: 1.2rem;
    color: #a0d8ff;
    margin: 0;
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
    margin: 0;
    padding: 0;
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

/* Main Content Layout */
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

/* Single Project Highlight */
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

/* Skills & Contact */
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
    margin: 0;
}

/* Mobile Responsiveness */
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
