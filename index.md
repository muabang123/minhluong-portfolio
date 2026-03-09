<style>
  /* 1. Font chữ & Hiệu ứng Typing Quý tộc */
  @import url('https://fonts.googleapis.com/css2?family=Playfair+Display:ital,wght@1,400;1,700&display=swap');

  .aristocratic-text {
    font-family: 'Playfair Display', serif;
    font-style: italic;
    font-size: 1.15rem;
    line-height: 1.6;
    color: #2c3e50;
    min-height: 80px;
  }

  .cursor {
    display: inline-block;
    width: 2px;
    background-color: #0366d6;
    margin-left: 3px;
    animation: blink 0.7s infinite;
  }

  @keyframes blink {
    0%, 100% { opacity: 1; }
    50% { opacity: 0; }
  }

  /* 2. CSS cho Project Cards với hiệu ứng ẩn ban đầu */
  .content-card {
    border: 1px solid #e1e4e8;
    border-radius: 8px;
    padding: 20px;
    margin-bottom: 25px;
    background-color: #ffffff;
    
    /* Trạng thái ẩn để chuẩn bị animation */
    opacity: 0;
    transform: translateY(40px);
    transition: all 0.8s cubic-bezier(0.25, 0.46, 0.45, 0.94); /* Mượt hơn ease-out */
  }

  /* Trạng thái hiện ra khi cuộn đến */
  .content-card.is-visible {
    opacity: 1;
    transform: translateY(0);
  }

  .content-card:hover {
    transform: translateY(-5px);
    box-shadow: 0 10px 20px rgba(0,0,0,0.1);
    border-color: #b8860b; /* Viền vàng gold nhẹ khi hover */
  }

  .project-header {
    display: flex;
    justify-content: space-between;
    align-items: center;
  }

  .project-link {
    display: flex;
    align-items: center;
    gap: 5px;
    text-decoration: none;
    font-weight: bold;
    color: #0366d6;
  }

  .skill-badge { margin: 2px; }
</style>

# 👋 Welcome to My Portfolio

---

<div class="content-card" id="about-card">
  <h2>👨‍💻 About Me</h2>
  <div class="aristocratic-text">
    <span id="typing-destination"></span><span id="cursor-element" class="cursor">&nbsp;</span>
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
  <p>A comprehensive real-time tracking application designed for school buses. It provides live location monitoring to ensure student safety and efficient fleet management.</p>
  <ul>
    <li><b>Core Features:</b> Real-time GPS tracking, Socket.IO integration.</li>
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
  <p>A desktop-based management software for airline agencies. It streamlines the ticket sales process and handles complex data management.</p>
  <ul>
    <li><b>Core Features:</b> Multiple ticket classes, filtering, and automated PDF receipt generation.</li>
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
    <li><b>Core Features:</b> Product catalog, shopping cart, user authentication.</li>
    <li><b>Tech Stack:</b> JavaScript, HTML, CSS, PHP, MySQL.</li>
  </ul>
</div>

<div class="content-card">
  <div class="project-header">
    <h3>📺 YouTube Lite</h3>
    <a href="https://github.com/muabang123/Youtube_Web" class="project-link">
      <img src="https://img.shields.io/badge/GitHub-View_Code-181717?style=flat&logo=github" alt="GitHub">
    </a>
  </div>
  <p>A lightweight video streaming platform that allows users to upload and play videos efficiently.</p>
  <ul>
    <li><b>Core Features:</b> Dual-storage architecture, user-friendly interface.</li>
    <li><b>Tech Stack:</b> Python, Flask, MySQL.</li>
  </ul>
</div>

---

<p align="center"><i>"Building the future, one line of code at a time."</i></p>

<script>
  // 1. Script cho Typing (About Me)
  const textToType = "I am a dedicated 3rd-year Software Engineering student at Saigon University (SGU) with a strong passion for building scalable and efficient applications. Currently, I am focusing on mastering both Front-end and Back-end development to become a versatile Full-stack Developer.";
  const destination = document.getElementById("typing-destination");
  const cursor = document.getElementById("cursor-element");
  let i = 0;

  function typeWriter() {
    if (i < textToType.length) {
      destination.innerHTML += textToType.charAt(i);
      i++;
      setTimeout(typeWriter, 25);
    } else {
      cursor.style.display = "none";
    }
  }

  // 2. Script cho Scroll Reveal (Từng dự án hiện ra khi cuộn)
  const observerOptions = {
    threshold: 0.15 // Hiện ra khi card lộ diện 15% diện tích
  };

  const observer = new IntersectionObserver((entries) => {
    entries.forEach(entry => {
      if (entry.isIntersecting) {
        entry.target.classList.add('is-visible');
        // Sau khi đã hiện rồi thì ngừng quan sát để tối ưu hiệu năng
        observer.unobserve(entry.target);
        
        // Nếu là About Me Card thì mới chạy Typing script
        if(entry.target.id === 'about-card') {
           typeWriter();
        }
      }
    });
  }, observerOptions);

  // Áp dụng quan sát cho tất cả các .content-card
  document.querySelectorAll('.content-card').forEach(card => {
    observer.observe(card);
  });
</script>
