# Portfolio
My portfolio and software development projects.
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Abhay Bhalekar — Portfolio</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Fraunces:opsz,wght@9..144,400;9..144,500;9..144,600&family=Inter:wght@400;500;600&family=IBM+Plex+Mono:wght@400;500&display=swap" rel="stylesheet">
<style>
  :root{
    --paper: #F2F1EA;
    --paper-dim: #EAE8DE;
    --ink: #1C1F1A;
    --ink-soft: #55584F;
    --line: #D3D0C3;
    --pine: #2F6B4F;
    --pine-dim: #E4EBE2;
    --gold: #A8791B;
  }

  * { box-sizing: border-box; }
  html { scroll-behavior: smooth; }

  body{
    margin:0;
    background: var(--paper);
    color: var(--ink);
    font-family: 'Inter', sans-serif;
    font-size: 16px;
    line-height: 1.6;
    -webkit-font-smoothing: antialiased;
  }

  a { color: var(--pine); text-decoration: none; border-bottom: 1px solid transparent; }
  a:hover { border-bottom-color: var(--pine); }
  a:focus-visible, button:focus-visible { outline: 2px solid var(--pine); outline-offset: 3px; }

  .wrap{
    max-width: 760px;
    margin: 0 auto;
    padding: 0 28px;
  }

  /* ---------- Hero ---------- */
  header.hero{
    padding: 88px 0 56px;
    border-bottom: 1px solid var(--line);
  }
  .hero h1{
    font-family: 'Fraunces', serif;
    font-size: clamp(2.4rem, 6vw, 3.6rem);
    font-weight: 500;
    letter-spacing: -0.01em;
    margin: 0 0 14px;
    line-height: 1.05;
  }
  .hero .role{
    font-size: 1.05rem;
    color: var(--ink-soft);
    max-width: 46ch;
    margin: 0 0 28px;
  }
  .contact-strip{
    display: flex;
    flex-wrap: wrap;
    gap: 0;
    font-family: 'IBM Plex Mono', monospace;
    font-size: 0.82rem;
    color: var(--ink-soft);
  }
  .contact-strip a, .contact-strip span{
    padding: 6px 16px 6px 0;
    margin-right: 16px;
    border-right: 1px solid var(--line);
  }
  .contact-strip a:last-child, .contact-strip span:last-child{
    border-right: none;
  }
  .contact-strip a{ color: var(--ink); border-bottom: none; }
  .contact-strip a:hover{ color: var(--pine); }

  /* ---------- Section shell ---------- */
  section{ padding: 56px 0; border-bottom: 1px solid var(--line); }
  section:last-of-type{ border-bottom: none; }

  h2.section-title{
    font-family: 'Fraunces', serif;
    font-size: 1.5rem;
    font-weight: 500;
    margin: 0 0 32px;
  }

  /* ---------- Focus grid ---------- */
  .focus-grid{
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
    gap: 32px 24px;
  }
  .focus-group h3{
    font-size: 0.78rem;
    font-family: 'IBM Plex Mono', monospace;
    font-weight: 500;
    color: var(--pine);
    margin: 0 0 10px;
  }
  .focus-group ul{
    list-style: none;
    margin: 0; padding: 0;
  }
  .focus-group li{
    padding: 5px 0;
    border-top: 1px solid var(--line);
    font-size: 0.95rem;
  }
  .focus-group li:first-child{ border-top: none; }

  /* ---------- Build log (timeline) ---------- */
  .log{
    position: relative;
    margin-left: 4px;
  }
  .log-item{
    position: relative;
    padding: 0 0 28px 28px;
    border-left: 1px solid var(--line);
  }
  .log-item:last-child{ padding-bottom: 0; border-left-color: transparent; }
  .log-item::before{
    content: '';
    position: absolute;
    left: -4.5px;
    top: 4px;
    width: 8px; height: 8px;
    border-radius: 50%;
    background: var(--paper);
    border: 1.5px solid var(--pine);
  }
  .log-item.in-progress::before{
    background: var(--gold);
    border-color: var(--gold);
  }
  .log-date{
    font-family: 'IBM Plex Mono', monospace;
    font-size: 0.76rem;
    color: var(--ink-soft);
    display: block;
    margin-bottom: 3px;
  }
  .log-title{ font-weight: 600; font-size: 0.98rem; }
  .log-meta{ color: var(--ink-soft); font-size: 0.9rem; margin-top: 2px; }

  /* ---------- Project ---------- */
  .project-card{
    border: 1px solid var(--line);
    background: var(--paper-dim);
    padding: 28px 28px 30px;
  }
  .project-card h3{
    font-family: 'Fraunces', serif;
    font-size: 1.2rem;
    font-weight: 500;
    margin: 0 0 12px;
  }
  .project-card p{ margin: 0 0 16px; color: var(--ink-soft); }
  .project-card p:last-child{ margin-bottom: 0; }
  .stack-line{
    font-family: 'IBM Plex Mono', monospace;
    font-size: 0.78rem;
    color: var(--pine);
  }

  /* ---------- Footer ---------- */
  footer{
    padding: 48px 0 80px;
  }
  footer h2.section-title{ margin-bottom: 18px; }
  footer p{ color: var(--ink-soft); max-width: 46ch; }
  .footer-actions{
    display: flex; gap: 14px; flex-wrap: wrap;
    margin-top: 22px;
  }
  .btn{
    font-family: 'IBM Plex Mono', monospace;
    font-size: 0.82rem;
    padding: 11px 20px;
    border: 1px solid var(--ink);
    color: var(--ink);
    border-bottom: 1px solid var(--ink);
  }
  .btn.primary{
    background: var(--pine);
    border-color: var(--pine);
    color: var(--paper);
  }
  .btn:hover{ background: var(--ink); color: var(--paper); border-color: var(--ink); }
  .btn.primary:hover{ background: #24523d; border-color: #24523d; color: var(--paper); }

  @media (max-width: 480px){
    .contact-strip a, .contact-strip span{ margin-right: 10px; padding-right: 10px; }
    header.hero{ padding-top: 64px; }
  }

  @media (prefers-reduced-motion: reduce){
    html{ scroll-behavior: auto; }
  }
</style>
</head>
<body>

<div class="wrap">

  <header class="hero">
    <h1>Abhay Bhalekar</h1>
    <p class="role">Computer science student in Latur, building with Python, Java and PHP, and learning to read data through Power BI. Looking for a place to put that to work.</p>
    <div class="contact-strip">
      <a href="mailto:bhalekarabhay365@gmail.com">bhalekarabhay365@gmail.com</a>
      <a href="tel:+917249238800">+91 72492 38800</a>
      <span>Latur, Maharashtra</span>
      <a href="#" target="_blank" rel="noopener">LinkedIn</a>
    </div>
  </header>

  <section id="focus">
    <h2 class="section-title">What I work with</h2>
    <div class="focus-grid">
      <div class="focus-group">
        <h3>LANGUAGES</h3>
        <ul>
          <li>Python</li>
          <li>Java</li>
          <li>C / C++</li>
          <li>PHP</li>
        </ul>
      </div>
      <div class="focus-group">
        <h3>WEB</h3>
        <ul>
          <li>HTML &amp; CSS</li>
          <li>JavaScript</li>
          <li>PHP backends</li>
        </ul>
      </div>
      <div class="focus-group">
        <h3>DATA</h3>
        <ul>
          <li>Power BI</li>
          <li>Excel</li>
          <li>MySQL</li>
          <li>SQL Server</li>
        </ul>
      </div>
      <div class="focus-group">
        <h3>TOOLS</h3>
        <ul>
          <li>VS Code</li>
          <li>Jupyter Notebook</li>
          <li>Eclipse IDE</li>
        </ul>
      </div>
    </div>
  </section>

  <section id="project">
    <h2 class="section-title">Project</h2>
    <div class="project-card">
      <h3>Complaint Registration System</h3>
      <p>A system for submitting, tracking and managing complaints, built around a secure and simple interface so people can follow a complaint from filing through to resolution without needing help to do it.</p>
      <p class="stack-line">Academic project — COCSIT, Latur</p>
    </div>
  </section>

  <section id="log">
    <h2 class="section-title">Build log</h2>
    <div class="log">

      <div class="log-item">
        <span class="log-date">2022</span>
        <div class="log-title">SSC — Yashwantrao Chavan Vidyaniketan School, Latur</div>
        <div class="log-meta">82.60%</div>
      </div>

      <div class="log-item">
        <span class="log-date">2024</span>
        <div class="log-title">HSC — Yashwant Jr. College, Pimpri (Amba), Latur</div>
        <div class="log-meta">80.67%</div>
      </div>

      <div class="log-item">
        <span class="log-date">2024 – 2027</span>
        <div class="log-title">B.Sc. Computer Science — COCSIT, Latur</div>
        <div class="log-meta">In progress · FY SGPA 7.36 · SY SGPA 8.77</div>
      </div>

      <div class="log-item">
        <span class="log-date">Dec 2025</span>
        <div class="log-title">5-Day AI Agents Intensive Course</div>
        <div class="log-meta">Kaggle &amp; Google</div>
      </div>

      <div class="log-item">
        <span class="log-date">Jun 2026</span>
        <div class="log-title">Google AI Essentials</div>
        <div class="log-meta">Google / Coursera · Certificate N4IAVGL5A7R7</div>
      </div>

      <div class="log-item">
        <span class="log-date">Jun 2026</span>
        <div class="log-title">Google Prompting Essentials</div>
        <div class="log-meta">Google / Coursera · Certificate WO5CILX3446T</div>
      </div>

      <div class="log-item">
        <span class="log-date">Aug 2026</span>
        <div class="log-title">Mastering Power BI: Data Analysis and Dashboard Creation</div>
        <div class="log-meta">Skill India Digital Hub</div>
      </div>

      <div class="log-item">
        <span class="log-date">Aug 2026</span>
        <div class="log-title">Cyber Job Simulation</div>
        <div class="log-meta">Deloitte, via Forage</div>
      </div>

      <div class="log-item in-progress">
        <span class="log-date">In progress</span>
        <div class="log-title">Microsoft Azure Fundamentals (AZ-900)</div>
      </div>

    </div>
  </section>

  <footer id="contact">
    <h2 class="section-title">Get in touch</h2>
    <p>Open to internships and entry-level roles in software development or data analysis. Based in Latur, happy to work remotely.</p>
    <div class="footer-actions">
      <a class="btn primary" href="mailto:bhalekarabhay365@gmail.com">Email me</a>
      <a class="btn" href="tel:+917249238800">Call</a>
    </div>
  </footer>

</div>

</body>
</html>
