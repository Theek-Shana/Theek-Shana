<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>Theekshana Vidushan — Futuristic Portfolio</title>
  <meta name="description" content="Futuristic neon portfolio / README-style single-file site for Theekshana Vidushan" />

  <!-- Google Font -->
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;800&family=Fira+Code:wght@400;700&display=swap" rel="stylesheet">

  <!-- Simple reset + styles -->
  <style>
    :root{
      --bg:#05060a; /* deep black */
      --panel: rgba(8,10,16,0.6);
      --accent: #00f7ff; /* neon cyan */
      --accent-2: #00d1ff;
      --muted:#9aa5b1;
      --glass: rgba(255,255,255,0.03);
    }
    *{box-sizing:border-box}
    html,body{height:100%;margin:0;font-family:Inter,system-ui,Arial; background: radial-gradient(1200px 800px at 10% 10%, rgba(0,247,255,0.03), transparent), linear-gradient(180deg,#03040a 0%, #07090f 60%); color:#e6edef}
    a{color:var(--accent);text-decoration:none}
    .container{max-width:1100px;margin:32px auto;padding:28px}

    /* Header */
    header{display:flex;gap:20px;align-items:center}
    .avatar{width:120px;height:120px;border-radius:14px;overflow:hidden;border:2px solid rgba(0,247,255,0.12);box-shadow:0 8px 30px rgba(0,247,255,0.06);}
    .avatar img{width:100%;height:100%;object-fit:cover}
    .title h1{margin:0;font-size:28px;letter-spacing:0.6px;color:var(--accent);text-shadow:0 0 12px rgba(0,247,255,0.18)}
    .title p{margin:6px 0 0;color:var(--muted)}

    /* neon box */
    .neon-box{background:linear-gradient(180deg, rgba(255,255,255,0.02), rgba(255,255,255,0.01));border-radius:12px;padding:18px;border:1px solid rgba(0,247,255,0.06);box-shadow:0 6px 40px rgba(0,247,255,0.03) inset, 0 6px 30px rgba(0,0,0,0.6)}

    /* layout */
    .grid{display:grid;grid-template-columns:1fr 320px;gap:22px;margin-top:22px}
    .full{grid-column:1/-1}

    /* About */
    .about{display:flex;gap:18px}
    .about .left{flex:1}
    .about .right{width:300px}
    .typing-svg{display:block}

    /* badges */
    .badges img{margin:6px 6px 6px 0;border-radius:8px}

    /* sections */
    section{margin-bottom:16px}
    h2{color:var(--accent);margin:6px 0 12px;font-size:18px}
    ul{margin:0;padding-left:18px;color:var(--muted)}

    /* GitHub stats area */
    .stats{display:flex;gap:12px;align-items:center}
    .stats img{border-radius:10px}

    /* footer */
    footer{margin-top:28px;padding:16px;border-radius:10px;background:linear-gradient(90deg, rgba(0,0,0,0.25), rgba(255,255,255,0.01));display:flex;justify-content:space-between;align-items:center}

    /* small interactive elements */
    .btn{display:inline-block;padding:8px 12px;border-radius:8px;background:linear-gradient(90deg,var(--accent),var(--accent-2));color:#021017;font-weight:600;box-shadow:0 6px 18px rgba(0,215,255,0.08);}

    /* Particle canvas */
    #bg-canvas{position:fixed;left:0;top:0;width:100%;height:100%;z-index:0;pointer-events:none}

    /* responsive */
    @media (max-width:980px){.grid{grid-template-columns:1fr}.about .right{display:none}.container{padding:18px}}

    /* small neon accent lines */
    .accent-line{height:4px;border-radius:8px;background:linear-gradient(90deg,var(--accent),#00a8ff);box-shadow:0 6px 18px rgba(0,167,255,0.06)}

    /* footer capsule */
    .capsule{padding:8px 12px;border-radius:999px;background:linear-gradient(90deg, rgba(0,247,255,0.08), rgba(0,160,255,0.04));border:1px solid rgba(0,247,255,0.06)}

    /* code like panel */
    pre{background:rgba(0,0,0,0.25);padding:12px;border-radius:8px;color:#bfefff;overflow:auto}

    /* hover subtle */
    .neon-box:hover{transform:translateY(-6px);transition:all .3s}

  </style>
</head>
<body>
  <canvas id="bg-canvas"></canvas>

  <div class="container" style="position:relative;z-index:2">

    <header class="neon-box" style="display:flex;align-items:center;gap:18px">
      <div class="avatar"><img src="https://user-images.githubusercontent.com/74038190/212749447-bfb7e725-6987-49d9-ae85-2015e3e7cc41.gif" alt="Shana GIF"/></div>
      <div class="title">
        <h1>&lt;img src=\"https://raw.githubusercontent.com/ABSphreak/ABSphreak/master/gifs/Hi.gif\" width=\"30px\"/&gt; Hello, I'm <strong style="color:var(--accent)">Theekshana Vidushan</strong>!</h1>
        <p>Final year Software Engineering Student @ ICBT Campus · Graphic Designer · Aspiring Full-Stack Dev</p>
        <div style="margin-top:8px;display:flex;gap:8px;align-items:center">
          <a class="btn" href="#contact">Contact</a>
          <a class="btn" href="#portfolio" style="background:transparent;border:1px solid rgba(0,247,255,0.06);color:var(--accent)">Portfolio</a>
        </div>
      </div>
    </header>

    <div class="grid">
      <main>
        <section class="neon-box about">
          <div class="left">
            <img class="typing-svg" src="https://readme-typing-svg.herokuapp.com?font=Fira+Code&weight=600&size=22&duration=3500&pause=1000&color=00F7FF&vCenter=true&width=500&lines=%F0%9F%9A%80+Passionate+Software+Engineering+Student; %F0%9F%8E%A8+Creative+Graphic+Designer; %F0%9F%92%BB+Aspiring+Full-Stack+Developer; %F0%9F%94%A5+Always+Learning+and+Building" alt="typing" />

            <h2>👨‍💻 About Me</h2>
            <ul>
              <li>🌱 Final year, <strong>Software Engineering Student @ ICBT Campus</strong></li>
              <li>🖥️ Love building <strong>web apps, creative projects, and software solutions</strong></li>
              <li>🎯 Goal: Become successful, build my dream career</li>
              <li>💬 Ask me about <strong>Web Development, Software Solutions, Graphic Design, Mobile App Dev, Freelancing</strong></li>
              <li>⚡ Fun fact: I believe in <em>hard work + smart work = success</em></li>
            </ul>

            <div style="height:14px"></div>
            <div class="accent-line"></div>

            <h2 id="tech">🛠️ Tech Stack</h2>
            <div class="neon-box">
              <h3 style="color:var(--accent);margin:0 0 10px">Languages</h3>
              <p class="badges">
                <img src="https://img.shields.io/badge/-Python-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Python"/>
                <img src="https://img.shields.io/badge/-Java-007396?style=for-the-badge&logo=java&logoColor=white" alt="Java"/>
                <img src="https://img.shields.io/badge/-PHP-777BB4?style=for-the-badge&logo=php&logoColor=white" alt="PHP"/>
                <img src="https://img.shields.io/badge/-JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black" alt="JS"/>
                <img src="https://img.shields.io/badge/-C%23-239120?style=for-the-badge&logo=c-sharp&logoColor=white" alt="C#"/>
                <img src="https://img.shields.io/badge/-C++-00599C?style=for-the-badge&logo=cplusplus&logoColor=white" alt="C++"/>
                <img src="https://img.shields.io/badge/-Kotlin-0095D5?style=for-the-badge&logo=kotlin&logoColor=white" alt="Kotlin"/>
                <img src="https://img.shields.io/badge/-Groovy-4298B8?style=for-the-badge&logo=apache-groovy&logoColor=white" alt="Groovy"/>
                <img src="https://img.shields.io/badge/-R-4298B8?style=for-the-badge&logo=R&logoColor=white" alt="R"/>
              </p>

              <h3 style="color:var(--accent);margin-top:12px">Frameworks & Tools</h3>
              <p class="badges">
                <img src="https://img.shields.io/badge/-HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white" alt="HTML5"/>
                <img src="https://img.shields.io/badge/-CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white" alt="CSS3"/>
                <img src="https://img.shields.io/badge/-Android%20Studio-3DDC84?style=for-the-badge&logo=android-studio&logoColor=white" alt="Android Studio"/>
                <img src="https://img.shields.io/badge/-MySQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white" alt="MySQL"/>
                <img src="https://img.shields.io/badge/-Git-F05032?style=for-the-badge&logo=git&logoColor=white" alt="Git"/>
                <img src="https://img.shields.io/badge/-GitHub-181717?style=for-the-badge&logo=github&logoColor=white" alt="GitHub"/>
              </p>
            </div>

            <h2 id="projects">💡 Projects & Portfolio</h2>
            <div class="neon-box">
              <p style="margin:0 0 8px">This site mirrors your README content — below are quick links and samples. Add links to repo pages or project demos here.</p>
              <ul>
                <li><strong>Web-based Rocket Fire Bubbles Game</strong> — (In progress) — built with HTML/CSS/JS</li>
                <li><strong>Fitness Center Web App</strong> — PHP + MySQL, profile system, booking trainers</li>
                <li><strong>Temperature Monitoring System</strong> — hardware + web dashboard</li>
              </ul>
            </div>

            <h2 id="contact">🌐 Connect With Me</h2>
            <div class="neon-box">
              <p style="margin:0 0 8px">Reach out on:</p>
              <p style="display:flex;gap:8px;flex-wrap:wrap;margin:0">
                <a class="capsule" href="https://www.linkedin.com/in/theekshana-vidushan-727689293/">LinkedIn</a>
                <a class="capsule" href="https://www.fiverr.com/">Fiverr</a>
                <a class="capsule" href="mailto:Theekshanavidushan.dev@gmail.com">Email</a>
              </p>
            </div>

          </div>

          <aside class="right neon-box" style="min-width:260px">
            <h3 style="margin-top:0;color:var(--accent)">Profile Snapshot</h3>
            <p style="color:var(--muted);margin-bottom:8px">Shana — Software Engineering student, Graphic Designer, aspiring Full-Stack dev.</p>

            <div class="stats">
              <img src="https://github-readme-stats.vercel.app/api?username=Theek-Shana&show_icons=true&theme=tokyonight&hide_border=true&bg_color=0D1117&title_color=00F7FF&icon_color=00F7FF&text_color=FFFFFF" alt="GitHub stats" style="width:100%"/>
            </div>

            <div style="height:12px"></div>
            <div style="font-size:13px;color:var(--muted)">Mobile: <strong style="color:var(--accent)">0717970580</strong></div>
            <div style="height:8px"></div>

            <div style="margin-top:12px">
              <a class="btn" href="#projects">View Projects</a>
            </div>
          </aside>
        </section>

        <section class="neon-box full" id="readme">
          <h2>📄 README (Original content preserved)</h2>
          <pre>
The original README content (title, tech stack, about, gifs, badges, contact links) is preserved exactly.
This web version displays it in an interactive, modern layout. If you want the raw README.md file generated too,
click the button at the bottom to download the ready-to-use README.md for GitHub.
          </pre>
          <div style="display:flex;gap:8px;margin-top:10px">
            <button id="download-readme" class="btn">Download README.md</button>
            <a class="btn" href="https://github.com/Theek-Shana" target="_blank">Open GitHub</a>
          </div>
        </section>

      </main>

      <aside>
        <section class="neon-box">
          <h3 style="margin-top:0;color:var(--accent)">Quick Links</h3>
          <ul>
            <li><a href="#tech">Tech Stack</a></li>
            <li><a href="#projects">Projects</a></li>
            <li><a href="#contact">Contact</a></li>
          </ul>
        </section>

        <section class="neon-box" style="margin-top:12px">
          <h3 style="color:var(--accent);margin-top:0">Contact</h3>
          <p style="color:var(--muted);margin:0 0 8px">Email: <strong style="color:var(--accent)">Theekshanavidushan.dev@gmail.com</strong></p>
          <p style="color:var(--muted);margin:0">Phone: <strong style="color:var(--accent)">0717970580</strong></p>
        </section>

        <section class="neon-box" style="margin-top:12px">
          <h3 style="color:var(--accent);margin-top:0">Extras</h3>
          <p style="color:var(--muted);margin:0 0 8px">Want more effects? Add particle background, 3D text, or a projects carousel.</p>
          <button id="more-effects" class="btn">Add sample particle</button>
        </section>
      </aside>

    </div>

    <footer>
      <div style="display:flex;gap:12px;align-items:center">
        <div class="capsule">⭐ From <a href="https://github.com/Theek-Shana">Shana</a></div>
        <div style="color:var(--muted);font-size:13px">Designed: Futuristic Neon • Dark Theme</div>
      </div>
      <div style="color:var(--muted);font-size:13px">Built with ❤️ · Copy this file for GitHub Pages</div>
    </footer>

  </div>

  <!-- README content file creation: we will generate a downloadable README.md blob on the fly -->
  <script>
    const originalReadme = `# Theekshana Vidushan\n\n<div align=\"center\"> \n \n# <img src=\"https://raw.githubusercontent.com/ABSphreak/ABSphreak/master/gifs/Hi.gif\" width=\"30px\"> Hello, I'm Theekshana Vidushan! \n\n</div>   \n\n<div align=\"center\">\n  \n<img align=\"right\" alt=\"Coding\" width=\"400\" src=\"https://user-images.githubusercontent.com/74038190/212749447-bfb7e725-6987-49d9-ae85-2015e3e7cc41.gif\">\n\n<div align=\"left\" style=\"padding-right: 420px;\">\n\n<img src=\"https://readme-typing-svg.herokuapp.com?font=Fira+Code&weight=600&size=22&duration=3500&pause=1000&color=00F7FF&vCenter=true&width=500&lines=🚀+Passionate+Software+Engineering+Student;🎨+Creative+Graphic+Designer;💻+Aspiring+Full-Stack+Developer;🔥+Always+Learning+and+Building\" alt=\"Typing SVG\" /> \n\n<br><br>\n\n### 👨‍💻 About Me \n\n- 🌱 Final year, **Software Engineering Student @ ICBT Campus**\n- 🖥️ Love building **web apps, creative projects, and Software Solutions**\n- 🎯 Goal: Become successful, build my dream career   \n- 💬 Ask me about **Web Development, Software Solutions, Graphic Design, Mobile Application Development, and Freelancing**\n- ⚡ Fun fact: I believe in **hard work + smart work = success**\n\n<br>\n\n</div>\n\n</div>\n\n<br clear=\"right\"/>\n\n---\n\n### 🛠️ Tech Stack  \n\n**Languages:**  \n\n<p>\n<img src=\"https://img.shields.io/badge/-Python-3776AB?style=for-the-badge&logo=python&logoColor=white\" />\n<img src=\"https://img.shields.io/badge/-Java-007396?style=for-the-badge&logo=java&logoColor=white\" />\n<img src=\"https://img.shields.io/badge/-PHP-777BB4?style=for-the-badge&logo=php&logoColor=white\" />\n<img src=\"https://img.shields.io/badge/-JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black\" />\n<img src=\"https://img.shields.io/badge/-C%23-239120?style=for-the-badge&logo=c-sharp&logoColor=white\" />\n<img src=\"https://img.shields.io/badge/-C++-00599C?style=for-the-badge&logo=cplusplus&logoColor=white\" />  \n<img src=\"https://img.shields.io/badge/-Kotlin-0095D5?style=for-the-badge&logo=kotlin&logoColor=white\" />\n<img src=\"https://img.shields.io/badge/-Groovy-4298B8?style=for-the-badge&logo=apache-groovy&logoColor=white\" />\n  <img src=\"https://img.shields.io/badge/-R-4298B8?style=for-the-badge&logo=R&logoColor=white\" />\n</p>\n\n**Frameworks & Tools:**  \n\n<p>\n<img src=\"https://img.shields.io/badge/-HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white\" />\n<img src=\"https://img.shields.io/badge/-CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white\" />\n<img src=\"https://img.shields.io/badge/-Android%20Studio-3DDC84?style=for-the-badge&logo=android-studio&logoColor=white\" />\n<img src=\"https://img.shields.io/badge/-MySQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white\" />\n<img src=\"https://img.shields.io/badge/-Git-F05032?style=for-the-badge&logo=git&logoColor=white\" />\n<img src=\"https://img.shields.io/badge/-GitHub-181717?style=for-the-badge&logo=github&logoColor=white\" />\n</p>\n\n---\n\n### 📊 Git Hub Stats         \n\n<div align=\"center\">\n  <img src=\"https://github-readme-stats.vercel.app/api?username=Theek-Shana&show_icons=true&theme=tokyonight&hide_border=true&bg_color=0D1117&title_color=00F7FF&icon_color=00F7FF&text_color=FFFFFF\" alt=\"GitHub Stats\" height=\"180\"/>\n  <img src=\"https://github-readme-streak-stats.herokuapp.com/?user=Theek-Shana&theme=tokyonight&hide_border=true&background=0D1117&ring=00F7FF&fire=FF5733&currStreakLabel=00F7FF\" alt=\"GitHub Streak\" height=\"180\"/>\n</div>\n\n---\n\n### 🌐 Connect With Me\n\n<p align=\"center\">\n  <a href=\"https://www.linkedin.com/in/theekshana-vidushan-727689293/\">\n    <img src=\"https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white\" />\n  </a>\n  <a href=\"https://www.fiverr.com/\">\n    <img src=\"https://img.shields.io/badge/Fiverr-1DBF73?style=for-the-badge&logo=fiverr&logoColor=white\" />\n  </a>\n  <a href=\"mailto:Theekshanavidushan.dev@gmail.com\">\n    <img src=\"https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white\" />\n  </a>\n</p>\n\n---  \n\n<div align=\"center\">\n  <img src=\"https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=6,11,20&height=100&section=footer&text=Thanks%20for%20visiting!&fontSize=20&fontColor=fff&animation=twinkling\" />\n</div>\n\n<p align=\"center\">\n  ⭐ From <a href=\"https://github.com/Theek-Shana\">Shana</a>\n</p>`;

    // Download README.md on button click
    document.getElementById('download-readme').addEventListener('click', ()=>{
      const blob = new Blob([originalReadme], {type: 'text/markdown;charset=utf-8'});
      const url = URL.createObjectURL(blob);
      const a = document.createElement('a');
      a.href = url; a.download = 'README.md'; document.body.appendChild(a); a.click(); a.remove();
      URL.revokeObjectURL(url);
    });

    // Simple particle background (lightweight)
    const canvas = document.getElementById('bg-canvas');
    const ctx = canvas.getContext('2d');
    function resize(){canvas.width=innerWidth;canvas.height=innerHeight}
    addEventListener('resize',resize);resize();

    const parts = [];
    for(let i=0;i<60;i++) parts.push({x:Math.random()*canvas.width,y:Math.random()*canvas.height,vx:(Math.random()-0.5)*0.3,vy:(Math.random()-0.5)*0.3,r:Math.random()*1.8+0.3});
    function tick(){ctx.clearRect(0,0,canvas.width,canvas.height);
      for(let p of parts){p.x+=p.vx;p.y+=p.vy;if(p.x<0)p.x=canvas.width;if(p.x>canvas.width)p.x=0;if(p.y<0)p.y=canvas.height;if(p.y>canvas.height)p.y=0;
        ctx.beginPath();ctx.fillStyle='rgba(0,247,255,0.06)';ctx.arc(p.x,p.y,p.r,0,Math.PI*2);ctx.fill();
      }
      requestAnimationFrame(tick);
    }
    tick();

    // 'More effects' button toggles extra particles
    document.getElementById('more-effects').addEventListener('click', ()=>{
      for(let i=0;i<120;i++) parts.push({x:Math.random()*canvas.width,y:Math.random()*canvas.height,vx:(Math.random()-0.5)*0.6,vy:(Math.random()-0.5)*0.6,r:Math.random()*2.6+0.3});
      document.getElementById('more-effects').textContent='Particles added ✓';
    });

  </script>
</body>
</html>
