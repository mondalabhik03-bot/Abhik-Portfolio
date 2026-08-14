<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Abhik Mondal — Applied AI/ML Engineer</title>
<meta name="description" content="Abhik Mondal — Applied AI/ML Engineer building RAG pipelines, self-healing Android agents, and science content for 128,000+ people.">
<meta name="theme-color" content="#0a0c12">
<meta property="og:title" content="Abhik Mondal — Applied AI/ML Engineer">
<meta property="og:description" content="RAG pipelines, a self-healing Android app, and science content for 128,000+ people.">
<meta property="og:type" content="website">
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=IBM+Plex+Mono:wght@400;500;600&family=Inter:wght@400;500;600;700&family=Space+Grotesk:wght@500;600;700&display=swap" rel="stylesheet">
<style>

/* ---------- tokens ---------- */
:root{
  --bg:#0a0c12;
  --bg-raised:#0e111a;
  --surface:#141926;
  --surface-2:#1a2032;
  --border:#262c3f;
  --border-soft:#1d2334;
  --text:#edeff5;
  --text-muted:#8d93a8;
  --text-faint:#5b6172;
  --violet:#8b6fff;
  --violet-dim:#5d4fb8;
  --amber:#ffb454;
  --cyan:#5eead4;
  --radius:14px;
  --radius-sm:8px;
  --font-display:'Space Grotesk', sans-serif;
  --font-body:'Inter', sans-serif;
  --font-mono:'IBM Plex Mono', monospace;
  --maxw:1120px;
}

*{box-sizing:border-box;}
html{scroll-behavior:smooth;}
body{
  margin:0;
  background:var(--bg);
  color:var(--text);
  font-family:var(--font-body);
  font-size:16px;
  line-height:1.6;
  -webkit-font-smoothing:antialiased;
}
h1,h2,h3{font-family:var(--font-display); margin:0; letter-spacing:-0.01em;}
p{margin:0;}
a{color:inherit;}
ul{margin:0;padding:0;list-style:none;}
img,svg{display:block;max-width:100%;}
button{font-family:inherit;cursor:pointer;}
:focus-visible{outline:2px solid var(--amber); outline-offset:3px; border-radius:4px;}

.wrap{max-width:var(--maxw); margin:0 auto; padding:0 28px;}
.eyebrow{
  font-family:var(--font-mono);
  font-size:12.5px;
  letter-spacing:0.14em;
  text-transform:uppercase;
  color:var(--text-faint);
  display:flex; align-items:center; gap:10px;
  margin-bottom:14px;
}
.eyebrow::before{content:"";width:16px;height:1px;background:var(--border);}
section{padding:96px 0; scroll-margin-top:76px;}
@media (max-width:720px){ section{padding:64px 0;} }

/* ---------- nav ---------- */
.nav{
  position:sticky; top:0; z-index:50;
  background:rgba(10,12,18,0.82);
  backdrop-filter:blur(10px);
  border-bottom:1px solid var(--border-soft);
}
.nav .wrap{
  display:flex; align-items:center; justify-content:space-between;
  padding-top:18px; padding-bottom:18px;
}
.nav-logo{
  font-family:var(--font-mono); font-size:14px; font-weight:600;
  letter-spacing:0.04em; color:var(--text);
  display:flex; align-items:center; gap:8px;
}
.nav-logo .dot{width:7px;height:7px;border-radius:50%;background:var(--amber); box-shadow:0 0 8px var(--amber);}
.nav-links{display:flex; gap:28px; overflow-x:auto; scrollbar-width:none;}
.nav-links::-webkit-scrollbar{display:none;}
.nav-links a{
  font-size:14px; color:var(--text-muted); text-decoration:none;
  white-space:nowrap; padding-bottom:2px; border-bottom:1px solid transparent;
  transition:color .15s ease, border-color .15s ease;
}
.nav-links a:hover{color:var(--text);}
.nav-links a.active{color:var(--amber); border-color:var(--amber);}
.nav-cta{
  font-family:var(--font-mono); font-size:13px;
  color:var(--bg); background:var(--amber);
  padding:8px 14px; border-radius:7px; text-decoration:none;
  white-space:nowrap;
}
@media (max-width:640px){ .nav-cta{display:none;} }

/* ---------- hero ---------- */
.hero{position:relative; padding-top:76px; overflow:hidden;}
.hero::before{
  content:"";
  position:absolute; top:-220px; left:50%;
  width:900px; height:560px;
  transform:translateX(-50%);
  background:radial-gradient(closest-side, rgba(139,111,255,0.20), rgba(139,111,255,0) 70%);
  filter:blur(10px);
  pointer-events:none;
  animation:pulse 8s ease-in-out infinite;
}
@keyframes pulse{ 0%,100%{opacity:0.7;} 50%{opacity:1;} }
@media (prefers-reduced-motion: reduce){ .hero::before{animation:none;} }

.hero-grid{
  position:relative;
  display:grid; grid-template-columns:1.05fr 0.95fr; gap:56px;
  align-items:start;
}
@media (max-width:900px){ .hero-grid{grid-template-columns:1fr; gap:44px;} }

.hero-name{
  font-size:clamp(42px, 6.4vw, 74px);
  font-weight:700;
  line-height:1.02;
  margin-bottom:16px;
}
.hero-role{
  font-family:var(--font-mono);
  color:var(--cyan);
  font-size:14px;
  letter-spacing:0.03em;
  margin-bottom:22px;
}
.hero-sub{
  font-size:18px;
  color:var(--text-muted);
  max-width:46ch;
  margin-bottom:34px;
}
.hero-sub b{color:var(--text); font-weight:600;}
.hero-ctas{display:flex; gap:14px; flex-wrap:wrap; margin-bottom:40px;}
.btn{
  font-size:14.5px; font-weight:600;
  padding:12px 20px; border-radius:9px;
  text-decoration:none; display:inline-flex; align-items:center; gap:8px;
  transition:transform .15s ease, border-color .15s ease, background .15s ease;
  border:1px solid transparent;
}
.btn:hover{transform:translateY(-1px);}
.btn-primary{background:var(--violet); color:#0a0c12;}
.btn-primary:hover{background:#9f87ff;}
.btn-ghost{border-color:var(--border); color:var(--text); background:transparent;}
.btn-ghost:hover{border-color:var(--amber); color:var(--amber);}

.hero-meta{
  display:flex; gap:26px; flex-wrap:wrap;
  font-family:var(--font-mono); font-size:12.5px; color:var(--text-faint);
}
.hero-meta strong{color:var(--text-muted); font-weight:500;}

/* ---------- avatar badge ---------- */
.avatar-badge{
  position:relative; width:56px; height:56px; border-radius:50%;
  display:flex; align-items:center; justify-content:center;
  margin-bottom:22px;
  background:linear-gradient(135deg, rgba(139,111,255,0.20), rgba(94,234,212,0.10));
  border:1px solid var(--border);
}
.avatar-initials{font-family:var(--font-display); font-weight:700; font-size:16px; letter-spacing:0.02em;}
.avatar-orbit{
  position:absolute; inset:-7px; border-radius:50%;
  border:1px dashed var(--border-soft);
  animation:spin 7s linear infinite;
}
.avatar-orbit::after{
  content:""; position:absolute; top:-2px; left:50%;
  width:5px; height:5px; margin-left:-2.5px; border-radius:50%;
  background:var(--amber); box-shadow:0 0 6px var(--amber);
}
@keyframes spin{ to{ transform:rotate(360deg); } }
@media (prefers-reduced-motion: reduce){ .avatar-orbit{animation:none;} }

/* ---------- terminal (signature element) ---------- */
.terminal{
  background:var(--surface);
  border:1px solid var(--border);
  border-radius:var(--radius);
  overflow:hidden;
  box-shadow:0 30px 60px -30px rgba(0,0,0,0.6);
}
.terminal-bar{
  display:flex; align-items:center; justify-content:space-between;
  padding:12px 16px;
  border-bottom:1px solid var(--border-soft);
  background:var(--bg-raised);
}
.terminal-bar-title{
  font-family:var(--font-mono); font-size:11.5px; color:var(--text-faint);
  letter-spacing:0.08em; text-transform:uppercase;
  display:flex; align-items:center; gap:8px;
}
.terminal-bar-dots{display:flex; gap:6px;}
.terminal-bar-dots span{width:8px;height:8px;border-radius:50%;background:var(--border);}
.terminal-badge{
  font-family:var(--font-mono); font-size:10.5px; color:var(--cyan);
  border:1px solid rgba(94,234,212,0.3); background:rgba(94,234,212,0.06);
  padding:3px 8px; border-radius:20px;
}
.terminal-body{padding:20px;}
.terminal-prompt{
  font-family:var(--font-mono); font-size:13px; color:var(--text-faint);
  margin-bottom:12px;
}
.terminal-prompt span{color:var(--amber);}
.terminal-form{display:flex; gap:8px; margin-bottom:14px;}
.terminal-input{
  flex:1; background:var(--surface-2); border:1px solid var(--border);
  color:var(--text); font-family:var(--font-mono); font-size:13.5px;
  padding:11px 13px; border-radius:8px;
}
.terminal-input::placeholder{color:var(--text-faint);}
.terminal-input:focus{border-color:var(--violet);}
.terminal-submit{
  background:var(--violet); color:var(--bg); border:none;
  padding:0 16px; border-radius:8px; font-family:var(--font-mono); font-size:13px; font-weight:600;
}
.terminal-submit:hover{background:#9f87ff;}
.chips{display:flex; gap:8px; flex-wrap:wrap; margin-bottom:18px;}
.chip{
  font-family:var(--font-mono); font-size:12px; color:var(--text-muted);
  background:var(--surface-2); border:1px solid var(--border);
  padding:6px 11px; border-radius:20px;
  transition:border-color .15s ease, color .15s ease;
}
.chip:hover{border-color:var(--amber); color:var(--amber);}

.terminal-output{
  border-top:1px dashed var(--border);
  padding-top:16px;
  min-height:64px;
}
.output-empty{
  font-family:var(--font-mono); font-size:12.5px; color:var(--text-faint);
}
.output-status{
  font-family:var(--font-mono); font-size:12px; color:var(--cyan);
  margin-bottom:12px;
  display:flex; align-items:center; gap:8px;
}
.output-status .blink{width:6px;height:12px;background:var(--cyan); animation:blink 1s steps(2) infinite;}
@keyframes blink{ 50%{opacity:0;} }
@media (prefers-reduced-motion: reduce){ .output-status .blink{animation:none;} }

.chunk{
  border:1px solid var(--border-soft); background:var(--bg-raised);
  border-radius:9px; padding:11px 13px; margin-bottom:8px;
  animation:rise .35s ease both;
}
@keyframes rise{ from{opacity:0; transform:translateY(6px);} to{opacity:1; transform:translateY(0);} }
@media (prefers-reduced-motion: reduce){ .chunk{animation:none;} }
.chunk-head{
  display:flex; align-items:center; justify-content:space-between;
  margin-bottom:6px;
}
.chunk-source{
  font-family:var(--font-mono); font-size:11px; color:var(--amber);
  letter-spacing:0.03em;
}
.chunk-score{font-family:var(--font-mono); font-size:10.5px; color:var(--text-faint);}
.chunk-text{font-size:13.5px; color:var(--text-muted); line-height:1.55;}

.answer-block{
  margin-top:14px; padding-top:14px; border-top:1px solid var(--border-soft);
}
.answer-label{
  font-family:var(--font-mono); font-size:11px; color:var(--text-faint);
  text-transform:uppercase; letter-spacing:0.1em; margin-bottom:8px;
}
.answer-text{font-size:14.5px; color:var(--text); line-height:1.65;}

/* ---------- waveform divider ---------- */
.wave{padding:8px 0 0; opacity:0.55;}
.wave svg{width:100%; height:44px;}
.wave path{stroke-dasharray:6 5; animation:dash 6s linear infinite;}
@keyframes dash{ to{stroke-dashoffset:-220;} }
@media (prefers-reduced-motion: reduce){ .wave path{animation:none;} }

/* ---------- about ---------- */
.about-text{
  font-size:19px; color:var(--text-muted); max-width:72ch; line-height:1.7;
}
.about-text b{color:var(--text); font-weight:600;}

/* ---------- skills ---------- */
.skill-groups{display:flex; flex-direction:column; gap:12px;}
.skill-group{
  display:grid; grid-template-columns:180px 1fr; gap:22px; align-items:start;
  padding:20px 22px;
  background:var(--surface); border:1px solid var(--border-soft); border-radius:12px;
  transition:border-color .15s ease;
}
.skill-group:hover{border-color:var(--border);}
@media (max-width:640px){ .skill-group{grid-template-columns:1fr; gap:10px; padding:18px;} }
.skill-group-label{
  font-family:var(--font-mono); font-size:12px; color:var(--amber);
  text-transform:uppercase; letter-spacing:0.08em; padding-top:4px;
}
.skill-chips{display:flex; flex-wrap:wrap; gap:8px;}
.skill-chip{
  font-size:13px; color:var(--text-muted);
  background:var(--bg-raised); border:1px solid var(--border);
  padding:6px 12px; border-radius:7px;
}

/* ---------- projects ---------- */
.section-head{display:flex; align-items:flex-end; justify-content:space-between; gap:20px; margin-bottom:40px; flex-wrap:wrap;}
.section-title{font-size:clamp(26px,3.4vw,36px); font-weight:600;}

.project-grid{display:grid; grid-template-columns:repeat(3,1fr); gap:20px; margin-bottom:20px;}
@media (max-width:900px){ .project-grid{grid-template-columns:1fr;} }
.card{
  background:var(--surface); border:1px solid var(--border);
  border-radius:var(--radius); padding:24px;
  transition:border-color .2s ease, transform .2s ease;
}
.card:hover{border-color:var(--violet-dim); transform:translateY(-2px);}
.card-icon{
  width:40px; height:40px; border-radius:10px;
  background:var(--surface-2); border:1px solid var(--border);
  display:flex; align-items:center; justify-content:center;
  margin-bottom:16px;
}
.card-icon svg{width:20px; height:20px;}
.card-icon.violet{color:var(--violet);}
.card-icon.cyan{color:var(--cyan);}
.card-icon.amber{color:var(--amber);}
.card-title{font-family:var(--font-display); font-size:18px; font-weight:600; margin-bottom:6px;}
.card-stack{font-family:var(--font-mono); font-size:11.5px; color:var(--cyan); margin-bottom:16px;}
.card-row{display:flex; gap:10px; margin-bottom:10px;}
.card-row:last-child{margin-bottom:0;}
.card-tag{
  font-family:var(--font-mono); font-size:10px; color:var(--amber);
  text-transform:uppercase; letter-spacing:0.06em; padding-top:2px; flex-shrink:0; width:64px;
}
.card-desc{font-size:13.5px; color:var(--text-muted); line-height:1.55;}

.more-row{display:grid; grid-template-columns:repeat(3,1fr); gap:16px;}
@media (max-width:900px){ .more-row{grid-template-columns:1fr;} }
.more-card{
  background:var(--bg-raised); border:1px solid var(--border-soft);
  border-radius:11px; padding:18px;
}
.more-title{font-size:14.5px; font-weight:600; margin-bottom:4px;}
.more-icon{
  width:26px; height:26px; border-radius:7px;
  background:var(--surface); border:1px solid var(--border-soft);
  display:flex; align-items:center; justify-content:center;
  color:var(--text-faint); margin-bottom:12px;
}
.more-icon svg{width:14px; height:14px;}
.more-stack{font-family:var(--font-mono); font-size:10.5px; color:var(--text-faint); margin-bottom:8px;}
.more-desc{font-size:12.5px; color:var(--text-muted); line-height:1.5;}

/* ---------- content creation ---------- */
.stat-row{display:grid; grid-template-columns:repeat(4,1fr); gap:18px; margin-bottom:40px;}
@media (max-width:900px){ .stat-row{grid-template-columns:repeat(2,1fr);} }
@media (max-width:520px){ .stat-row{grid-template-columns:1fr;} }
.stat{
  border:1px solid var(--border); border-radius:var(--radius);
  padding:22px 20px; background:var(--surface);
}
.stat-num{font-family:var(--font-display); font-size:30px; font-weight:700; color:var(--amber);}
.stat-label{font-size:12.5px; color:var(--text-muted); margin-top:6px; line-height:1.4;}
.creation-note{font-size:15.5px; color:var(--text-muted); max-width:70ch; line-height:1.7;}
.creation-note b{color:var(--text); font-weight:600;}

/* ---------- education / achievements ---------- */
.two-col{display:grid; grid-template-columns:1fr 1fr; gap:48px;}
@media (max-width:760px){ .two-col{grid-template-columns:1fr; gap:36px;} }
.col-label{
  font-family:var(--font-mono); font-size:12px; color:var(--text-faint);
  text-transform:uppercase; letter-spacing:0.08em; margin-bottom:18px;
}
.edu-item{padding:16px 0; border-top:1px solid var(--border-soft);}
.edu-item:last-child{border-bottom:1px solid var(--border-soft);}
.edu-item-top{display:flex; justify-content:space-between; gap:10px; margin-bottom:4px;}
.edu-name{font-size:15px; font-weight:600;}
.edu-score{font-family:var(--font-mono); font-size:13px; color:var(--cyan);}
.edu-sub{font-size:13px; color:var(--text-muted);}

.ach-item{display:flex; gap:14px; padding:16px 0; border-top:1px solid var(--border-soft);}
.ach-item:last-child{border-bottom:1px solid var(--border-soft);}
.ach-icon{width:8px; height:8px; border-radius:50%; background:var(--violet); margin-top:8px; flex-shrink:0; box-shadow:0 0 8px var(--violet);}
.ach-title{font-size:14.5px; font-weight:600; margin-bottom:3px;}
.ach-desc{font-size:13px; color:var(--text-muted); line-height:1.5;}

/* ---------- contact ---------- */
.contact-inner{
  border:1px solid var(--border); border-radius:20px;
  padding:56px 44px; background:linear-gradient(160deg, var(--surface), var(--bg-raised));
  text-align:center;
}
@media (max-width:600px){ .contact-inner{padding:40px 22px;} }
.contact-title{font-size:clamp(26px,4vw,40px); font-weight:600; margin-bottom:14px;}
.contact-sub{color:var(--text-muted); font-size:16px; max-width:50ch; margin:0 auto 30px;}
.contact-ctas{display:flex; gap:14px; justify-content:center; flex-wrap:wrap; margin-bottom:26px;}
.contact-meta{
  font-family:var(--font-mono); font-size:12.5px; color:var(--text-faint);
  display:flex; gap:20px; justify-content:center; flex-wrap:wrap;
}

footer{padding:36px 0 60px; text-align:center;}
footer p{font-family:var(--font-mono); font-size:11.5px; color:var(--text-faint);}

/* ---------- back to top ---------- */
.to-top{
  position:fixed; right:22px; bottom:22px; z-index:60;
  width:42px; height:42px; border-radius:50%;
  background:var(--surface-2); border:1px solid var(--border);
  color:var(--text-muted); display:flex; align-items:center; justify-content:center;
  opacity:0; visibility:hidden; transform:translateY(8px);
  transition:opacity .25s ease, transform .25s ease, border-color .15s ease, color .15s ease;
}
.to-top.show{opacity:1; visibility:visible; transform:translateY(0);}
.to-top:hover{border-color:var(--amber); color:var(--amber);}

/* ---------- reveal on scroll ---------- */
.reveal{opacity:0; transform:translateY(16px); transition:opacity .6s ease, transform .6s ease;}
.reveal.in{opacity:1; transform:translateY(0);}
@media (prefers-reduced-motion: reduce){ .reveal{opacity:1; transform:none; transition:none;} }

</style>
</head>
<body>

<nav class="nav">
  <div class="wrap">
    <div class="nav-logo"><span class="dot"></span>ABHIK MONDAL</div>
    <div class="nav-links">
      <a href="#about">About</a>
      <a href="#projects">Projects</a>
      <a href="#creation">Content</a>
      <a href="#education">Education</a>
      <a href="#contact">Contact</a>
    </div>
    <a class="nav-cta" href="mailto:abhik_24a12res20@iitp.ac.in">Say hi</a>
  </div>
</nav>

<header class="hero">
  <div class="wrap hero-grid">
    <div>
      <p class="hero-role">// applied ai/ml engineer — rag &amp; llm systems — android</p>
      <h1 class="hero-name">Abhik Mondal</h1>
      <p class="hero-sub">Final-year CS &amp; Data Analytics student at <b>IIT Patna</b>. I build retrieval-augmented systems and self-healing Android agents — then spend the rest of my time explaining how things work to <b>128,000+ people</b> on YouTube.</p>
      <div class="hero-ctas">
        <a class="btn btn-primary" href="#projects">See the work</a>
        <button class="btn btn-ghost" id="tryDemoBtn" type="button">Try the RAG demo ↓</button>
      </div>
      <div class="hero-meta">
        <span><strong>CGPA</strong> 9.29 / 10</span>
        <span><strong>Grad</strong> July 2027</span>
        <span><strong>Based in</strong> Delhi NCR</span>
        <span><strong>Available</strong> Immediately</span>
      </div>
    </div>

    <div class="terminal" id="terminal">
      <div class="terminal-bar">
        <div class="terminal-bar-title">
          <span class="terminal-bar-dots"><span></span><span></span><span></span></span>
          rag-qa.engine
        </div>
        <span class="terminal-badge">live demo</span>
      </div>
      <div class="terminal-body">
        <p class="terminal-prompt"><span>$</span> ask anything about abhik — this runs on the same retrieval pipeline as his Document Q&amp;A project</p>
        <form class="terminal-form" id="ragForm">
          <input class="terminal-input" id="ragInput" type="text" autocomplete="off" placeholder="e.g. what RAG projects has he built?">
          <button class="terminal-submit" type="submit">Run</button>
        </form>
        <div class="chips">
          <button class="chip" data-q="What RAG projects has he built?" type="button">RAG projects?</button>
          <button class="chip" data-q="Does he have Android experience?" type="button">Android experience?</button>
          <button class="chip" data-q="How big is his YouTube reach?" type="button">YouTube reach?</button>
          <button class="chip" data-q="What is his academic background?" type="button">Academic background?</button>
        </div>
        <div class="terminal-output" id="ragOutput">
          <p class="output-empty">// results will appear here — retrieved chunks first, then a synthesized answer</p>
        </div>
      </div>
    </div>
  </div>

  <div class="wave wrap"><svg viewBox="0 0 1000 44" preserveAspectRatio="none"><path d="M0,22 C 60,4 120,40 180,22 S 300,4 360,22 S 480,40 540,22 S 660,4 720,22 S 840,40 900,22 S 1000,4 1000,22" fill="none" stroke="#262c3f" stroke-width="1.5"/></svg></div>
</header>

<section id="about">
  <div class="wrap reveal">
    <p class="eyebrow">About</p>
    <p class="about-text">I'm a final-year <b>B.S. (Honours) in Computer Science &amp; Data Analytics</b> student at IIT Patna, graduating July 2027 with a 9.29/10 CGPA. Most of my time goes into shipping <b>production-style RAG pipelines</b> and an autonomous Android app — the rest goes into <b>SpacePlasmaPhysics.com</b> and two YouTube channels, where I've spent years turning dense science into video content people actually finish watching.</p>
  </div>
</section>

<section id="skills">
  <div class="wrap reveal">
    <p class="eyebrow">What I work with</p>
    <h2 class="section-title" style="margin-bottom:34px;">Stack &amp; tools</h2>

    <div class="skill-groups">
    <div class="skill-group">
      <div class="skill-group-label">AI/ML &amp; RAG</div>
      <div class="skill-chips">
        <span class="skill-chip">RAG Pipelines</span><span class="skill-chip">LangChain</span><span class="skill-chip">ChromaDB</span><span class="skill-chip">FAISS</span><span class="skill-chip">PaddleOCR</span><span class="skill-chip">Tesseract</span><span class="skill-chip">Prompt Engineering</span><span class="skill-chip">Embeddings</span><span class="skill-chip">Hugging Face</span><span class="skill-chip">LoRA / PEFT</span><span class="skill-chip">Ollama</span><span class="skill-chip">AI4Bharat / BHASHINI</span>
      </div>
    </div>
    <div class="skill-group">
      <div class="skill-group-label">Android &amp; Software</div>
      <div class="skill-chips">
        <span class="skill-chip">Kotlin</span><span class="skill-chip">Java</span><span class="skill-chip">Android SDK</span><span class="skill-chip">Multi-Agent Systems</span><span class="skill-chip">OOP</span><span class="skill-chip">Data Structures &amp; Algorithms</span><span class="skill-chip">DBMS</span><span class="skill-chip">Operating Systems</span>
      </div>
    </div>
    <div class="skill-group">
      <div class="skill-group-label">Data &amp; Web</div>
      <div class="skill-chips">
        <span class="skill-chip">Python</span><span class="skill-chip">SQL</span><span class="skill-chip">Pandas</span><span class="skill-chip">Streamlit</span><span class="skill-chip">HTML</span><span class="skill-chip">CSS</span><span class="skill-chip">JavaScript</span>
      </div>
    </div>
    <div class="skill-group">
      <div class="skill-group-label">Dashboards</div>
      <div class="skill-chips">
        <span class="skill-chip">Power BI</span><span class="skill-chip">Plotly</span><span class="skill-chip">Streamlit</span>
      </div>
    </div>
    <div class="skill-group">
      <div class="skill-group-label">Tools &amp; Platforms</div>
      <div class="skill-chips">
        <span class="skill-chip">Git</span><span class="skill-chip">GitHub</span><span class="skill-chip">Linux</span><span class="skill-chip">VS Code</span><span class="skill-chip">Local &amp; Server-Side LLM Inference</span>
      </div>
    </div>
    <div class="skill-group">
      <div class="skill-group-label">Content &amp; Comms</div>
      <div class="skill-chips">
        <span class="skill-chip">Journalism</span><span class="skill-chip">Scriptwriting</span><span class="skill-chip">Graphic Design</span><span class="skill-chip">Video Production</span><span class="skill-chip">Public Speaking &amp; Debate</span>
      </div>
    </div>
    </div>
  </div>
</section>

<section id="projects">
  <div class="wrap reveal">
    <div class="section-head">
      <div>
        <p class="eyebrow">Projects</p>
        <h2 class="section-title">Selected builds</h2>
      </div>
    </div>

    <div class="project-grid">
      <div class="card">
        <h3 class="card-title">RAG Document Q&amp;A Assistant</h3>
        <p class="card-stack">LangChain · ChromaDB · PaddleOCR · Streamlit</p>
        <div class="card-row"><span class="card-tag">Outcome</span><span class="card-desc">Cited, source-traceable answers over scanned PDF corpora.</span></div>
        <div class="card-row"><span class="card-tag">Method</span><span class="card-desc">500-char chunking with 50-char overlap, tuned against a 10-question eval set.</span></div>
        <div class="card-row"><span class="card-tag">Built</span><span class="card-desc">Streamlit chat UI with upload, history, and inline citations.</span></div>
      </div>
      <div class="card">
        <h3 class="card-title">Multi-Document RAG Chat</h3>
        <p class="card-stack">LangChain · ChromaDB · FAISS · Streamlit</p>
        <div class="card-row"><span class="card-tag">Outcome</span><span class="card-desc">Accurate retrieval across a growing, multi-document library.</span></div>
        <div class="card-row"><span class="card-tag">Method</span><span class="card-desc">Metadata-filtered retrieval, conversational memory, OCR fallback.</span></div>
        <div class="card-row"><span class="card-tag">Built</span><span class="card-desc">Benchmarked ChromaDB vs. FAISS and documented the tradeoffs.</span></div>
      </div>
      <div class="card">
        <h3 class="card-title">Gaya — Self-Healing Android App</h3>
        <p class="card-stack">Kotlin · Android SDK · LLM APIs · Multi-Agent</p>
        <div class="card-row"><span class="card-tag">Outcome</span><span class="card-desc">Agents detect and resolve in-app issues with minimal manual input.</span></div>
        <div class="card-row"><span class="card-tag">Method</span><span class="card-desc">LLM-powered agents collaboratively diagnose and apply code-level fixes.</span></div>
        <div class="card-row"><span class="card-tag">Built</span><span class="card-desc">Local on-device inference paired with a server-side backend.</span></div>
      </div>
    </div>

    <div class="more-row">
      <div class="more-card">
        <p class="more-title">AI-Powered Chatbot</p>
        <p class="more-stack">Python · NLP</p>
        <p class="more-desc">Rule-based intent-recognition pipeline that measurably cut irrelevant replies in manual QA testing.</p>
      </div>
      <div class="more-card">
        <p class="more-title">Student Management System</p>
        <p class="more-stack">Java · OOP</p>
        <p class="more-desc">Desktop app with validated CRUD across 100+ sample records and zero data loss.</p>
      </div>
      <div class="more-card">
        <p class="more-title">Personal Portfolio Website</p>
        <p class="more-stack">HTML · CSS · JavaScript</p>
        <p class="more-desc">Responsive single-page site with an interactive hero, project showcase, and skills directory.</p>
      </div>
    </div>
  </div>
</section>

<section id="creation">
  <div class="wrap reveal">
    <p class="eyebrow">Science communication</p>
    <h2 class="section-title" style="margin-bottom:34px;">Beyond the code</h2>

    <div class="stat-row">
      <div class="stat"><div class="stat-num">128,000+</div><div class="stat-label">Combined subscribers across two channels</div></div>
      <div class="stat"><div class="stat-num">94K / 34K</div><div class="stat-label">Split across the two channels</div></div>
      <div class="stat"><div class="stat-num">2×</div><div class="stat-label">YouTube Silver Creator Award</div></div>
      <div class="stat"><div class="stat-num">1</div><div class="stat-label">Independent site founded — SpacePlasmaPhysics.com</div></div>
    </div>

    <p class="creation-note">I own the full pipeline on both channels — <b>research synthesis, scriptwriting, graphic design, video production, publishing, and community management</b> — at sustained, professional scale. I've also represented IIT Patna as an <b>Inter-IIT Representative</b>, competing at IIT Kharagpur and IIT Hyderabad across Machine Learning, Generative AI, and Debate.</p>
  </div>
</section>

<section id="education">
  <div class="wrap reveal">
    <div class="two-col">
      <div>
        <p class="col-label">Education</p>
        <div class="edu-item">
          <div class="edu-item-top"><span class="edu-name">IIT Patna</span><span class="edu-score">9.29 CGPA</span></div>
          <p class="edu-sub">B.S. (Honours), CS &amp; Data Analytics · Final year, 5th semester · Expected July 2027</p>
        </div>
        <div class="edu-item">
          <div class="edu-item-top"><span class="edu-name">NIOS — Class XII</span><span class="edu-score">90%</span></div>
          <p class="edu-sub">National Institute of Open Schooling</p>
        </div>
        <div class="edu-item">
          <div class="edu-item-top"><span class="edu-name">Satitpur Kumar Mahim Chandra Institution — Class X</span><span class="edu-score">86%</span></div>
        </div>
      </div>
      <div>
        <p class="col-label">Achievements</p>
        <div class="ach-item">
          <span class="ach-icon"></span>
          <div><p class="ach-title">Inter-IIT Representative, IIT Patna</p><p class="ach-desc">Competed at IIT Kharagpur and IIT Hyderabad in Machine Learning, Generative AI, and Debate.</p></div>
        </div>
        <div class="ach-item">
          <span class="ach-icon"></span>
          <div><p class="ach-title">Government of India IPR Internship</p><p class="ach-desc">Direct exposure to IP law, innovation policy, and government project workflows.</p></div>
        </div>
        <div class="ach-item">
          <span class="ach-icon"></span>
          <div><p class="ach-title">2× YouTube Silver Creator Award</p><p class="ach-desc">Awarded at the 100,000-subscriber milestone on two separate channels.</p></div>
        </div>
      </div>
    </div>
  </div>
</section>

<section id="contact">
  <div class="wrap reveal">
    <div class="contact-inner">
      <h2 class="contact-title">Let's build something.</h2>
      <p class="contact-sub">Open to Applied AI/ML and Android internships — available immediately, based in Delhi NCR.</p>
      <div class="contact-ctas">
        <a class="btn btn-primary" href="mailto:abhik_24a12res20@iitp.ac.in">Email me</a>
        <a class="btn btn-ghost" href="./Abhik_Mondal_Resume.pdf" target="_blank" rel="noopener">Download résumé</a>
      </div>
      <div class="contact-meta">
        <span>abhik_24a12res20@iitp.ac.in</span>
        <span>+91 82396 65061</span>
        <span>Patna, Bihar / Delhi NCR</span>
      </div>
    </div>
  </div>
</section>

<footer>
  <p>Designed &amp; built by Abhik Mondal — retrieval, agents, and a bit of plasma physics.</p>
</footer>

<button class="to-top" id="toTop" type="button" aria-label="Back to top">↑</button>

<script>
(function(){
  // ---------- corpus for the RAG demo ----------
  var corpus = [
    { id:'c1', source:'Objective', text:"Abhik is a final-year B.S. (Honours) student in Computer Science & Data Analytics at IIT Patna, CGPA 9.29/10, graduating July 2027, based in Delhi NCR and available immediately." },
    { id:'c2', source:'Project — RAG Document Q&A', text:"He built a RAG pipeline with LangChain, ChromaDB and PaddleOCR for scanned PDFs, tuning 500-character chunks with 50-character overlap, delivering cited, source-traceable answers via a Streamlit chat interface." },
    { id:'c3', source:'Project — Multi-Doc RAG Chat', text:"He built a multi-document RAG system with LangChain, ChromaDB and FAISS supporting metadata-filtered retrieval and conversational memory, and benchmarked ChromaDB against FAISS for storage tradeoffs." },
    { id:'c4', source:'Project — Gaya (Android)', text:"He architected Gaya, a self-healing multi-agent Android app in Kotlin where LLM-powered agents diagnose issues and apply code-level fixes, combining local on-device inference with a server-side backend." },
    { id:'c5', source:'Content Creation', text:"He founded, wrote, produced and edited two YouTube science/technology channels reaching 128,000+ combined subscribers (94K and 34K), earning two YouTube Silver Creator Awards, and founded SpacePlasmaPhysics.com." },
    { id:'c6', source:'Competitions', text:"He was selected as an Inter-IIT Representative for IIT Patna, competing at IIT Kharagpur and IIT Hyderabad in Machine Learning, Generative AI, and Debate." },
    { id:'c7', source:'Skills', text:"His core stack spans Python, LangChain, ChromaDB, FAISS, OCR (PaddleOCR, Tesseract), Hugging Face, LoRA/PEFT fine-tuning, Ollama, Kotlin, Java, SQL, and AI4Bharat/BHASHINI for Indic NLP." },
    { id:'c8', source:'Achievements', text:"He completed a Government of India IPR internship, gaining exposure to IP law and innovation policy, alongside two YouTube Silver Creator Awards for 100,000-subscriber milestones." },
    { id:'c9', source:'Education', text:"He studies at IIT Patna with a 9.29 CGPA, having previously scored 90% in Class XII via NIOS and 86% in Class X at Satitpur Kumar Mahim Chandra Institution." },
    { id:'c10', source:'Other Projects', text:"He also built a rule-based AI chatbot for intent recognition, a Java Student Management System with validated CRUD across 100+ entries, and a responsive personal portfolio site." }
  ];
  var STOP = new Set(['the','a','an','is','are','was','were','has','have','had','of','in','on','at','for','to','and','or','with','about','what','whats',"what's",'does','do','his','he','him','any','how','big','much','it','this','that','background']);

  function tokenize(s){
    return s.toLowerCase().replace(/[^a-z0-9\s]/g,'').split(/\s+/).filter(function(w){return w.length>2 && !STOP.has(w);});
  }
  function retrieve(query){
    var q = tokenize(query);
    var scored = corpus.map(function(c){
      var t = c.text.toLowerCase();
      var score = 0;
      q.forEach(function(w){ if(t.indexOf(w) !== -1) score++; });
      return { c:c, score:score };
    });
    scored.sort(function(a,b){ return b.score - a.score; });
    var top = scored.filter(function(s){ return s.score > 0; }).slice(0,3);
    if(top.length === 0) top = [scored[0]];
    var maxScore = Math.max.apply(null, top.map(function(s){return s.score;}).concat([1]));
    return top.map(function(s){ return { source:s.c.source, text:s.c.text, pct: Math.max(30, Math.round((s.score/maxScore)*100)) }; });
  }
  function wait(ms){ return new Promise(function(res){ setTimeout(res, ms); }); }

  function escapeHtml(str){
    var d = document.createElement('div');
    d.textContent = str;
    return d.innerHTML;
  }

  async function runQuery(query){
    var out = document.getElementById('ragOutput');
    out.innerHTML = '<div class="output-status"><span class="blink"></span> retrieving relevant context…</div>';
    await wait(500);

    var chunks = retrieve(query);
    var html = '<div class="output-status" style="color:var(--amber);">✓ retrieved ' + chunks.length + ' chunk' + (chunks.length>1?'s':'') + '</div>';
    chunks.forEach(function(ch){
      html += '<div class="chunk"><div class="chunk-head"><span class="chunk-source">' + escapeHtml(ch.source) + '</span><span class="chunk-score">match ' + ch.pct + '%</span></div><div class="chunk-text">' + escapeHtml(ch.text) + '</div></div>';
    });
    out.innerHTML = html;
    await wait(450);

    var answer = chunks.map(function(ch){ return ch.text; }).join(' ');
    var sources = chunks.map(function(ch){ return ch.source; }).join(' · ');
    out.innerHTML += '<div class="answer-block"><div class="answer-label">Synthesized answer</div><div class="answer-text">' + escapeHtml(answer) + '</div><div class="chunk-score" style="margin-top:10px;">Sources: ' + escapeHtml(sources) + '</div></div>';
  }

  var form = document.getElementById('ragForm');
  var input = document.getElementById('ragInput');
  form.addEventListener('submit', function(e){
    e.preventDefault();
    var q = input.value.trim();
    if(!q) return;
    runQuery(q);
  });
  document.querySelectorAll('.chip').forEach(function(chip){
    chip.addEventListener('click', function(){
      var q = chip.getAttribute('data-q');
      input.value = q;
      runQuery(q);
    });
  });
  document.getElementById('tryDemoBtn').addEventListener('click', function(){
    document.getElementById('terminal').scrollIntoView({behavior:'smooth', block:'center'});
    input.focus();
  });

  // ---------- reveal on scroll ----------
  if('IntersectionObserver' in window){
    var io = new IntersectionObserver(function(entries){
      entries.forEach(function(entry){
        if(entry.isIntersecting){ entry.target.classList.add('in'); io.unobserve(entry.target); }
      });
    }, { threshold:0.12 });
    document.querySelectorAll('.reveal').forEach(function(el){ io.observe(el); });
  } else {
    document.querySelectorAll('.reveal').forEach(function(el){ el.classList.add('in'); });
  }

  // ---------- scrollspy: highlight the nav link for the section in view ----------
  var navLinks = Array.prototype.slice.call(document.querySelectorAll('.nav-links a'));
  var navMap = {};
  navLinks.forEach(function(a){ navMap[a.getAttribute('href').slice(1)] = a; });
  var spySections = Object.keys(navMap).map(function(id){ return document.getElementById(id); }).filter(Boolean);
  if('IntersectionObserver' in window && spySections.length){
    var spy = new IntersectionObserver(function(entries){
      entries.forEach(function(entry){
        var link = navMap[entry.target.id];
        if(!link) return;
        if(entry.isIntersecting){
          navLinks.forEach(function(a){ a.classList.remove('active'); });
          link.classList.add('active');
        }
      });
    }, { rootMargin:'-45% 0px -50% 0px', threshold:0 });
    spySections.forEach(function(el){ spy.observe(el); });
  }

  // ---------- back to top ----------
  var toTop = document.getElementById('toTop');
  window.addEventListener('scroll', function(){
    toTop.classList.toggle('show', window.scrollY > 700);
  }, { passive:true });
  toTop.addEventListener('click', function(){
    window.scrollTo({ top:0, behavior:'smooth' });
  });
})();
</script>

</body>
</html>
