<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>D GOKUL | Portfolio</title>
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <!-- Font Awesome for icons -->
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.2/css/all.min.css">
  <style>
    :root {
      --main1: #ca1c2a;
      --highlight: #fa5252;
      --github-linkedin: #7f1c1c;
      --accent: #941012;
      --dot: #ca1c2a;
      --dot-hover: #df1b1b;
      --bg: #fff0f0;
      --box-bg: #fff1f3;
      --box-border: #fc8d93;
      --shadow: 0 8px 32px #bc232733;
      --radius: 1.22rem;
      --topic-size: 2.6rem;
      --subtopic-size: 2.15rem;
      --data-size: 1.38rem;
    }
    html, body {
      height: 100%;
      margin: 0;
      background: linear-gradient(120deg,#fff0f0 0,#ffd3d3 100%);
      font-family: "Times New Roman", Times, serif;
      color: #82191d;
    }
    .container {
      max-width: 980px;
      margin: 2.3rem auto 1.3rem auto;
      background: var(--bg);
      border-radius: var(--radius);
      box-shadow: var(--shadow);
      padding: 2.4rem 1.1rem 2.3rem 1.1rem;
      border: 2px solid var(--main1);
    }
    header {
      background: linear-gradient(90deg, var(--main1) 10%, var(--highlight) 100%);
      color: #fff;
      text-align: center;
      border-radius: var(--radius) var(--radius) 0 0;
      box-shadow: 0 8px 26px #a000192a;
      padding: 2.6rem 1rem 1.35rem 1rem;
    }
    .profile-photo {
      width: 320px;
      height: 320px;
      object-fit: cover;
      border-radius: 0;
      margin-bottom: 2.2rem;
      box-shadow: 0 10px 44px #ca1c2a99;
      border: 8px solid #fff;
      display: block;
      margin-left: auto;
      margin-right: auto;
      background: #ffe7e9;
    }
    .main-title {
      font-size: 3.2rem;
      font-weight: 900;
      letter-spacing: 0.11em;
      color: #fff;
      margin-bottom: .38rem;
      font-family: "Times New Roman", Times, serif;
      text-shadow: 0 2px 20px #b341411c;
    }
    header p {
      font-size: 1.22rem;
      color: #fff6f6;
      font-weight: 600;
      text-shadow: 0 0 8px #fff6;
      margin-bottom: 0;
    }
    .section-block {
      background: #fff4f4;
      border-radius: var(--radius);
      box-shadow: 0 4px 22px #ce232733;
      border: 2px solid var(--box-border);
      padding: 1.25rem 1.15rem 1.19rem 1.22rem;
      margin-bottom: 1.25rem;
      font-family: "Times New Roman", Times, serif;
      opacity: 0;
      transform: translateY(52px) scale(.97);
      animation: fadeSlideIn .77s cubic-bezier(.36,1.16,.49,1.09) forwards;
    }
    .section-block:nth-child(even) {
      animation-delay: .13s;
      animation-name: fadeSlideInLeft;
    }
    @keyframes fadeSlideIn {
      0%{opacity:0;transform:translateY(74px) scale(.93);}
      55%{opacity:.9;transform:translateY(-4px) scale(1.02);}
      100%{opacity:1;transform:translateY(0) scale(1);}
    }
    @keyframes fadeSlideInLeft {
      0%{opacity:0;transform:translateY(78px) translateX(-31px) scale(.92);}
      55%{opacity:.93;transform:translateY(-4px) translateX(5px) scale(1.02);}
      100%{opacity:1;transform:translateY(0) scale(1);}
    }
    .section-title {
      font-size: var(--topic-size);
      font-weight: 900;
      text-transform: uppercase;
      margin-bottom: 1.1rem;
      letter-spacing: 0.09em;
      color: var(--main1);
      display: flex;
      align-items: center;
      gap: 0.76rem;
      border-bottom: 3px solid #fbc2c4;
      transition: border 0.19s;
    }
    .section-title:hover {
      border-bottom: 3px solid var(--main1);
      color: var(--highlight);
    }
    .section-title i {
      font-size: 1.4em;
      color: var(--highlight);
    }
    /* Update for Contact bar with icons at the far right */
    .section-title.contact-title-bar {
      display: flex;
      align-items: center;
      justify-content: space-between;
      padding-right: 12px;
    }
    .contact-icons {
      display: flex;
      align-items: center;
      gap: 16px;
      margin-left: auto;
    }
    .contact-icons .icon-link {
      font-size: 1.5em;
      line-height: 1;
    }
    .icon-link, .section-block a img {
      display: inline-block;
      transition: transform 0.31s cubic-bezier(.56,1.7,.41,1.18), box-shadow 0.19s, filter 0.14s;
      border-radius: 18px;
      background: transparent;
      filter: drop-shadow(0 2px 10px var(--highlight));
      box-shadow: 0 2px 12px #f44a4a14;
    }
    .icon-link:last-child { margin-right: 0;}
    .icon-link:hover, .section-block a img:hover {
      transform: scale(1.1) translateY(-3px);
      background: linear-gradient(94deg,#ffe2e21a 10%,#fa525214 89%);
      box-shadow: 0 4px 17px #f13c3c40;
      filter: drop-shadow(0 3px 10px var(--main1));
    }
    .icon-link.github i,
    .icon-link.linkedin i {
      color: var(--github-linkedin) !important;
    }
    .subtopic-title {
      font-size: var(--subtopic-size);
      font-weight: 800;
      margin: 1.6rem 0 0.6rem 0;
      letter-spacing: 0.01em;
      color: var(--main1);
      border-bottom: 2px solid #fcc;
      line-height: 2.2rem;
      transition: color 0.15s, border 0.17s;
      text-transform: capitalize;
      display: inline-block;
      vertical-align: middle;
    }
    .subtopic-title:hover {
      color: var(--highlight);
      border-bottom: 2px solid var(--highlight);
    }
    .edu-score {
      color: var(--highlight);
      font-weight: bold;
      font-size: var(--subtopic-size);
      margin-left: 12px;
      vertical-align: middle;
      display: inline-block;
    }
    .boxed-content,
    .reference-block {
      background: var(--box-bg);
      color: #b22527;
      border-left: 4px solid var(--main1);
      border-radius: 1rem;
      padding: 1.13rem 1.21rem 1.08rem 1.22rem;
      font-size: var(--data-size);
      font-family: "Times New Roman", Times, serif;
      text-align: left;
      margin: .01em 0 0.04em 0;
      font-weight: 400;
      box-shadow: 0 2.5px 14px #fa52522a;
      line-height: 1.72;
    }
    .boxed-content > div,
    .boxed-content > ul,
    .education-lines > div {
      font-size: var(--data-size);
    }
    .education-lines > div {
      margin-bottom: 0.6em;
      padding-left: 0.1em;
      line-height: 1.56;
      font-family: "Times New Roman", Times, serif;
    }
    .styled-list {
      list-style: none;
      margin: .13rem 0 .36rem 0;
      padding: 0;
    }
    .styled-list li:before {
      content: "\2022";
      position: absolute;
      left: 0em;
      top: 50%;
      transform: translateY(-50%);
      font-size: 1.33em;
      color: var(--dot);
      font-weight: 900;
      opacity: 0.95;
      border-radius: 50%;
      filter: blur(0.05px) drop-shadow(0 1px 4px #fa525227);
      transition: color .13s, transform .15s;
      animation: dotPop 0.5s cubic-bezier(.5,1.15,.55,1.05) backwards;
    }
    @keyframes dotPop{
      0%{transform:translateY(-50%) scale(.34);}
      60%{transform:translateY(-50%) scale(1.11);}
      100%{transform:translateY(-50%) scale(1);}
    }
    .styled-list li {
      display: block;
      position: relative;
      font-size: var(--data-size);
      margin-bottom: .23rem;
      padding-left: 1.33em;
      color: #b02525;
      font-family: "Times New Roman", Times, serif;
      transition: color .11s;
      background: #ffe7e9;
      border-radius: .7em;
      margin-right:.2em;
    }
    .styled-list li:hover:before {
      color: var(--dot-hover);
      transform: translateY(-50%) scale(1.1);
    }
    @media (max-width:700px) {
      :root {
        --topic-size: 1.28rem;
        --subtopic-size: 1.08rem;
        --data-size: 0.95rem;
      }
      .container{ padding: .36rem;}
      .section-block{ padding: .79rem .62rem .82rem .69rem;}
      .profile-photo { width: 180px; height: 180px;}
      .edu-score { font-size: var(--subtopic-size);}
      .section-title.contact-title-bar {
        padding-right: 5px;
      }
      .contact-icons .icon-link {
        font-size: 1.15em;
      }
    }
  </style>
</head>
<body>
<header>
  <img src="gokul.jpg" alt="D Gokul Photo" class="profile-photo">
  <div class="main-title">D GOKUL</div>
  <p>Junior Cyber Security & Forensics | Technology Explorer  </p>
</header>
<div class="container">
  <!-- Contact -->
  <div class="section-block" id="contact">
    <div class="section-title contact-title-bar">
      <div style="display:flex;align-items:center;gap:0.76rem;">
        <i class="fa-solid fa-address-card"></i>
        Contact
      </div>
      <div class="contact-icons">
        <a class="icon-link linkedin" href="https://www.linkedin.com/in/1107g?utm_source=share&utm_campaign=share_via&utm_content=profile&utm_medium=android_app" target="_blank" aria-label="LinkedIn profile">
          <i class="fab fa-linkedin"></i>
        </a>
        <a class="icon-link github" href="https://github.com/Gokulera" target="_blank" aria-label="GitHub profile">
          <i class="fab fa-github"></i>
        </a>
      </div>
    </div>
    <div class="boxed-content" style="padding-top:.7em;display:flex;flex-direction:column;">
      <div style="margin-bottom:.36em;"><i class="fa-solid fa-phone"></i> <strong>8098460812</strong></div>
      <div style="margin-bottom:.36em;"><i class="fa-solid fa-envelope"></i> gokuldharmaraja@gmail.com</div>
      <div style="margin-bottom:.5em;"><i class="fa-solid fa-location-dot"></i> Salem, Tamil Nadu</div>
    </div>
  </div>
  <!-- Objective -->
  <div class="section-block" id="objective">
    <div class="section-title"><i class="fa-solid fa-bullseye"></i> Objective</div>
    <div class="boxed-content">
      <div>To utilize my strong background in computer science for innovative solutions and security. To consistently apply analytical and problem-solving skills in real-world environments. To contribute positively and professionally in the field of cyber security.</div>
    </div>
  </div>
  <!-- Education -->
  <div class="section-block" id="education">
    <div class="section-title"><i class="fa-solid fa-graduation-cap"></i> Education</div>
    <div class="boxed-content education-lines">
      <div>
        <span class="subtopic-title">PG (2023–2025) :<span class="edu-score">75%</span></span>
        <div>AJK College Of Arts And Science<br>MSc. Cyber Security</div>
      </div>
      <div>
        <span class="subtopic-title">UG (2020–2023) :<span class="edu-score">62%</span></span>
        <div>Rathinam College Of Arts And Science<br>BSc. Digital and Cyber Forensic Science</div>
      </div>
      <div>
        <span class="subtopic-title">HSC 2020 :<span class="edu-score">65%</span></span>
        <div>Paavendhar Matric Hr. Sec School<br></div>
      </div>
      <div>
        <span class="subtopic-title">SSLC 2018 :<span class="edu-score">83%</span></span>
        <div>Paavendhar Matric Hr. Sec School<br></div>
      </div>
    </div>
  </div>
  <!-- Skills -->
  <div class="section-block" id="skills">
    <div class="section-title"><i class="fa-solid fa-star"></i> Skills</div>
    <div class="boxed-content">
      <div style="font-size: 18px" class="subtopic-title">Technical Skills</div>
      <ul class="styled-list">
        <li>HTML, CSS, JavaScript & Python</li>
        <li>Linux & Its Tools</li>
        <li>MS Office & Excel</li>
      </ul>
      <div style="font-size: 18px" class="subtopic-title">Soft Skills</div>
      <ul class="styled-list">
        <li>Active listening</li>
        <li>Time management</li>
        <li>Problem-solving abilities</li>
        <li>Ability to work in a team</li>
      </ul>
    </div>
  </div>
  <!-- Activity -->
  <div class="section-block" id="activity">
    <div class="section-title"><i class="fa-solid fa-bolt"></i> Activity</div>
    <div class="boxed-content">
      <div style="font-size: 18px" class="subtopic-title">Internship</div>
      <ul class="styled-list">
        <li>Concept of Python, Ether infotech, June 2023</li>
        <li>Cybersecurity tool development: Github, Pip and Security vulnerabilities, Cappricio Securities, May & June 2024</li>
      </ul>
      <div style="font-size: 18px" class="subtopic-title">Course</div>
      <ul class="styled-list">
        <li>Demystifying Networking & Ethical Hacking, Savam, March 2023</li>
        <li>Full Stack Python, Ether infotech, April & May 2023</li>
      </ul>
      <div style="font-size: 18px" class="subtopic-title">Project</div>
      <ul class="styled-list">
        <li>Multiple Encryption using Python, May 2023</li>
        <li>ARP poisoning detection tool, August 2024</li>
        <li>DDOS attack detection using machine learning, April 2025</li>
      </ul>
    </div>
  </div>
  <!-- Language -->
  <div class="section-block" id="language">
    <div class="section-title"><i class="fa-solid fa-language"></i> Language</div>
    <div class="boxed-content">
      <ul class="styled-list">
        <li>Tamil (RWS)</li>
        <li>English (RWS)</li>
      </ul>
    </div>
  </div>
  <!-- Hobbies -->
  <div class="section-block" id="hobbies">
    <div class="section-title"><i class="fa-solid fa-heart"></i> Hobbies</div>
    <div class="boxed-content">
      <ul class="styled-list">
        <li>Farming</li>
        <li>Gaming</li>
      </ul>
    </div>
  </div>
  <!-- Reference -->
  <div class="section-block" id="reference">
    <div class="section-title"><i class="fa-solid fa-user-tie"></i> Reference</div>
    <div class="boxed-content reference-block">
      <strong>Mr. KAMARAJ</strong><br>
      HOD, PG Department of Cyber Security at AJK<br>
      Phone: +91 9790556494
    </div>
  </div>
  <!-- Declaration -->
  <div class="section-block" id="declaration">
    <div class="section-title"><i class="fa-solid fa-scroll"></i> Declaration</div>
    <div class="boxed-content">
      <div>I hereby declare that the facts given above are genuine to the best of my knowledge and belief. I take responsibility for the correctness of the above-mentioned particulars. This declaration is made truly and honestly to the best of my knowledge.</div>
    </div>
  </div>
</div>
<footer style="text-align:center; padding:1rem 0 .42rem 0;font-size:1rem;letter-spacing:.01em;font-family:'Times New Roman',Times,serif;color:#c82333;">
  &copy; Last Update on Aug 06 2025 by D GOKUL.
</footer>
</body>
</html>
