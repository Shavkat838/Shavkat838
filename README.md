<!DOCTYPE html>
<html lang="uz">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>GitHub Profil README</title>
<style>
  * { margin: 0; padding: 0; box-sizing: border-box; }
  body {
    background: #0d1117;
    color: #c9d1d9;
    font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, sans-serif;
    line-height: 1.6;
    padding: 20px;
  }
  .container {
    max-width: 900px;
    margin: 0 auto;
    background: #0d1117;
    border-radius: 12px;
    overflow: hidden;
    box-shadow: 0 0 40px rgba(54, 188, 247, 0.15);
  }


  .header {
    position: relative;
    background: linear-gradient(135deg, #0f2027 0%, #203a43 50%, #2c5364 100%);
    padding: 60px 30px 70px 30px;
    text-align: center;
    overflow: hidden;
    border-radius: 0 0 50% 50% / 0 0 30px 30px;
  }


  .header::before,
  .header::after {
    content: "";
    position: absolute;
    border-radius: 50%;
    filter: blur(60px);
    opacity: 0.5;
    animation: floatCircle 6s ease-in-out infinite;
  }
  .header::before {
    width: 200px; height: 200px;
    background: #36BCF7;
    top: -50px; left: -50px;
  }
  .header::after {
    width: 180px; height: 180px;
    background: #764ba2;
    bottom: -60px; right: -40px;
    animation-delay: 2s;
  }
  @keyframes floatCircle {
    0%, 100% { transform: translate(0, 0) scale(1); }
    50%      { transform: translate(20px, -15px) scale(1.1); }
  }

  .header-content {
    position: relative;
    z-index: 2;
    animation: fadeDown 1.2s ease both;
  }
  @keyframes fadeDown {
    from { opacity: 0; transform: translateY(-20px); }
    to   { opacity: 1; transform: translateY(0); }
  }


  .header-title {
    font-size: 42px;
    font-weight: 800;
    color: #ffffff;
    letter-spacing: 1px;
    margin-bottom: 12px;
    text-shadow: 0 4px 20px rgba(54, 188, 247, 0.6);
  }
  .header-title span {
    background: linear-gradient(90deg, #36BCF7, #a78bfa, #36BCF7);
    background-size: 200% auto;
    -webkit-background-clip: text;
    background-clip: text;
    -webkit-text-fill-color: transparent;
    animation: shine 3s linear infinite;
  }
  @keyframes shine {
    to { background-position: 200% center; }
  }

  .header-subtitle {
    font-size: 18px;
    color: #b6d4e8;
    font-weight: 500;
    letter-spacing: 0.5px;
  }
  .header-line {
    width: 80px;
    height: 4px;
    background: linear-gradient(90deg, #36BCF7, #764ba2);
    margin: 18px auto 0 auto;
    border-radius: 4px;
    animation: growLine 1.5s ease both;
  }
  @keyframes growLine {
    from { width: 0; opacity: 0; }
    to   { width: 80px; opacity: 1; }
  }


  .typing-wrap {
    text-align: center;
    padding: 25px 0 10px 0;
  }
  .typing {
    font-family: "Fira Code", monospace;
    font-size: 22px;
    font-weight: 600;
    color: #36BCF7;
    display: inline-block;
    border-right: 3px solid #36BCF7;
    white-space: nowrap;
    overflow: hidden;
    animation: blink 0.8s step-end infinite;
  }
  @keyframes blink { 50% { border-color: transparent; } }

  .socials {
    text-align: center;
    padding: 15px 0;
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    gap: 10px;
  }
  .socials img {
    height: 32px;
    transition: transform 0.3s ease;
  }
  .socials img:hover {
    transform: translateY(-4px) scale(1.05);
  }


  .section-title {
    max-width: 900px;
    margin: 30px auto 15px auto;
    padding: 10px 20px;
    background: linear-gradient(90deg, #36BCF7, #0f2027);
    border-radius: 8px;
    color: #ffffff;
    font-size: 20px;
    font-weight: 700;
    text-align: center;
    letter-spacing: 0.5px;
    box-shadow: 0 4px 15px rgba(54, 188, 247, 0.25);
    transition: transform 0.3s ease;
  }
  .section-title:hover {
    transform: scale(1.02);
  }

  .code-block {
    background: #161b22;
    border-radius: 10px;
    padding: 20px 25px;
    margin: 15px 25px;
    font-family: "Fira Code", monospace;
    font-size: 14px;
    color: #c9d1d9;
    border: 1px solid #30363d;
    overflow-x: auto;
  }
  .code-block .key { color: #79c0ff; }
  .code-block .str { color: #a5d6ff; }
  .code-block .punc { color: #ff7b72; }


  .tech-grid {
    text-align: center;
    padding: 10px 20px;
  }
  .tech-grid h3 {
    color: #58a6ff;
    margin: 20px 0 12px 0;
    font-size: 18px;
  }
  .tech-grid img {
    height: 30px;
    margin: 5px 4px;
    transition: transform 0.25s ease;
  }
  .tech-grid img:hover {
    transform: translateY(-5px) scale(1.1);
  }

  .stats {
    display: flex;
    justify-content: center;
    flex-wrap: wrap;
    gap: 15px;
    padding: 10px 15px;
  }
  .stats img { max-width: 100%; height: auto; border-radius: 8px; }
  .center { text-align: center; padding: 15px 0; }
  .center img { max-width: 100%; }


  .footer {
    margin-top: 40px;
    background: linear-gradient(135deg, #2c5364 0%, #203a43 50%, #0f2027 100%);
    padding: 40px 20px;
    text-align: center;
    border-radius: 30px 30px 0 0;
  }
  .footer-text {
    color: #ffffff;
    font-size: 18px;
    font-weight: 600;
    letter-spacing: 1px;
    animation: twinkle 2.5s ease-in-out infinite;
  }
  .footer-sub {
    color: #b6d4e8;
    font-size: 13px;
    margin-top: 8px;
  }
  @keyframes twinkle {
    0%, 100% { opacity: 1; text-shadow: 0 0 10px rgba(54,188,247,0.5); }
    50%      { opacity: 0.7; text-shadow: 0 0 20px rgba(54,188,247,0.9); }
  }

  .fade-in { animation: fadeIn 1.2s ease-in both; }
  @keyframes fadeIn {
    from { opacity: 0; transform: translateY(15px); }
    to   { opacity: 1; transform: translateY(0); }
  }

  @media (max-width: 600px) {
    .header-title { font-size: 28px; }
    .header-subtitle { font-size: 15px; }
    .typing { font-size: 16px; }
    .section-title { font-size: 16px; }
  }
</style>
</head>
<body>

<div class="container fade-in">


  <div class="header">
    <div class="header-content">

      <h1 class="header-title">Salom, men <span>Shavkat Boltayev</span> 👋</h1>


      <p class="header-subtitle">Software Engineer | Full-Stack Developer</p>

      <div class="header-line"></div>
    </div>
  </div>


  <div class="typing-wrap">
    <span class="typing" id="typing"></span>
  </div>


  <div class="socials">
    <a href="https://linkedin.com/in/shavkat-boltayev/">
      <img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" />
    </a>
    <a href="https://t.me/shb_1_4">
      <img src="https://img.shields.io/badge/Telegram-26A5E4?style=for-the-badge&logo=telegram&logoColor=white" />
    </a>
    <a href="boltayevshavkat216@gmail.com">
      <img src="https://img.shields.io/badge/Gmail-EA4335?style=for-the-badge&logo=gmail&logoColor=white" />
    </a>
    <a href="https://yourportfolio.com">
      <img src="https://img.shields.io/badge/Portfolio-000000?style=for-the-badge&logo=vercel&logoColor=white" />
    </a>
  </div>


  <div class="section-title">👨‍💻 Men haqimda</div>

  <div class="code-block">
    <span class="key">const</span> developer <span class="punc">=</span> {<br>
    &nbsp;&nbsp;name<span class="punc">:</span> <span class="str">"Ali Valiyev"</span>,<br>
    &nbsp;&nbsp;role<span class="punc">:</span> <span class="str">"Software Engineer"</span>,<br>
    &nbsp;&nbsp;location<span class="punc">:</span> <span class="str">"Uzbekistan 🇺🇿"</span>,<br>
    &nbsp;&nbsp;languages<span class="punc">:</span> [<span class="str">"JavaScript"</span>, <span class="str">"TypeScript"</span>],<br>
    &nbsp;&nbsp;frontend<span class="punc">:</span> [<span class="str">"React.js"</span>, <span class="str">"Next.js"</span>, <span class="str">"TailwindCSS"</span>, <span class="str">"Redux"</span>],<br>
    &nbsp;&nbsp;backend<span class="punc">:</span> [<span class="str">"Node.js"</span>, <span class="str">"Express.js"</span>, <span class="str">"NestJS"</span>, <span class="str">"MongoDB"</span>, <span class="str">"PostgreSQL"</span>],<br>
    &nbsp;&nbsp;tools<span class="punc">:</span> [<span class="str">"Git"</span>, <span class="str">"Docker"</span>, <span class="str">"VS Code"</span>, <span class="str">"Figma"</span>, <span class="str">"Postman"</span>],<br>
    &nbsp;&nbsp;focus<span class="punc">:</span> <span class="str">"Clean Architecture & Scalable Web Apps"</span>,<br>
    &nbsp;&nbsp;hobbies<span class="punc">:</span> [<span class="str">"Open Source"</span>, <span class="str">"Coding"</span>, <span class="str">"Learning 🚀"</span>]<br>
    };
  </div>

  <div class="section-title">🛠️ Texnologiyalar</div>

  <div class="tech-grid">
    <h3>🎨 Frontend</h3>
    <img src="https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB" />
    <img src="https://img.shields.io/badge/Next.js-000000?style=for-the-badge&logo=nextdotjs&logoColor=white" />
    <img src="https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white" />
    <img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black" />
    <img src="https://img.shields.io/badge/Tailwind_CSS-06B6D4?style=for-the-badge&logo=tailwindcss&logoColor=white" />
    <img src="https://img.shields.io/badge/Redux-764ABC?style=for-the-badge&logo=redux&logoColor=white" />

    <h3>⚙️ Backend</h3>
    <img src="https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=nodedotjs&logoColor=white" />
    <img src="https://img.shields.io/badge/Express-000000?style=for-the-badge&logo=express&logoColor=white" />
    <img src="https://img.shields.io/badge/NestJS-E0234E?style=for-the-badge&logo=nestjs&logoColor=white" />
    <img src="https://img.shields.io/badge/MongoDB-47A248?style=for-the-badge&logo=mongodb&logoColor=white" />
    <img src="https://img.shields.io/badge/PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white" />
    <img src="https://img.shields.io/badge/Prisma-2D3748?style=for-the-badge&logo=prisma&logoColor=white" />

    <h3>🚀 Tools & DevOps</h3>
    <img src="https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white" />
    <img src="https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white" />
    <img src="https://img.shields.io/badge/Vercel-000000?style=for-the-badge&logo=vercel&logoColor=white" />
    <img src="https://img.shields.io/badge/Figma-F24E1E?style=for-the-badge&logo=figma&logoColor=white" />
  </div>


  <div class="section-title">📊 GitHub Statistikam</div>

  <div class="stats">
    <img src="https://github-readme-stats.vercel.app/api?username=USERNAME&show_icons=true&theme=tokyonight&hide_border=true&bg_color=0d1117&title_color=36BCF7&icon_color=36BCF7&text_color=c9d1d9" />
    <img src="https://github-readme-streak-stats.herokuapp.com/?user=USERNAME&theme=tokyonight&hide_border=true&background=0d1117&stroke=36BCF7&ring=36BCF7&fire=36BCF7&currStreakLabel=36BCF7" />
  </div>

  <div class="center">
    <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=USERNAME&layout=compact&theme=tokyonight&hide_border=true&bg_color=0d1117&title_color=36BCF7&text_color=c9d1d9" />
  </div>

  <div class="center">
    <img src="https://github-profile-trophy.vercel.app/?username=USERNAME&theme=tokyonight&no-frame=true&no-bg=true&row=1&column=6" />
  </div>

  <div class="center">
    <img src="https://raw.githubusercontent.com/USERNAME/USERNAME/output/github-contribution-grid-snake-dark.svg" />
  </div>

  <div class="footer">
    <p class="footer-text">✨ Tashrifingiz uchun rahmat! ✨</p>
  </div>

</div>

<script>

  const lines = [
    "Software Engineer 💻",
    "React.js | Next.js | Node.js",
    "Clean Code | Scalable Apps",
    "Always Learning New Things 🚀"
  ];
  let lineIdx = 0, charIdx = 0, deleting = false;
  const el = document.getElementById("typing");

  function type() {
    const current = lines[lineIdx];
    if (!deleting) {
      el.textContent = current.substring(0, charIdx++);
      if (charIdx > current.length) {
        deleting = true;
        setTimeout(type, 1500);
        return;
      }
    } else {
      el.textContent = current.substring(0, charIdx--);
      if (charIdx < 0) {
        deleting = false;
        lineIdx = (lineIdx + 1) % lines.length;
      }
    }
    setTimeout(type, deleting ? 40 : 90);
  }
  type();
</script>

</body>
</html>
