<!-- CSS Animations -->
<style>
  /* Base Animations */
  @keyframes float {
    0%, 100% { transform: translateY(0); }
    50% { transform: translateY(-15px); }
  }
  
  @keyframes pulse {
    0%, 100% { transform: scale(1); opacity: 1; }
    50% { transform: scale(1.05); opacity: 0.8; }
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
  
  @keyframes wave {
    0%, 100% { transform: rotate(0deg); }
    25% { transform: rotate(15deg); }
    75% { transform: rotate(-15deg); }
  }
  
  @keyframes flip-in {
    0% { transform: rotateY(90deg); opacity: 0; }
    100% { transform: rotateY(0deg); opacity: 1; }
  }

  /* Element Classes */
  .pulse { animation: pulse 3s infinite; }
  
  .typing { 
    overflow: hidden;
    white-space: nowrap;
    animation: typing 3.5s steps(40, end), blink-caret 0.75s step-end infinite;
  }
  
  .path-animate { animation: path-animate 2s linear infinite; }
  .wave { display: inline-block; animation: wave 1.5s infinite; }
  
  /* Tech Cards */
  .tech-card {
    width: 100px; height: 100px;
    border-radius: 15px;
    box-shadow: 0 10px 20px rgba(0,0,0,0.2);
    transition: transform 0.6s;
    transform-style: preserve-3d;
    cursor: pointer;
  }
  
  .tech-card:hover { transform: rotateY(180deg); }
  
  .tech-card-inner {
    position: relative;
    width: 100%;
    height: 100%;
    text-align: center;
    transform-style: preserve-3d;
  }
  
  .tech-card-front, .tech-card-back {
    position: absolute;
    width: 100%;
    height: 100%;
    backface-visibility: hidden;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    color: white;
    border-radius: 15px;
    padding: 10px;
  }
  
  .tech-card-back {
    transform: rotateY(180deg);
    background: rgba(0,0,0,0.7);
  }

  /* Contact Buttons */
  .contact-button {
    position: relative;
    padding: 12px 25px;
    color: white;
    text-decoration: none;
    text-transform: uppercase;
    letter-spacing: 1px;
    overflow: hidden;
    border-radius: 5px;
    box-shadow: 0 5px 15px rgba(0,0,0,0.2);
  }
  
  .contact-button span {
    position: absolute;
    display: block;
  }
  
  .contact-button span:nth-child(1) {
    top: 0; left: -100%;
    width: 100%; height: 2px;
    background: linear-gradient(90deg, transparent, var(--color));
    animation: btn-anim1 2s linear infinite;
  }
  
  @keyframes btn-anim1 { 0% { left: -100%; } 50%,100% { left: 100%; } }
  
  .contact-button span:nth-child(2) {
    top: -100%; right: 0;
    width: 2px; height: 100%;
    background: linear-gradient(180deg, transparent, var(--color));
    animation: btn-anim2 2s linear infinite 0.5s;
  }
  
  @keyframes btn-anim2 { 0% { top: -100%; } 50%,100% { top: 100%; } }
  
  .contact-button span:nth-child(3) {
    bottom: 0; right: -100%;
    width: 100%; height: 2px;
    background: linear-gradient(270deg, transparent, var(--color));
    animation: btn-anim3 2s linear infinite 1s;
  }
  
  @keyframes btn-anim3 { 0% { right: -100%; } 50%,100% { right: 100%; } }
  
  .contact-button span:nth-child(4) {
    bottom: -100%; left: 0;
    width: 2px; height: 100%;
    background: linear-gradient(360deg, transparent, var(--color));
    animation: btn-anim4 2s linear infinite 1.5s;
  }
  
  @keyframes btn-anim4 { 0% { bottom: -100%; } 50%,100% { bottom: 100%; } }

  /* Responsive Adjustments */
  @media (max-width: 768px) {
    .tech-card { width: 80px; height: 80px; }
    .contact-button { padding: 10px 20px; font-size: 14px; }
  }
</style>

<!-- Script for Interactive Elements -->
<script>
document.addEventListener('DOMContentLoaded', function() {
  // Animate elements on scroll
  const animateOnScroll = function() {
    const elements = document.querySelectorAll('.fade-in, .slide-in-left');
    elements.forEach(el => {
      const elTop = el.getBoundingClientRect().top;
      if (elTop < window.innerHeight * 0.8) {
        el.style.opacity = '1';
        el.style.transform = 'translate(0)';
      }
    });
  };
  
  document.querySelectorAll('.fade-in').forEach(el => {
    el.style.opacity = '0';
    el.style.transition = 'opacity 0.8s ease, transform 0.8s ease';
  });
  
  document.querySelectorAll('.slide-in-left').forEach(el => {
    el.style.opacity = '0';
    el.style.transform = 'translateX(-50px)';
    el.style.transition = 'opacity 0.8s ease, transform 0.8s ease';
  });
  
  window.addEventListener('scroll', animateOnScroll);
  animateOnScroll(); // Run once on load

  // Stats cards hover effect
  document.querySelectorAll('.stats-card').forEach(card => {
    card.style.transition = 'transform 0.3s ease, box-shadow 0.3s ease';
    card.style.boxShadow = '0 5px 15px rgba(0,0,0,0.1)';
    card.addEventListener('mouseenter', () => {
      card.style.transform = 'translateY(-5px)';
      card.style.boxShadow = '0 10px 25px rgba(0,0,0,0.2)';
    });
    card.addEventListener('mouseleave', () => {
      card.style.transform = 'translateY(0)';
      card.style.boxShadow = '0 5px 15px rgba(0,0,0,0.1)';
    });
  });
});
</script>

<!-- Profile Typing SVG -->
<div align="center">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&pause=1000&color=22D3EE&width=435&lines=Hello%2C+I'm+Matvey+Sviadysh;DevOps+Enthusiast;Problem+Solver" alt="Typing SVG" />
</div>

---

## 🛠️ Tech Stack & Tools

<div align="center">
  <!-- Core Technologies -->
  ![Ruby](https://img.shields.io/badge/-Ruby-CC342D?style=for-the-badge&logo=ruby&logoColor=white)
  ![Python](https://img.shields.io/badge/-Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
  ![React](https://img.shields.io/badge/-React-61DAFB?style=for-the-badge&logo=react&logoColor=black)
  ![Django](https://img.shields.io/badge/-Django-092E20?style=for-the-badge&logo=django&logoColor=white)
</div>















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

