<div align="center">
  <!-- Анимированный заголовок с эффектом печати и 3D текстом -->
  <svg width="100%" height="120" viewBox="0 0 800 120">
    <defs>
      <linearGradient id="titleGradient" x1="0%" y1="0%" x2="100%" y2="0%">
        <stop offset="0%" stop-color="#22D3EE"/>
        <stop offset="100%" stop-color="#3B82F6"/>
      </linearGradient>
      <filter id="3dEffect" height="130%">
        <feGaussianBlur in="SourceAlpha" stdDeviation="4" result="blur"/>
        <feOffset in="blur" dx="4" dy="4" result="offsetBlur"/>
        <feComposite in="SourceGraphic" in2="offsetBlur" operator="over"/>
      </filter>
    </defs>
    
    <text x="50%" y="50%" font-family="Arial" font-size="50" font-weight="bold" 
          text-anchor="middle" fill="url(#titleGradient)" filter="url(#3dEffect)">
      Matvey Sviadysh
    </text>
    <text x="50%" y="80%" font-family="Arial" font-size="20" text-anchor="middle" 
          fill="#22D3EE" class="typing-text">
      DevOps Engineer | Cloud Architect
    </text>
  </svg>

  <!-- Плавающие 3D кубики -->
  <div style="display: flex; justify-content: center; gap: 20px; margin: 30px 0;">
    <div class="floating-cube" style="--color: #FF9900; animation-delay: 0s;">
      <div class="cube-face front">AWS</div>
      <div class="cube-face back">EC2/S3</div>
      <div class="cube-face right">Lambda</div>
      <div class="cube-face left">RDS</div>
      <div class="cube-face top">EKS</div>
      <div class="cube-face bottom">IAM</div>
    </div>
    
    <div class="floating-cube" style="--color: #2496ED; animation-delay: 0.2s;">
      <div class="cube-face front">Docker</div>
      <div class="cube-face back">Swarm</div>
      <div class="cube-face right">Compose</div>
      <div class="cube-face left">Hub</div>
      <div class="cube-face top">Images</div>
      <div class="cube-face bottom">Volumes</div>
    </div>
    
    <div class="floating-cube" style="--color: #326CE5; animation-delay: 0.4s;">
      <div class="cube-face front">K8s</div>
      <div class="cube-face back">Helm</div>
      <div class="cube-face right">CRDs</div>
      <div class="cube-face left">Operators</div>
      <div class="cube-face top">Pods</div>
      <div class="cube-face bottom">Services</div>
    </div>
  </div>
</div>

<!-- Анимированный разделитель -->
<div align="center">
  <svg width="80%" height="40">
    <path d="M0,20 Q400,40 800,20" stroke="#22D3EE" stroke-width="2" fill="none" 
          stroke-dasharray="10,5" class="path-animate"/>
  </svg>
</div>

## 🧩 Tech Stack Cubes

<div class="cube-container">
  <div class="tech-cube">
    <div class="cube-face front" style="background: #CC342D;">
      <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/ruby/ruby-original.svg" width="40"/>
      <span>Ruby</span>
    </div>
    <div class="cube-face back" style="background: #A62D27;">Rails</div>
    <div class="cube-face right" style="background: #B2302A;">Sinatra</div>
    <div class="cube-face left" style="background: #8D2823;">Gems</div>
    <div class="cube-face top" style="background: #D13831;">RSpec</div>
    <div class="cube-face bottom" style="background: #E73C35;">JRuby</div>
  </div>
  
  <div class="tech-cube">
    <div class="cube-face front" style="background: #3776AB;">
      <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/python/python-original.svg" width="40"/>
      <span>Python</span>
    </div>
    <div class="cube-face back" style="background: #2D5F8A;">Django</div>
    <div class="cube-face right" style="background: #326B9C;">Flask</div>
    <div class="cube-face left" style="background: #23527B;">Pandas</div>
    <div class="cube-face top" style="background: #3C82BA;">NumPy</div>
    <div class="cube-face bottom" style="background: #4193D1;">FastAPI</div>
  </div>
  
  <div class="tech-cube">
    <div class="cube-face front" style="background: #61DAFB;">
      <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/react/react-original.svg" width="40"/>
      <span>React</span>
    </div>
    <div class="cube-face back" style="background: #4FC3F7;">Redux</div>
    <div class="cube-face right" style="background: #56D5FA;">Hooks</div>
    <div class="cube-face left" style="background: #4AC8F5;">Router</div>
    <div class="cube-face top" style="background: #6BE0FD;">Context</div>
    <div class="cube-face bottom" style="background: #7FE7FF;">Next.js</div>
  </div>
</div>

## 🚀 DevOps Galaxy

<div class="galaxy-container">
  <div class="orbiting-tech">
    <div class="center-tech">CI/CD</div>
    <div class="orbit" style="--i:1;">
      <div class="tech-item" style="--j:1;">Jenkins</div>
    </div>
    <div class="orbit" style="--i:2;">
      <div class="tech-item" style="--j:2;">GitLab</div>
    </div>
    <div class="orbit" style="--i:3;">
      <div class="tech-item" style="--j:3;">GitHub Actions</div>
    </div>
    <div class="orbit" style="--i:4;">
      <div class="tech-item" style="--j:4;">ArgoCD</div>
    </div>
  </div>
</div>

<style>
  /* Основные анимации */
  @keyframes float {
    0%, 100% { transform: translateY(0) rotate(0deg); }
    50% { transform: translateY(-20px) rotate(5deg); }
  }
  
  @keyframes typing {
    from { width: 0; }
    to { width: 100%; }
  }
  
  @keyframes blink-caret {
    from, to { border-color: transparent; }
    50% { border-color: #22D3EE; }
  }
  
  @keyframes path-animate {
    from { stroke-dashoffset: 100; }
    to { stroke-dashoffset: 0; }
  }
  
  @keyframes rotate-cube {
    from { transform: rotateX(0) rotateY(0); }
    to { transform: rotateX(360deg) rotateY(360deg); }
  }
  
  @keyframes orbit {
    from { transform: rotate(0deg); }
    to { transform: rotate(360deg); }
  }
  
  /* Стили для элементов */
  .typing-text {
    overflow: hidden;
    white-space: nowrap;
    animation: typing 3.5s steps(40, end), blink-caret 0.75s step-end infinite;
  }
  
  .path-animate {
    animation: path-animate 3s linear infinite;
  }
  
  /* 3D Кубики технологий */
  .cube-container {
    display: flex;
    justify-content: center;
    gap: 40px;
    flex-wrap: wrap;
    perspective: 1000px;
    margin: 40px 0;
  }
  
  .tech-cube, .floating-cube {
    width: 120px;
    height: 120px;
    position: relative;
    transform-style: preserve-3d;
    animation: rotate-cube 20s infinite linear;
    transition: transform 0.5s;
  }
  
  .floating-cube {
    animation: float 6s ease-in-out infinite, rotate-cube 25s infinite linear;
  }
  
  .cube-face {
    position: absolute;
    width: 100%;
    height: 100%;
    border: 2px solid white;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    font-weight: bold;
    color: white;
    opacity: 0.9;
    background: var(--color);
    box-shadow: 0 0 15px rgba(0,0,0,0.3);
  }
  
  .tech-cube:hover, .floating-cube:hover {
    animation-play-state: paused;
    transform: scale(1.1);
  }
  
  /* Позиционирование граней куба */
  .front  { transform: rotateY(0deg) translateZ(60px); }
  .back   { transform: rotateY(180deg) translateZ(60px); }
  .right  { transform: rotateY(90deg) translateZ(60px); }
  .left   { transform: rotateY(-90deg) translateZ(60px); }
  .top    { transform: rotateX(90deg) translateZ(60px); }
  .bottom { transform: rotateX(-90deg) translateZ(60px); }
  
  /* Галактика технологий */
  .galaxy-container {
    display: flex;
    justify-content: center;
    margin: 60px 0;
  }
  
  .orbiting-tech {
    position: relative;
    width: 300px;
    height: 300px;
    border-radius: 50%;
  }
  
  .center-tech {
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    width: 80px;
    height: 80px;
    background: linear-gradient(135deg, #3B82F6, #22D3EE);
    border-radius: 50%;
    display: flex;
    align-items: center;
    justify-content: center;
    color: white;
    font-weight: bold;
    box-shadow: 0 0 20px #22D3EE;
    z-index: 10;
  }
  
  .orbit {
    position: absolute;
    width: 100%;
    height: 100%;
    border: 1px dashed rgba(59, 130, 246, 0.3);
    border-radius: 50%;
    animation: orbit calc(10s * var(--i)) linear infinite;
  }
  
  .tech-item {
    position: absolute;
    left: calc(50% - 40px);
    top: -15px;
    width: 80px;
    height: 30px;
    background: linear-gradient(135deg, #3B82F6, #22D3EE);
    border-radius: 15px;
    display: flex;
    align-items: center;
    justify-content: center;
    color: white;
    font-size: 12px;
    font-weight: bold;
    transform-origin: center calc(150px - (var(--i) * 20px));
    box-shadow: 0 0 10px rgba(59, 130, 246, 0.5);
  }
  
  /* Адаптивность */
  @media (max-width: 768px) {
    .tech-cube, .floating-cube {
      width: 80px;
      height: 80px;
    }
    .cube-face {
      font-size: 12px;
    }
    .galaxy-container {
      transform: scale(0.7);
    }
  }
</style>

<script>
  // Интерактивность для кубов
  document.addEventListener('DOMContentLoaded', function() {
    const cubes = document.querySelectorAll('.tech-cube, .floating-cube');
    
    cubes.forEach(cube => {
      cube.addEventListener('mouseenter', () => {
        cube.style.animationPlayState = 'paused';
      });
      
      cube.addEventListener('mouseleave', () => {
        cube.style.animationPlayState = 'running';
      });
    });
    
    // Параллакс эффект для галактики
    const galaxy = document.querySelector('.galaxy-container');
    if (galaxy) {
      document.addEventListener('mousemove', (e) => {
        const x = e.clientX / window.innerWidth;
        const y = e.clientY / window.innerHeight;
        galaxy.style.transform = `perspective(1000px) rotateX(${y * 20}deg) rotateY(${x * 20}deg)`;
      });
    }
  });
</script>












<div align="center">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&pause=1000&color=22D3EE&width=435&lines=Hello%2C+I'm+Matvey+Sviadysh;DevOps+Enthusiast;Problem+Solver" alt="Typing SVG" />
</div>

---

## 🛠️ Tech Stack & Tools

<div align="center">
  
### 🔥 Core Technologies
![Ruby](https://img.shields.io/badge/-Ruby-CC342D?style=for-the-badge&logo=ruby&logoColor=white)
![Python](https://img.shields.io/badge/-Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![React](https://img.shields.io/badge/-React-61DAFB?style=for-the-badge&logo=react&logoColor=black)
![Django](https://img.shields.io/badge/-Django-092E20?style=for-the-badge&logo=django&logoColor=white)

### 🚀 DevOps & Cloud
![AWS](https://img.shields.io/badge/AWS-%23FF9900.svg?style=for-the-badge&logo=amazon-aws&logoColor=white)
![Docker](https://img.shields.io/badge/-Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![Kubernetes](https://img.shields.io/badge/-Kubernetes-326CE5?style=for-the-badge&logo=kubernetes&logoColor=white)
![Jenkins](https://img.shields.io/badge/-Jenkins-D24939?style=for-the-badge&logo=jenkins&logoColor=white)

### 🗃️ Databases
![Redis](https://img.shields.io/badge/-Redis-DC382D?style=for-the-badge&logo=redis&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/-PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white)

</div>

---

## 📈 Coding Activity

<div align="center">
  
### 🏆 CodeWars
[![Codewars](https://www.codewars.com/users/MatveySviadysh/badges/large)](https://www.codewars.com/users/MatveySviadysh)

### 🧠 LeetCode
[![LeetCode Stats](https://leetcard.jacoblin.cool/MavteySviadysh?theme=dark&font=baloo_thambi&ext=activity)](https://leetcode.com/u/MavteySviadysh/)

</div>

---

## 📊 GitHub Stats

<div align="center">
  
![Profile Details](https://github-profile-summary-cards.vercel.app/api/cards/profile-details?username=MatveySviadysh&theme=github_dark)

![Top Languages](https://github-readme-stats.vercel.app/api/top-langs/?username=MatveySviadysh&layout=compact&theme=vision-friendly-dark&hide_border=true)


</div>

---

## 🌐 Connect With Me

<div align="center">
  
[![Telegram](https://img.shields.io/badge/-Telegram-26A5E4?style=for-the-badge&logo=telegram&logoColor=white)](https://t.me/MatveiSviadysh)
[![LinkedIn](https://img.shields.io/badge/-LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/matvey-sviadysh-a59947373/)
[![Email](https://img.shields.io/badge/-Email-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:your.email@example.com)

</div>

