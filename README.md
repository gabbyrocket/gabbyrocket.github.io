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
  radial-gradient(50vw 45vh at 85% 8%,rgba(123,108,255,.34),transparent 70%),
  radial-gradient(45vw 40vh at 8% 30%,rgba(95,224,238,.14),transparent 70%),
  radial-gradient(35vw 30vh at 30% 75%,rgba(214,90,200,.14),transparent 70%),
  radial-gradient(60vw 40vh at 60% 100%,rgba(255,106,43,.2),transparent 70%),var(--void);background-attachment:fixed}
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
.roles{margin-top:12px}
.roles details{border-top:1px solid var(--line)}
.roles summary{display:flex;align-items:center;gap:12px;padding:12px 0;cursor:pointer;list-style:none}
.roles summary::-webkit-details-marker{display:none}
.roles summary::before{content:"";flex:none;border-left:7px solid var(--ember);border-top:5px solid transparent;border-bottom:5px solid transparent;transition:transform .2s}
.roles details[open] summary::before{transform:rotate(90deg)}
.roles summary:hover{color:var(--flame)}
.roles summary span:first-of-type{flex:1;font-weight:500}
.roles .dates{color:var(--muted);font-size:.86rem;white-space:nowrap}
.roles details ul{margin:0 0 14px 34px}

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

/* Cosmic extras */
.planet-bg{position:fixed;left:-14vmin;bottom:-20vmin;width:52vmin;height:52vmin;border-radius:50%;z-index:-2;pointer-events:none;opacity:.6;
  background:radial-gradient(circle at 68% 30%,#ffb27a 0,#e2557f 32%,#5a2a9c 68%,#140a38 100%);
  box-shadow:inset -3vmin -3vmin 6vmin rgba(0,0,0,.65),0 0 8vmin rgba(214,90,200,.35)}
.planet-bg::after{content:"";position:absolute;left:-28%;right:-28%;top:42%;bottom:42%;border-radius:50%;border:3px solid rgba(255,194,71,.4);transform:rotate(-14deg)}
.orbit{position:absolute;left:50%;top:50%;width:160%;aspect-ratio:1;margin:-80% 0 0 -80%;border:1px dashed rgba(95,224,238,.4);border-radius:50%;animation:spin 24s linear infinite;pointer-events:none}
.orbit i{position:absolute;top:-7px;left:50%;width:14px;height:14px;margin-left:-7px;border-radius:50%;background:radial-gradient(circle at 35% 30%,#fff,#9fb0ff 60%,#3b4aa8);box-shadow:0 0 14px rgba(159,176,255,.8)}
@keyframes spin{to{transform:rotate(360deg)}}
h2{display:flex;align-items:center;gap:14px}
h2::before{content:"";flex:none;width:.6em;height:1em;background:url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 24 40'%3E%3Cpath d='M12 1c5 6 6 14 5 24H7C6 15 7 7 12 1z' fill='%23f2f4ff'/%3E%3Ccircle cx='12' cy='12' r='2.4' fill='%235fe0ee'/%3E%3Cpath d='M7 20l-5 9 5-2zM17 20l5 9-5-2z' fill='%23ff6a2b'/%3E%3Cpath d='M9 26h6l-3 12z' fill='%23ffc247'/%3E%3C/svg%3E") center/contain no-repeat}
h2::after{content:"";flex:1;border-top:2px dotted var(--line)}
.contact h2{justify-content:center}
.contact h2::after{display:none}
.card li::marker{content:"\2726  ";color:var(--flame)}

@media(max-width:800px){
  .hero{grid-template-columns:1fr;padding-top:90px;min-height:auto}
  .pad{order:-1;width:min(180px,45vw)}
  .brief,.stage{grid-template-columns:1fr}
  .tag{position:static}
  .tag b{display:inline;font-size:2rem;margin-right:10px}
}
@media(prefers-reduced-motion:reduce){html{scroll-behavior:auto}.pad svg,.flame,.orbit{animation:none}}

/* Nebula depth and a distant moon */
body{background:
  radial-gradient(50vw 45vh at 85% 8%,rgba(123,108,255,.34),transparent 70%),
  radial-gradient(45vw 40vh at 8% 55%,rgba(95,224,238,.14),transparent 70%),
  radial-gradient(55vw 45vh at 65% 100%,rgba(255,106,43,.2),transparent 70%),
  radial-gradient(35vw 30vh at 30% 15%,rgba(255,127,176,.12),transparent 70%),
  linear-gradient(115deg,transparent 38%,rgba(150,160,255,.07) 50%,transparent 62%),var(--void);background-attachment:fixed}
.moon-bg{position:fixed;right:6vmin;top:16vmin;width:9vmin;height:9vmin;border-radius:50%;z-index:-2;pointer-events:none;opacity:.7;
  background:radial-gradient(circle at 30% 28%,#fff 0,#c9d0ff 45%,#59639f 100%);
  box-shadow:inset -1.2vmin -1.2vmin 2.4vmin rgba(0,0,0,.5),0 0 4vmin rgba(159,176,255,.4)}
.payload details{margin:14px 22px 0}
.payload summary{cursor:pointer;color:var(--signal);font-size:.95rem}
.payload ul{margin:8px 0 0 18px;color:var(--muted);font-size:.95rem}
.payload li+li{margin-top:4px}
.payload .when{margin-top:2px;font-size:.86rem}

/* Project pages and cards */
.thumb{display:block;width:100%;height:170px;object-fit:cover;border-bottom:1px solid var(--line)}
.page{max-width:960px;margin:auto;padding:100px 24px 40px}
.back{display:inline-block;margin-bottom:22px;text-decoration:none}
.phead h1{font-size:clamp(2.4rem,7vw,4.6rem);font-weight:800;margin-top:6px}
.eyebrow{color:var(--ember);font:700 1.1rem var(--display);letter-spacing:.08em;text-transform:uppercase}
.meta{color:var(--muted);margin-top:10px}
.cols{display:grid;grid-template-columns:1.15fr .85fr;gap:32px;align-items:start;margin-top:30px}
.cols.solo{grid-template-columns:1fr;max-width:68ch}
.body p{margin-top:12px;color:var(--hull)}
.body h2,.sec h2{margin-top:6px}
figure{margin:0 0 18px}
figure img{display:block;width:100%;height:auto;border-radius:6px;border:1px solid var(--line)}
figcaption{color:var(--muted);font-size:.88rem;margin-top:6px;text-align:center}
.sec{margin-top:36px}
.sec h2{font-size:clamp(1.6rem,4vw,2.2rem)}
.lists{display:grid;grid-template-columns:repeat(auto-fit,minmax(260px,1fr));gap:18px}
.facts{margin:10px 0 0 20px;color:var(--muted)}
.facts li+li{margin-top:5px}
.steps{list-style:none;padding:0;display:grid;gap:12px}
.steps li{display:grid;grid-template-columns:58px 1fr;gap:14px;background:var(--panel);border:1px solid var(--line);border-radius:6px;padding:16px 20px}
.steps b{font:800 2.2rem var(--display);color:var(--ember);line-height:1}
.steps h3{font-size:1.25rem}
.steps p{color:var(--muted);margin-top:2px}
.paper{margin-top:44px;padding:24px;border:1px dashed var(--flame);border-radius:6px;background:var(--panel)}
.paper p{color:var(--muted);margin:6px 0 16px}
.btn.off{opacity:.6;pointer-events:none;border-style:dashed}
.pn{display:flex;justify-content:space-between;gap:16px;margin-top:40px;flex-wrap:wrap}
@media(max-width:800px){.cols{grid-template-columns:1fr}}

</style>
</head>
<body>
<div class="planet-bg" aria-hidden="true"></div>
<div class="moon-bg" aria-hidden="true"></div>
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
    <div class="orbit"><i></i></div>
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
      <p class="lead">Aerospace Engineering graduate student specializing in propulsion, with hands-on experience in high-power rocketry, structural design, FEA, CNC machining, and mechanical systems integration and testing. Skilled in CAD modeling, ANSYS, MATLAB, and Simulink, with a track record of taking systems from concept through design, analysis, manufacturing, and tested hardware.</p>
      <dl class="readout">
        <div><dt>Base</dt><dd>Los Angeles, California</dd></div>
        <div><dt>Academy</dt><dd>University of Southern California</dd></div>
        <div><dt>Focus</dt><dd>Propulsion</dd></div>
        <div><dt>Undergrad</dt><dd>B.S. Mechanical Engineering, Florida Tech</dd></div>
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
        <div class="card wide">
          <h3>Drafting / Submittal Tech</h3>
          <p class="where">CO2 Monitoring LLC, Las Vegas, Nevada</p>
          <p class="when">Jan 2026 – May 2026</p>
          <ul>
            <li>Prepare and submit permit drawings through city, state, and fire department portals, ensuring full code compliance.</li>
            <li>Create detailed floor plans and layouts for restaurants, bars, and commercial facilities in Bluebeam.</li>
            <li>Verify equipment locations and specifications, including CO₂ tanks, BIB racks, fill boxes, carbonators, and dispensers.</li>
            <li>Organize project documentation and permit files and track job statuses, working with estimators, technicians, and operations teams.</li>
          </ul>
        </div>
      </div>
    </div>

    <div class="stage">
      <div class="tag"><b>Stage 2</b><span>Florida Tech<br>2023 – 2025</span></div>
      <div class="cards">
        <div class="card wide">
          <h3>AIAA Florida Tech</h3>
          <p class="where">Officer and representative roles. Click a role to see what I did.</p>
          <div class="roles">
        <details><summary><span>Treasurer</span><span class="dates">Aug 2024 – Dec 2025</span></summary>
            <ul>
              <li>Managed organization finances, including tracking expenses, maintaining accurate records, and monitoring available funds.</li>
              <li>Coordinated budgeting and financial planning for AIAA events, projects, and competition teams while ensuring responsible use of funds.</li>
              <li>Worked with AIAA leadership and university departments to process funding requests, reimbursements, and other transactions.</li>
            </ul>
          </details>
        <details><summary><span>Safety Chair / Safety &amp; Legal Compliance Officer (AIAA &amp; Panther Rocketry)</span><span class="dates">Aug 2023 – Dec 2025</span></summary>
            <ul>
              <li>Maintained and updated safety documentation, procedures, and the organization’s safety binder for events, projects, and competition teams.</li>
              <li>Worked with university EHS and other departments to ensure compliance with safety requirements and applicable BiProp standards.</li>
              <li>Identified potential hazards across competition teams and AIAA activities, working with members to address risks and improve safety practices.</li>
        <li>Held the same safety and legal compliance role for Panther Rocketry.</li>
            </ul>
          </details>
        <details><summary><span>Social Media Chair</span><span class="dates">Aug 2023 – Dec 2024</span></summary>
            <ul>
              <li>Managed AIAA’s social media and promotional content to raise awareness of events, projects, meetings, and activities.</li>
              <li>Created graphics, announcements, and event promotions to communicate with members and the broader student community.</li>
              <li>Collaborated with AIAA leadership and competition teams to highlight projects, achievements, and opportunities.</li>
            </ul>
          </details>
        <details><summary><span>Student Government Association Representative</span><span class="dates">Aug 2023 – Dec 2024</span></summary>
            <ul>
              <li>Represented AIAA within the Student Government Association (SGA), communicating organization needs, concerns, and initiatives.</li>
              <li>Attended SGA meetings and relayed updates, policies, and opportunities back to AIAA leadership and members.</li>
              <li>Collaborated with student organizations and university representatives to support AIAA events, funding initiatives, and activities.</li>
            </ul>
          </details>
          </div>
        </div>
        <div class="card wide">
          <h3>Panther Peer Mentoring</h3>
          <p class="where">Florida Institute of Technology. Click a role to see what I did.</p>
          <div class="roles">
            <details><summary><span>First Year Experience Panther Peer Mentor</span><span class="dates">Aug 2024 – Present</span></summary>
              <ul>
            <li>Mentored a cohort of about 24 first-year engineering students through group meetings, workshops, and structured programming.</li>
            <li>Led group discussions on goal setting, professional development, and adjusting to college-level engineering coursework.</li>
            <li>Guided students in study strategies, time management, and campus resource navigation.</li>
          </ul>
            </details>
            <details><summary><span>Panther Peer Mentor</span><span class="dates">Aug 2024 – Present</span></summary>
              <ul>
            <li>Provided one-on-one academic and personal mentorship to a transfer student, supporting their transition into a rigorous engineering curriculum.</li>
            <li>Worked with peer mentors and program coordinators to identify at-risk students and connect them with academic and wellness resources.</li>
            <li>Completed formal mentor training, strengthening leadership, coaching, and communication skills.</li>
          </ul>
            </details>
          </div>
        </div>
        <div class="card">
          <h3>Student Activities Funding Committee Member</h3>
          <p class="where">Student Government Association</p>
        </div>
        <div class="card">
          <h3>Peer Tutor</h3>
          <p class="where">Florida Institute of Technology</p>
          <p class="when">Sept 2025 – Dec 2025</p>
          <ul>
            <li>Taught one-on-one and small groups in Thermodynamics II, Fluid Mechanics, and Solids Modeling (Creo).</li>
            <li>Adapted methods to different learning styles to build comprehension and confidence.</li>
            <li>Guided students through CAD workflows, parametric design, and manufacturing-ready part modeling in Creo.</li>
            <li>Reinforced unit analysis, boundary conditions, and solution verification in heat transfer, fluid flow, and energy balance problems.</li>
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
          <ul><li>Supported water security research on metal-organic frameworks (MOFs), synthesizing them and running spray-dry experiments with a graduate student.</li><li>Applied materials science and chemistry coursework to hands-on electrochemistry and material characterization experiments.</li></ul>
        </div>
        <div class="card">
          <h3>Campus Ambassador &amp; Club President</h3>
          <p class="where">Hot Girl Walk</p>
          <p class="when">Nov 2024 – Dec 2025</p>
          <ul><li>Built a supportive student community around wellness and personal growth, representing a global female empowerment brand on campus.</li></ul>
        </div>
        <div class="card">
          <h3>Lead Engineer</h3>
          <p class="where">NASA L'SPACE Academy: Proposal Writing and Evaluation Experience (NPWEE)</p>
          <p class="when">Jan 2024 – Apr 2024</p>
          <ul>
            <li>Crafted, reviewed, and scored proposals from a NASA reviewer’s perspective, serving as primary reviewer and co-leading discussion with the Deputy Center Chief Technologist for Marshall Space Flight Center.</li>
            <li>Researched AI/ML inverse modeling for exoplanet atmospheric retrieval in support of the NASA ARIEL Mission, developing algorithms as faster alternatives to MCMC retrieval.</li>
            <li>Generated simulated spectra and benchmarked accuracy, convergence, and computational efficiency.</li>
            <li>Contributed to NASA-style proposal writing and the final technical report with a multidisciplinary team.</li>
          </ul>
        </div>
      </div>
    </div>

    <div class="stage">
      <div class="tag"><b>Stage 1</b><span>Launch pad<br>2016 – 2022</span></div>
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
          <h3>Service Leader</h3>
          <p class="where">Days For Girls, Southern Utah University</p>
          <p class="when">Aug 2020 – May 2022</p>
          <ul>
            <li>Led community service initiatives supporting menstrual health education and access to sustainable hygiene products.</li>
            <li>Organized volunteer teams during packing and assembly events, delegating tasks and keeping quality, safety, and distribution standards.</li>
          </ul>
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
    <p class="sub">Hardware I've designed, built, and flown. <a href="projects.html">See all projects</a></p>
    <div class="payloads">
      <article class="payload"><div class="bay"></div><img class="thumb" src="images/end-effector-1.jpg" alt="" loading="lazy">
        <h3>Flexible End Effectors</h3>
        <p>A flexible end effector built to grasp inner door panels from multiple vehicle models, taken from CAD to load-tested hardware.</p>
        <div class="chips" style="margin-top:12px"><span class="chip">Creo</span><span class="chip">SolidWorks</span><span class="chip">FEA</span><span class="chip">CNC machining</span></div>
        <div class="links"><a href="project-end-effectors.html">View project →</a></div>
      </article>
      <article class="payload"><div class="bay"></div><img class="thumb" src="images/vaporchill.jpg" alt="" loading="lazy">
        <h3>VaporChill: Computer Chip Cooling System</h3>
        <p>Can an HVAC refrigeration cycle cool a high-performance chip better than air or liquid cooling? In the team’s model, yes, even below 0 °C.</p>
        <div class="chips" style="margin-top:12px"><span class="chip">Refrigeration cycle</span><span class="chip">Heat transfer</span><span class="chip">Thermal modeling</span></div>
        <div class="links"><a href="project-vaporchill.html">View project →</a></div>
      </article>
      <article class="payload"><div class="bay"></div><img class="thumb" src="images/cubesat-1.png" alt="" loading="lazy">
        <h3>CubeSat Thermal Management</h3>
        <p>A passive, lightweight thermal-control study for a 1U CubeSat in low Earth orbit, centered on surface coatings.</p>
        <div class="chips" style="margin-top:12px"><span class="chip">Passive thermal control</span><span class="chip">Surface coatings</span><span class="chip">LEO</span></div>
        <div class="links"><a href="project-cubesat-thermal.html">View project →</a></div>
      </article>
      <article class="payload"><div class="bay"></div><img class="thumb" src="images/nar-level-2.jpg" alt="" loading="lazy">
        <h3>NAR Level 2 High-Power Rocketry Certification</h3>
        <p>A K-motor high-power rocket modeled in OpenRocket and flown to about 9,000 ft with avionics and GPS.</p>
        <div class="chips" style="margin-top:12px"><span class="chip">K-class motor</span><span class="chip">OpenRocket</span><span class="chip">Avionics / GPS</span></div>
        <div class="links"><a href="project-nar-level-2.html">View project →</a></div>
      </article>
      <article class="payload"><div class="bay"></div>
        <h3>NAR Level 1 High-Power Rocketry Certification</h3>
        <p>An H-motor high-power rocket designed, built, and flown to 2,000 ft with stability analysis and recovery integration.</p>
        <div class="chips" style="margin-top:12px"><span class="chip">H-class motor</span><span class="chip">Stability analysis</span><span class="chip">Recovery systems</span></div>
        <div class="links"><a href="project-nar-level-1.html">View project →</a></div>
      </article>
    </div>
  </section>

  <section id="education">
    <h2>Training</h2>
    <div class="cards">
      <div class="card">
        <h3>University of Southern California</h3>
        <p class="where">Aerospace Engineering (graduate)</p>
        <p class="when">2026 – Present</p>
      </div>
      <div class="card">
        <h3>Florida Institute of Technology</h3>
        <p class="where">B.S. Mechanical Engineering, Melbourne, Florida</p>
        <p class="when">Aug 2022 – Dec 2025</p>
      </div>
      <div class="card">
        <h3>Jesus College, Oxford</h3>
        <p class="where">Study abroad, England</p>
        <p class="when">Jun 2023 – Aug 2023</p>
      </div>
      <div class="card">
        <h3>Southern Utah University</h3>
        <p class="where">B.S. Mechanical Engineering (transferred)</p>
        <p class="when">Sept 2020 – Apr 2022</p>
      </div>
      <div class="card">
        <h3>Colorado State University</h3>
        <p class="where">Online summer course</p>
        <p class="when">May 2025 – Jul 2025</p>
      </div>
    </div>
    <div class="patches">
      <div class="patch"><b>DL</b>Dean’s List<small>Spring 2023 &amp; Fall 2024</small></div>
      <div class="patch"><b>OS</b>Outstanding Student of the Year<small>Mech. &amp; Civil Eng., 2024 &amp; 2025</small></div>
      <div class="patch"><b>L2</b>NAR Level 1 &amp; 2<small>High-power rocketry, 2022 &amp; 2025</small></div>
      <div class="patch"><b>PM</b>Certificate of Leadership<small>Panther Peer Mentorship, 2025</small></div>
      <div class="patch"><b>AI</b>AIAA Short Courses<small>Digital Engineering; Test &amp; Evaluation, 2025</small></div>
      <div class="patch"><b>ZC</b>Clearance Readiness<small>Zeltech, 2024</small></div>
    </div>
  </section>

  <section id="skills">
    <h2>Toolkit</h2>
    <div class="toolkit">
      <div><h3>Analysis</h3><div class="chips"><span class="chip">FEA</span><span class="chip">CFD</span><span class="chip">ANSYS</span><span class="chip">MATLAB</span><span class="chip">Simulink</span></div></div>
      <div><h3>Design and build</h3><div class="chips"><span class="chip">Creo</span><span class="chip">SolidWorks</span><span class="chip">Fusion 360</span><span class="chip">CNC machining</span><span class="chip">Hardware fabrication</span><span class="chip">Arduino</span><span class="chip">Soldering</span><span class="chip">High-power rocketry</span><span class="chip">Permit drafting (Bluebeam)</span></div></div>
      <div><h3>Code</h3><div class="chips"><span class="chip">C++</span><span class="chip">Python</span><span class="chip">Java</span><span class="chip">OpenCV</span></div></div>
      <div><h3>Team</h3><div class="chips"><span class="chip">Leadership</span><span class="chip">Mentoring</span><span class="chip">Tutoring</span><span class="chip">Safety compliance</span><span class="chip">Media and marketing</span></div></div>
      <div><h3>Memberships</h3><div class="chips"><span class="chip">ASME</span><span class="chip">SWE</span><span class="chip">AIAA</span><span class="chip">FIRST Robotics</span><span class="chip">National Association of Rocketry</span></div></div>
      <div><h3>Community</h3><div class="chips"><span class="chip">Habitat for Humanity</span><span class="chip">Relay for Life</span></div></div>
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
const yr = document.getElementById('yr'); if(yr) yr.textContent = new Date().getFullYear();

// Rocket on the gauge climbs with scroll progress
(function(){
  const r = document.getElementById('climber'); if(!r) return; const g = r.parentElement;
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
  let w, h, stars = [], shoot = null, rk = null;
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
      if(!rk && Math.random() < .002) rk = {x:-40, y:h*(.5+Math.random()*.4), vx:2.2, vy:-1.5};
      if(rk){
        x.save(); x.translate(rk.x, rk.y); x.rotate(Math.atan2(rk.vy, rk.vx));
        const t = x.createLinearGradient(-110,0,0,0);
        t.addColorStop(0,'rgba(255,106,43,0)'); t.addColorStop(1,'rgba(255,194,71,.85)');
        x.fillStyle = t; x.fillRect(-110,-2,110,4);
        x.fillStyle = '#f2f4ff'; x.beginPath(); x.moveTo(18,0); x.quadraticCurveTo(7,-7,-9,-5.5); x.lineTo(-9,5.5); x.quadraticCurveTo(7,7,18,0); x.fill();
        x.fillStyle = '#ff6a2b';
        x.beginPath(); x.moveTo(-2,-5.5); x.lineTo(-11,-12); x.lineTo(-10,-4); x.fill();
        x.beginPath(); x.moveTo(-2,5.5); x.lineTo(-11,12); x.lineTo(-10,4); x.fill();
        x.fillStyle = '#5fe0ee'; x.beginPath(); x.arc(5,0,2.4,0,6.28); x.fill();
        x.restore();
        rk.x += rk.vx; rk.y += rk.vy;
        if(rk.x > w+130 || rk.y < -60) rk = null;
      }
      requestAnimationFrame(draw);
    }
  }
  addEventListener('resize', () => { size(); if(still) draw(); });
  size(); draw();
})();

// Paper buttons: if the PDF has not been uploaded yet, show "coming soon" instead of a broken link
document.querySelectorAll('a[data-paper]').forEach(a => {
  fetch(a.href, {method:'HEAD'}).then(r => { if(!r.ok) throw 0; })
    .catch(() => { a.removeAttribute('href'); a.classList.add('off'); a.textContent = 'Paper coming soon'; });
});

</script>
</body>
</html>
