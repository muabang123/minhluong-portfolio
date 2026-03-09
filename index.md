
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Portfolio</title>
<style>
  @import url('https://fonts.googleapis.com/css2?family=Playfair+Display:ital,wght@1,400;1,700&display=swap');

  html, body {
    cursor: none !important; 
    min-height: 100vh;
    margin: 0;
    font-family: sans-serif;
    background: transparent;
    padding: 20px;
  }

  a, button, .content-card, .project-link {
    cursor: none !important;
  }

  #cursor-dot {
    width: 8px;
    height: 8px;
    background-color: #0366d6;
    border-radius: 50%;
    position: fixed;
    pointer-events: none;
    z-index: 9999;
    transform: translate(-50%, -50%);
  }

  #cursor-outline {
    width: 30px;
    height: 30px;
    border: 2px solid rgba(184, 134, 11, 0.5);
    border-radius: 50%;
    position: fixed;
    pointer-events: none;
    z-index: 9998;
    transform: translate(-50%, -50%);
    transition: width 0.3s, height 0.3s, background-color 0.3s;
  }

  .cursor-hover-active {
    width: 50px !important;
    height: 50px !important;
    background-color: rgba(184, 134, 11, 0.1);
    border-color: #b8860b !important;
  }

  .aristocratic-text {
    font-family: 'Playfair Display', serif;
    font-style: italic;
    font-size: 1.15rem;
    line-height: 1.6;
    color: #2c3e50;
    min-height: 80px;
  }

  .typing-cursor {
    display: inline-block;
    width: 2px;
    background-color: #0366d6;
    margin-left: 3px;
    animation: blink 0.7s infinite;
  }

  @keyframes blink {
    50% { opacity: 0; }
  }

  .content-card {
    border: 1px solid #e1e4e8;
    border-radius: 8px;
    padding: 20px;
    margin-bottom: 25px;
    background-color: #ffffff;
    opacity: 0;
    transform: translateY(40px);
    transition: all 0.8s cubic-bezier(0.25, 0.46, 0.45, 0.94);
  }

  .content-card.is-visible {
    opacity: 1;
    transform: translateY(0);
  }

  .content-card:hover {
    transform: translateY(-5px);
    box-shadow: 0 10px 20px rgba(0,0,0,0.1);
    border-color: #b8860b;
  }

  .project-header { display: flex; justify-content: space-between; align-items: center; }
  .project-link { display: flex; align-items: center; gap: 5px; text-decoration: none; font-weight: bold; color: #0366d6; }
  .skill-badge { margin: 2px; }

  .tech-stack-container {
    display: flex;
    flex-wrap: wrap;
    gap: 8px;
    margin-top: 12px;
  }

  .tech-tag {
    padding: 6px 14px;
    border-radius: 10px;
    font-size: 0.85rem;
    font-weight: 700;
    color: white;
    display: inline-block;
    cursor: none !important;
    box-shadow: 0 2px 4px rgba(0,0,0,0.1);
  }

  .ts { background-color: #3178c6; }
  .js { background-color: #f7df1e; color: #000; }
  .php { background-color: #777bb4; }
  .css { background-color: #264de4; }
  .html { background-color: #e34f26; }
  .react { background-color: #61dafb; color: #000; }
  .node { background-color: #339933; }
  .mysql { background-color: #4479a1; }
  .socketio { background-color: #010101; }
  .redis { background-color: #dc382d; }
  .csharp { background-color: #239120; }
  .dotnet { background-color: #512bd4; }
  .flask { background-color: #000000; }
  .python { background-color: #3776ab; }

  /* ===== TECHNOLOGIES SECTION ===== */
  .tech-section {
    opacity: 0;
    transform: translateY(40px);
    transition: all 0.8s cubic-bezier(0.25, 0.46, 0.45, 0.94);
    margin-bottom: 25px;
  }

  .tech-section.is-visible {
    opacity: 1;
    transform: translateY(0);
  }

  .tech-section-title {
    text-align: center;
    font-size: 1.6rem;
    font-weight: 800;
    margin-bottom: 6px;
    color: #1a1a2e;
    letter-spacing: -0.5px;
  }

  .tech-section-underline {
    width: 80px;
    height: 3px;
    background: linear-gradient(90deg, #0366d6, #b8860b);
    margin: 0 auto 28px auto;
    border-radius: 2px;
  }

  .tech-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 18px;
  }

  @media (max-width: 600px) {
    .tech-grid { grid-template-columns: 1fr; }
  }

  .tech-card {
    background: #fff;
    border-radius: 16px;
    padding: 24px;
    border: 1px solid #e8ecf0;
    box-shadow: 0 2px 12px rgba(0,0,0,0.06);
    transition: transform 0.3s ease, box-shadow 0.3s ease, border-color 0.3s ease;
    cursor: none !important;
  }

  .tech-card:hover {
    transform: translateY(-6px);
    box-shadow: 0 14px 32px rgba(0,0,0,0.12);
    border-color: #b8860b;
  }

  .tech-card-header {
    display: flex;
    align-items: center;
    gap: 14px;
    margin-bottom: 18px;
  }

  .tech-card-icon {
    width: 48px;
    height: 48px;
    border-radius: 12px;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 1.5rem;
    flex-shrink: 0;
  }

  .icon-lang   { background: linear-gradient(135deg, #ff6b35, #f7c59f); }
  .icon-frame  { background: linear-gradient(135deg, #56cfe1, #72efdd); }
  .icon-db     { background: linear-gradient(135deg, #7b2d8b, #c77dff); }
  .icon-tools  { background: linear-gradient(135deg, #f72585, #ff9e00); }

  .tech-card-label {
    font-size: 0.95rem;
    font-weight: 900;
    letter-spacing: 1.5px;
    color: #1a1a2e;
    text-transform: uppercase;
  }

  .pill-grid {
    display: flex;
    flex-wrap: wrap;
    gap: 8px;
  }

  .pill {
    display: inline-flex;
    align-items: center;
    gap: 6px;
    padding: 7px 14px;
    border-radius: 12px;
    font-size: 0.78rem;
    font-weight: 800;
    letter-spacing: 0.5px;
    color: #fff;
    box-shadow: 0 2px 6px rgba(0,0,0,0.15);
    transition: transform 0.2s ease, box-shadow 0.2s ease;
    cursor: none !important;
    text-transform: uppercase;
  }

  .pill:hover {
    transform: scale(1.07);
    box-shadow: 0 4px 12px rgba(0,0,0,0.22);
  }

  .pill-emoji { font-size: 1rem; }

  .p-java       { background: #e76f51; }
  .p-js         { background: #e9c46a; color: #222; }
  .p-ts         { background: #3178c6; }
  .p-csharp     { background: #239120; }
  .p-cpp        { background: #e91e8c; }
  .p-python     { background: #3776ab; }
  .p-html       { background: #e34f26; }
  .p-css        { background: #264de4; }
  .p-spring     { background: #6db33f; }
  .p-react      { background: #00b4d8; color: #000; }
  .p-node       { background: #339933; }
  .p-next       { background: #1a1a2e; }
  .p-dotnet     { background: #512bd4; }
  .p-mysql      { background: #4479a1; }
  .p-sqlserver  { background: #cc2927; }
  .p-workbench  { background: #2d6a4f; }
  .p-mongo      { background: #4caf50; }
  .p-docker     { background: #2496ed; }
  .p-git        { background: #f4511e; }
  .p-postman    { background: #ff6c37; }
  .p-ghactions  { background: #2088ff; }
  .p-kafka      { background: #1a1a2e; }
</style>
</head>
<body>
<iframe src="background.html" style="position:fixed;inset:0;width:100%;height:100%;border:none;z-index:-1;pointer-events:none;"></iframe>
<div id="cursor-dot"></div>
<div id="cursor-outline"></div>

<h1>👋 Welcome to My Portfolio</h1>

<hr>

<div class="content-card" id="about-card">
  <h2>👨‍💻 About Me</h2>
  <div class="aristocratic-text">
    <span id="typing-destination"></span><span id="typing-cursor-el" class="typing-cursor">&nbsp;</span>
  </div>

  <br>
  <h3>🎓 Education & Details</h3>
  <ul>
    <li><b>University:</b> Saigon University (SGU)</li>
    <li><b>Major:</b> Software Engineering</li>
    <li><b>Current Status:</b> 3rd-year Student</li>
    <li><b>GPA:</b> <b>3.10 / 4.0</b></li>
    <li><b>Birthday:</b> December 26, 2005</li>
  </ul>
</div>

<hr>

<h1>🚀 Featured Projects</h1>

<div class="content-card">
  <div class="project-header">
    <h3>🚌 Smart School Bus Tracking System</h3>
    <a href="https://github.com/muabang123/Smart-School-Bus-Tracking-System---SSB" class="project-link">
      <img src="https://img.shields.io/badge/GitHub-View_Code-181717?style=flat&logo=github" alt="GitHub">
    </a>
  </div>
  <p>A comprehensive real-time tracking application designed for school buses.</p>
  <div class="tech-stack-container">
    <span class="tech-tag react">React</span>
    <span class="tech-tag node">Node.js</span>
    <span class="tech-tag mysql">MySQL</span>
    <span class="tech-tag socketio">Socket.IO</span>
    <span class="tech-tag redis">Redis</span>
  </div>
</div>

<div class="content-card">
  <div class="project-header">
    <h3>✈️ Airline Ticket Management System</h3>
    <a href="https://github.com/muabang123/Plane_Ticket" class="project-link">
      <img src="https://img.shields.io/badge/GitHub-View_Code-181717?style=flat&logo=github" alt="GitHub">
    </a>
  </div>
  <p>A desktop-based management software for airline agencies.</p>
  <div class="tech-stack-container">
    <span class="tech-tag csharp">C#</span>
    <span class="tech-tag dotnet">.NET WinForms</span>
    <span class="tech-tag mysql">MySQL</span>
  </div>
</div>

<div class="content-card">
  <div class="project-header">
    <h3>👟 Online Shoes Store</h3>
    <a href="https://github.com/muabang123/Shoes_Store" class="project-link">
      <img src="https://img.shields.io/badge/GitHub-View_Code-181717?style=flat&logo=github" alt="GitHub">
    </a>
  </div>
  <p>A dynamic e-commerce web application developed to manage footwear sales.</p>
  <div class="tech-stack-container">
    <span class="tech-tag js">JavaScript</span>
    <span class="tech-tag php">PHP</span>
    <span class="tech-tag mysql">MySQL</span>
  </div>
</div>

<div class="content-card">
  <div class="project-header">
    <h3>🍎 Fresh Fruit E-Commerce (Front-end)</h3>
    <a href="https://github.com/muabang123/shop_hoa_qua" class="project-link">
      <img src="https://img.shields.io/badge/GitHub-View_Code-181717?style=flat&logo=github" alt="GitHub">
    </a>
  </div>
  <p>A specialized e-commerce interface designed for a premium fresh fruit boutique. This project prioritizes a high-end visual experience with a modern, product-centric layout. Currently, it focuses on delivering a polished user interface and seamless transitions (Front-end implementation only)..</p>
  <div class="tech-stack-container">
    <span class="tech-tag html">HTML5</span>
    <span class="tech-tag css">CSS3</span>
    <span class="tech-tag js">JavaScript</span>
  </div>
</div>

<div class="content-card">
  <div class="project-header">
    <h3>📺 YouTube Lite</h3>
    <a href="https://github.com/muabang123/Youtube_Web" class="project-link">
      <img src="https://img.shields.io/badge/GitHub-View_Code-181717?style=flat&logo=github" alt="GitHub">
    </a>
  </div>
  <p>A lightweight video streaming platform.</p>
  <div class="tech-stack-container">
    <span class="tech-tag python">Python</span>
    <span class="tech-tag flask">Flask</span>
    <span class="tech-tag mysql">MySQL</span>
  </div>
</div>

<hr>

<!-- ===== TECHNOLOGIES SECTION ===== -->
<div class="tech-section" id="tech-section">
  <div class="tech-section-title">Technologies and tools I work with</div>
  <div class="tech-section-underline"></div>

  <div class="tech-grid">

    <div class="tech-card">
      <div class="tech-card-header">
        <div class="tech-card-icon icon-lang">💻</div>
        <div class="tech-card-label">Languages</div>
      </div>
      <div class="pill-grid">
        <span class="pill p-java"><span class="pill-emoji">☕</span> Java</span>
        <span class="pill p-js"><span class="pill-emoji">🟨</span> JavaScript</span>
        <span class="pill p-ts"><span class="pill-emoji">🟦</span> ShellScript</span>
        <span class="pill p-csharp"><span class="pill-emoji">⚡</span> C#</span>
        <span class="pill p-cpp"><span class="pill-emoji">🔧</span> C/C++</span>
        <span class="pill p-python"><span class="pill-emoji">🐍</span> Python</span>
        <span class="pill p-html"><span class="pill-emoji">🌐</span> HTML</span>
        <span class="pill p-css"><span class="pill-emoji">🎨</span> CSS</span>
      </div>
    </div>

    <div class="tech-card">
      <div class="tech-card-header">
        <div class="tech-card-icon icon-frame">🔨</div>
        <div class="tech-card-label">Frameworks</div>
      </div>
      <div class="pill-grid">
        <span class="pill p-spring"><span class="pill-emoji">🌿</span> Spring Boot</span>
        <span class="pill p-react"><span class="pill-emoji">⚛️</span> React</span>
        <span class="pill p-node"><span class="pill-emoji">🟢</span> Node.js</span>
        <span class="pill p-next"><span class="pill-emoji">⚫</span> Next.js</span>
        <span class="pill p-dotnet"><span class="pill-emoji">🟣</span> .NET</span>
      </div>
    </div>

    <div class="tech-card">
      <div class="tech-card-header">
        <div class="tech-card-icon icon-db">💾</div>
        <div class="tech-card-label">Cloud &amp; Databases</div>
      </div>
      <div class="pill-grid">
        <span class="pill p-mysql"><span class="pill-emoji">🐬</span> MySQL</span>
        <span class="pill p-sqlserver"><span class="pill-emoji">🔴</span> SQL Server</span>
        <span class="pill p-workbench"><span class="pill-emoji">🔧</span> MySQL Workbench</span>
        <span class="pill p-mongo"><span class="pill-emoji">🍃</span> Xampp</span>
      </div>
    </div>

    <div class="tech-card">
      <div class="tech-card-header">
        <div class="tech-card-icon icon-tools">⚙️</div>
        <div class="tech-card-label">Tools &amp; DevOps</div>
      </div>
      <div class="pill-grid">
        <span class="pill p-docker"><span class="pill-emoji">🐳</span> Docker</span>
        <span class="pill p-git"><span class="pill-emoji">🔶</span> Git</span>
        <span class="pill p-postman"><span class="pill-emoji">📮</span> Cisco PacketTracer</span>
        <span class="pill p-ghactions"><span class="pill-emoji">🦄</span> GitHub Actions</span>
        <span class="pill p-kafka"><span class="pill-emoji">⚡</span> Apache Kafka</span>
      </div>
    </div>

  </div>
</div>

<hr>

<p align="center"><i>"Building the future, one line of code at a time."</i></p>

<script>
  // CUSTOM CURSOR
  const dot = document.getElementById("cursor-dot");
  const outline = document.getElementById("cursor-outline");

  window.addEventListener("mousemove", (e) => {
    dot.style.left = e.clientX + "px";
    dot.style.top = e.clientY + "px";
    outline.animate({
      left: e.clientX + "px",
      top: e.clientY + "px"
    }, { duration: 500, fill: "forwards" });
  });

  document.querySelectorAll('a, .content-card, .tech-card').forEach(el => {
    el.addEventListener('mouseenter', () => outline.classList.add('cursor-hover-active'));
    el.addEventListener('mouseleave', () => outline.classList.remove('cursor-hover-active'));
  });

  // TYPING
  const text = "I am a dedicated 3rd-year Software Engineering student at Saigon University (SGU) with a strong passion for building scalable and efficient applications. Currently, I am focusing on mastering both Front-end and Back-end development to become a versatile Full-stack Developer.";
  const dest = document.getElementById("typing-destination");
  const curEl = document.getElementById("typing-cursor-el");
  let charIdx = 0;

  function startTyping() {
    if (charIdx < text.length) {
      dest.innerHTML += text.charAt(charIdx);
      charIdx++;
      setTimeout(startTyping, 25);
    } else {
      curEl.style.display = "none";
    }
  }

  // SCROLL REVEAL for content-cards
  const obs = new IntersectionObserver((entries) => {
    entries.forEach(entry => {
      if (entry.isIntersecting) {
        entry.target.classList.add('is-visible');
        if (entry.target.id === 'about-card') startTyping();
        obs.unobserve(entry.target);
      }
    });
  }, { threshold: 0.1 });

  document.querySelectorAll('.content-card').forEach(c => obs.observe(c));

  // SCROLL REVEAL for tech section with staggered animations
  const techObs = new IntersectionObserver((entries) => {
    entries.forEach(entry => {
      if (entry.isIntersecting) {
        entry.target.classList.add('is-visible');

        // Stagger each tech-card
        const cards = entry.target.querySelectorAll('.tech-card');
        cards.forEach((card, i) => {
          card.style.opacity = '0';
          card.style.transform = 'translateY(30px)';
          card.style.transition = `opacity 0.6s ease ${i * 0.12}s, transform 0.6s ease ${i * 0.12}s`;
          requestAnimationFrame(() => {
            setTimeout(() => {
              card.style.opacity = '1';
              card.style.transform = 'translateY(0)';
            }, 50);
          });
        });

        // Stagger each pill
        const pills = entry.target.querySelectorAll('.pill');
        pills.forEach((pill, i) => {
          pill.style.opacity = '0';
          pill.style.transform = 'scale(0.7)';
          pill.style.transition = `opacity 0.35s ease ${0.25 + i * 0.045}s, transform 0.35s ease ${0.25 + i * 0.045}s`;
          requestAnimationFrame(() => {
            setTimeout(() => {
              pill.style.opacity = '1';
              pill.style.transform = 'scale(1)';
            }, 50);
          });
        });

        techObs.unobserve(entry.target);
      }
    });
  }, { threshold: 0.08 });

  const techSection = document.getElementById('tech-section');
  if (techSection) techObs.observe(techSection);
</script>

</body>
</html>
