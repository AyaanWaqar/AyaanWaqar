<!doctype html>
<html lang="en">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<title>Ayaan Waqar</title>
<meta name="description" content="Ayaan Waqar — Computer Engineering student building embedded systems, robotics, and AI for real-world problems.">
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=Sora:wght@500;600;700;800&family=IBM+Plex+Sans:ital,wght@0,400;0,500;0,600;1,400&family=IBM+Plex+Mono:wght@400;500;600&display=swap">
<style>
  :root{
    --bg:#F3F4F7; --surface:#FFFFFF; --surface-2:#E9ECF1; --ink:#151A21; --muted:#5A6472;
    --line:#DBDFE7; --accent:#DE6B2B; --accent-ink:#B4531C; --accent-soft:#FBEADE;
    --max:1080px;
    --sans:"IBM Plex Sans",system-ui,-apple-system,Segoe UI,sans-serif;
    --disp:"Sora",var(--sans); --mono:"IBM Plex Mono",ui-monospace,Menlo,monospace;
  }
  @media (prefers-color-scheme: dark){
    :root:not([data-theme="light"]){
      --bg:#0E1116; --surface:#161B22; --surface-2:#1C232E; --ink:#E9ECF2; --muted:#98A2B2;
      --line:#252D38; --accent:#F0803D; --accent-ink:#F0803D; --accent-soft:#241913;
      color-scheme:dark;
    }
  }
  :root[data-theme="dark"]{
    --bg:#0E1116; --surface:#161B22; --surface-2:#1C232E; --ink:#E9ECF2; --muted:#98A2B2;
    --line:#252D38; --accent:#F0803D; --accent-ink:#F0803D; --accent-soft:#241913;
    color-scheme:dark;
  }
  *{box-sizing:border-box}
  html{scroll-behavior:smooth}
  body{margin:0;background:var(--bg);color:var(--ink);font-family:var(--sans);font-size:16px;line-height:1.6;-webkit-font-smoothing:antialiased}
  a{color:inherit}
  img{max-width:100%}
  .wrap{max-width:var(--max);margin:0 auto;padding:0 24px}
  .eyebrow{font-family:var(--mono);font-size:.72rem;letter-spacing:.18em;text-transform:uppercase;color:var(--accent-ink);font-weight:600}

  /* nav */
  header.nav{position:sticky;top:0;z-index:20;background:color-mix(in srgb,var(--bg) 88%,transparent);backdrop-filter:blur(10px);border-bottom:1px solid var(--line)}
  .nav-inner{max-width:var(--max);margin:0 auto;padding:14px 24px;display:flex;align-items:center;justify-content:space-between;gap:16px}
  .brand{font-family:var(--disp);font-weight:800;letter-spacing:-.01em;font-size:1.05rem}
  .brand span{color:var(--accent)}
  .nav-links{display:flex;gap:22px;align-items:center}
  .nav-links a{font-size:.9rem;text-decoration:none;color:var(--muted);font-weight:500}
  .nav-links a:hover{color:var(--ink)}
  .toggle{background:var(--surface-2);border:1px solid var(--line);color:var(--ink);border-radius:8px;padding:7px 10px;cursor:pointer;font-family:var(--mono);font-size:.75rem}
  @media(max-width:680px){ .nav-links a:not(.toggle-wrap){display:none} }

  /* hero */
  .hero{padding:76px 0 56px;border-bottom:1px solid var(--line)}
  .hero h1{font-family:var(--disp);font-weight:800;letter-spacing:-.025em;line-height:1.02;font-size:clamp(2.6rem,7vw,4.6rem);margin:.35em 0 .3em;text-wrap:balance}
  .hero .lede{font-size:1.2rem;color:var(--muted);max-width:60ch;margin:0}
  .cta{display:flex;flex-wrap:wrap;gap:12px;margin-top:30px}
  .btn{display:inline-flex;align-items:center;gap:8px;padding:11px 18px;border-radius:10px;text-decoration:none;font-weight:600;font-size:.92rem;border:1px solid var(--line);background:var(--surface);color:var(--ink);transition:transform .12s,border-color .12s}
  .btn:hover{transform:translateY(-2px);border-color:var(--accent)}
  .btn.primary{background:var(--accent);border-color:var(--accent);color:#fff}
  .btn.primary:hover{border-color:var(--accent)}
  .stats{display:grid;grid-template-columns:repeat(4,1fr);gap:18px;margin-top:44px}
  @media(max-width:680px){ .stats{grid-template-columns:repeat(2,1fr)} }
  .stat .n{font-family:var(--disp);font-weight:700;font-size:1.7rem;color:var(--ink);line-height:1}
  .stat .l{font-size:.82rem;color:var(--muted);margin-top:6px}

  section.block{padding:60px 0;border-bottom:1px solid var(--line)}
  h2.section{font-family:var(--disp);font-weight:700;font-size:clamp(1.5rem,3.5vw,2.1rem);letter-spacing:-.02em;margin:.4em 0 .1em}
  .section-sub{color:var(--muted);margin:0 0 26px;max-width:60ch}

  /* flagship project cards */
  .grid{display:grid;grid-template-columns:1fr 1fr;gap:20px}
  @media(max-width:760px){ .grid{grid-template-columns:1fr} }
  .card{background:var(--surface);border:1px solid var(--line);border-radius:16px;padding:24px;display:flex;flex-direction:column;gap:12px;transition:border-color .15s,transform .15s}
  .card:hover{border-color:var(--accent);transform:translateY(-3px)}
  .card h3{font-family:var(--disp);font-weight:700;font-size:1.22rem;margin:0;letter-spacing:-.01em}
  .card .role{font-family:var(--mono);font-size:.72rem;letter-spacing:.08em;text-transform:uppercase;color:var(--accent-ink)}
  .card p{margin:0;color:var(--muted);font-size:.95rem}
  .metrics{display:flex;flex-wrap:wrap;gap:14px;margin-top:2px}
  .metric{font-family:var(--mono);font-size:.78rem;color:var(--ink);background:var(--surface-2);border-radius:7px;padding:4px 9px}
  .metric b{color:var(--accent-ink)}
  .tags{display:flex;flex-wrap:wrap;gap:7px;margin-top:auto;padding-top:6px}
  .tag{font-family:var(--mono);font-size:.7rem;color:var(--muted);border:1px solid var(--line);border-radius:999px;padding:3px 9px}

  /* experience */
  .exp{display:flex;flex-direction:column;gap:0}
  .exp-row{display:grid;grid-template-columns:200px 1fr;gap:18px;padding:18px 0;border-top:1px solid var(--line)}
  .exp-row:first-child{border-top:0}
  @media(max-width:680px){ .exp-row{grid-template-columns:1fr;gap:4px} }
  .exp .org{font-family:var(--disp);font-weight:600}
  .exp .when{font-family:var(--mono);font-size:.76rem;color:var(--muted);margin-top:3px}
  .exp .what{color:var(--muted);font-size:.95rem}

  /* foundations */
  .found{display:grid;grid-template-columns:repeat(3,1fr);gap:12px}
  @media(max-width:760px){ .found{grid-template-columns:repeat(2,1fr)} }
  @media(max-width:460px){ .found{grid-template-columns:1fr} }
  .fitem{background:var(--surface);border:1px solid var(--line);border-radius:11px;padding:13px 15px}
  .fitem b{font-family:var(--disp);font-weight:600;font-size:.95rem;display:block}
  .fitem span{font-size:.82rem;color:var(--muted)}

  /* skills */
  .skillwrap{display:flex;flex-wrap:wrap;gap:10px}
  .skill{font-family:var(--mono);font-size:.82rem;background:var(--surface);border:1px solid var(--line);border-radius:9px;padding:8px 13px}

  footer{padding:52px 0 70px}
  footer .row{display:flex;flex-wrap:wrap;justify-content:space-between;align-items:center;gap:16px}
  footer a{color:var(--muted);text-decoration:none;font-size:.9rem}
  footer a:hover{color:var(--accent)}
  .foot-links{display:flex;gap:20px;flex-wrap:wrap}
  ::selection{background:var(--accent-soft)}
  a:focus-visible,button:focus-visible{outline:2px solid var(--accent);outline-offset:3px;border-radius:6px}
  @media(prefers-reduced-motion:reduce){html{scroll-behavior:auto} *{transition:none!important}}
</style>
</head>
<body>

<header class="nav">
  <div class="nav-inner">
    <div class="brand">Ayaan<span>.</span>Waqar</div>
    <nav class="nav-links">
      <a href="#work">Work</a>
      <a href="#experience">Experience</a>
      <a href="#foundations">Foundations</a>
      <a href="#contact">Contact</a>
      <button class="toggle" id="themeBtn" aria-label="Toggle theme">theme</button>
    </nav>
  </div>
</header>

<main>
  <section class="hero">
    <div class="wrap">
      <span class="eyebrow">Computer Engineering · UW–Madison</span>
      <h1>I build hardware, robotics, and AI that solve real problems.</h1>
      <p class="lede">Computer Engineering student and lifelong builder — from pediatric medical wearables and seizure-detection devices to autonomous vehicles and production AI systems. I like taking things from a sensor on a breadboard to a working product.</p>
      <div class="cta">
        <a class="btn primary" href="https://github.com/AyaanWaqar" target="_blank" rel="noopener">GitHub</a>
        <a class="btn" href="https://www.linkedin.com/in/ayaan-waqar/" target="_blank" rel="noopener">LinkedIn</a>
        <a class="btn" href="mailto:ayaanwaqar1@gmail.com">Email</a>
        <a class="btn" href="Ayaan_Waqar_Resume.pdf" target="_blank" rel="noopener">Résumé</a>
      </div>
      <div class="stats">
        <div class="stat"><div class="n">8 yrs</div><div class="l">in robotics</div></div>
        <div class="stat"><div class="n">3×</div><div class="l">WRO World Finalist (Team Pakistan captain)</div></div>
        <div class="stat"><div class="n">5+</div><div class="l">health &amp; hardware products built</div></div>
        <div class="stat"><div class="n">1/300</div><div class="l">class rank, Head Boy · Aitchison</div></div>
      </div>
    </div>
  </section>

  <section class="block" id="work">
    <div class="wrap">
      <span class="eyebrow">Selected Work</span>
      <h2 class="section">Flagship projects</h2>
      <p class="section-sub">End-to-end builds where I owned the hardware, firmware, and software, and was judged on whether the system actually worked.</p>
      <div class="grid">

        <div class="card">
          <div class="role">Technical Advisor · Children's Hospital of Philadelphia</div>
          <h3>Pediatric Remote-Monitoring Wearable</h3>
          <p>Designed and built the MVP for a wearable that tracks sleep and vitals in hospitalized children, integrating IMU, accelerometer, and temperature sensors with custom firmware, then designed the PCB that made it viable for clinical testing.</p>
          <div class="metrics"><span class="metric"><b>&gt;90%</b> sleep/wake accuracy</span><span class="metric"><b>−60%</b> component cost</span><span class="metric"><b>24h+</b> monitoring</span></div>
          <div class="tags"><span class="tag">Embedded C</span><span class="tag">PCB Design</span><span class="tag">Sensor Fusion</span><span class="tag">Firmware</span></div>
        </div>

        <div class="card">
          <div class="role">Founder · Designer &amp; Developer</div>
          <h3>Epilet — Seizure-Detection Wearable</h3>
          <p>A wristband that detects tonic-clonic (epileptic) seizures and alerts caregivers in real time. Built the sensing and alert system with input from neurologists so it meets a real clinical need, not just a demo.</p>
          <div class="metrics"><span class="metric">Real-time alerts</span><span class="metric">Clinically informed</span></div>
          <div class="tags"><span class="tag">Wearable</span><span class="tag">Signal Processing</span><span class="tag">Health Tech</span></div>
        </div>

        <div class="card">
          <div class="role">Captain · Team Pakistan · World Robotics Olympiad</div>
          <h3>Autonomous Vehicle</h3>
          <p>Built a self-driving car that completes the competition track in three laps while detecting and responding to traffic signals in real time. Wrote the perception and control software and debugged it live under competition constraints — three years as national team captain at the international finals.</p>
          <div class="metrics"><span class="metric">Real-time perception</span><span class="metric">Autonomous control</span></div>
          <div class="tags"><span class="tag">Robotics</span><span class="tag">Computer Vision</span><span class="tag">Control Systems</span></div>
        </div>

        <div class="card">
          <div class="role">Intern · Naseeb Online</div>
          <h3>Production Conversational AI</h3>
          <p>Worked on LLM-powered conversational systems used inside live recruitment workflows — building with RAG architecture, vector databases, and model training (RLHF/DPO), and integrating long- and short-term memory for more coherent conversations.</p>
          <div class="metrics"><span class="metric">RAG</span><span class="metric">Vector DBs</span><span class="metric">LangGraph</span></div>
          <div class="tags"><span class="tag">Python</span><span class="tag">Machine Learning</span><span class="tag">LLMs</span></div>
        </div>

        <div class="card">
          <div class="role">Founder</div>
          <h3>Pak Maweshi — Agritech Platform</h3>
          <p>Founded a platform that helps farmers manage livestock and productivity, built from direct interviews with farming communities. Secured roughly PKR 900,000 in funding through the Spark Tank program and won the NSIT Innovator Award.</p>
          <div class="metrics"><span class="metric"><b>~PKR 900k</b> raised</span><span class="metric">NSIT Innovator Award</span></div>
          <div class="tags"><span class="tag">Full-Stack</span><span class="tag">Agritech</span><span class="tag">Product</span></div>
        </div>

        <div class="card">
          <div class="role">Creator</div>
          <h3>Diabetic Foot Analyzer</h3>
          <p>An Arduino-based device that monitors foot conditions in diabetic patients to catch early signs of complications, combining multiple sensors into continuous, user-friendly monitoring.</p>
          <div class="metrics"><span class="metric">Early detection</span><span class="metric">Continuous monitoring</span></div>
          <div class="tags"><span class="tag">Embedded</span><span class="tag">Sensors</span><span class="tag">Health Tech</span></div>
        </div>

      </div>
    </div>
  </section>

  <section class="block" id="experience">
    <div class="wrap">
      <span class="eyebrow">Where I've worked</span>
      <h2 class="section">Experience</h2>
      <div class="exp">
        <div class="exp-row">
          <div><div class="org">Children's Hospital of Philadelphia</div><div class="when">Technical Advisor · Wearable Prototyping</div></div>
          <div class="what">Built the MVP and custom PCB for a pediatric remote-monitoring wearable used in clinical testing.</div>
        </div>
        <div class="exp-row">
          <div><div class="org">Naseeb Online</div><div class="when">AI/ML Intern</div></div>
          <div class="what">Developed LLM-enabled conversational systems (RAG, vector databases, RLHF/DPO) for production recruitment workflows.</div>
        </div>
        <div class="exp-row">
          <div><div class="org">Medvice Enterprises B.V.</div><div class="when">Software Intern</div></div>
          <div class="what">Debugging, testing, and building algorithms for medical-history diagnosis with the Technical University of Delft.</div>
        </div>
        <div class="exp-row">
          <div><div class="org">Punjab Information Technology Board</div><div class="when">Software Intern</div></div>
          <div class="what">Product development on the Pakistan Animal Identification &amp; Traceability System (PAITS); UI design and project management.</div>
        </div>
        <div class="exp-row">
          <div><div class="org">The Tech School</div><div class="when">Founder · Curriculum Designer &amp; Instructor</div></div>
          <div class="what">Built and taught an inclusive Python program for differently-abled learners, in partnership with the Harvard Spark Summer Program.</div>
        </div>
      </div>
    </div>
  </section>

  <section class="block" id="foundations">
    <div class="wrap">
      <span class="eyebrow">How I learned to build</span>
      <h2 class="section">Foundations</h2>
      <p class="section-sub">The hands-on electronics and microcontroller projects I cut my teeth on — from a first blinking LED to autonomous and sensor-driven systems. Full code for each on GitHub.</p>
      <div class="found">
        <div class="fitem"><b>Fingerprint Door Lock</b><span>Fingerprint sensor, servo, and LCD access control.</span></div>
        <div class="fitem"><b>Bluetooth RC Car</b><span>RC car driven over a Bluetooth module.</span></div>
        <div class="fitem"><b>Line-Following Car</b><span>Multi-IR-sensor line tracking.</span></div>
        <div class="fitem"><b>Obstacle-Avoiding Car</b><span>Ultrasonic-sensor navigation.</span></div>
        <div class="fitem"><b>Timed-Trial Car</b><span>Hard-coded routines for timed courses.</span></div>
        <div class="fitem"><b>Sound Detection</b><span>Clap-activated switching.</span></div>
        <div class="fitem"><b>Motion Detection</b><span>PIR motion sensing.</span></div>
        <div class="fitem"><b>MLX Temperature Sensor</b><span>Live Fahrenheit/Celsius readout.</span></div>
        <div class="fitem"><b>Relay Control</b><span>Switching high-voltage loads from an Arduino.</span></div>
        <div class="fitem"><b>Servo &amp; LCD Modules</b><span>Actuation and display building blocks.</span></div>
        <div class="fitem"><b>LDR &amp; IR Sensors</b><span>Light and proximity sensing fundamentals.</span></div>
        <div class="fitem"><b>LED Fundamentals</b><span>Where it all started.</span></div>
      </div>
      <div style="margin-top:22px"><a class="btn" href="https://github.com/AyaanWaqar" target="_blank" rel="noopener">See all repositories on GitHub →</a></div>
    </div>
  </section>

  <section class="block" id="skills">
    <div class="wrap">
      <span class="eyebrow">Toolkit</span>
      <h2 class="section">Skills</h2>
      <div class="skillwrap">
        <span class="skill">Python</span><span class="skill">C / C++</span><span class="skill">Java</span>
        <span class="skill">Arduino / Embedded</span><span class="skill">PCB Design</span><span class="skill">Sensor Integration</span>
        <span class="skill">Robotics</span><span class="skill">Computer Vision</span><span class="skill">Machine Learning</span>
        <span class="skill">RAG / LLMs</span><span class="skill">Vector Databases</span><span class="skill">Git</span>
      </div>
    </div>
  </section>
</main>

<footer id="contact">
  <div class="wrap">
    <span class="eyebrow">Get in touch</span>
    <h2 class="section" style="margin-bottom:18px">Let's build something.</h2>
    <div class="row">
      <div class="foot-links">
        <a href="mailto:ayaanwaqar1@gmail.com">ayaanwaqar1@gmail.com</a>
        <a href="https://github.com/AyaanWaqar" target="_blank" rel="noopener">GitHub</a>
        <a href="https://www.linkedin.com/in/ayaan-waqar/" target="_blank" rel="noopener">LinkedIn</a>
      </div>
      <div style="font-family:var(--mono);font-size:.78rem;color:var(--muted)">© <span id="yr"></span> Ayaan Waqar</div>
    </div>
  </div>
</footer>

<script>
  (function(){
    var root=document.documentElement, btn=document.getElementById('themeBtn');
    function sysDark(){return window.matchMedia&&window.matchMedia('(prefers-color-scheme: dark)').matches;}
    try{var saved=localStorage.getItem('theme'); if(saved)root.setAttribute('data-theme',saved);}catch(e){}
    function label(){var d=root.getAttribute('data-theme')|| (sysDark()?'dark':'light'); btn.textContent=d==='dark'?'☀ light':'☾ dark';}
    label();
    btn.addEventListener('click',function(){
      var cur=root.getAttribute('data-theme')|| (sysDark()?'dark':'light');
      var next=cur==='dark'?'light':'dark';
      root.setAttribute('data-theme',next);
      try{localStorage.setItem('theme',next);}catch(e){}
      label();
    });
    document.getElementById('yr').textContent=new Date().getFullYear();
  })();
</script>
</body>
</html>
