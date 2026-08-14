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
.btn:active{transform:translateY(0) scale(.96);}
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

/* ---------- journey timeline (storytelling) ---------- */
.timeline{position:relative; margin-top:10px;}
.timeline::before{
  content:""; position:absolute; left:23px; top:6px; bottom:6px; width:1.5px;
  background:linear-gradient(180deg, var(--violet), var(--cyan) 45%, var(--amber) 100%);
  opacity:0.35;
}
@media (max-width:720px){ .timeline::before{left:15px;} }
.tl-item{
  position:relative; display:grid; grid-template-columns:48px 1fr; gap:22px;
  padding-bottom:34px;
  opacity:0; transform:translateY(16px);
  transition:opacity .55s ease, transform .55s ease;
}
.reveal.in .tl-item{opacity:1; transform:translateY(0);}
.reveal.in .tl-item:nth-child(1){transition-delay:.03s;}
.reveal.in .tl-item:nth-child(2){transition-delay:.10s;}
.reveal.in .tl-item:nth-child(3){transition-delay:.17s;}
.reveal.in .tl-item:nth-child(4){transition-delay:.24s;}
.reveal.in .tl-item:nth-child(5){transition-delay:.31s;}
.reveal.in .tl-item:nth-child(6){transition-delay:.38s;}
.reveal.in .tl-item:nth-child(7){transition-delay:.45s;}
.reveal.in .tl-item:nth-child(8){transition-delay:.52s;}
@media (prefers-reduced-motion: reduce){ .tl-item{transition:none; opacity:1; transform:none;} }
.tl-item:last-child{padding-bottom:0;}
@media (max-width:720px){ .tl-item{grid-template-columns:32px 1fr; gap:14px;} }
.tl-node{
  position:relative; width:48px; height:48px; border-radius:50%;
  background:var(--surface); border:1px solid var(--border);
  display:flex; align-items:center; justify-content:center;
  font-family:var(--font-mono); font-size:11px; color:var(--text-faint);
  z-index:1;
}
@media (max-width:720px){ .tl-node{width:32px; height:32px; font-size:9px;} }
.tl-node svg{width:20px; height:20px; stroke:currentColor;}
@media (max-width:720px){ .tl-node svg{width:15px; height:15px;} }
.tl-item.violet .tl-node{color:var(--violet); border-color:var(--violet-dim);}
.tl-item.cyan .tl-node{color:var(--cyan); border-color:rgba(94,234,212,0.4);}
.tl-item.amber .tl-node{color:var(--amber); border-color:rgba(255,180,84,0.4);}
.tl-card{
  background:var(--surface); border:1px solid var(--border-soft); border-radius:12px;
  padding:18px 20px; transition:border-color .15s ease, transform .15s ease;
}
.tl-card:hover{border-color:var(--border); transform:translateX(3px);}
.tl-tag{
  font-family:var(--font-mono); font-size:10.5px; text-transform:uppercase; letter-spacing:0.08em;
  color:var(--text-faint); margin-bottom:5px; display:block;
}
.tl-title{font-family:var(--font-display); font-size:16.5px; font-weight:600; margin-bottom:6px;}
.tl-desc{font-size:13.5px; color:var(--text-muted); line-height:1.55;}
.tl-now .tl-card{border-color:var(--amber); box-shadow:0 0 0 1px rgba(255,180,84,0.15);}

/* ---------- radar / bar chart (skills + academics as visuals) ---------- */
.chart-panel{
  background:var(--surface); border:1px solid var(--border); border-radius:var(--radius);
  padding:26px; margin-bottom:34px;
}
.chart-panel-head{display:flex; align-items:center; justify-content:space-between; gap:14px; margin-bottom:6px; flex-wrap:wrap;}
.chart-panel-title{font-family:var(--font-mono); font-size:12px; color:var(--text-faint); text-transform:uppercase; letter-spacing:0.08em;}
.chart-grid-2{display:grid; grid-template-columns:1fr 1fr; gap:20px;}
@media (max-width:840px){ .chart-grid-2{grid-template-columns:1fr;} }
.radar-wrap{display:flex; justify-content:center; padding:8px 0;}
.radar-wrap svg{width:100%; max-width:340px; height:auto;}
.radar-poly{
  fill:rgba(139,111,255,0.16); stroke:var(--violet); stroke-width:1.6;
  stroke-linejoin:round;
  transform-origin:center; transform-box:fill-box;
  transform:scale(0); transition:transform 1s cubic-bezier(.2,.8,.25,1);
}
.chart-panel.in .radar-poly{transform:scale(1);}
.radar-axis{stroke:var(--border); stroke-width:1;}
.radar-ring{fill:none; stroke:var(--border-soft); stroke-width:1;}
.radar-label{font-family:var(--font-mono); font-size:9.5px; fill:var(--text-faint);}
.radar-dot{fill:var(--violet);}

.bar-chart{display:flex; flex-direction:column; gap:14px; padding:6px 4px;}
.bar-row{display:grid; grid-template-columns:96px 1fr 48px; align-items:center; gap:10px;}
.bar-row-label{font-family:var(--font-mono); font-size:11.5px; color:var(--text-muted);}
.bar-track{height:10px; border-radius:6px; background:var(--surface-2); border:1px solid var(--border-soft); overflow:hidden;}
.bar-fill{height:100%; border-radius:6px; width:0%; transition:width 1.1s cubic-bezier(.2,.8,.25,1); background:linear-gradient(90deg, var(--cyan), var(--violet));}
.chart-panel.in .bar-fill{width:var(--w);}
.bar-row-val{font-family:var(--font-mono); font-size:11.5px; color:var(--text); text-align:right;}
.chart-note{font-size:12px; color:var(--text-faint); margin-top:14px; line-height:1.5;}

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
.reveal{
  opacity:0; transform:perspective(1000px) translateY(22px) rotateX(7deg);
  transform-origin:50% 100%;
  transition:opacity .7s ease, transform .7s cubic-bezier(.2,.7,.3,1);
}
.reveal.in{opacity:1; transform:perspective(1000px) translateY(0) rotateX(0deg);}
@media (prefers-reduced-motion: reduce){ .reveal{opacity:1; transform:none; transition:none;} }

/* ---------- starfield backdrop ---------- */
#starfield{
  position:fixed; inset:0; width:100%; height:100%;
  z-index:-1; pointer-events:none; background:var(--bg);
}

/* ---------- project / more card visuals ---------- */
.card-icon svg{stroke:currentColor;}
.more-icon svg{stroke:currentColor;}

/* ---------- 3D tilt (site-wide) ---------- */
.tilt{
  transform-style:preserve-3d; will-change:transform;
  transition:transform .15s ease-out, border-color .15s ease;
  position:relative;
}
.tilt::before{
  content:""; position:absolute; inset:0; border-radius:inherit;
  background:radial-gradient(circle at var(--mx,50%) var(--my,50%), rgba(255,255,255,0.07), transparent 55%);
  opacity:0; transition:opacity .25s ease; pointer-events:none;
}
.tilt:hover::before{opacity:1;}

/* ---------- reach panel (science communication) ---------- */
.reach-panel{
  background:var(--surface); border:1px solid var(--border); border-radius:var(--radius);
  overflow:hidden; box-shadow:0 34px 80px -38px rgba(0,0,0,0.7);
  margin-bottom:34px;
}
.reach-stage{
  position:relative; width:100%;
  padding:26px 24px 22px;
  background:radial-gradient(ellipse at 18% 0%, rgba(94,234,212,0.07), transparent 60%), #05070c;
}
.reach-bars{display:flex; align-items:flex-end; gap:22px; height:150px; padding:0 4px 14px;}
@media (max-width:520px){ .reach-bars{height:120px; gap:14px;} }
.reach-bar-col{flex:1; display:flex; flex-direction:column; align-items:center; justify-content:flex-end; height:100%; gap:8px;}
.reach-bar{
  width:100%; max-width:64px; border-radius:6px 6px 3px 3px;
  background:linear-gradient(180deg, var(--cyan), rgba(94,234,212,0.25));
  transform:scaleY(0); transform-origin:bottom; transition:transform 1.1s cubic-bezier(.2,.8,.25,1);
  box-shadow:0 0 18px -4px rgba(94,234,212,0.5);
}
.reach-bar.amber{background:linear-gradient(180deg, var(--amber), rgba(255,180,84,0.25)); box-shadow:0 0 18px -4px rgba(255,180,84,0.5);}
.reach-bar.violet{background:linear-gradient(180deg, var(--violet), rgba(139,111,255,0.25)); box-shadow:0 0 18px -4px rgba(139,111,255,0.5);}
.reach-panel.in .reach-bar{transform:scaleY(1);}
.reach-bar-num{font-family:var(--font-mono); font-size:12.5px; color:var(--text); font-weight:600;}
.reach-bar-label{font-family:var(--font-mono); font-size:10.5px; color:var(--text-faint); text-align:center;}
.reach-hud{
  display:flex; flex-wrap:wrap; gap:16px;
  font-family:var(--font-mono); font-size:10.5px; color:var(--text-faint);
  border-top:1px dashed var(--border-soft); padding-top:14px; margin-top:4px;
}
.reach-hud b{color:var(--cyan); font-weight:500;}
.reach-hud .pulse-dot{width:5px; height:5px; border-radius:50%; background:var(--amber); box-shadow:0 0 6px var(--amber); display:inline-block; margin-right:6px; animation:pulseDot 1.8s ease-in-out infinite;}
@keyframes pulseDot{ 0%,100%{opacity:1; transform:scale(1);} 50%{opacity:0.4; transform:scale(0.7);} }
@media (prefers-reduced-motion: reduce){ .reach-hud .pulse-dot{animation:none;} .reach-panel.in .reach-bar{transition:none;} }

/* ---------- command palette (signature feature) ---------- */
.cmdk-launcher{
  position:fixed; left:22px; bottom:22px; z-index:60;
  display:flex; align-items:center; gap:9px;
  background:var(--surface-2); border:1px solid var(--border);
  color:var(--text-muted); font-family:var(--font-mono); font-size:12.5px;
  padding:10px 14px; border-radius:24px; cursor:pointer;
  box-shadow:0 14px 30px -14px rgba(0,0,0,0.6);
  transition:border-color .15s ease, color .15s ease;
}
.cmdk-launcher:hover{border-color:var(--violet); color:var(--text);}
.cmdk-launcher kbd{
  font-family:var(--font-mono); font-size:10.5px; color:var(--text-faint);
  background:var(--bg-raised); border:1px solid var(--border); border-radius:5px;
  padding:1.5px 6px;
}
@media (max-width:640px){ .cmdk-launcher span.hide-mobile{display:none;} }

.cmdk-overlay{
  position:fixed; inset:0; z-index:100;
  background:rgba(5,6,10,0.72); backdrop-filter:blur(3px);
  display:flex; align-items:flex-start; justify-content:center;
  padding:11vh 20px 20px;
  opacity:0; visibility:hidden; transition:opacity .18s ease;
}
.cmdk-overlay.open{opacity:1; visibility:visible;}
.cmdk-box{
  width:100%; max-width:620px;
  background:var(--surface); border:1px solid var(--border); border-radius:var(--radius);
  box-shadow:0 50px 100px -30px rgba(0,0,0,0.8);
  transform:translateY(-10px); transition:transform .18s ease;
  overflow:hidden;
}
.cmdk-overlay.open .cmdk-box{transform:translateY(0);}
.cmdk-input-row{
  display:flex; align-items:center; gap:10px;
  padding:15px 18px; border-bottom:1px solid var(--border-soft);
}
.cmdk-prompt{font-family:var(--font-mono); color:var(--amber); font-size:15px;}
.cmdk-input{
  flex:1; background:transparent; border:none; outline:none;
  color:var(--text); font-family:var(--font-mono); font-size:14.5px;
}
.cmdk-input::placeholder{color:var(--text-faint);}
.cmdk-esc{
  font-family:var(--font-mono); font-size:10.5px; color:var(--text-faint);
  border:1px solid var(--border); border-radius:5px; padding:2px 6px;
}
.cmdk-body{max-height:52vh; overflow-y:auto; padding:14px 18px 18px;}
.cmdk-line{font-family:var(--font-mono); font-size:13px; line-height:1.75; color:var(--text-muted); white-space:pre-wrap;}
.cmdk-line b{color:var(--text); font-weight:600;}
.cmdk-line.cmd{color:var(--cyan);}
.cmdk-line.cmd::before{content:"❯ "; color:var(--amber);}
.cmdk-line a{color:var(--violet); text-decoration:underline;}
.cmdk-hint-row{display:flex; flex-wrap:wrap; gap:6px; margin-top:6px;}
.cmdk-hint{
  font-family:var(--font-mono); font-size:11px; color:var(--text-muted);
  background:var(--surface-2); border:1px solid var(--border); border-radius:16px;
  padding:4px 10px;
}
.cmdk-hint:hover{border-color:var(--amber); color:var(--amber); cursor:pointer;}

</style>
</head>
<body>

<canvas id="starfield" aria-hidden="true"></canvas>

<nav class="nav">
  <div class="wrap">
    <div class="nav-logo"><span class="dot"></span>ABHIK MONDAL</div>
    <div class="nav-links">
      <a href="#about">About</a>
      <a href="#journey">Journey</a>
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

    <div class="terminal tilt" id="terminal">
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

<section id="journey">
  <div class="wrap reveal">
    <p class="eyebrow">How I got here</p>
    <h2 class="section-title" style="margin-bottom:34px;">The journey</h2>

    <div class="timeline">
      <div class="tl-item cyan">
        <div class="tl-node"><svg viewBox="0 0 24 24" fill="none" stroke-width="1.6" stroke-linecap="round" stroke-linejoin="round"><path d="M3 9.5 12 5l9 4.5-9 4.5-9-4.5Z"/><path d="M7 11.5V16c0 1.1 2.2 2.5 5 2.5s5-1.4 5-2.5v-4.5"/></svg></div>
        <div class="tl-card">
          <span class="tl-tag">Where it started</span>
          <p class="tl-title">Class X — 86%</p>
          <p class="tl-desc">Satitpur Kumar Mahim Chandra Institution. Nothing remarkable yet — just the baseline everything else got built on.</p>
        </div>
      </div>
      <div class="tl-item cyan">
        <div class="tl-node"><svg viewBox="0 0 24 24" fill="none" stroke-width="1.6" stroke-linecap="round" stroke-linejoin="round"><path d="M4 6h16M4 12h16M4 18h10"/></svg></div>
        <div class="tl-card">
          <span class="tl-tag">Class XII · NIOS</span>
          <p class="tl-title">Took the unconventional path — 90%</p>
          <p class="tl-desc">Studied through the National Institute of Open Schooling instead of a traditional classroom track, and still pushed the score up.</p>
        </div>
      </div>
      <div class="tl-item violet">
        <div class="tl-node"><svg viewBox="0 0 24 24" fill="none" stroke-width="1.6" stroke-linecap="round" stroke-linejoin="round"><path d="M12 3 3 7l9 4 9-4-9-4Z"/><path d="M3 7v10l9 4 9-4V7"/><path d="M12 11v10"/></svg></div>
        <div class="tl-card">
          <span class="tl-tag">IIT Patna</span>
          <p class="tl-title">Started B.S. (Honours), CS &amp; Data Analytics</p>
          <p class="tl-desc">Currently 9.29/10 CGPA, final year. This is where AI/ML, Android, and data analytics became the actual focus.</p>
        </div>
      </div>
      <div class="tl-item violet">
        <div class="tl-node"><svg viewBox="0 0 24 24" fill="none" stroke-width="1.6" stroke-linecap="round" stroke-linejoin="round"><path d="M6 3.5h8l4 4V20a.5.5 0 0 1-.5.5h-11A.5.5 0 0 1 6 20z"/><path d="M14 3.5V7.5h4"/><path d="M8.5 12h5"/><path d="M8.5 15h3.2"/></svg></div>
        <div class="tl-card">
          <span class="tl-tag">First RAG builds</span>
          <p class="tl-title">Shipped two production-style RAG pipelines</p>
          <p class="tl-desc">Document Q&amp;A over scanned PDFs with PaddleOCR + LangChain + ChromaDB, then a multi-document system benchmarking ChromaDB against FAISS.</p>
        </div>
      </div>
      <div class="tl-item violet">
        <div class="tl-node"><svg viewBox="0 0 24 24" fill="none" stroke-width="1.6" stroke-linecap="round" stroke-linejoin="round"><rect x="7.5" y="3" width="9" height="18" rx="2"/><circle cx="12" cy="10.4" r="2.3"/></svg></div>
        <div class="tl-card">
          <span class="tl-tag">Gaya</span>
          <p class="tl-title">Built a self-healing Android agent</p>
          <p class="tl-desc">LLM-powered agents that diagnose in-app issues and apply code-level fixes, balancing on-device inference with a server-side backend.</p>
        </div>
      </div>
      <div class="tl-item amber">
        <div class="tl-node"><svg viewBox="0 0 24 24" fill="none" stroke-width="1.6" stroke-linecap="round" stroke-linejoin="round"><path d="M12 2 4 7v6c0 5 3.5 7.5 8 9 4.5-1.5 8-4 8-9V7l-8-5Z"/></svg></div>
        <div class="tl-card">
          <span class="tl-tag">Inter-IIT Representative</span>
          <p class="tl-title">Competed at IIT Kharagpur and IIT Hyderabad</p>
          <p class="tl-desc">Selected to represent IIT Patna across Machine Learning, Generative AI, and Debate — three very different kinds of pressure.</p>
        </div>
      </div>
      <div class="tl-item amber">
        <div class="tl-node"><svg viewBox="0 0 24 24" fill="none" stroke-width="1.6" stroke-linecap="round" stroke-linejoin="round"><path d="M15 10 21 6v12l-6-4"/><rect x="3" y="6" width="12" height="12" rx="2"/></svg></div>
        <div class="tl-card">
          <span class="tl-tag">Parallel track</span>
          <p class="tl-title">Grew two YouTube channels to 128,000+ combined</p>
          <p class="tl-desc">Owned research, scriptwriting, design, and production end to end — earning two Silver Creator Awards — while founding SpacePlasmaPhysics.com.</p>
        </div>
      </div>
      <div class="tl-item amber tl-now">
        <div class="tl-node"><svg viewBox="0 0 24 24" fill="none" stroke-width="1.6" stroke-linecap="round" stroke-linejoin="round"><circle cx="12" cy="12" r="9"/><path d="M12 7v5l3.2 2"/></svg></div>
        <div class="tl-card">
          <span class="tl-tag">Right now</span>
          <p class="tl-title">Final year — open to Applied AI/ML &amp; Android internships</p>
          <p class="tl-desc">Based in Delhi NCR, available immediately. Looking for a team building real retrieval or agent systems at production scale.</p>
        </div>
      </div>
    </div>
  </div>
</section>

<section id="skills">
  <div class="wrap reveal">
    <p class="eyebrow">What I work with</p>
    <h2 class="section-title" style="margin-bottom:34px;">Stack &amp; tools</h2>

    <div class="chart-panel" id="skillsChartPanel">
      <div class="chart-panel-head">
        <span class="chart-panel-title">Skill area breadth</span>
        <span class="terminal-badge">by tool count</span>
      </div>
      <div class="chart-grid-2">
        <div class="radar-wrap">
          <svg viewBox="0 0 300 300" id="radarSvg" aria-label="Radar chart of skill area breadth">
            <!-- rings drawn by JS -->
          </svg>
        </div>
        <div style="display:flex; flex-direction:column; justify-content:center;">
          <p class="chart-note" style="margin-top:0;">Each axis reflects the breadth of tools/technologies I bring to that area, drawn from my résumé — a quick map of where my stack is widest, not a precision skill rating.</p>
          <div class="bar-chart" style="margin-top:6px;">
            <div class="bar-row"><span class="bar-row-label">AI/ML &amp; RAG</span><div class="bar-track"><div class="bar-fill" style="--w:100%"></div></div><span class="bar-row-val">12</span></div>
            <div class="bar-row"><span class="bar-row-label">Android &amp; SW</span><div class="bar-track"><div class="bar-fill" style="--w:75%"></div></div><span class="bar-row-val">9</span></div>
            <div class="bar-row"><span class="bar-row-label">Data &amp; Web</span><div class="bar-track"><div class="bar-fill" style="--w:67%"></div></div><span class="bar-row-val">8</span></div>
            <div class="bar-row"><span class="bar-row-label">Tools &amp; Platforms</span><div class="bar-track"><div class="bar-fill" style="--w:58%"></div></div><span class="bar-row-val">7</span></div>
            <div class="bar-row"><span class="bar-row-label">Content &amp; Comms</span><div class="bar-track"><div class="bar-fill" style="--w:50%"></div></div><span class="bar-row-val">6</span></div>
            <div class="bar-row"><span class="bar-row-label">Dashboards</span><div class="bar-track"><div class="bar-fill" style="--w:42%"></div></div><span class="bar-row-val">5</span></div>
          </div>
        </div>
      </div>
    </div>

    <div class="skill-groups">
    <div class="skill-group tilt">
      <div class="skill-group-label">AI/ML &amp; RAG</div>
      <div class="skill-chips">
        <span class="skill-chip">RAG Pipelines</span><span class="skill-chip">LangChain</span><span class="skill-chip">ChromaDB</span><span class="skill-chip">FAISS</span><span class="skill-chip">PaddleOCR</span><span class="skill-chip">Tesseract</span><span class="skill-chip">Prompt Engineering</span><span class="skill-chip">Embeddings</span><span class="skill-chip">Hugging Face</span><span class="skill-chip">LoRA / PEFT</span><span class="skill-chip">Ollama</span><span class="skill-chip">AI4Bharat / BHASHINI</span>
      </div>
    </div>
    <div class="skill-group tilt">
      <div class="skill-group-label">Android &amp; Software</div>
      <div class="skill-chips">
        <span class="skill-chip">Kotlin</span><span class="skill-chip">Java</span><span class="skill-chip">Android SDK</span><span class="skill-chip">Multi-Agent Systems</span><span class="skill-chip">OOP</span><span class="skill-chip">Data Structures &amp; Algorithms</span><span class="skill-chip">DBMS</span><span class="skill-chip">Operating Systems</span>
      </div>
    </div>
    <div class="skill-group tilt">
      <div class="skill-group-label">Data &amp; Web</div>
      <div class="skill-chips">
        <span class="skill-chip">Python</span><span class="skill-chip">SQL</span><span class="skill-chip">Pandas</span><span class="skill-chip">Streamlit</span><span class="skill-chip">HTML</span><span class="skill-chip">CSS</span><span class="skill-chip">JavaScript</span>
      </div>
    </div>
    <div class="skill-group tilt">
      <div class="skill-group-label">Dashboards</div>
      <div class="skill-chips">
        <span class="skill-chip">Power BI</span><span class="skill-chip">Plotly</span><span class="skill-chip">Streamlit</span>
      </div>
    </div>
    <div class="skill-group tilt">
      <div class="skill-group-label">Tools &amp; Platforms</div>
      <div class="skill-chips">
        <span class="skill-chip">Git</span><span class="skill-chip">GitHub</span><span class="skill-chip">Linux</span><span class="skill-chip">VS Code</span><span class="skill-chip">Local &amp; Server-Side LLM Inference</span>
      </div>
    </div>
    <div class="skill-group tilt">
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
      <div class="card tilt">
        <div class="card-icon violet"><svg viewBox="0 0 24 24" fill="none" stroke-width="1.6" stroke-linecap="round" stroke-linejoin="round"><path d="M6 3.5h8l4 4V20a.5.5 0 0 1-.5.5h-11A.5.5 0 0 1 6 20z"/><path d="M14 3.5V7.5h4"/><path d="M8.5 12h5"/><path d="M8.5 15h3.2"/><circle cx="15.6" cy="16.6" r="2.3"/><path d="M17.4 18.4 19 20"/></svg></div>
        <h3 class="card-title">RAG Document Q&amp;A Assistant</h3>
        <p class="card-stack">LangChain · ChromaDB · PaddleOCR · Streamlit</p>
        <div class="card-row"><span class="card-tag">Outcome</span><span class="card-desc">Cited, source-traceable answers over scanned PDF corpora.</span></div>
        <div class="card-row"><span class="card-tag">Method</span><span class="card-desc">500-char chunking with 50-char overlap, tuned against a 10-question eval set.</span></div>
        <div class="card-row"><span class="card-tag">Built</span><span class="card-desc">Streamlit chat UI with upload, history, and inline citations.</span></div>
      </div>
      <div class="card tilt">
        <div class="card-icon cyan"><svg viewBox="0 0 24 24" fill="none" stroke-width="1.6" stroke-linecap="round" stroke-linejoin="round"><path d="M5.5 8.5h9a1 1 0 0 1 1 1v7a1 1 0 0 1-1 1h-9a1 1 0 0 1-1-1v-7a1 1 0 0 1 1-1z"/><path d="M8 5.2h9a1 1 0 0 1 1 1v7"/><path d="M10.5 4h6.7a1 1 0 0 1 1 1v6.4" opacity="0.55"/><circle cx="10" cy="12.3" r="0.9" fill="currentColor" stroke="none"/><circle cx="13" cy="12.3" r="0.9" fill="currentColor" stroke="none"/><circle cx="16" cy="12.3" r="0.9" fill="currentColor" stroke="none"/></svg></div>
        <h3 class="card-title">Multi-Document RAG Chat</h3>
        <p class="card-stack">LangChain · ChromaDB · FAISS · Streamlit</p>
        <div class="card-row"><span class="card-tag">Outcome</span><span class="card-desc">Accurate retrieval across a growing, multi-document library.</span></div>
        <div class="card-row"><span class="card-tag">Method</span><span class="card-desc">Metadata-filtered retrieval, conversational memory, OCR fallback.</span></div>
        <div class="card-row"><span class="card-tag">Built</span><span class="card-desc">Benchmarked ChromaDB vs. FAISS and documented the tradeoffs.</span></div>
      </div>
      <div class="card tilt">
        <div class="card-icon amber"><svg viewBox="0 0 24 24" fill="none" stroke-width="1.6" stroke-linecap="round" stroke-linejoin="round"><rect x="7.5" y="3" width="9" height="18" rx="2"/><path d="M10.2 18.2h3.6"/><circle cx="12" cy="10.4" r="2.3"/><path d="M12 6.6v1.2M12 11.8v1.2M15.2 10.4h-1.2M9 10.4H7.8M14.4 8.2l-.85.85M10.45 11.35l-.85.85M14.4 12.6l-.85-.85M10.45 9.45l-.85-.85"/></svg></div>
        <h3 class="card-title">Gaya — Self-Healing Android App</h3>
        <p class="card-stack">Kotlin · Android SDK · LLM APIs · Multi-Agent</p>
        <div class="card-row"><span class="card-tag">Outcome</span><span class="card-desc">Agents detect and resolve in-app issues with minimal manual input.</span></div>
        <div class="card-row"><span class="card-tag">Method</span><span class="card-desc">LLM-powered agents collaboratively diagnose and apply code-level fixes.</span></div>
        <div class="card-row"><span class="card-tag">Built</span><span class="card-desc">Local on-device inference paired with a server-side backend.</span></div>
      </div>
    </div>

    <div class="more-row">
      <div class="more-card tilt">
        <div class="more-icon"><svg viewBox="0 0 24 24" fill="none" stroke-width="1.6" stroke-linecap="round" stroke-linejoin="round"><path d="M4.5 6.5h15a1 1 0 0 1 1 1v7a1 1 0 0 1-1 1H10l-4 3.2V15.5H4.5a1 1 0 0 1-1-1v-7a1 1 0 0 1 1-1z"/><circle cx="9" cy="11" r="0.9" fill="currentColor" stroke="none"/><circle cx="12" cy="11" r="0.9" fill="currentColor" stroke="none"/><circle cx="15" cy="11" r="0.9" fill="currentColor" stroke="none"/></svg></div>
        <p class="more-title">AI-Powered Chatbot</p>
        <p class="more-stack">Python · NLP</p>
        <p class="more-desc">Rule-based intent-recognition pipeline that measurably cut irrelevant replies in manual QA testing.</p>
      </div>
      <div class="more-card tilt">
        <div class="more-icon"><svg viewBox="0 0 24 24" fill="none" stroke-width="1.6" stroke-linecap="round" stroke-linejoin="round"><rect x="4" y="4.5" width="16" height="15" rx="1.5"/><path d="M4 9.8h16"/><path d="M9.6 9.8V19.5"/></svg></div>
        <p class="more-title">Student Management System</p>
        <p class="more-stack">Java · OOP</p>
        <p class="more-desc">Desktop app with validated CRUD across 100+ sample records and zero data loss.</p>
      </div>
      <div class="more-card tilt">
        <div class="more-icon"><svg viewBox="0 0 24 24" fill="none" stroke-width="1.6" stroke-linecap="round" stroke-linejoin="round"><rect x="3.5" y="5" width="17" height="14" rx="1.5"/><path d="M3.5 8.5h17"/><circle cx="6" cy="6.75" r="0.6" fill="currentColor" stroke="none"/><circle cx="8" cy="6.75" r="0.6" fill="currentColor" stroke="none"/></svg></div>
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

    <div class="reach-panel" id="reachPanel">
      <div class="terminal-bar">
        <div class="terminal-bar-title">
          <span class="terminal-bar-dots"><span></span><span></span><span></span></span>
          audience.stats() — channel breakdown
        </div>
        <span class="terminal-badge">live</span>
      </div>
      <div class="reach-stage">
        <div class="reach-bars">
          <div class="reach-bar-col">
            <span class="reach-bar-num">94K</span>
            <div class="reach-bar" style="height:88%;"></div>
            <span class="reach-bar-label">Channel A</span>
          </div>
          <div class="reach-bar-col">
            <span class="reach-bar-num">34K</span>
            <div class="reach-bar amber" style="height:33%;"></div>
            <span class="reach-bar-label">Channel B</span>
          </div>
          <div class="reach-bar-col">
            <span class="reach-bar-num">2×</span>
            <div class="reach-bar violet" style="height:20%;"></div>
            <span class="reach-bar-label">Silver Awards</span>
          </div>
          <div class="reach-bar-col">
            <span class="reach-bar-num">128K+</span>
            <div class="reach-bar" style="height:100%;"></div>
            <span class="reach-bar-label">Combined</span>
          </div>
        </div>
        <div class="reach-hud">
          <span><span class="pulse-dot"></span>ORIGIN <b>Patna / Delhi NCR</b></span>
          <span>PIPELINE <b>research → script → produce → publish</b></span>
          <span>SITE <b>SpacePlasmaPhysics.com</b></span>
        </div>
      </div>
    </div>

    <div class="stat-row">
      <div class="stat tilt"><div class="stat-num">128,000+</div><div class="stat-label">Combined subscribers across two channels</div></div>
      <div class="stat tilt"><div class="stat-num">94K / 34K</div><div class="stat-label">Split across the two channels</div></div>
      <div class="stat tilt"><div class="stat-num">2×</div><div class="stat-label">YouTube Silver Creator Award</div></div>
      <div class="stat tilt"><div class="stat-num">1</div><div class="stat-label">Independent site founded — SpacePlasmaPhysics.com</div></div>
    </div>

    <p class="creation-note">I own the full pipeline on both channels — <b>research synthesis, scriptwriting, graphic design, video production, publishing, and community management</b> — at sustained, professional scale. I've also represented IIT Patna as an <b>Inter-IIT Representative</b>, competing at IIT Kharagpur and IIT Hyderabad across Machine Learning, Generative AI, and Debate.</p>
  </div>
</section>

<section id="education">
  <div class="wrap reveal">
    <div class="chart-panel" id="eduChartPanel">
      <div class="chart-panel-head">
        <span class="chart-panel-title">Academic trend</span>
        <span class="terminal-badge">score over time</span>
      </div>
      <div class="bar-chart" style="margin-top:10px;">
        <div class="bar-row"><span class="bar-row-label">Class X</span><div class="bar-track"><div class="bar-fill" style="--w:86%"></div></div><span class="bar-row-val">86%</span></div>
        <div class="bar-row"><span class="bar-row-label">Class XII (NIOS)</span><div class="bar-track"><div class="bar-fill" style="--w:90%"></div></div><span class="bar-row-val">90%</span></div>
        <div class="bar-row"><span class="bar-row-label">IIT Patna CGPA</span><div class="bar-track"><div class="bar-fill" style="--w:92.9%"></div></div><span class="bar-row-val">9.29/10</span></div>
      </div>
      <p class="chart-note">CGPA shown scaled to a 100-point track (9.29/10 → 92.9%) purely so the three stages sit on one comparable bar — the upward line holds at every stage.</p>
    </div>

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
    <div class="contact-inner tilt">
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

<button class="cmdk-launcher tilt" id="cmdkLauncher" type="button" aria-label="Open command palette">
  <span>⌘</span><span class="hide-mobile">ask this site anything</span><kbd>/</kbd>
</button>

<div class="cmdk-overlay" id="cmdkOverlay">
  <div class="cmdk-box">
    <div class="cmdk-input-row">
      <span class="cmdk-prompt">❯</span>
      <input class="cmdk-input" id="cmdkInput" type="text" autocomplete="off" spellcheck="false" placeholder="type a command… try 'help'">
      <span class="cmdk-esc">esc</span>
    </div>
    <div class="cmdk-body" id="cmdkBody"></div>
  </div>
</div>

<script>
// ---------- ambient starfield backdrop ----------
(function(){
  var canvas = document.getElementById('starfield');
  if(!canvas) return;
  var ctx = canvas.getContext('2d');
  var reduceMotion = window.matchMedia && window.matchMedia('(prefers-reduced-motion: reduce)').matches;
  var stars = [];
  var dpr = Math.min(window.devicePixelRatio || 1, 2);

  function resize(){
    canvas.width = window.innerWidth * dpr;
    canvas.height = window.innerHeight * dpr;
    canvas.style.width = window.innerWidth + 'px';
    canvas.style.height = window.innerHeight + 'px';
    var count = Math.round((window.innerWidth * window.innerHeight) / 9000);
    stars = [];
    for(var i=0;i<count;i++){
      stars.push({
        x: Math.random()*canvas.width,
        y: Math.random()*canvas.height,
        r: (Math.random()*1.1 + 0.3) * dpr,
        phase: Math.random()*Math.PI*2,
        speed: 0.4 + Math.random()*0.8
      });
    }
  }
  resize();
  var resizeTimer;
  window.addEventListener('resize', function(){
    clearTimeout(resizeTimer);
    resizeTimer = setTimeout(resize, 200);
  });

  function draw(t){
    ctx.clearRect(0,0,canvas.width,canvas.height);
    for(var i=0;i<stars.length;i++){
      var s = stars[i];
      var tw = reduceMotion ? 0.75 : 0.55 + 0.45*Math.sin((t/1000)*s.speed + s.phase);
      ctx.beginPath();
      ctx.arc(s.x, s.y, s.r, 0, Math.PI*2);
      ctx.fillStyle = 'rgba(237,239,245,' + (tw*0.55) + ')';
      ctx.fill();
    }
    if(!reduceMotion){ requestAnimationFrame(draw); }
  }
  requestAnimationFrame(draw);
  if(reduceMotion){ draw(0); }
})();

// ---------- site-wide 3D tilt on hover ----------
(function(){
  var reduceMotion = window.matchMedia && window.matchMedia('(prefers-reduced-motion: reduce)').matches;
  if(reduceMotion) return;
  var els = document.querySelectorAll('.tilt');
  els.forEach(function(el){
    var maxTilt = 6;
    el.addEventListener('pointermove', function(e){
      if(e.pointerType === 'touch') return;
      var r = el.getBoundingClientRect();
      var px = (e.clientX - r.left) / r.width;
      var py = (e.clientY - r.top) / r.height;
      var rx = (py - 0.5) * -maxTilt;
      var ry = (px - 0.5) * maxTilt;
      el.style.transform = 'perspective(700px) rotateX(' + rx + 'deg) rotateY(' + ry + 'deg) translateY(-2px)';
      el.style.setProperty('--mx', (px*100) + '%');
      el.style.setProperty('--my', (py*100) + '%');
    });
    el.addEventListener('pointerleave', function(){
      el.style.transform = '';
    });
  });
})();
</script>


<script>
(function(){
  // ---------- skills radar chart (pure SVG, no deps) ----------
  var svg = document.getElementById('radarSvg');
  if(!svg) return;
  var NS = 'http://www.w3.org/2000/svg';
  var cx = 150, cy = 150, maxR = 105;
  var axes = [
    { label:'AI/ML & RAG', value:12 },
    { label:'Android & SW', value:9 },
    { label:'Data & Web', value:8 },
    { label:'Tools', value:7 },
    { label:'Content', value:6 },
    { label:'Dashboards', value:5 }
  ];
  var maxVal = 12;
  var n = axes.length;

  function pt(i, r){
    var angle = (Math.PI * 2 * i / n) - Math.PI / 2;
    return { x: cx + r * Math.cos(angle), y: cy + r * Math.sin(angle) };
  }
  function el(tag, attrs){
    var e = document.createElementNS(NS, tag);
    Object.keys(attrs).forEach(function(k){ e.setAttribute(k, attrs[k]); });
    return e;
  }

  // rings
  [0.25, 0.5, 0.75, 1].forEach(function(f){
    var pts = [];
    for(var i=0;i<n;i++){ var p = pt(i, maxR*f); pts.push(p.x+','+p.y); }
    svg.appendChild(el('polygon', { points: pts.join(' '), class:'radar-ring' }));
  });
  // axes + labels
  for(var i=0;i<n;i++){
    var p = pt(i, maxR);
    svg.appendChild(el('line', { x1:cx, y1:cy, x2:p.x, y2:p.y, class:'radar-axis' }));
    var lp = pt(i, maxR + 20);
    var textEl = el('text', { x:lp.x, y:lp.y, class:'radar-label', 'text-anchor':'middle', 'dominant-baseline':'middle' });
    textEl.textContent = axes[i].label;
    svg.appendChild(textEl);
  }
  // data polygon
  var dataPts = axes.map(function(a, i){ return pt(i, maxR * (a.value / maxVal)); });
  svg.appendChild(el('polygon', { points: dataPts.map(function(p){ return p.x+','+p.y; }).join(' '), class:'radar-poly' }));
  dataPts.forEach(function(p){ svg.appendChild(el('circle', { cx:p.x, cy:p.y, r:2.6, class:'radar-dot' })); });
})();
</script>

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
  var chartPanelIds = ['reachPanel','skillsChartPanel','eduChartPanel'];
  if('IntersectionObserver' in window){
    var io = new IntersectionObserver(function(entries){
      entries.forEach(function(entry){
        if(entry.isIntersecting){ entry.target.classList.add('in'); io.unobserve(entry.target); }
      });
    }, { threshold:0.12 });
    document.querySelectorAll('.reveal').forEach(function(el){ io.observe(el); });

    var panelIo = new IntersectionObserver(function(entries){
      entries.forEach(function(entry){
        if(entry.isIntersecting){ entry.target.classList.add('in'); panelIo.unobserve(entry.target); }
      });
    }, { threshold:0.3 });
    chartPanelIds.forEach(function(id){
      var el = document.getElementById(id);
      if(el) panelIo.observe(el);
    });
  } else {
    document.querySelectorAll('.reveal').forEach(function(el){ el.classList.add('in'); });
    chartPanelIds.forEach(function(id){
      var el = document.getElementById(id);
      if(el) el.classList.add('in');
    });
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

<script>
(function(){
  // ---------- command palette: a tiny fake shell over the resume ----------
  var overlay = document.getElementById('cmdkOverlay');
  var input = document.getElementById('cmdkInput');
  var body = document.getElementById('cmdkBody');
  var launcher = document.getElementById('cmdkLauncher');
  var history = [];
  var histIndex = -1;

  var THEMES = {
    dark: null, // default :root values already in CSS
    light: {
      '--bg':'#f4f5f9', '--bg-raised':'#ffffff', '--surface':'#ffffff', '--surface-2':'#eef0f6',
      '--border':'#d9dce6', '--border-soft':'#e4e7ef', '--text':'#161a25', '--text-muted':'#565d72',
      '--text-faint':'#8c92a5'
    }
  };
  var currentTheme = 'dark';
  function setTheme(name){
    if(!THEMES.hasOwnProperty(name)) return false;
    var root = document.documentElement.style;
    if(name === 'dark'){
      Object.keys(THEMES.light).forEach(function(k){ root.removeProperty(k); });
    } else {
      Object.keys(THEMES[name]).forEach(function(k){ root.setProperty(k, THEMES[name][k]); });
    }
    currentTheme = name;
    return true;
  }

  function line(html, cls){
    var d = document.createElement('div');
    d.className = 'cmdk-line' + (cls ? ' ' + cls : '');
    d.innerHTML = html;
    body.appendChild(d);
  }
  function hints(list){
    var row = document.createElement('div');
    row.className = 'cmdk-hint-row';
    list.forEach(function(h){
      var b = document.createElement('span');
      b.className = 'cmdk-hint';
      b.textContent = h;
      b.addEventListener('click', function(){ input.value = h; runCommand(h); input.focus(); });
      row.appendChild(b);
    });
    body.appendChild(row);
  }
  function jumpTo(id){
    var el = document.getElementById(id);
    if(el){ closePalette(); setTimeout(function(){ el.scrollIntoView({behavior:'smooth', block:'start'}); }, 150); }
  }

  var COMMANDS = {
    help: function(){
      line('Available commands: <b>about</b>, <b>journey</b>, <b>skills</b>, <b>projects</b>, <b>education</b>, <b>contact</b>, <b>resume</b>, <b>theme [dark|light]</b>, <b>sudo hire me</b>, <b>clear</b>');
      hints(['about','journey','skills','projects','contact','resume','theme light','sudo hire me']);
    },
    about: function(){
      line('Final-year <b>B.S. (Honours), CS &amp; Data Analytics</b> @ IIT Patna · CGPA 9.29/10 · grad July 2027.');
      line('Builds RAG pipelines and a self-healing Android agent — also runs two YouTube channels at 128,000+ combined subscribers.');
      jumpTo('about');
    },
    journey: function(){
      line('Class X (86%) → NIOS Class XII (90%) → IIT Patna (9.29 CGPA) → RAG pipelines → Gaya (Android agent) → Inter-IIT → 128,000+ YouTube reach → open to internships now.');
      jumpTo('journey');
    },
    skills: function(){
      line('AI/ML: LangChain, ChromaDB, FAISS, PaddleOCR, Hugging Face, LoRA/PEFT, Ollama, AI4Bharat/BHASHINI');
      line('Android: Kotlin, Java, Android SDK, Multi-Agent Systems');
      line('Data/Web: Python, SQL, Pandas, Streamlit, HTML/CSS/JS');
      jumpTo('skills');
    },
    projects: function(){
      line('<b>RAG Document Q&amp;A Assistant</b> — LangChain + ChromaDB + PaddleOCR, cited answers over scanned PDFs.');
      line('<b>Multi-Document RAG Chat</b> — metadata-filtered retrieval across ChromaDB/FAISS with conversational memory.');
      line('<b>Gaya</b> — self-healing multi-agent Android app that diagnoses and fixes issues at runtime.');
      jumpTo('projects');
    },
    education: function(){
      line('IIT Patna — 9.29 CGPA, B.S. (Honours) CS &amp; Data Analytics, expected July 2027.');
      line('NIOS Class XII — 90% · Satitpur Kumar Mahim Chandra Institution Class X — 86%.');
      jumpTo('education');
    },
    contact: function(){
      line('Email: <a href="mailto:abhik_24a12res20@iitp.ac.in">abhik_24a12res20@iitp.ac.in</a>');
      line('Phone: +91 82396 65061 · Based in Patna, Bihar / Delhi NCR · available immediately.');
      jumpTo('contact');
    },
    resume: function(){
      line('Opening résumé in a new tab…');
      window.open('./Abhik_Mondal_Resume.pdf', '_blank', 'noopener');
    },
    clear: function(){ body.innerHTML = ''; },
    whoami: function(){ line('abhik_mondal — applied ai/ml engineer, rag &amp; llm systems, android.'); },
    exit: function(){ closePalette(); }
  };

  function runCommand(raw){
    var q = raw.trim();
    if(!q) return;
    history.push(q); histIndex = history.length;
    line(escapeCmd(q), 'cmd');

    var lower = q.toLowerCase();
    var parts = lower.split(/\s+/);

    if(lower === 'sudo hire me'){
      line('<b>Permission granted.</b> Reaching out at abhik_24a12res20@iitp.ac.in or +91 82396 65061 — available immediately.');
      return;
    }
    if(parts[0] === 'theme'){
      var target = parts[1];
      if(target === 'light' || target === 'dark'){
        setTheme(target);
        line('Theme switched to <b>' + target + '</b>.');
      } else {
        line('Usage: <b>theme light</b> or <b>theme dark</b> — currently <b>' + currentTheme + '</b>.');
      }
      return;
    }
    if(COMMANDS.hasOwnProperty(parts[0])){
      COMMANDS[parts[0]]();
      return;
    }
    line('command not found: <b>' + escapeCmd(q) + '</b> — try <b>help</b>');
  }

  function escapeCmd(str){
    var d = document.createElement('div');
    d.textContent = str;
    return d.innerHTML;
  }

  function openPalette(){
    overlay.classList.add('open');
    if(body.children.length === 0){
      line('Hey — this is a tiny shell over Abhik\'s résumé. Type <b>help</b> to see what it can do.');
      hints(['help','about','projects','resume']);
    }
    input.value = '';
    setTimeout(function(){ input.focus(); }, 50);
  }
  function closePalette(){
    overlay.classList.remove('open');
  }

  launcher.addEventListener('click', openPalette);
  overlay.addEventListener('click', function(e){ if(e.target === overlay) closePalette(); });

  document.addEventListener('keydown', function(e){
    var tag = (document.activeElement && document.activeElement.tagName) || '';
    var typing = tag === 'INPUT' || tag === 'TEXTAREA';
    if(e.key === '/' && !typing){ e.preventDefault(); openPalette(); }
    else if((e.metaKey || e.ctrlKey) && e.key.toLowerCase() === 'k'){ e.preventDefault(); openPalette(); }
    else if(e.key === 'Escape' && overlay.classList.contains('open')){ closePalette(); }
  });

  input.addEventListener('keydown', function(e){
    if(e.key === 'Enter'){
      runCommand(input.value);
      input.value = '';
      body.scrollTop = body.scrollHeight;
    } else if(e.key === 'ArrowUp'){
      if(histIndex > 0){ histIndex--; input.value = history[histIndex]; e.preventDefault(); }
    } else if(e.key === 'ArrowDown'){
      if(histIndex < history.length - 1){ histIndex++; input.value = history[histIndex]; }
      else { histIndex = history.length; input.value = ''; }
      e.preventDefault();
    }
  });
})();
</script>

</body>
</html>
