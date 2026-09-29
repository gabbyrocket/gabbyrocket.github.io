<html lang="en">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<title>Gabrielle Yeager | Aerospace Portfolio</title>
<meta name="description" content="Portfolio of Gabrielle Yeager: propulsion, rocketry, projects, skills and contact.">
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Big+Shoulders+Display:wght@700;800&family=Space+Grotesk:wght@400;500&display=swap" rel="stylesheet">
<style>
:root{
  --void:#040614; --hull:#f2f4ff; --muted:#a3abd0; --panel:rgba(12,16,44,.78); --line:rgba(160,175,255,.2);
  --ember:#ff6a2b; --flame:#ffc247; --signal:#5fe0ee; --nebula:#7b6cff;
  --display:"Big Shoulders Display","Arial Narrow",Impact,sans-serif; --body:"Space Grotesk","Segoe UI",system-ui,sans-serif;
  color-scheme:dark;
}
*{box-sizing:border-box;margin:0}
html{scroll-behavior:smooth;scroll-padding-top:80px}
body{font:17px/1.65 var(--body);color:var(--hull);background:
  radial-gradient(50vw 45vh at 85% 8%,rgba(123,108,255,.28),transparent 70%),
  radial-gradient(50vw 40vh at 5% 60%,rgba(95,224,238,.1),transparent 70%),
  radial-gradient(60vw 40vh at 60% 100%,rgba(255,106,43,.16),transparent 70%),var(--void);background-attachment:fixed}
#sky{position:fixed;inset:0;width:100%;height:100%;z-index:-1}
a{color:var(--signal)} a:hover{color:var(--flame)}
:focus-visible{outline:2px solid var(--flame);outline-offset:3px;border-radius:6px}
h1,h2,h3{font-family:var(--display);line-height:1.05;text-transform:uppercase;letter-spacing:.01em}

/* Mission-control bar */
nav{position:fixed;top:0;left:0;right:0;z-index:5;background:rgba(4,6,20,.85);backdrop-filter:blur(10px);border-bottom:1px solid var(--line)}
nav ul{list-style:none;display:flex;gap:4px;padding:8px 16px;overflow-x:auto;max-width:1100px;margin:auto}
nav a{display:block;padding:5px 14px;border-radius:4px;color:var(--muted);text-decoration:none;font-size:.9rem;white-space:nowrap}
nav a:hover{color:var(--hull);background:rgba(255,106,43,.18)}

/* Altitude gauge: the rocket climbs as you scroll */
.gauge{position:fixed;right:18px;top:90px;bottom:40px;width:2px;background:var(--line);z-index:4}
.gauge svg{position:absolute;left:-11px;top:0;width:24px;transform:translateY(0)}
@media(max-width:900px){.gauge{display:none}}

/* Hero */
.hero{max-width:1100px;margin:auto;padding:110px 24px 50px;min-height:100vh;display:grid;grid-template-columns:1.2fr .8fr;align-items:center;gap:30px}
.hero h1{font-size:clamp(3.6rem,11vw,8rem);font-weight:800}
.hero h1 span{color:var(--ember)}
.headline{font-size:1.2rem;margin-top:18px;max-width:34ch}
.loc{color:var(--muted);margin-top:8px}
.actions{display:flex;flex-wrap:wrap;gap:12px;margin-top:28px}
.btn{padding:10px 22px;border-radius:4px;font-weight:500;text-decoration:none;border:1px solid var(--signal);color:var(--signal)}
.btn.primary{background:var(--ember);border-color:var(--ember);color:#170a04}
.btn:hover{background:rgba(95,224,238,.15);color:var(--hull)}
.btn.primary:hover{background:var(--flame);color:#170a04}
.pad{position:relative;width:min(300px,70vw);margin:auto}
.pad svg{width:100%;height:auto;overflow:visible;animation:hover 4s ease-in-out infinite}
.flame{transform-origin:100px 262px;animation:burn .16s ease-in-out infinite alternate}
@keyframes burn{to{transform:scaleY(1.25) scaleX(.9)}}
@keyframes hover{50%{transform:translateY(-10px)}}

/* Sections */
main{max-width:1100px;margin:auto;padding:0 24px 40px}
section{padding:60px 0}
h2{font-size:clamp(2rem,5vw,3rem);font-weight:800;margin-bottom:8px}
h2 + .sub{color:var(--muted);margin-bottom:32px;max-width:60ch}
.brief{display:grid;grid-template-columns:1.5fr 1fr;gap:36px;align-items:start}
.lead{font-size:1.15rem;max-width:62ch}
.readout{background:var(--panel);border:1px solid var(--line);border-top:3px solid var(--ember);border-radius:6px;padding:8px 22px}
.readout div{display:flex;justify-content:space-between;gap:18px;padding:11px 0;border-top:1px solid var(--line)}
.readout div:first-child{border-top:0}
.readout dt{color:var(--muted)} .readout dd{text-align:right}

/* Flight path: three stages, current stage first */
.stage{display:grid;grid-template-columns:150px 1fr;gap:26px;padding:28px 0;border-top:1px solid var(--line)}
.stage:first-of-type{border-top:0}
.tag{position:sticky;top:80px;align-self:start}
.tag b{display:block;font:800 2.6rem var(--display);color:var(--ember);line-height:1}
.tag span{color:var(--muted);font-size:.9rem}
.cards{display:grid;grid-template-columns:repeat(auto-fit,minmax(280px,1fr));gap:16px}
.card{background:var(--panel);border:1px solid var(--line);border-radius:6px;padding:20px 22px}
.card.live{border-color:var(--ember);box-shadow:0 0 30px rgba(255,106,43,.18)}
.card.wide{grid-column:1/-1}
.card h3{font-size:1.35rem;font-weight:700}
.where{color:var(--signal);font-size:.95rem}
.when{color:var(--muted);font-size:.86rem}
.card ul{margin:10px 0 0 18px;color:var(--muted);font-size:.96rem}
.card li+li{margin-top:4px}
.roles{list-style:none;margin:10px 0 0;padding:0;color:var(--muted);font-size:.96rem}
.roles li{display:flex;justify-content:space-between;gap:14px;padding:6px 0;border-top:1px solid var(--line)}
.roles li span:last-child{white-space:nowrap;font-size:.86rem}

/* Payloads (projects) */
.payloads{display:grid;grid-template-columns:repeat(auto-fit,minmax(270px,1fr));gap:18px}
.payload{background:var(--panel);border:1px solid var(--line);border-radius:6px;padding:0 0 20px;overflow:hidden}
.payload .bay{height:8px;background:repeating-linear-gradient(90deg,var(--ember) 0 18px,#170a04 18px 26px)}
.payload h3,.payload p,.payload .chips,.payload .links{margin-left:22px;margin-right:22px}
.payload h3{font-size:1.4rem;margin-top:18px}
.payload p{color:var(--muted);margin-top:6px;font-size:.98rem}
.links{margin-top:12px;display:flex;gap:16px;font-size:.95rem}
.chips{display:flex;flex-wrap:wrap;gap:8px}
.chip{padding:4px 12px;border-radius:4px;font-size:.9rem;border:1px solid var(--line);background:rgba(123,108,255,.12)}
.patches{display:flex;flex-wrap:wrap;gap:24px;margin-top:30px}
.patch{width:130px;text-align:center;font-size:.9rem}
.patch b{display:grid;place-items:center;width:72px;height:72px;margin:0 auto 8px;border-radius:50%;border:2px dashed var(--flame);font:700 1.5rem var(--display);color:var(--flame)}
.patch small{display:block;color:var(--muted)}
.toolkit{display:grid;grid-template-columns:repeat(auto-fit,minmax(250px,1fr));gap:28px}
.toolkit h3{font-size:1.2rem;color:var(--flame);margin-bottom:10px}

/* Contact */
.contact{text-align:center}
.contact h2{margin-bottom:14px}
.mail{display:inline-block;margin:10px 0 18px;font:800 clamp(1.8rem,6vw,3.2rem) var(--display);text-decoration:none;border-bottom:3px solid var(--ember);color:var(--hull)}
.mail:hover{color:var(--flame)}
footer{text-align:center;color:var(--muted);font-size:.88rem;padding:20px 0 40px}

@media(max-width:800px){
  .hero{grid-template-columns:1fr;padding-top:90px;min-height:auto}
  .pad{order:-1;width:min(180px,45vw)}
  .brief,.stage{grid-template-columns:1fr}
  .tag{position:static}
  .tag b{display:inline;font-size:2rem;margin-right:10px}
}
@media(prefers-reduced-motion:reduce){html{scroll-behavior:auto}.pad svg,.flame{animation:none}}
</style>
</head>
<body>
<canvas id="sky" aria-hidden="true"></canvas>

<nav aria-label="Sections">
  <ul>
    <li><a href="#top">Launch</a></li>
    <li><a href="#about">Briefing</a></li>
    <li><a href="#experience">Flight path</a></li>
    <li><a href="#projects">Payloads</a></li>
    <li><a href="#education">Training</a></li>
    <li><a href="#skills">Toolkit</a></li>
    <li><a href="#contact">Contact</a></li>
  </ul>
</nav>

<div class="gauge" aria-hidden="true">
  <svg id="climber" viewBox="0 0 24 40"><path d="M12 1c5 6 6 14 5 24H7C6 15 7 7 12 1z" fill="#f2f4ff"/><circle cx="12" cy="12" r="2.4" fill="#5fe0ee"/><path d="M7 20l-5 9 5-2zM17 20l5 9-5-2z" fill="#ff6a2b"/><path d="M9 26h6l-3 12z" fill="#ffc247"/></svg>
</div>

<header class="hero" id="top">
  <div>
    <h1>Gabrielle <span>Y.</span></h1>
    <p class="headline">Aerospace Engineering graduate student at the University of Southern California, focused on propulsion.</p>
    <p class="loc">Los Angeles, California</p>
    <div class="actions">
      <a class="btn primary" href="#contact">Contact me</a>
      <a class="btn" href="https://github.com/gabbyrocket" target="_blank" rel="noopener">GitHub</a>
      <a class="btn" href="https://www.linkedin.com/in/gabrielle-y-240b4028a/" target="_blank" rel="noopener">LinkedIn</a>
      <a class="btn" href="resume.pdf">Résumé</a>
    </div>
  </div>
  <div class="pad" role="img" aria-label="Illustration of a rocket with an engine flame">
    <svg viewBox="0 0 200 300">
      <g class="flame"><path d="M84 236c-4 22 4 44 16 62 12-18 20-40 16-62z" fill="#ff6a2b"/><path d="M92 236c-2 14 2 28 8 40 6-12 10-26 8-40z" fill="#ffc247"/></g>
      <path d="M100 6c34 36 44 96 36 210H64C56 102 66 42 100 6z" fill="#f2f4ff"/>
      <path d="M100 6c34 36 44 96 36 210h-18C124 110 118 50 100 6z" fill="#c9cdf0"/>
      <path d="M64 150L26 214l4 26 34-22zM136 150l38 64-4 26-34-22z" fill="#ff6a2b"/>
      <rect x="86" y="216" width="28" height="22" rx="3" fill="#5c6390"/>
      <circle cx="100" cy="104" r="19" fill="#182055" stroke="#5fe0ee" stroke-width="5"/>
      <circle cx="94" cy="98" r="5" fill="#5fe0ee" opacity=".6"/>
      <rect x="64" y="176" width="72" height="8" fill="#ff6a2b"/>
    </svg>
  </div>
</header>

<main>
  <section id="about">
    <h2>Mission briefing</h2>
    <div class="brief">
      <p class="lead">Aerospace Engineering graduate student specializing in propulsion, with hands-on experience in high-power rocketry, structural design, FEA, and hardware fabrication. Skilled in CAD modeling, ANSYS, MATLAB, and Simulink, with a track record of taking systems from concept through tested hardware.</p>
      <dl class="readout">
        <div><dt>Base</dt><dd>Los Angeles, California</dd></div>
        <div><dt>Academy</dt><dd>University of Southern California</dd></div>
        <div><dt>Focus</dt><dd>Propulsion</dd></div>
      </dl>
    </div>
  </section>
  <section id="experience">
    <h2>Flight path</h2>
    <p class="sub">Three stages, newest first.</p>
    <div class="stage">
      <div class="tag"><b>Stage 3</b><span>Graduate<br>2026 – now</span></div>
      <div class="cards">
        <div class="card live wide">
          <h3>Engine Design Engineer</h3>
          <p class="where">USC Liquid Propulsion Laboratory</p>
          <p class="when">Aug 2026 – Present</p>
          <ul>
            <li>Develop and update CAD models of Nova’s coaxial-swirl injector, incorporating design iterations and engineering requirements.</li>
            <li>Perform FEA on injector components to evaluate stress, deformation, and design integrity under operating conditions.</li>
            <li>Conduct CFD analyses of injector flow behavior to support evaluation of fluid-flow and atomization characteristics.</li>
            <li>Work with the team to fold FEA/CFD results into design iterations, supporting performance and manufacturability.</li>
          </ul>
        </div>
      </div>
    </div>
    <div class="stage">
      <div class="tag"><b>Stage 2</b><span>Florida Tech<br>2023 – 2025</span></div>
      <div class="cards">
        <div class="card wide">
          <h3>AIAA Florida Tech</h3>
          <p class="where">Officer and representative roles</p>
          <ul class="roles">
            <li><span>Treasurer</span><span>Aug 2024 – Dec 2025</span></li>
            <li><span>Safety Chair / Safety &amp; Legal Compliance Officer</span><span>Aug 2023 – Dec 2025</span></li>
            <li><span>Social Media Chair</span><span>Aug 2023 – Dec 2024</span></li>
            <li><span>Student Government Association Representative</span><span>Aug 2023 – Dec 2024</span></li>
          </ul>
          <ul>
            <li>Managed finances, budgets, funding requests, and reimbursements for AIAA events, projects, and competition teams.</li>
            <li>Maintained the safety binder and procedures, working with university EHS to meet requirements and applicable BiProp standards, and identifying hazards across competition teams.</li>
            <li>Ran social media and promotion, creating graphics and announcements to highlight projects and events.</li>
            <li>Represented AIAA at SGA meetings and relayed updates, policies, and funding opportunities to members.</li>
          </ul>
        </div>
        <div class="card">
          <h3>Peer Tutor</h3>
          <p class="where">Florida Institute of Technology</p>
          <p class="when">Sept 2025 – Dec 2025</p>
          <ul>
            <li>Taught one-on-one and small groups in Thermodynamics II, Fluid Mechanics, and Solids Modeling (Creo).</li>
            <li>Adapted methods to different learning styles to build comprehension and confidence.</li>
          </ul>
        </div>
        <div class="card">
          <h3>Volunteer Student Course Proctor</h3>
          <p class="where">AIAA</p>
          <p class="when">Mar 2025 – May 2025</p>
          <ul>
            <li>Hosted online short courses: tech checks, recordings, audio controls, and troubleshooting.</li>
            <li>Introduced instructors, explained procedures, and moderated Q&amp;A across 8–36 hours of live instruction.</li>
          </ul>
        </div>
        <div class="card">
          <h3>Volunteer Undergraduate Research Assistant</h3>
          <p class="where">He Group</p>
          <p class="when">Oct 2024 – Feb 2025</p>
          <ul><li>Supported water security research on metal-organic frameworks (MOFs), synthesizing them and running spray-dry experiments with a graduate student.</li></ul>
        </div>
        <div class="card">
          <h3>Campus Ambassador</h3>
          <p class="where">Hot Girl Walk</p>
          <p class="when">Nov 2024 – Dec 2025</p>
          <ul><li>Built a supportive student community around wellness and personal growth, representing a global female empowerment brand on campus.</li></ul>
        </div>
        <div class="card">
          <h3>Lead Engineer</h3>
          <p class="where">NASA L'SPACE Academy</p>
          <p class="when">Jan 2024 – Apr 2024</p>
          <!-- Add 1-2 bullets on what you built or led -->
        </div>
      </div>
    </div>
    <div class="stage">
      <div class="tag"><b>Stage 1</b><span>Launch pad<br>2016 – 2021</span></div>
      <div class="cards">
        <div class="card">
          <h3>Payload Sub-Systems Lead</h3>
          <p class="where">Rocketbirds</p>
          <p class="when">Aug 2020 – May 2021</p>
          <!-- Add 1-2 bullets -->
        </div>
        <div class="card">
          <h3>VP, Lead Electrical, Media and Marketing</h3>
          <p class="where">FIRST Robotics: FRC Team 5429, FTC Team 12445</p>
          <p class="when">Aug 2016 – May 2020 &middot; Also FLL Judge (2016–2020)</p>
          <!-- Add bullets -->
        </div>
        <div class="card">
          <h3>Media and Marketing, Summer Camp Mentor</h3>
          <p class="where">VEX Robotics: Team 7853</p>
          <p class="when">Aug 2016 – May 2020 &middot; VEX IQ camp mentor (2018–2020)</p>
          <!-- Add bullets -->
        </div>
      </div>
    </div>
  </section>

  <section id="projects">
    <h2>Payloads</h2>
    <p class="sub">Things I've built. Replace these three with your own.</p>
    <div class="payloads">
      <article class="payload"><div class="bay"></div>
        <h3>NAR Level 2 High-Power Rocketry Certification</h3>
        <p>Used OpenRocket to evaluate the vehicles's predicted performance. Fabricated and assembled the necessary flight hardware. Integrated avionics/GPS and prepared the vehicle for high-power flight. The rocket reached approximately 9,000 ft using a K motor. The experience strengthened my interest in propulsion and aerospace systems by showing how closely propulsion, aerodynamics, structures, avionics, and flight operations are connected.</p>
        <div class="chips" style="margin-top:12px"><span class="chip">OpenRocket</span><span class="chip">High-Power Rocketry</span></div>
        </div>
      </article>
      <article class="payload"><div class="bay"></div>
        <h3>Project Two</h3>
        <p>One or two sentences on what it does and why you built it.</p>
        <div class="chips" style="margin-top:12px"><span class="chip">CAD</span><span class="chip">Fabrication</span></div>
        <div class="links"><a href="https://github.com/gabbyrocket/project-two" target="_blank" rel="noopener">Code</a></div>
      </article>
      <article class="payload"><div class="bay"></div>
        <h3>Project Three</h3>
        <p>One or two sentences on what it does and why you built it.</p>
        <div class="chips" style="margin-top:12px"><span class="chip">Simulink</span><span class="chip">Rocketry</span></div>
        <div class="links"><a href="https://github.com/gabbyrocket/project-three" target="_blank" rel="noopener">Code</a></div>
      </article>
    </div>
  </section>

  <section id="education">
    <h2>Training</h2>
    <div class="cards">
      <div class="card">
        <h3>University of Southern California</h3>
        <p class="where">M.S. Aerospace Engineering</p>
        <p class="when">2026 – Present</p>
      </div>
      <div class="card">
        <h3>Florida Institute of Technology</h3>
        <p class="where">B.S. Mechanical Engineeringr</p>
        <p class="when">2022 – 2025</p>
      </div>
    </div>
    <div class="patches">
      <div class="patch"><b>C1</b>Certification Name<small>Issuer, 2025</small></div>
      <div class="patch"><b>C2</b>Certification Name<small>Issuer, 2024</small></div>
    </div>
  </section>

  <section id="skills">
    <h2>Toolkit</h2>
    <div class="toolkit">
      <div><h3>Analysis</h3><div class="chips"><span class="chip">FEA</span><span class="chip">CFD</span><span class="chip">ANSYS</span><span class="chip">MATLAB</span><span class="chip">Simulink</span></div></div>
      <div><h3>Design and build</h3><div class="chips"><span class="chip">CAD</span><span class="chip">Creo</span><span class="chip">Hardware Fabrication</span><span class="chip">High-Power Rocketry</span><span class="chip">Siemens NXy</span></div></div>
      <div><h3>Team</h3><div class="chips"><span class="chip">Leadership</span><span class="chip">Tutoring</span><span class="chip">Mentoring</span></div></div>
    </div>
  </section>

  <section id="contact" class="contact">
    <h2>Open a channel</h2>
    <p>Have a project or an opening in mind? Email me:</p>
    <a class="mail" href="mailto:gabrielleyeager26@gmail.com">gabrielleyeager26@gmail.com</a>
    <p><a href="https://www.linkedin.com/in/gabrielle-y-240b4028a/" target="_blank" rel="noopener">LinkedIn</a> &nbsp;|&nbsp; <a href="https://github.com/gabbyrocket" target="_blank" rel="noopener">GitHub</a></p>
  </section>
</main>

<footer>&copy; <span id="yr"></span> Gabrielle Y.</footer>

<script>
document.getElementById('yr').textContent = new Date().getFullYear();

// Rocket on the gauge climbs with scroll progress
(function(){
  const r = document.getElementById('climber'), g = r.parentElement;
  function move(){
    const max = document.documentElement.scrollHeight - innerHeight;
    const p = max > 0 ? scrollY / max : 0;
    r.style.transform = 'translateY(' + p * (g.clientHeight - 40) + 'px) rotate(180deg)';
  }
  addEventListener('scroll', move, {passive:true}); addEventListener('resize', move); move();
})();

// Starfield with an occasional shooting star
(function(){
  const c = document.getElementById('sky'), x = c.getContext('2d');
  const still = matchMedia('(prefers-reduced-motion: reduce)').matches;
  let w, h, stars = [], shoot = null;
  const tints = ['255,255,255','255,255,255','170,190,255','255,194,71'];
  function size(){
    w = c.width = innerWidth; h = c.height = innerHeight;
    const n = Math.min(320, Math.floor(w * h / 5500));
    stars = Array.from({length:n}, () => {
      const z = Math.floor(Math.random()*3);
      return {x:Math.random()*w, y:Math.random()*h, r:.3+z*.5+Math.random()*.4, v:.05*(z+1),
        p:Math.random()*6.28, s:.004+Math.random()*.02, t:tints[Math.floor(Math.random()*tints.length)]};
    });
  }
  function draw(){
    x.clearRect(0,0,w,h);
    for(const s of stars){
      if(!still){ s.p += s.s; s.y += s.v; if(s.y > h+2){ s.y = -2; s.x = Math.random()*w; } }
      const a = still ? .8 : .4 + .6*Math.abs(Math.sin(s.p));
      x.fillStyle = 'rgba('+s.t+','+a+')';
      x.beginPath(); x.arc(s.x,s.y,s.r,0,6.28); x.fill();
    }
    if(!still){
      if(!shoot && Math.random() < .004) shoot = {x:w*(.3+Math.random()*.7), y:Math.random()*h*.4, vx:-11, vy:5, life:1};
      if(shoot){
        const g = x.createLinearGradient(shoot.x, shoot.y, shoot.x-shoot.vx*7, shoot.y-shoot.vy*7);
        g.addColorStop(0,'rgba(255,255,255,'+shoot.life+')'); g.addColorStop(1,'rgba(255,255,255,0)');
        x.strokeStyle = g; x.lineWidth = 1.6; x.beginPath();
        x.moveTo(shoot.x, shoot.y); x.lineTo(shoot.x-shoot.vx*7, shoot.y-shoot.vy*7); x.stroke();
        shoot.x += shoot.vx; shoot.y += shoot.vy; shoot.life -= .02;
        if(shoot.life <= 0) shoot = null;
      }
      requestAnimationFrame(draw);
    }
  }
  addEventListener('resize', () => { size(); if(still) draw(); });
  size(); draw();
})();
</script>
</body>
</html>
