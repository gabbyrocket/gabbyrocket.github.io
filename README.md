<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Gabrielle Yeager | Engineering Portfolio</title>

<style>
body {
    margin: 0;
    font-family: 'Segoe UI', sans-serif;
    color: white;
    background: black;
    overflow-x: hidden;
}

/* STARFIELD BACKGROUND */
.stars, .stars2 {
    position: fixed;
    width: 200%;
    height: 200%;
    background: transparent url('https://www.transparenttextures.com/patterns/stardust.png');
    animation: moveStars 200s linear infinite;
    z-index: -2;
}
.stars2 {
    animation-duration: 300s;
    opacity: 0.5;
}

@keyframes moveStars {
    from {transform: translate(0,0);}
    to {transform: translate(-1000px,-1000px);}
}

/* SHOOTING STAR */
.shooting-star {
    position: fixed;
    width: 2px;
    height: 80px;
    background: linear-gradient(white, transparent);
    top: 10%;
    left: 80%;
    transform: rotate(45deg);
    animation: shoot 6s infinite;
}

@keyframes shoot {
    0% {opacity: 0; transform: translate(0,0) rotate(45deg);}
    10% {opacity: 1;}
    100% {transform: translate(-800px,800px) rotate(45deg); opacity: 0;}
}

/* HERO */
header {
    text-align: center;
    padding: 120px 20px;
}

header h1 {
    font-size: 3rem;
}

header p {
    color: #9ca3af;
    max-width: 700px;
    margin: auto;
}

/* NAV */
nav {
    text-align: center;
    padding: 15px;
    background: rgba(0,0,0,0.85);
    position: sticky;
    top: 0;
}

nav a {
    margin: 0 15px;
    color: #38bdf8;
    text-decoration: none;
}

/* SECTIONS */
section {
    max-width: 1000px;
    margin: auto;
    padding: 80px 20px;
}

/* CARDS */
.card {
    background: rgba(30,41,59,0.85);
    padding: 20px;
    margin-top: 20px;
    border-radius: 12px;
    opacity: 0;
    transform: translateY(40px);
    transition: all 0.8s ease;
}

.card.visible {
    opacity: 1;
    transform: translateY(0);
}

/* GRID */
.grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
    gap: 20px;
}

/* FOOTER */
footer {
    text-align: center;
    padding: 30px;
    color: #6b7280;
}
</style>
</head>

<body>

<div class="stars"></div>
<div class="stars2"></div>
<div class="shooting-star"></div>

<header>
<h1>Gabrielle Yeager</h1>
<p>
Engineering Student → Incoming Aerospace Graduate Student<br><br>
Building rockets. Documenting the journey. Aiming beyond Earth.
</p>
</header>

<nav>
<a href="#about">About</a>
<a href="#projects">Projects</a>
<a href="#experience">Experience</a>
<a href="#content">Content</a>
<a href="#contact">Contact</a>
</nav>

<section id="about">
<h2>About Me</h2>
<div class="card">
<p>
Aerospace engineering graduate student specializing in propulsion, with hands-on experience in high-power rocketry, structural
design, FEA, and hardware fabrication. Skilled in SolidWorks, ANSYS, MATLAB, and Simulink, with a track record of taking
systems from concept through tested hardware. Pursuing a Master of Science in Aerospace Engineering at USC with a propulsion
specialization, targeting roles in aerospace and defense.
</p>
</div>
</section>

<section id="projects">
<h2>Projects 🚀</h2>
<div class="grid">

<div class="card">
<h3>Flexible End Effector</h3>
<p>Designed structural components, latch mechanisms, and guide-arm assemblies in SolidWorks/Fusion 360, producing full assembly drawings and tolerance analyses for deliverables.</p>
<p>Performed FEA on structural members to evaluate stress, deflection, and safety factors; iterated the design for stiffness, weight reduction, and manufacturability.</p>
<p>Fabricated custom aluminum hardware using CNC machining, drilling/tapping/ metal cutting, and precision press-fit operations; built and assembled motor mounts, L-bars, linear-rail supports, bearing housings, and latch hardware.</p>
<p>Integrated hardware with motors, linear rails, sensors, and software controls; developed and executed load testing, grip-force evaluation, cycle testing, and reliability validation, taking the design from concept through tested hardware.</p>
</div>

<div class="card">
<h3>High-Powered Rocketry NAR - Level 1 & 2 Certification</h3>
<p>Designed, built, and launched high-power rockets on H and K-class motors to altitudes up to 9,000 ft, integrating avionics, motor retention, and recovery deployment systems.</p>
</div>

</div>
</section>

<section id="experience">
<h2>Experience</h2>

<div class="card">
<h3>Mechanical Engineering Peer Tutor</h3>
<p>Teaching Thermo, Fluids, and CAD systems.</p>
</div>

<div class="card">
<h3>Research Assistant</h3>
<p>Worked on advanced materials and sustainability-focused engineering research.</p>
</div>

</section>

<section id="content">
<h2>Content Journey 🌌</h2>

<div class="card">
<p>
Follow my journey into aerospace engineering as I begin my Master’s and continue building toward a career in the space industry.
</p>
<p><strong>Instagram:</strong> @gabbyrocket</p>
</div>

</section>

<script>
/* SCROLL ANIMATIONS */
const cards = document.querySelectorAll('.card');

const observer = new IntersectionObserver(entries => {
    entries.forEach(entry => {
        if(entry.isIntersecting){
            entry.target.classList.add('visible');
        }
    });
});

cards.forEach(card => observer.observe(card));
</script>

</body>
</html>
