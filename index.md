<style>
  /* Import font chữ phong cách cổ điển/quý tộc */
  @import url('https://fonts.googleapis.com/css2?family=Playfair+Display:ital,wght@1,400;1,700&display=swap');

  .aristocratic-text {
    font-family: 'Playfair Display', serif;
    font-style: italic;
    font-size: 1.15rem;
    line-height: 1.6;
    color: #2c3e50;
    min-height: 120px; /* Tránh giật khung khi xóa chữ */
  }

  /* Hiệu ứng con trỏ nhấp nháy */
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

  .highlight-gold {
    color: #b8860b; /* Màu vàng đồng quý tộc */
    font-weight: 700;
  }
</style>

<div class="content-card">
  <h2>👨‍💻 About Me</h2>
  <div class="aristocratic-text">
    <span id="typing-destination"></span><span class="cursor">&nbsp;</span>
  </div>

  <script>
    const textToType = "I am a dedicated 3rd-year Software Engineering student at Saigon University (SGU) with a strong passion for building scalable and efficient applications. Currently, I am focusing on mastering both Front-end and Back-end development to become a versatile Full-stack Developer.";
    const destination = document.getElementById("typing-destination");
    
    let i = 0;
    const speed = 25; // Tốc độ đánh máy (ms) - Đã chỉnh nhanh để nhà tuyển dụng dễ đọc
    const stayTime = 3000; // Thời gian dừng sau khi hoàn thành (3 giây)

    function typeWriter() {
      if (i < textToType.length) {
        destination.innerHTML += textToType.charAt(i);
        i++;
        setTimeout(typeWriter, speed);
      } else {
        cursor.style.display = "none";
      }
    }

    // Khởi chạy animation
    typeWriter();
  </script>

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
    <li><b>Core Features:</b> Real-time GPS tracking, Socket.IO integration, and a dynamic dashboard for administrators.</li>
    <li><b>Tech Stack:</b> React, Node.js, MySQL, Socket.IO, Redis, and Google Maps API.</li>
  </ul>
</div>

<div class="content-card">
  <div class="project-header">
    <h3>✈️ Airline Ticket Management System</h3>
    <a href="https://github.com/muabang123/Plane_Ticket" class="project-link">
      <img src="https://img.shields.io/badge/GitHub-View_Code-181717?style=flat&logo=github" alt="GitHub">
    </a>
  </div>
  <p>A desktop-based management software for airline agencies. It streamlines the ticket sales process and handles complex data management for various flight classes.</p>
  <ul>
    <li><b>Core Features:</b> Supports multiple ticket classes (Economy, Premium, Business, First Class). Includes ticket searching, filtering, and automated PDF receipt generation using iTextSharp.</li>
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
  <p>A dynamic e-commerce web application developed to manage footwear sales, providing a seamless shopping experience from product selection to checkout.</p>
  <ul>
    <li><b>Core Features:</b> Responsive product catalog, integrated shopping cart system, user authentication, and administrative inventory management.</li>
    <li><b>Tech Stack:</b> JavaScript , HTML , CSS , PHP , and MySQL.</li>
  </ul>
</div>

<div class="content-card">
  <div class="project-header">
    <h3>📺 YouTube Lite</h3>
    <a href="https://github.com/muabang123/Youtube_Web" class="project-link">
      <img src="https://img.shields.io/badge/GitHub-View_Code-181717?style=flat&logo=github" alt="GitHub">
    </a>
  </div>
  <p>A lightweight video streaming platform that allows users to upload, store, and play videos efficiently.</p>
  <ul>
    <li><b>Core Features:</b> Dual-storage architecture for storing video files both on a local server and metadata in a database. User-friendly interface for browsing content.</li>
    <li><b>Tech Stack:</b> Python, Flask, MySQL.</li>
  </ul>
</div>

---

<p align="center"><i>"Building the future, one line of code at a time."</i></p>
