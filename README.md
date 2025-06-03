<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Harini A - Animated GitHub Profile</title>
  <link href="https://fonts.googleapis.com/css2?family=Fira+Code&display=swap" rel="stylesheet">
  <style>
    body {
      background-color: #0d1117;
      color: #fff;
      font-family: 'Fira Code', monospace;
      margin: 0;
      padding: 0;
      text-align: center;
    }
    h1, h2, h3 {
      color: #FF69B4;
    }
    .section {
      margin: 50px 0;
      padding: 20px;
    }
    .badge {
      margin: 5px;
    }
    .type-text {
      font-size: 1.5rem;
      color: #FFC0CB;
    }
    .icon {
      width: 80px;
      margin: 15px;
      transition: transform 0.4s;
    }
    .icon:hover {
      transform: scale(1.2);
    }
    .fade-in {
      animation: fadeIn 2s ease-in;
    }
    @keyframes fadeIn {
      from { opacity: 0; transform: translateY(20px); }
      to { opacity: 1; transform: translateY(0); }
    }
  </style>
</head>
<body>

  <h1 data-tilt class="fade-in">
    <img src="https://media.giphy.com/media/26xBwdIuRJiAIqHwA/giphy.gif" height="40px"> Harini A
    <img src="https://media.giphy.com/media/xT9IgzoKnwFNmISR8I/giphy.gif" height="40px" />
  </h1>

  <div class="type-text" id="typed"></div>

  <div class="section">
    <h2>🚀 Tech Stack</h2>
    <div>
      <img class="icon" src="https://img.icons8.com/color/96/000000/python.png" />
      <img class="icon" src="https://img.icons8.com/color/96/000000/java-coffee-cup-logo.png" />
      <img class="icon" src="https://img.icons8.com/color/96/000000/react-native.png" />
      <img class="icon" src="https://img.icons8.com/color/96/000000/mysql-logo.png" />
      <img class="icon" src="https://img.icons8.com/color/96/000000/figma--v1.png" />
    </div>
  </div>

  <div class="section">
    <h2>📈 GitHub Stats</h2>
    <img src="https://github-readme-stats.vercel.app/api?username=HARINII2415&show_icons=true&theme=radical&title_color=FF69B4&icon_color=FF69B4&text_color=ffffff&bg_color=0d1117" width="49%"/>
    <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=HARINII2415&layout=compact&theme=radical&title_color=FF69B4&text_color=ffffff&bg_color=0d1117" width="49%"/>
    <br><br>
    <img src="https://github-readme-streak-stats.herokuapp.com/?user=HARINII2415&theme=radical&ring=FF69B4&fire=FF69B4&currStreakLabel=FF69B4" width="80%"/>
  </div>

  <div class="section">
    <h2>🌈 Connect With Me</h2>
    <a href="mailto:harinii2415@gmail.com"><img class="badge" src="https://img.shields.io/badge/Gmail-FF69B4?style=for-the-badge&logo=gmail&logoColor=white" /></a>
    <a href="https://www.linkedin.com/in/harini-a-9a014925a/"><img class="badge" src="https://img.shields.io/badge/LinkedIn-FF69B4?style=for-the-badge&logo=linkedin&logoColor=white" /></a>
    <a href="https://harinii2415.github.io"><img class="badge" src="https://img.shields.io/badge/Portfolio-FF69B4?style=for-the-badge&logo=githubpages&logoColor=white" /></a>
  </div>

  <!-- Scripts -->
  <script src="https://cdn.jsdelivr.net/npm/typed.js@2.0.12"></script>
  <script src="https://cdnjs.cloudflare.com/ajax/libs/vanilla-tilt/1.7.0/vanilla-tilt.min.js"></script>
  <script>
    VanillaTilt.init(document.querySelector("h1"), {
      max: 25,
      speed: 400,
      glare: true,
      "max-glare": 0.5
    });

    new Typed("#typed", {
      strings: [
        "Vanakkam 👋 I'm Harinii 💖",
        "Aspiring Data Scientist 📊",
        "Java Full Stack Learner 💻",
        "Creative Tech Explorer 🌈"
      ],
      typeSpeed: 50,
      backSpeed: 30,
      loop: true
    });
  </script>
</body>
</html>
