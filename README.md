<html lang="en">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<title>Gabrielle Yeager | Portfolio</title>
<meta name="description" content="Portfolio of Gabrielle Yeager: experience, projects, skills and contact.">
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Unbounded:wght@500;700&family=Space+Grotesk:wght@400;500&display=swap" rel="stylesheet">
<style>
:root{
  --void:#05061a; --panel:rgba(14,17,46,.72); --line:rgba(150,165,255,.2);
  --text:#eaeeff; --muted:#a9b0da; --nebula:#8b7bff; --star:#ffd98a; --ion:#6fe3f0; --rose:#ff7fb0;
  --display:"Unbounded","Trebuchet MS",system-ui,sans-serif; --body:"Space Grotesk","Segoe UI",system-ui,sans-serif;
  color-scheme:dark;
}
*{box-sizing:border-box;margin:0}
html{scroll-behavior:smooth;scroll-padding-top:90px}
body{font:17px/1.65 var(--body);color:var(--text);min-height:100vh;background:
  radial-gradient(55vw 50vh at 88% 6%,rgba(139,123,255,.34),transparent 70%),
  radial-gradient(45vw 45vh at 0% 45%,rgba(111,227,240,.16),transparent 70%),
  radial-gradient(60vw 45vh at 70% 100%,rgba(255,127,176,.18),transparent 70%),
  var(--void);background-attachment:fixed}
#sky{position:fixed;inset:0;width:100%;height:100%;z-index:-1}
a{color:var(--ion)} a:hover{color:var(--star)}
:focus-visible{outline:2px solid var(--star);outline-offset:3px;border-radius:6px}
h1,h2{font-family:var(--display);line-height:1.15}

/* Navigation */
nav{position:fixed;top:14px;left:50%;transform:translateX(-50%);z-index:5;max-width:calc(100% - 24px);
  background:rgba(5,6,26,.78);backdrop-filter:blur(12px);border:1px solid var(--line);border-radius:999px}
nav ul{list-style:none;display:flex;gap:2px;padding:5px;overflow-x:auto}
nav a{display:block;padding:6px 14px;border-radius:999px;color:var(--muted);text-decoration:none;font-size:.9rem;white-space:nowrap}
nav a:hover{color:var(--text);background:rgba(139,123,255,.22)}

/* Hero with ringed planet */
.hero{max-width:1040px;margin:auto;padding:120px 20px 40px;min-height:100vh;display:grid;
  grid-template-columns:1.15fr .85fr;align-items:center;gap:30px}
.hero h1{font-size:clamp(2.4rem,6.5vw,4.6rem);font-weight:700;letter-spacing:-.02em}
.headline{font-size:1.2rem;margin-top:16px;max-width:36ch}
.status{display:flex;align-items:center;gap:10px;margin-top:14px;color:var(--muted)}
.status::before{content:"";width:9px;height:9px;border-radius:50%;background:var(--ion);box-shadow:0 0 12px var(--ion)}
.actions{display:flex;flex-wrap:wrap;gap:12px;margin-top:28px}
.btn{padding:10px 22px;border-radius:999px;font-weight:500;text-decoration:none;border:1px solid var(--ion);color:var(--ion)}
.btn.primary{background:var(--star);border-color:var(--star);color:#1a1530}
.btn:hover{background:rgba(111,227,240,.14);color:var(--text)}
.btn.primary:hover{background:#ffe6ab;color:#1a1530}
.system{position:relative;width:min(400px,80vw);aspect-ratio:1;margin:auto}
.planet{position:absolute;inset:14%;z-index:1;border-radius:50%;
  background:radial-gradient(circle at 30% 28%,#ffe3ac 0,#ff8fb1 26%,#7a4bd6 60%,#1a1250 100%);
  box-shadow:inset -34px -34px 60px rgba(0,0,0,.6),0 0 100px rgba(139,123,255,.5)}
.ring{position:absolute;left:-6%;right:-6%;top:37%;bottom:37%;border-radius:50%;transform:rotate(-16deg);
  border:5px solid rgba(255,217,138,.65);box-shadow:0 0 22px rgba(255,217,138,.35)}
.ring.back{z-index:0}
.ring.front{z-index:2;clip-path:polygon(0 50%,100% 50%,100% 100%,0 100%)}
.orbit{position:absolute;inset:0;z-index:3;animation:spin 26s linear infinite}
.orbit i{position:absolute;top:2%;left:50%;width:20px;height:20px;border-radius:50%;
  background:radial-gradient(circle at 35% 30%,#fff,#9fb0ff 60%,#3b4aa8);box-shadow:0 0 16px rgba(159,176,255,.8)}
@keyframes spin{to{transform:rotate(360deg)}}

/* Sections */
main{max-width:1040px;margin:auto;padding:0 20px 40px}
section{padding:56px 0}
h2{font-size:1.5rem;font-weight:500;display:flex;align-items:center;gap:18px;margin-bottom:28px}
h2::after{content:"";flex:1;height:1px;background:linear-gradient(90deg,var(--line),transparent)}
.lead{font-size:1.15rem;max-width:62ch}

/* Timeline (experience, education) */
.log{position:relative;padding-left:36px}
.log::before{content:"";position:absolute;left:7px;top:8px;bottom:8px;width:2px;background:linear-gradient(var(--ion),var(--nebula),transparent)}
.item{position:relative;padding-bottom:30px}
.item:last-child{padding-bottom:0}
.item::before{content:"";position:absolute;left:-36px;top:7px;width:16px;height:16px;border-radius:50%;
  background:var(--void);border:2px solid var(--star);box-shadow:0 0 12px rgba(255,217,138,.7)}
.item.now::before{background:var(--star)}
.item h3{font-size:1.15rem;font-weight:500}
.item .where{color:var(--ion)}
.when{color:var(--muted);font-size:.9rem}
.item ul{margin:8px 0 0 18px;color:var(--muted)}
.item p.desc{color:var(--muted);margin-top:6px}

/* Projects as planets */
.worlds{display:grid;grid-template-columns:repeat(auto-fit,minmax(270px,1fr));gap:20px}
.world{background:var(--panel);border:1px solid var(--line);border-radius:22px;padding:24px;backdrop-filter:blur(8px);
  transition:transform .25s,border-color .25s}
.world:hover{transform:translateY(-5px);border-color:var(--nebula)}
.globe{width:68px;height:68px;border-radius:50%;margin-bottom:16px;
  background:radial-gradient(circle at 32% 28%,var(--a),var(--b) 72%);
  box-shadow:inset -10px -10px 18px rgba(0,0,0,.5),0 0 28px var(--glow)}
.world h3{font-size:1.15rem;font-weight:500}
.world p{color:var(--muted);margin-top:6px;font-size:.98rem}
.links{margin-top:12px;font-size:.95rem;display:flex;gap:16px}

/* Skills as stars */
.orbits{display:grid;grid-template-columns:repeat(auto-fit,minmax(250px,1fr));gap:28px}
.orbits h3{font-size:1rem;font-weight:500;color:var(--star);margin-bottom:10px}
.chips{display:flex;flex-wrap:wrap;gap:8px}
.chip{display:inline-flex;align-items:center;gap:8px;padding:5px 14px;border-radius:999px;font-size:.92rem;
  border:1px solid var(--line);background:rgba(139,123,255,.1)}
.chip::before{content:"";width:6px;height:6px;border-radius:50%;background:var(--star);box-shadow:0 0 8px var(--star)}

/* Certifications as mission patches */
.patches{display:flex;flex-wrap:wrap;gap:24px;margin-top:36px}
.patch{width:120px;text-align:center;font-size:.9rem}
.patch b{display:grid;place-items:center;width:68px;height:68px;margin:0 auto 8px;border-radius:50%;
  border:2px dashed var(--star);font:500 1.3rem var(--display);color:var(--star);background:rgba(255,217,138,.08)}
.patch small{display:block;color:var(--muted)}

/* Recommendations as transmissions */
.signals{display:grid;grid-template-columns:repeat(auto-fit,minmax(300px,1fr));gap:20px}
blockquote{background:var(--panel);border:1px solid var(--line);border-left:3px solid var(--rose);
  border-radius:6px 22px 22px 6px;padding:22px 24px;color:var(--muted)}
blockquote cite{display:block;margin-top:10px;color:var(--text);font-style:normal;font-size:.92rem}

/* Contact */
.contact{text-align:center}
.contact .mail{display:inline-block;margin:6px 0 18px;font:500 clamp(1.2rem,4vw,2rem) var(--display);text-decoration:none;
  border-bottom:2px solid var(--star);color:var(--text)}
.contact .mail:hover{color:var(--star)}
footer{text-align:center;color:var(--muted);font-size:.88rem;padding:20px 0 40px}

@media(max-width:800px){
  .hero{grid-template-columns:1fr;padding-top:100px;min-height:auto}
  .system{order:-1;width:min(270px,64vw)}
}
@media(prefers-reduced-motion:reduce){html{scroll-behavior:auto}.orbit{animation:none}.world{transition:none}}

/* Briefing panel and zig-zag flight log */
.brief{display:grid;grid-template-columns:1.5fr 1fr;gap:36px;align-items:start}
.specs{border:1px dashed rgba(255,217,138,.55);border-radius:20px;padding:10px 22px;background:var(--panel);backdrop-filter:blur(8px)}
.specs div{display:flex;justify-content:space-between;gap:18px;padding:11px 0;border-top:1px solid var(--line)}
.specs div:first-child{border-top:0}
.specs dt{color:var(--muted)}
.specs dd{text-align:right}
@media(max-width:800px){.brief{grid-template-columns:1fr}}
@media(min-width:801px){
  .zig{padding-left:0}
  .zig::before{left:50%;transform:translateX(-1px)}
  .zig .item{width:50%;padding-right:44px;text-align:right}
  .zig .item:nth-child(even){margin-left:50%;padding-left:44px;padding-right:0;text-align:left}
  .zig .item::before{left:auto;right:-8px}
  .zig .item:nth-child(even)::before{left:-8px;right:auto}
}
</style>
</head>
<body>
<canvas id="sky" aria-hidden="true"></canvas>

<nav aria-label="Sections">
  <ul>
    <li><a href="#top">Launch</a></li>
    <li><a href="#about">Briefing</a></li>
    <li><a href="#experience">Flight log</a></li>
    <li><a href="#projects">Discoveries</a></li>
    <li><a href="#education">Training</a></li>
    <li><a href="#skills">Toolkit</a></li>
    <li><a href="#recommendations">Transmissions</a></li>
    <li><a href="#contact">Contact</a></li>
  </ul>
</nav>

<!-- HERO: replace the placeholder text -->
<header class="hero" id="top">
  <div>
    <h1>Gabrielle Y.</h1>
    <p class="headline">University of Southern California. Aerospace Engineering Graduate Student.</p>
    <p class="status">Los Angeles, California</p>
    <div class="actions">
      <a class="btn primary" href="#contact">Contact me</a>
      <a class="btn" href="https://github.com/yourusername" target="_blank" rel="noopener">GitHub</a>
      <a class="btn" href="https://www.linkedin.com/in/gabrielle-y-240b4028a/" target="_blank" rel="noopener">LinkedIn</a>
      <a class="btn" href="resume.pdf">Résumé</a>
    </div>
  </div>
  <div class="system" role="img" aria-label="Decorative ringed planet with a moon orbiting it">
    <div class="ring back"></div><div class="planet"></div><div class="ring front"></div>
    <div class="orbit"><i></i></div>
  </div>
</header>

<main>
  <section id="about">
    <h2>Mission briefing</h2>
    <div class="brief">
      <p class="lead">Aerospace Engineering graduate student specializing in propulsion, with hands-on experience in high-power rocketry, structural design, FEA, and hardware fabrication. Skilled in CAD modeling, ANSYS, MATLAB, and Simulink, with a track record of taking systems from concept through tested hardware.</p>
      <dl class="specs">
        <div><dt>Base</dt><dd>Los Angeles, California</dd></div>
        <div><dt>Academy</dt><dd>University of Southern California</dd></div>
        <div><dt>Focus</dt><dd>Propulsion</dd></div>
      </dl>
    </div>
  </section>

  <section id="experience">
    <h2>Flight Log</h2>
    <div class="log zig">
            <div class="item">
        <h3>Engine Design Engineer</h3>
        <p class="where">USC Liquid Propulsion Laboratory</p>
        <p class="when">Aug 2026 – Present</p>
<ul>
    <li>Develop and update CAD models of Nova’s coaxial-swirl injector, incorporating design iterations and engineering requirements.</li>
    <li>Perform FEA on injector components to evaluate structural performance, stress, deformation, and design integrity under operating conditions.</li>
  <li>Conduct CFD analyses to investigate injector flow behavior and support evaluation of fluid-flow and atomization characteristics.</li>
  <li>Collaborate with the rest of the  team to incorporate FEA/CFD results into injector design iterations, supporting performance and manufacturability.</li>
  </ul>
            </div>
      <div class="item">
        <h3>Peer Tutor</h3>
        <p class="where">Florida Institute of Technology</p>
        <p class="when">Sept 2025 – Dec 2025</p>
<ul>
    <li>Provided one-on-one and small-group instruction for upper-division engineering courses, including Thermodynamics II, Fluid Mechanics, and Solids Modeling (Creo), strengthening communication of technical concepts to diverse audiences.</li>
    <li>Adapt tutoring methods to different learning styles to improve comprehension, confidence, and academic performance.
      <li>Maintain a professional, supportive learning environment that promotes student success, accountability, and ethical academic practices.</li>
  </ul>
        <!-- Add 1-3 bullets on what you built or led: <ul><li>...</li></ul> -->
      </div>
            <div class="item">
        <h3>Volunteer Undergraduate Research Assistant</h3>
        <p class="where">He Group</p>
        <p class="when">Oct 2024 – Feb 2025</p>
              <ul>
    <li>Supported research on water security through advanced materials, collaborating with a graduate student on synthesizing metal-organic frameworks (MOFs) and conducting spray-dry experiments. </li>
  </ul>
              <!-- Add 1-3 bullets on what you built or led: <ul><li>...</li></ul> -->
            </div>
       <div class="item">
        <h3>Campus Ambassador</h3>
        <p class="where">Hot Girl Walk</p>
        <p class="when">Nov 2024 – Dec 2025</p>
         <ul>
    <li>Fostered a supportive community of students by connecting individuals through shared wellness, personal growth, and empowerment goals.</li>
    <li>Served as a representative of a global wellness and female empowerment brand, helping expand its campus presence and community reach.</li>
  </ul>
        <!-- Add 1-3 bullets on what you built or led: <ul><li>...</li></ul> -->
       </div>
                  <div class="item">
        <h3>Treasurer</h3>
        <p class="where">AIAA Florida Tech</p>
        <p class="when">Aug 2024 – Dec 2025</p>
                    <ul>
    <li>Managed organization finances, including tracking expenses, maintaining accurate financial records, and monitoring available funds.</li>
    <li>Coordinated budgeting and financial planning for AIAA events, projects, and competition teams while ensuring responsible use of organization funds.</li>
        <li>Collaborated with AIAA leadership and university departments to process funding requests, reimbursements, and other financial transactions.</li>
  </ul>
        <!-- Add 1-3 bullets on what you built or led: <ul><li>...</li></ul> -->
                  </div>
                   <div class="item">
        <h3>Safety Chair / Safety & Legal Compliance Officer</h3>
        <p class="where">AIAA Florida Tech</p>
        <p class="when">Aug 2023 – Dec 2025</p>
                     <ul>
    <li>Maintained and updated safety documentation, procedures, and the organizationrsquo;s safety binder for events, projects, and competition teams.</li>
    <li>Collaborated with university EHS and other departments to ensure compliance with safety requirements and applicable BiProp standards.</li>
                       <li>Identified potential hazards across competition teams and AIAA activities, working proactively with members to address risks and improve overall safety practices.</li>
  </ul>
        <!-- Add 1-3 bullets on what you built or led: <ul><li>...</li></ul> -->
                   </div>
                    <div class="item">
        <h3>Social Media Chair</h3>
        <p class="where">AIAA Florida Tech</p>
        <p class="when">Aug 2023 – Dec 2024</p>
                      <ul>
    <li>Managed AIAA's social media and promotional content to increase awareness of organization events, projects, meetings, and activities.</li>
    <li>Created and coordinated digital content, including graphics, announcements, and event promotions, to effectively communicate with members and the broader student community.</li>
                        <li>Collaborated with AIAA leadership and competition teams to highlight projects, achievements, and opportunities while maintaining a consistent organizational presence.</li>
  </ul>
        <!-- Add 1-3 bullets on what you built or led: <ul><li>...</li></ul> -->
                    </div>
                     <div class="item">
        <h3>Student Government Association Representative</h3>
        <p class="where">AIAA Florida Tech</p>
        <p class="when">Aug 2023 – Dec 2024</p>
                       <ul>
    <li>Represented AIAA within the Student Government Association (SGA), communicating organization needs, concerns, and initiatives to university representatives.</li>
    <li>Attended SGA meetings and relayed relevant updates, policies, and opportunities back to AIAA leadership and members.</li>
    <li>Collaborated with student organizations and university representatives to support AIAA events, funding initiatives, and organizational activities.</li>        
  </ul>
        <!-- Add 1-3 bullets on what you built or led: <ul><li>...</li></ul> -->
                     </div>
                      <div class="item">
        <h3>Volunteer Student Course Proctor</h3>
        <p class="where">AIAA</p>
        <p class="when">Mar 2025 – May 2025</p>
                               <ul>
    <li>Hosted AIAA online short course sessions by starting Zoom meetings/webinars early, performing tech checks, and ensuring instructor audio/visual systems were fully functional.</li>
    <li>Assisted instructors throughout the course by troubleshooting technical issues, starting/monitoring lecture recordings, and managing participant audio controls.</li>
    <li>Delivered scripted course introductions, explained class procedures to attendees, and introduced instructors by presenting their professional bios.</li>        
    <li>Moderated Q&A during lectures and supported smooth course flow through real-time communication with instructors and participants.</li>
     <li>Completed AIAA’s official proctor training and provided reliable technical and logistical support across 8–36 hours of live instructional time.</li>
  </ul>
        <!-- Add 1-3 bullets on what you built or led: <ul><li>...</li></ul> -->
                      </div>
       <div class="item">
        <h3>Lead Engineer</h3>
        <p class="where">NASA L'SPACE Academy</p>
        <p class="when">Jan 2024 – Apr 2024</p>
        <!-- Add 1-3 bullets on what you built or led: <ul><li>...</li></ul> -->         
            </div>
      <div class="item">
        <h3>Payload Sub-Systems Lead</h3>
        <p class="where">Rocketbirds</p>
        <p class="when">Aug 2020 – May 2021</p>
 <!-- Add 1-3 bullets on what you built or led: <ul><li>...</li></ul> -->
      </div>
      <div class="item">
        <h3>Vice President, Lead Electrical, Media and Marketing</h3>
        <p class="where">FIRST Robotics: FRC Team 5429 (2016–2020), FTC Team 12445 (2018–2020)</p>
        <p class="when">Aug 2016 – May 2020 &middot; Also FLL Judge (2016–2020)</p>
 <!-- Add bullets here -->
      </div>
      <div class="item">
        <h3>Media and Marketing, Summer Camp Mentor</h3>
        <p class="where">VEX Robotics: Team 7853 (2016–2020)</p>
        <p class="when">Aug 2016 – May 2020 &middot; VEX IQ summer camp mentor (2018–2020)</p>
 <!-- Add bullets here -->
      </div>
    </div>
  </section>

  <section id="projects">
    <h2>Discoveries</h2>
    <div class="worlds">
      <article class="world">
        <div class="globe" style="--a:#6fe3f0;--b:#22409a;--glow:rgba(111,227,240,.45)"></div>
        <h3>Project One</h3>
        <p>One or two sentences on what it does and why you built it.</p>
        <div class="chips" style="margin-top:12px"><span class="chip">Python</span><span class="chip">React</span></div>
        <div class="links"><a href="https://github.com/yourusername/project-one" target="_blank" rel="noopener">Code</a><a href="#" target="_blank" rel="noopener">Live demo</a></div>
      </article>
      <article class="world">
        <div class="globe" style="--a:#ffd98a;--b:#c4457a;--glow:rgba(255,127,176,.45)"></div>
        <h3>Project Two</h3>
        <p>One or two sentences on what it does and why you built it.</p>
        <div class="chips" style="margin-top:12px"><span class="chip">JavaScript</span><span class="chip">Node.js</span></div>
        <div class="links"><a href="https://github.com/yourusername/project-two" target="_blank" rel="noopener">Code</a></div>
      </article>
      <article class="world">
        <div class="globe" style="--a:#c7b8ff;--b:#4a2fa8;--glow:rgba(139,123,255,.5)"></div>
        <h3>Project Three</h3>
        <p>One or two sentences on what it does and why you built it.</p>
        <div class="chips" style="margin-top:12px"><span class="chip">SQL</span><span class="chip">Docker</span></div>
        <div class="links"><a href="https://github.com/yourusername/project-three" target="_blank" rel="noopener">Code</a></div>
      </article>
    </div>
  </section>

  <section id="education">
    <h2>Training and certifications</h2>
    <div class="log">
      <div class="item">
        <h3>Florida Institute of Technology</h3>
        <p class="where">Your degree and major</p>
        <p class="when">Start year – End year</p>
        <p class="desc">Relevant coursework, honors, clubs or activities.</p>
      </div>
    </div>
    <div class="patches">
      <div class="patch"><b>C1</b>Certification Name<small>Issuer, 2025</small></div>
      <div class="patch"><b>C2</b>Certification Name<small>Issuer, 2024</small></div>
    </div>
  </section>

  <section id="skills">
    <h2>Toolkit</h2>
    <div class="orbits">
      <div><h3>Engineering</h3><div class="chips"><span class="chip">Electrical systems</span><span class="chip">Payload sub-systems</span></div></div>
      <div><h3>Robotics programs</h3><div class="chips"><span class="chip">FRC</span><span class="chip">FTC</span><span class="chip">FLL</span><span class="chip">VEX IQ</span></div></div>
      <div><h3>Communication and leadership</h3><div class="chips"><span class="chip">Media and marketing</span><span class="chip">Team leadership</span><span class="chip">Mentoring</span></div></div>
    </div>
  </section>

  <section id="recommendations">
    <h2>Transmissions</h2>
    <div class="signals">
      <blockquote>Paste a short quote from a manager, teacher or colleague about working with you.Person Name, Title at Company</blockquote>
      <blockquote>A second recommendation, if you have one.Person Name, Title at Company</blockquote>
    </div>
  </section>

  <section id="contact" class="contact">
    <h2>Open a channel</h2>
    <p>Have a project or an opening in mind? Email me:</p>
    <a class="mail" href="mailto:you@example.com">you@example.com</a>
    <p><a href="https://www.linkedin.com/in/gabrielle-y-240b4028a/" target="_blank" rel="noopener">LinkedIn</a> &nbsp;|&nbsp; <a href="https://github.com/yourusername" target="_blank" rel="noopener">GitHub</a></p>
  </section>
</main>

<footer>&copy; <span id="yr"></span> Gabrielle Y.</footer>

<script>
document.getElementById('yr').textContent = new Date().getFullYear();

// Starfield: three depth layers drifting upward, plus an occasional shooting star
(function(){
  const c = document.getElementById('sky'), x = c.getContext('2d');
  const still = matchMedia('(prefers-reduced-motion: reduce)').matches;
  let w, h, stars = [], shoot = null;
  const tints = ['255,255,255','255,255,255','170,190,255','255,217,138'];
  function size(){
    w = c.width = innerWidth; h = c.height = innerHeight;
    const n = Math.min(320, Math.floor(w * h / 5500));
    stars = Array.from({length:n}, () => {
      const z = Math.floor(Math.random()*3);
      return {x:Math.random()*w, y:Math.random()*h, z, r:.3+z*.5+Math.random()*.4,
        v:.03*(z+1), p:Math.random()*6.28, s:.004+Math.random()*.02,
        t:tints[Math.floor(Math.random()*tints.length)]};
    });
  }
  function draw(){
    x.clearRect(0,0,w,h);
    for(const s of stars){
      if(!still){ s.p += s.s; s.y -= s.v; if(s.y < -2){ s.y = h+2; s.x = Math.random()*w; } }
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
