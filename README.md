<!doctype html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0, viewport-fit=cover">
<title>Ayaan Waqar</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=Sora:wght@500;600;700;800&family=IBM+Plex+Sans:wght@400;500;600&family=IBM+Plex+Mono:wght@400;500&display=swap">
<style>
/* ---------- THEME: dark is the default ---------- */
:root{
  --bg:#0E1116; --surface:#161B22; --surface-2:#1C232E; --ink:#E9ECF2;
  --muted:#98A2B2; --line:#252D38; --accent:#F0803D; --accent-ink:#F79A63;
  --accent-soft:#241913; --shadow:0 10px 30px rgba(0,0,0,.35);
  --max:1080px;
  --sans:"IBM Plex Sans",system-ui,-apple-system,Segoe UI,sans-serif;
  --disp:"Sora",var(--sans);
  --mono:"IBM Plex Mono",ui-monospace,Menlo,monospace;
  color-scheme:dark;
}
:root[data-theme="light"]{
  --bg:#F3F4F7; --surface:#FFFFFF; --surface-2:#E9ECF1; --ink:#151A21;
  --muted:#5A6472; --line:#DBDFE7; --accent:#DE6B2B; --accent-ink:#B4531C;
  --accent-soft:#FBEADE; --shadow:0 10px 30px rgba(20,26,33,.08);
  color-scheme:light;
}
*{box-sizing:border-box}
html{scroll-behavior:smooth}
body{margin:0;background:var(--bg);color:var(--ink);font-family:var(--sans);font-size:16px;line-height:1.65;-webkit-font-smoothing:antialiased}
a{color:inherit}
img{max-width:100%;display:block}
.wrap{max-width:var(--max);margin:0 auto;padding:0 24px}
.eyebrow{font-family:var(--mono);font-size:.72rem;letter-spacing:.18em;text-transform:uppercase;color:var(--accent-ink);font-weight:500}

/* ---------- nav ---------- */
header.nav{position:sticky;top:env(safe-area-inset-top,0px);z-index:30;background:color-mix(in srgb,var(--bg) 86%,transparent);backdrop-filter:blur(10px);border-bottom:1px solid var(--line)}
.nav-inner{max-width:var(--max);margin:0 auto;padding:14px 24px;display:flex;align-items:center;justify-content:space-between;gap:16px}
.brand{font-family:var(--disp);font-weight:800;letter-spacing:-.01em;font-size:1.05rem;text-decoration:none;cursor:pointer}
.brand span{color:var(--accent)}
.nav-links{display:flex;gap:22px;align-items:center}
.nav-links a{font-size:.9rem;text-decoration:none;color:var(--muted);font-weight:500}
.nav-links a:hover{color:var(--ink)}
.toggle{background:var(--surface-2);border:1px solid var(--line);color:var(--ink);border-radius:8px;padding:7px 11px;cursor:pointer;font-family:var(--mono);font-size:.75rem}
@media(max-width:680px){ .nav-links a.navlink{display:none} }

/* ---------- hero ---------- */
.hero{padding:74px 0 54px;border-bottom:1px solid var(--line)}
.hero h1{font-family:var(--disp);font-weight:800;letter-spacing:-.025em;line-height:1.02;font-size:clamp(2.6rem,7vw,4.4rem);margin:.35em 0 .3em;text-wrap:balance}
.hero .lede{font-size:1.18rem;color:var(--muted);max-width:60ch;margin:0}
.cta{display:flex;flex-wrap:wrap;gap:12px;margin-top:28px}
.btn{display:inline-flex;align-items:center;gap:8px;padding:11px 18px;border-radius:10px;text-decoration:none;font-weight:600;font-size:.92rem;border:1px solid var(--line);background:var(--surface);color:var(--ink);transition:transform .12s,border-color .12s;cursor:pointer}
.btn:hover{transform:translateY(-2px);border-color:var(--accent)}
.btn.primary{background:var(--accent);border-color:var(--accent);color:#fff}
.stats{display:grid;grid-template-columns:repeat(4,1fr);gap:18px;margin-top:44px}
@media(max-width:680px){ .stats{grid-template-columns:repeat(2,1fr)} }
.stat .n{font-family:var(--disp);font-weight:700;font-size:1.7rem;color:var(--ink);line-height:1}
.stat .l{font-size:.82rem;color:var(--muted);margin-top:6px}

section.block{padding:58px 0;border-bottom:1px solid var(--line)}
h2.section{font-family:var(--disp);font-weight:700;font-size:clamp(1.5rem,3.5vw,2.1rem);letter-spacing:-.02em;margin:.4em 0 .1em}
.section-sub{color:var(--muted);margin:0 0 26px;max-width:62ch}

/* ---------- flagship cards ---------- */
.grid{display:grid;grid-template-columns:1fr 1fr;gap:20px}
@media(max-width:760px){ .grid{grid-template-columns:1fr} }
.card{background:var(--surface);border:1px solid var(--line);border-radius:16px;overflow:hidden;display:flex;flex-direction:column;transition:border-color .15s,transform .15s,box-shadow .15s;cursor:pointer;text-align:left;padding:0;font:inherit;color:inherit;width:100%}
.card:hover{border-color:var(--accent);transform:translateY(-3px);box-shadow:var(--shadow)}
.card .thumb{aspect-ratio:16/9;width:100%;background:linear-gradient(135deg,var(--surface-2),var(--surface));border-bottom:1px solid var(--line);position:relative;overflow:hidden}
.card .thumb img{width:100%;height:100%;object-fit:cover}
.card .thumb.logo{background:#fff}
.card .thumb.logo img{object-fit:contain;padding:22px}
.card .thumb .ph{position:absolute;inset:0;display:flex;align-items:center;justify-content:center;font-family:var(--disp);font-weight:700;font-size:2.4rem;color:var(--accent);opacity:.55;letter-spacing:.05em}
.card .body{padding:22px 24px 24px;display:flex;flex-direction:column;gap:11px;flex:1}
.card .role{font-family:var(--mono);font-size:.72rem;letter-spacing:.06em;text-transform:uppercase;color:var(--accent-ink)}
.card h3{font-family:var(--disp);font-weight:700;font-size:1.22rem;margin:0;letter-spacing:-.01em}
.card p{margin:0;color:var(--muted);font-size:.95rem}
.metrics{display:flex;flex-wrap:wrap;gap:10px;margin-top:2px}
.metric{font-family:var(--mono);font-size:.76rem;color:var(--ink);background:var(--surface-2);border-radius:7px;padding:4px 9px}
.metric b{color:var(--accent-ink)}
.tags{display:flex;flex-wrap:wrap;gap:7px;margin-top:auto;padding-top:8px}
.tag{font-family:var(--mono);font-size:.7rem;color:var(--muted);border:1px solid var(--line);border-radius:999px;padding:3px 9px}
.more{font-family:var(--mono);font-size:.75rem;color:var(--accent-ink);margin-top:10px}

/* ---------- experience ---------- */
.exp-row{display:grid;grid-template-columns:210px 1fr;gap:18px;padding:18px 0;border-top:1px solid var(--line)}
.exp-row:first-child{border-top:0}
@media(max-width:680px){ .exp-row{grid-template-columns:1fr;gap:4px} }
.exp .org{font-family:var(--disp);font-weight:600}
.exp .when{font-family:var(--mono);font-size:.76rem;color:var(--muted);margin-top:3px}
.exp .what{color:var(--muted);font-size:.95rem}

/* ---------- foundations ---------- */
.found{display:grid;grid-template-columns:repeat(3,1fr);gap:16px}
@media(max-width:760px){ .found{grid-template-columns:repeat(2,1fr)} }
@media(max-width:460px){ .found{grid-template-columns:1fr} }
.fitem{background:var(--surface);border:1px solid var(--line);border-radius:13px;overflow:hidden;text-decoration:none;display:flex;flex-direction:column;transition:border-color .15s,transform .15s,box-shadow .15s}
.fitem:hover{border-color:var(--accent);transform:translateY(-3px);box-shadow:var(--shadow)}
.fitem .fthumb{aspect-ratio:4/3;width:100%;background:linear-gradient(135deg,var(--surface-2),var(--surface));border-bottom:1px solid var(--line);position:relative;overflow:hidden}
.fitem .fthumb img{width:100%;height:100%;object-fit:cover}
.fitem .fthumb .ph{position:absolute;inset:0;display:flex;align-items:center;justify-content:center;font-family:var(--disp);font-weight:700;font-size:1.6rem;color:var(--accent);opacity:.45}
.fitem .fbody{padding:14px 16px 16px}
.fitem b{font-family:var(--disp);font-weight:600;font-size:.98rem;display:block;margin-bottom:3px}
.fitem span{font-size:.83rem;color:var(--muted)}
.fitem .newtag{display:inline-block;font-family:var(--mono);font-size:.62rem;letter-spacing:.08em;text-transform:uppercase;color:#fff;background:var(--accent);border-radius:999px;padding:2px 8px;margin-bottom:6px}

/* ---------- skills ---------- */
.skillwrap{display:flex;flex-wrap:wrap;gap:10px}
.skill{font-family:var(--mono);font-size:.82rem;background:var(--surface);border:1px solid var(--line);border-radius:9px;padding:8px 13px}

footer{padding:52px 0 70px}
footer .row{display:flex;flex-wrap:wrap;justify-content:space-between;align-items:center;gap:16px}
footer a{color:var(--muted);text-decoration:none;font-size:.9rem}
footer a:hover{color:var(--accent)}
.foot-links{display:flex;gap:20px;flex-wrap:wrap}

/* ---------- project detail view ---------- */
#detail{display:none}
.d-back{display:inline-flex;align-items:center;gap:7px;font-family:var(--mono);font-size:.8rem;color:var(--muted);text-decoration:none;margin:30px 0 8px;cursor:pointer;background:none;border:0;padding:0}
.d-back:hover{color:var(--accent)}
.d-head{padding:8px 0 22px;border-bottom:1px solid var(--line);margin-bottom:26px}
.d-head h1{font-family:var(--disp);font-weight:800;letter-spacing:-.02em;font-size:clamp(2rem,5vw,3rem);margin:.2em 0 .15em;text-wrap:balance}
.d-role{font-family:var(--mono);font-size:.76rem;letter-spacing:.06em;text-transform:uppercase;color:var(--accent-ink)}
.d-lede{font-size:1.12rem;color:var(--muted);max-width:64ch;margin:.5em 0 0}
.d-metrics{display:flex;flex-wrap:wrap;gap:12px;margin-top:20px}
.gallery{display:grid;grid-template-columns:repeat(3,1fr);gap:14px;margin:6px 0 30px}
@media(max-width:680px){ .gallery{grid-template-columns:1fr 1fr} }
.gtile{aspect-ratio:4/3;border:1px solid var(--line);border-radius:12px;overflow:hidden;background:linear-gradient(135deg,var(--surface-2),var(--surface));position:relative}
.gtile img{width:100%;height:100%;object-fit:cover}
.gtile.logo{background:#fff}
.gtile.logo img{object-fit:contain;padding:18px}
.gtile .ph{position:absolute;inset:0;display:flex;flex-direction:column;align-items:center;justify-content:center;gap:6px;color:var(--muted);font-family:var(--mono);font-size:.72rem;text-align:center;padding:10px}
.gtile .ph b{font-family:var(--disp);font-size:1.4rem;color:var(--accent);opacity:.5;font-weight:700}
.d-body{display:grid;grid-template-columns:1fr 300px;gap:40px;align-items:start}
@media(max-width:820px){ .d-body{grid-template-columns:1fr} }
.d-body h3{font-family:var(--disp);font-weight:700;font-size:1.15rem;margin:26px 0 10px}
.d-body h3:first-child{margin-top:0}
.d-body p{color:var(--ink);margin:0 0 12px}
.d-list{list-style:none;padding:0;margin:0;display:flex;flex-direction:column;gap:10px}
.d-list li{padding-left:20px;position:relative;color:var(--muted)}
.d-list li::before{content:"";position:absolute;left:0;top:.62em;width:7px;height:7px;border-radius:2px;background:var(--accent)}
.d-aside{background:var(--surface);border:1px solid var(--line);border-radius:14px;padding:20px;position:sticky;top:calc(env(safe-area-inset-top,0px) + 80px)}
.d-aside h4{font-family:var(--mono);font-size:.7rem;letter-spacing:.12em;text-transform:uppercase;color:var(--muted);margin:0 0 12px;font-weight:500}
.d-aside .tags{margin:0 0 20px}
.d-aside .btn{width:100%;justify-content:center;margin-bottom:10px}

::selection{background:var(--accent-soft)}
a:focus-visible,button:focus-visible{outline:2px solid var(--accent);outline-offset:3px;border-radius:6px}
@media(prefers-reduced-motion:reduce){html{scroll-behavior:auto} *{transition:none!important}}
</style>
</head>
<body>

<header class="nav">
  <div class="nav-inner">
    <a class="brand" data-nav="home">Ayaan<span>.</span>Waqar</a>
    <nav class="nav-links">
      <a class="navlink" data-nav="home" href="#work">Work</a>
      <a class="navlink" href="#experience">Experience</a>
      <a class="navlink" href="#foundations">Foundations</a>
      <a class="navlink" href="#contact">Contact</a>
      <button class="toggle" id="themeBtn" aria-label="Toggle color theme">theme</button>
    </nav>
  </div>
</header>

<!-- ============ HOME ============ -->
<main id="home">
  <section class="hero">
    <div class="wrap">
      <div class="eyebrow">Computer Engineering, UW Madison</div>
      <h1>I build hardware, robotics, and AI that solve real problems.</h1>
      <p class="lede">Computer Engineering student and lifelong builder, from pediatric medical wearables and seizure detection devices to autonomous vehicles and production AI systems. I like taking things from a sensor on a breadboard to a working product.</p>
      <div class="cta">
        <a class="btn primary" href="Ayaan_Waqar_Resume.pdf" target="_blank" rel="noopener">Résumé</a>
        <a class="btn" href="https://github.com/AyaanWaqar" target="_blank" rel="noopener">GitHub</a>
        <a class="btn" href="https://www.linkedin.com/in/ayaan-waqar/" target="_blank" rel="noopener">LinkedIn</a>
        <a class="btn" href="mailto:awaqar2@gmail.com">Email</a>
      </div>
      <div class="stats">
        <div class="stat"><div class="n">8 yrs</div><div class="l">building in robotics</div></div>
        <div class="stat"><div class="n">3&times;</div><div class="l">WRO World Finalist, Team Pakistan captain</div></div>
        <div class="stat"><div class="n">8</div><div class="l">research papers and articles</div></div>
        <div class="stat"><div class="n">1/300</div><div class="l">class rank, Head Boy at Aitchison</div></div>
      </div>
    </div>
  </section>

  <section class="block" id="work">
    <div class="wrap">
      <div class="eyebrow">Selected Work</div>
      <h2 class="section">Flagship projects</h2>
      <p class="section-sub">End to end builds where I owned the hardware, firmware, and software, and was judged on whether the system actually worked. Click any project to see the full story and photos.</p>
      <div class="grid" id="cardGrid"></div>
    </div>
  </section>

  <section class="block" id="experience">
    <div class="wrap">
      <div class="eyebrow">Where I have worked</div>
      <h2 class="section">Experience</h2>
      <div class="exp" style="margin-top:20px">
        <div class="exp-row"><div><div class="org">Children's Hospital of Philadelphia</div><div class="when">Aug 2024 to Aug 2026</div></div><div class="what">Technical Advisor, Wearable Prototyping. Designed and built the MVP and custom PCB for a pediatric remote patient monitoring wearable used in clinical testing.</div></div>
        <div class="exp-row"><div><div class="org">Naseeb Online</div><div class="when">Aug 2025 to Dec 2025</div></div><div class="what">AI and ML Intern. Developed LLM enabled conversational systems using RAG, vector databases, and model training (RLHF and DPO) for production recruitment workflows.</div></div>
        <div class="exp-row"><div><div class="org">Medvice Enterprises B.V.</div><div class="when">Jun 2024 to Aug 2024</div></div><div class="what">Software Intern. Debugging, testing, and building algorithms for medical history diagnosis in partnership with the Technical University of Delft.</div></div>
        <div class="exp-row"><div><div class="org">Punjab Information Technology Board</div><div class="when">Jun 2023 to Aug 2023</div></div><div class="what">Software Intern. Product development on the Pakistan Animal Identification and Traceability System (PAITS), with UI design and project management.</div></div>
        <div class="exp-row"><div><div class="org">The Tech School</div><div class="when">2021 to Present</div></div><div class="what">Founder, Curriculum Designer and Instructor. Built and taught an inclusive Python program for differently abled learners, in partnership with the Harvard Spark program.</div></div>
      </div>
    </div>
  </section>

  <section class="block" id="foundations">
    <div class="wrap">
      <div class="eyebrow">How I learned to build</div>
      <h2 class="section">Foundations</h2>
      <p class="section-sub">The hands on electronics and microcontroller projects I cut my teeth on, from a first blinking LED to autonomous and sensor driven systems. Full code for each on GitHub.</p>
      <div class="found" id="foundGrid"></div>
      <p style="margin-top:22px"><a class="btn" href="https://github.com/AyaanWaqar?tab=repositories" target="_blank" rel="noopener">See all repositories on GitHub</a></p>
    </div>
  </section>

  <section class="block" id="skills">
    <div class="wrap">
      <div class="eyebrow">Toolkit</div>
      <h2 class="section">Skills</h2>
      <div class="skillwrap" style="margin-top:20px">
        <span class="skill">Python</span><span class="skill">C / C++</span><span class="skill">Java</span>
        <span class="skill">Arduino / Embedded</span><span class="skill">PCB Design</span><span class="skill">Sensor Integration</span>
        <span class="skill">Robotics</span><span class="skill">Computer Vision</span><span class="skill">Machine Learning</span>
        <span class="skill">RAG / LLMs</span><span class="skill">Vector Databases</span><span class="skill">Git</span>
      </div>
    </div>
  </section>

  <footer id="contact">
    <div class="wrap">
      <div class="eyebrow">Get in touch</div>
      <h2 class="section" style="margin-bottom:22px">Let's build something.</h2>
      <div class="row">
        <div class="foot-links">
          <a href="mailto:awaqar2@gmail.com">awaqar2@gmail.com</a>
          <a href="https://github.com/AyaanWaqar" target="_blank" rel="noopener">GitHub</a>
          <a href="https://www.linkedin.com/in/ayaan-waqar/" target="_blank" rel="noopener">LinkedIn</a>
        </div>
        <div style="color:var(--muted);font-size:.85rem">&copy; <span id="yr"></span> Ayaan Waqar</div>
      </div>
    </div>
  </footer>
</main>

<!-- ============ PROJECT DETAIL ============ -->
<main id="detail" class="wrap"></main>

<script>
/* ---------------- DATA ---------------- */
var PROJECTS = [
  {
    id:"chop",
    title:"Pediatric Remote Monitoring Wearable",
    role:"Technical Advisor, Children's Hospital of Philadelphia",
    initial:"CH",
    tagline:"A wearable that tracks sleep and vitals in hospitalized children, built to hold up in a real clinical setting.",
    metrics:[["&gt;90%","sleep and wake accuracy"],["&minus;60%","component cost"],["24h+","continuous monitoring"]],
    overview:"I designed and built the MVP for a wearable that monitors sleep and vital signs in hospitalized children. The device fuses data from an IMU, an accelerometer, and a temperature sensor, all driven by custom firmware. Once the prototype proved out, I designed the PCB that brought the cost down and made the device viable for clinical testing.",
    contributions:[
      "Integrated IMU, accelerometer, and temperature sensors into a single wearable form factor",
      "Wrote custom firmware for continuous, low power data capture",
      "Designed the PCB that cut component cost by roughly 60 percent",
      "Tuned the sleep and wake classification to above 90 percent accuracy"
    ],
    tech:["Embedded C","PCB Design","Sensor Fusion","Firmware"],
    links:[],
    images:1,
    logo:true
  },
  {
    id:"epilet",
    title:"Epilet, Seizure Detection Wearable",
    role:"Founder, Designer and Developer",
    initial:"EP",
    tagline:"A wristband that detects tonic clonic seizures and alerts caregivers in real time.",
    metrics:[["Real time","caregiver alerts"],["Clinically","informed design"]],
    overview:"Epilet is a wristband that detects tonic clonic (epileptic) seizures and alerts caregivers the moment one is detected. I built the sensing and alert system with direct input from neurologists so it addresses a real clinical need rather than a demo. The focus throughout was a practical, accessible alert system that improves safety for people living with epilepsy.",
    contributions:[
      "Built the seizure detection sensing pipeline and alert logic",
      "Worked with neurology experts to validate the detection approach",
      "Designed a wearable form factor meant for everyday use",
      "Published the design in a peer reviewed journal on epilepsy management"
    ],
    tech:["Wearable","Signal Processing","Health Tech","Arduino"],
    links:[["View on GitHub","https://github.com/AyaanWaqar/Epilet-Watch"]],
    images:1
  },
  {
    id:"wro",
    title:"Autonomous Vehicle, World Robotics Olympiad",
    role:"Captain, Team Pakistan",
    initial:"AV",
    tagline:"A self driving car that completes the WRO track in three laps while reading and reacting to traffic signals, built under live competition constraints.",
    metrics:[["3 laps","fully autonomous"],["3&times;","international finalist"]],
    overview:"As national team captain for Pakistan, I built a self driving car that completes the competition track in three laps while detecting and responding to traffic signals in real time. I wrote the perception and control software and debugged it live under competition constraints, across three years at the WRO international finals in Panama, Germany, and Hungary.",
    contributions:[
      "Wrote the perception software that identifies and reacts to traffic signals",
      "Built the autonomous control loop to complete the track in the lowest time",
      "Led Team Pakistan as captain at three WRO international finals",
      "Won the autonomous car category at regional and national levels"
    ],
    tech:["Robotics","Computer Vision","Control Systems","Embedded"],
    links:[["Related RC car code","https://github.com/AyaanWaqar/Obstacle-Avoiding-RCcars"]],
    images:1
  },
  {
    id:"naseeb",
    title:"Production Conversational AI",
    role:"Intern, Naseeb Online",
    initial:"AI",
    tagline:"LLM powered conversational systems running inside live recruitment workflows.",
    metrics:[["RAG","architecture"],["RLHF / DPO","model training"]],
    overview:"At Naseeb Online I worked on LLM powered conversational systems used inside live recruitment workflows. I built with a RAG architecture and vector databases, worked on model training with RLHF and DPO, and integrated long term and short term memory so conversations stayed coherent over time.",
    contributions:[
      "Implemented conversational AI on a RAG architecture with vector databases",
      "Worked on model training using RLHF and DPO",
      "Integrated long term and short term memory for coherent, adaptive conversations",
      "Built with LangGraph inside production recruitment workflows"
    ],
    tech:["Python","Machine Learning","LLMs","LangGraph","Vector DBs"],
    links:[["Visit rozee.pk","https://www.rozee.pk/"]],
    images:1,
    logo:true
  },
  {
    id:"pakmaweshi",
    title:"Pak Maweshi, Agritech Platform",
    role:"Founder",
    initial:"PM",
    tagline:"A livestock management platform for farmers, built from direct interviews with farming communities.",
    metrics:[["PKR 900k","raised via Spark Tank"],["NSIT","Innovator Award"]],
    overview:"I founded Pak Maweshi, a platform that helps farmers manage livestock productivity and animal management, built from direct interviews with farming communities. It secured roughly PKR 900,000 in funding through the Spark Tank program and won the NSIT Innovator Award. The work later supported Maweshi Madadgar, a women centered livestock program backed by PKR 9 million in funding.",
    contributions:[
      "Interviewed farming communities to define the real problem set",
      "Built a full stack platform for livestock and productivity management",
      "Secured roughly PKR 900,000 through Spark Tank and NSIT awards",
      "Helped seed Maweshi Madadgar, a women centered follow on program"
    ],
    tech:["Full-Stack","Agritech","Product","Research"],
    links:[["Visit pakmaweshi.com","https://pakmaweshi.com/"]],
    images:1,
    logo:true
  },
  {
    id:"diabeticfoot",
    title:"Diabetic Foot Analyzer",
    role:"Creator",
    initial:"DF",
    tagline:"An Arduino based device that monitors foot conditions in diabetic patients to catch early signs of complications.",
    metrics:[["Early","complication detection"],["Continuous","monitoring"]],
    overview:"I created an Arduino based device that monitors foot conditions in diabetic patients to help detect early signs of complications. It combines multiple sensors into continuous, user friendly monitoring so problems can be caught before they become serious.",
    contributions:[
      "Combined multiple sensors into one continuous monitoring device",
      "Built the Arduino firmware for real time readings",
      "Focused the design on early detection of diabetic foot complications",
      "Kept the interface simple enough for everyday patient use"
    ],
    tech:["Embedded","Sensors","Health Tech","Arduino"],
    links:[["View on GitHub","https://github.com/AyaanWaqar/DiabeticFoot"]],
    images:1
  }
];

// [name, description, url, image slug (or ""), isNew]
var FOUNDATIONS = [
  ["Smart Greenhouse","Automated climate control with a DHT sensor, cooling fan, and relay switching under a sealed canopy.","https://github.com/AyaanWaqar?tab=repositories","greenhouse",true],
  ["Autonomous Boat","Self navigating boat driven by dual brushless motors and 30A ESCs on a custom hull.","https://github.com/AyaanWaqar?tab=repositories","boat",true],
  ["Bluetooth RC Car","RC car driven over a Bluetooth module.","https://github.com/AyaanWaqar/BluetoothRC","bluetooth",false],
  ["Obstacle Avoiding Car","Ultrasonic sensor navigation with front facing range finders.","https://github.com/AyaanWaqar/Obstacle-Avoiding-RCcars","obstacle",false],
  ["Fingerprint Door Lock","Fingerprint sensor, servo, and LCD access control.","https://github.com/AyaanWaqar/FingerPrintDoorLock","fingerprint",false],
  ["Weather Station","Live humidity, temperature, and rain readout on an LCD.","https://github.com/AyaanWaqar/TempSensor","weather",false],
  ["Relay Control","Switching high voltage loads and lights from an Arduino.","https://github.com/AyaanWaqar/RelayModules","relay",false],
  ["Timed Trial Car","Hard coded drive routines for timed courses.","https://github.com/AyaanWaqar/HardCodeRc","car2",false],
  ["Line Following Car","Multi IR sensor line tracking.","https://github.com/AyaanWaqar/LineFollowingRc","",false],
  ["Sound Detection","Clap activated switching.","https://github.com/AyaanWaqar/SoundSensor","",false],
  ["Motion Detection","PIR motion sensing.","https://github.com/AyaanWaqar/MotionSensor","",false],
  ["Servo and LCD Modules","Actuation and display building blocks.","https://github.com/AyaanWaqar/ServoMotor","",false],
  ["LDR and IR Sensors","Light and proximity sensing fundamentals.","https://github.com/AyaanWaqar/LDR-IR-Sensors","",false],
  ["LED Fundamentals","Where it all started.","https://github.com/AyaanWaqar/LEDs","",false]
];

/* ---------------- RENDER HOME ---------------- */
function imgTile(pid, n, cls, phInner){
  var wrap = document.createElement('div');
  wrap.className = cls;
  var img = document.createElement('img');
  img.alt = "";
  img.loading = "lazy";
  img.src = pid + "-" + n + ".jpg";
  var ph = document.createElement('div');
  ph.className = "ph";
  ph.innerHTML = phInner;
  img.onerror = function(){ img.remove(); };
  wrap.appendChild(img);
  wrap.appendChild(ph);
  return wrap;
}

function renderCards(){
  var grid = document.getElementById('cardGrid');
  PROJECTS.forEach(function(p){
    var btn = document.createElement('button');
    btn.className = 'card';
    btn.setAttribute('data-project', p.id);

    var thumb = document.createElement('div');
    thumb.className = 'thumb' + (p.logo ? ' logo' : '');
    var img = document.createElement('img');
    img.alt = ""; img.loading = "lazy";
    img.src = p.id + "-1.jpg";
    var ph = document.createElement('div');
    ph.className = 'ph'; ph.textContent = p.initial;
    img.onerror = function(){ img.remove(); };
    img.onload = function(){ ph.remove(); };
    thumb.appendChild(img); thumb.appendChild(ph);

    var body = document.createElement('div');
    body.className = 'body';
    var metrics = p.metrics.map(function(m){
      return '<span class="metric"><b>'+m[0]+'</b> '+m[1]+'</span>';
    }).join('');
    var tags = p.tech.slice(0,4).map(function(t){ return '<span class="tag">'+t+'</span>'; }).join('');
    body.innerHTML =
      '<div class="role">'+p.role+'</div>'+
      '<h3>'+p.title+'</h3>'+
      '<p>'+p.tagline+'</p>'+
      '<div class="metrics">'+metrics+'</div>'+
      '<div class="tags">'+tags+'</div>'+
      '<div class="more">Read more &rarr;</div>';

    btn.appendChild(thumb);
    btn.appendChild(body);
    btn.addEventListener('click', function(){ location.hash = 'project/' + p.id; });
    grid.appendChild(btn);
  });
}

function renderFoundations(){
  var grid = document.getElementById('foundGrid');
  FOUNDATIONS.forEach(function(f){
    var a = document.createElement('a');
    a.className = 'fitem';
    a.href = f[2]; a.target = "_blank"; a.rel = "noopener";

    var thumb = document.createElement('div');
    thumb.className = 'fthumb';
    var initials = f[0].split(' ').slice(0,2).map(function(w){return w[0];}).join('');
    if(f[3]){
      var img = document.createElement('img');
      img.alt = f[0]; img.loading = "lazy";
      img.src = "f-" + f[3] + ".jpg";
      var ph = document.createElement('div'); ph.className='ph'; ph.textContent=initials;
      img.onerror = function(){ img.remove(); };
      img.onload = function(){ ph.remove(); };
      thumb.appendChild(img); thumb.appendChild(ph);
    } else {
      var ph2 = document.createElement('div'); ph2.className='ph'; ph2.textContent=initials;
      thumb.appendChild(ph2);
    }

    var body = document.createElement('div');
    body.className = 'fbody';
    body.innerHTML = (f[4] ? '<span class="newtag">New</span><br>' : '') +
      '<b>'+f[0]+'</b><span>'+f[1]+'</span>';

    a.appendChild(thumb);
    a.appendChild(body);
    grid.appendChild(a);
  });
}

/* ---------------- RENDER DETAIL ---------------- */
function renderDetail(p){
  var d = document.getElementById('detail');
  var gallery = '';
  for(var i=1;i<=p.images;i++){
    gallery += '<div class="gtile'+(p.logo?' logo':'')+'" data-g="'+p.id+'-'+i+'"></div>';
  }
  var metrics = p.metrics.map(function(m){
    return '<span class="metric"><b>'+m[0]+'</b> '+m[1]+'</span>';
  }).join('');
  var tags = p.tech.map(function(t){ return '<span class="tag">'+t+'</span>'; }).join('');
  var links = p.links.map(function(l){
    return '<a class="btn primary" href="'+l[1]+'" target="_blank" rel="noopener">'+l[0]+'</a>';
  }).join('');
  var contribs = p.contributions.map(function(c){ return '<li>'+c+'</li>'; }).join('');

  d.innerHTML =
    '<button class="d-back" id="backBtn">&larr; Back to all work</button>'+
    '<div class="d-head">'+
      '<div class="d-role">'+p.role+'</div>'+
      '<h1>'+p.title+'</h1>'+
      '<p class="d-lede">'+p.tagline+'</p>'+
      '<div class="d-metrics">'+metrics+'</div>'+
    '</div>'+
    '<div class="gallery" id="gal">'+gallery+'</div>'+
    '<div class="d-body">'+
      '<div>'+
        '<h3>Overview</h3><p>'+p.overview+'</p>'+
        '<h3>What I built</h3><ul class="d-list">'+contribs+'</ul>'+
      '</div>'+
      '<aside class="d-aside">'+
        '<h4>Built with</h4><div class="tags">'+tags+'</div>'+
        (links ? '<h4>Links</h4>'+links : '')+
      '</aside>'+
    '</div>';

  // fill gallery tiles with images if present, else placeholder
  var tiles = d.querySelectorAll('.gtile');
  tiles.forEach(function(t,idx){
    var key = t.getAttribute('data-g');
    var img = new Image();
    img.alt=""; img.loading="lazy";
    img.onload = function(){ t.innerHTML=''; t.appendChild(img); };
    img.onerror = function(){
      t.innerHTML = '<div class="ph"><b>'+p.initial+'</b><span>photo '+(idx+1)+'</span></div>';
    };
    img.src = key + ".jpg";
  });

  document.getElementById('backBtn').addEventListener('click', function(){ location.hash=''; });
}

/* ---------------- ROUTER ---------------- */
function router(){
  var hash = location.hash.replace(/^#/,'');
  var home = document.getElementById('home');
  var detail = document.getElementById('detail');
  if(hash.indexOf('project/')===0){
    var id = hash.split('/')[1];
    var p = PROJECTS.filter(function(x){return x.id===id;})[0];
    if(p){
      home.style.display='none';
      detail.style.display='block';
      renderDetail(p);
      window.scrollTo(0,0);
      return;
    }
  }
  detail.style.display='none';
  home.style.display='block';
}

/* ---------------- THEME + INIT ---------------- */
(function(){
  var root=document.documentElement, btn=document.getElementById('themeBtn');
  try{ var saved=localStorage.getItem('theme'); if(saved) root.setAttribute('data-theme',saved); }catch(e){}
  function label(){ var d=root.getAttribute('data-theme')||'dark'; btn.textContent = d==='light' ? '☾ dark' : '☀ light'; }
  label();
  btn.addEventListener('click',function(){
    var cur=root.getAttribute('data-theme')||'dark';
    var next=cur==='light'?'dark':'light';
    root.setAttribute('data-theme',next);
    try{localStorage.setItem('theme',next);}catch(e){}
    label();
  });
  document.querySelectorAll('[data-nav="home"]').forEach(function(el){
    el.addEventListener('click', function(e){
      if(el.classList.contains('navlink')) return; // let anchor links work
      e.preventDefault(); location.hash='';
      window.scrollTo(0,0);
    });
  });
  document.getElementById('yr').textContent=new Date().getFullYear();
  renderCards();
  renderFoundations();
  window.addEventListener('hashchange', router);
  router();
})();
</script>
</body>
</html>
