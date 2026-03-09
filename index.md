<style>
  /* 1. FIX LỖI CURSOR: Phủ kín toàn bộ màn hình kể cả khoảng trắng */
  html, body {
    cursor: none !important;
    min-height: 100vh; /* Ép trang luôn cao ít nhất bằng màn hình */
    margin: 0;
    padding: 0;
  }

  /* Ẩn chuột trên tất cả các thành phần tương tác */
  a, button, .content-card, .project-link, img {
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
    z-index: 10000;
    transform: translate(-50%, -50%);
  }

  #cursor-outline {
    width: 30px;
    height: 30px;
    border: 2px solid rgba(184, 134, 11, 0.5);
    border-radius: 50%;
    position: fixed;
    pointer-events: none;
    z-index: 9999;
    transform: translate(-50%, -50%);
    transition: width 0.3s, height 0.3s, background-color 0.3s, border-color 0.3s;
  }

  .cursor-hover-active {
    width: 50px !important;
    height: 50px !important;
    background-color: rgba(184, 134, 11, 0.1);
    border-color: #b8860b !important;
  }

  /* 3. FIX LỖI LOGO & BADGE (Tránh bị phóng to 898 như hình cũ) */
  header img[src*="logo"] {
    border-radius: 50% !important;
    width: 120px !important;
    height: 120px !important;
    object-fit: cover !important;
    display: block !important;
    margin: 0 auto 15px auto !important;
  }

  .skill-badge, p align="center" img {
    width: auto !important;
    height: 20px !important; /* Độ cao chuẩn cho các Badge Shields.io */
    border-radius: 0 !important;
    margin: 2px !important;
  }

  /* 4. PHONG CÁCH QUÝ TỘC & TYPING */
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

  @keyframes blink { 50% { opacity: 0; } }

  /* 5. ANIMATION CUỘN TRANG (SCROLL REVEAL) */
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
    <img src="https://img.shields.io/badge/GitHub-181717?style=flat-square&logo=github&logoColor=white" />
    <img src="https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white" />
    <img src="https://img.shields.io/badge/SQL-CC2927?style=flat-square&logo=postgresql&logoColor=white" />
    <img src="https://img.shields.io/badge/VS_Code-007ACC?style=flat-square&logo=visual-studio-code&logoColor=white" />
    <img src="https://img.shields.io/badge/Android_Studio-3DDC84?style=flat-square&logo=android-studio&logoColor=white" />
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
  <p>A comprehensive real-time tracking application for school buses using Node.js and Socket.IO.</p>
</div>

<div class="content-card">
  <div class="project-header">
    <h3>✈️ Airline Ticket Management System</h3>
    <a href="https://github.com/muabang123/Plane_Ticket" class="project-link">
      <img src="https://img.shields.io/badge/GitHub-View_Code-181717?style=flat&logo=github" alt="GitHub">
    </a>
  </div>
  <p>A desktop-based management software for airline agencies developed with C# WinForms.</p>
</div>

---

<p align="center"><i>"Building the future, one line of code at a time."</i></p>

<script>
  const dot = document.getElementById("cursor-dot");
  const outline = document.getElementById("cursor-outline");

  // 1. Cập nhật vị trí chuột cho toàn bộ màn hình
  window.addEventListener("mousemove", (e) => {
    dot.style.left = e.clientX + "px";
    dot.style.top = e.clientY + "px";
    
    outline.animate({
      left: e.clientX + "px",
      top: e.clientY + "px"
    }, { duration: 400, fill: "forwards" });
  });

  // Hiệu ứng hover
  document.querySelectorAll('a, .content-card, button').forEach(el => {
    el.addEventListener('mouseenter', () => outline.classList.add('cursor-hover-active'));
    el.addEventListener('mouseleave', () => outline.classList.remove('cursor-hover-active'));
  });

  // 2. TYPING ANIMATION (CHỈ CHẠY 1 LẦN)
  const text = "I am a dedicated 3rd-year Software Engineering student at Saigon University (SGU) with a strong passion for building scalable and efficient applications. Currently, I am focusing on mastering both Front-end and Back-end development to become a versatile Full-stack Developer.";
  const dest = document.getElementById("typing-destination");
  const curEl = document.getElementById("typing-cursor-el");
  let idx = 0;

  function type() {
    if (idx < text.length) {
      dest.innerHTML += text.charAt(idx);
      idx++;
      setTimeout(type, 25);
    } else {
      curEl.style.display = "none";
    }
  }

  // 3. SCROLL REVEAL & TYPING TRIGGER
  const observer = new IntersectionObserver((entries) => {
    entries.forEach(entry => {
      if (entry.isIntersecting) {
        entry.target.classList.add('is-visible');
        if(entry.target.id === 'about-card') type();
        observer.unobserve(entry.target);
      }
    });
  }, { threshold: 0.15 });

  document.querySelectorAll('.content-card').forEach(c => observer.observe(c));
</script>
