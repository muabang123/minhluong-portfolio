<style>
  /* 1. SETUP FONT & CURSOR CƠ BẢN */
  @import url('https://fonts.googleapis.com/css2?family=Playfair+Display:ital,wght@1,400;1,700&display=swap');

  html, body {
    cursor: none !important; 
    min-height: 100vh;
    margin: 0;
  }

  a, button, .content-card, .project-link {
    cursor: none !important;
  }

  /* 2. CUSTOM CURSOR AURA */
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

  /* Hiệu ứng con trỏ khi hover */
  .cursor-hover-active {
    width: 50px !important;
    height: 50px !important;
    background-color: rgba(184, 134, 11, 0.1);
    border-color: #b8860b !important;
  }

  /* 3. PHONG CÁCH QUÝ TỘC & TYPING */
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

  /* 4. ANIMATION CUỘN TRANG (SCROLL REVEAL) */
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
</style>

<div id="cursor-dot"></div>
<div id="cursor-outline"></div>

# 👋 Welcome to My Portfolio

---

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

  <h3>🛠 Core Technical Skills</h3>
  <div class="tech-stack">
    <img src="https://img.shields.io/badge/GitHub-181717?style=flat-square&logo=github&logoColor=white" class="skill-badge" />
    <img src="https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white" class="skill-badge" />
    <img src="https://img.shields.io/badge/SQL-CC2927?style=flat-square&logo=postgresql&logoColor=white" class="skill-badge" />
    <img src="https://img.shields.io/badge/VS_Code-007ACC?style=flat-square&logo=visual-studio-code&logoColor=white" class="skill-badge" />
    <img src="https://img.shields.io/badge/Android_Studio-3DDC84?style=flat-square&logo=android-studio&logoColor=white" class="skill-badge" />
  </div>
</div>

---

# 🚀 Featured Projects

<div class="content-card">
  <div class="project-header">
    <h3>🚌 Smart School Bus Tracking System</h3>
    <a href="https://github.com/muabang123/Smart-School-Bus-Tracking-System---SSB" class="project-link">
      <img src="https://img.shields.io/badge/GitHub-View_Code-181717?style=flat&logo=github" alt="GitHub">
    </a>
  </div>
  <p>A comprehensive real-time tracking application designed for school buses.</p>
  <ul>
    <li><b>Tech Stack:</b> React, Node.js, MySQL, Socket.IO, Redis.</li>
  </ul>
</div>

<div class="content-card">
  <div class="project-header">
    <h3>✈️ Airline Ticket Management System</h3>
    <a href="https://github.com/muabang123/Plane_Ticket" class="project-link">
      <img src="https://img.shields.io/badge/GitHub-View_Code-181717?style=flat&logo=github" alt="GitHub">
    </a>
  </div>
  <p>A desktop-based management software for airline agencies.</p>
  <ul>
    <li><b>Tech Stack:</b> C# (.NET WinForms), MySQL, iTextSharp.</li>
  </ul>
</div>

<div class="content-card">
  <div class="project-header">
    <h3>👟 Online Shoes Store</h3>
    <a href="https://github.com/muabang123/Shoes_Store" class="project-link">
      <img src="https://img.shields.io/badge/GitHub-View_Code-181717?style=flat&logo=github" alt="GitHub">
    </a>
  </div>
  <p>A dynamic e-commerce web application developed to manage footwear sales.</p>
  <ul>
    <li><b>Tech Stack:</b> JavaScript, PHP, MySQL.</li>
  </ul>
</div>

<div class="content-card">
  <div class="project-header">
    <h3>🍎 Fresh Fruit E-Commerce (Front-end)</h3>
    <a href="https://github.com/muabang123/shop_hoa_qua" class="project-link">
      <img src="https://img.shields.io/badge/GitHub-View_Code-181717?style=flat&logo=github" alt="GitHub">
    </a>
  </div>
  <p>A specialized e-commerce interface designed for a premium fresh fruit boutique. This project prioritizes a high-end visual experience with a modern, product-centric layout. Currently, it focuses on delivering a polished user interface and seamless transitions (Front-end implementation only).</p>
  <ul>
    <li><b>Key Highlights:</b> Fully responsive design across all devices, intuitive UI/UX optimized for product discovery, and smooth CSS animations.</li>
    <li><b>Tech Stack:</b> HTML5, CSS3, JavaScript (Core Front-end).</li>
  </ul>
</div>
---

<p align="center"><i>"Building the future, one line of code at a time."</i></p>

<script>
  // 1. XỬ LÝ CON TRỎ CHUỘT CUSTOM
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

  document.querySelectorAll('a, .content-card').forEach(el => {
    el.addEventListener('mouseenter', () => outline.classList.add('cursor-hover-active'));
    el.addEventListener('mouseleave', () => outline.classList.remove('cursor-hover-active'));
  });

  // 2. XỬ LÝ TYPING (ABOUT ME)
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

  // 3. XỬ LÝ SCROLL REVEAL
  const obs = new IntersectionObserver((entries) => {
    entries.forEach(entry => {
      if (entry.isIntersecting) {
        entry.target.classList.add('is-visible');
        if(entry.target.id === 'about-card') startTyping();
        obs.unobserve(entry.target);
      }
    });
  }, { threshold: 0.15 });

  document.querySelectorAll('.content-card').forEach(c => obs.observe(c));
</script>
