<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Harini A - Portfolio README</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://fonts.googleapis.com/css2?family=Fira+Code:wght@400;600&family=Poppins:wght@300;400;600;700&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
    <style>
        :root {
            --primary-color: #FF69B4; /* Hot Pink */
            --secondary-color: #FFC0CB; /* Pink */
            --bg-dark: #0d1117; /* GitHub dark background */
            --bg-light: #161b22; /* GitHub lighter background */
            --text-primary: #c9d1d9; /* GitHub primary text */
            --text-secondary: #8b949e; /* GitHub secondary text */
            --border-color: #30363d; /* GitHub border color */
            --link-color: #58a6ff; /* GitHub link color */
        }

        body {
            font-family: 'Poppins', sans-serif;
            background-color: var(--bg-dark);
            color: var(--text-primary);
            line-height: 1.7;
            scroll-behavior: smooth;
        }

        .typing-svg {
            display: block;
            margin-left: auto;
            margin-right: auto;
            max-width: 100%;
        }

        .section-title {
            font-family: 'Fira Code', monospace;
            color: var(--primary-color);
            border-bottom: 3px solid var(--primary-color);
            padding-bottom: 8px;
            margin-bottom: 25px;
            display: inline-block;
            font-size: 1.6rem; /* Slightly larger */
        }
        @media (min-width: 768px) {
            .section-title {
                font-size: 2rem;
            }
        }


        .tech-icon-container img:hover {
            transform: scale(1.1) rotate(5deg);
            transition: transform 0.3s ease-in-out;
        }

        .project-card {
            background-color: var(--bg-light);
            border: 1px solid var(--border-color);
            border-radius: 12px; /* More rounded */
            transition: transform 0.35s ease, box-shadow 0.35s ease, border-color 0.35s ease;
            overflow: hidden;
            display: flex;
            flex-direction: column;
            justify-content: space-between; /* Ensures footer links are at bottom */
        }

        .project-card:hover {
            transform: translateY(-8px) scale(1.02);
            box-shadow: 0 12px 25px rgba(255, 105, 180, 0.25);
            border-color: var(--primary-color);
        }

        .project-card-content {
            padding: 20px; /* Consistent padding */
        }
        
        .project-card h3 {
            color: var(--primary-color);
            font-size: 1.3rem;
            font-weight: 600;
        }
        
        .project-card .tech-stack {
            font-size: 0.85rem;
            color: var(--text-secondary);
            margin-bottom: 12px;
            font-style: italic;
        }

        .project-card .description {
            font-size: 0.95rem;
            color: var(--text-primary);
            margin-bottom: 16px;
            flex-grow: 1; /* Allows description to take available space */
        }
        
        .project-links {
            padding: 15px 20px;
            background-color: rgba(0,0,0,0.1); /* Subtle footer background */
            border-top: 1px solid var(--border-color);
            display: flex;
            gap: 15px; /* Space between links */
        }

        .project-links a {
            color: var(--link-color);
            text-decoration: none;
            transition: color 0.3s ease, transform 0.2s ease;
            font-size: 0.9rem;
            display: inline-flex; /* Align icon and text */
            align-items: center;
        }
        .project-links a i {
            margin-right: 6px; /* Space between icon and text */
        }

        .project-links a:hover {
            color: var(--primary-color);
            transform: translateY(-2px);
        }

        .badge {
            transition: transform 0.2s ease-in-out, filter 0.2s ease-in-out;
        }
        .badge:hover {
            transform: scale(1.08);
            filter: brightness(1.2);
        }

        .connect-link img {
            transition: transform 0.3s ease, filter 0.3s ease;
        }
        .connect-link img:hover {
            transform: scale(1.15);
            filter: drop-shadow(0 0 5px var(--primary-color));
        }

        .wave-footer {
            width: 100%;
            display: block;
        }

        .github-stats-img, .github-activity-img {
            max-width: 100%;
            height: auto;
            border-radius: 10px;
            border: 1px solid var(--border-color);
            transition: box-shadow 0.3s ease;
        }
        .github-stats-img:hover, .github-activity-img:hover {
             box-shadow: 0 0 15px rgba(255, 105, 180, 0.3);
        }

        .github-stats-container > div {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 1.5rem;
        }
        .github-stats-container img {
            flex-grow: 1;
            min-width: 280px; /* Adjusted min-width */
        }

        .about-me-container {
            display: flex;
            flex-wrap: wrap;
            align-items: center; /* Vertically center align items */
            gap: 20px; /* Gap between text and image */
        }
        .about-me-text {
            flex: 1;
            min-width: 300px;
        }
        .about-me-gif {
            width: 200px;
            height: 200px;
            object-fit: cover;
            border-radius: 50%; /* Circular GIF */
            border: 3px solid var(--primary-color);
            box-shadow: 0 0 15px rgba(255, 105, 180, 0.3);
            transition: transform 0.3s ease;
        }
        .about-me-gif:hover {
            transform: scale(1.05);
        }

        .custom-hr {
            border: 0;
            height: 2px;
            background-image: linear-gradient(to right, rgba(0, 0, 0, 0), var(--primary-color), rgba(0, 0, 0, 0));
            margin: 50px 0;
        }
        
        .portfolio-button {
            display: inline-block;
            background: linear-gradient(45deg, var(--primary-color), var(--secondary-color));
            color: white;
            font-weight: bold;
            padding: 12px 28px;
            border-radius: 50px; /* Pill shape */
            margin-top: 10px;
            transition: transform 0.3s ease, box-shadow 0.3s ease;
            text-decoration: none;
            box-shadow: 0 4px 15px rgba(255, 105, 180, 0.2);
        }
        .portfolio-button:hover {
            transform: translateY(-3px) scale(1.03);
            box-shadow: 0 6px 20px rgba(255, 105, 180, 0.4);
        }


        @media (max-width: 768px) {
            .about-me-container {
                flex-direction: column;
                text-align: center; /* Center text on small screens */
            }
            .about-me-gif {
                margin: 20px auto; /* Center GIF */
            }
            .section-title {
                font-size: 1.5rem;
            }
            .project-card h3 {
                font-size: 1.15rem;
            }
             .github-stats-container > div {
                flex-direction: column;
                align-items: center;
            }
            .github-stats-container img {
                width: 90%;
                max-width: 400px;
            }
        }
    </style>
</head>
<body class="p-4 md:p-8">

    <!-- Typing Intro -->
    <div class="text-center mb-8 md:mb-12">
        <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=28&md:size=32&duration=3000&pause=1000&color=FF69B4&center=true&vCenter=true&width=600&md:width=800&lines=Vanakkam+%F0%9F%91%8B+I'm+Harinii;Aspiring+Data+Scientist;Analytics+Enthusiast;Java+Full+Stack+Learner;Creative+Tech+Explorer" alt="Typing Intro - Vanakkam, I'm Harinii, Aspiring Data Scientist, Analytics Enthusiast, Java Full Stack Learner, Creative Tech Explorer" class="typing-svg"/>
    </div>

    <!-- Header Name -->
    <header class="text-center mb-10 md:mb-16">
        <h1 class="text-3xl md:text-5xl font-bold flex items-center justify-center text-white">
            <img src="https://media.giphy.com/media/26xBwdIuRJiAIqHwA/giphy.gif" height="50px" alt="Wave Left GIF" class="mx-2 h-10 md:h-12"/>
            Harini A
            <img src="https://media.giphy.com/media/xT9IgzoKnwFNmISR8I/giphy.gif" height="50px" alt="Sparkle GIF" class="mx-2 h-10 md:h-12"/>
        </h1>
    </header>

    <!-- Coding GIF -->
    <div class="text-center mb-12 md:mb-16">
        <img src="https://media.giphy.com/media/qgQUggAC3Pfv687qPC/giphy.gif" width="300px" alt="Coding GIF" class="mx-auto rounded-xl shadow-xl border-2 border-pink-500/50"/>
    </div>

    <hr class="custom-hr">

    <!-- About Me Section -->
    <section id="about-me" class="mb-12 md:mb-16">
        <h2 class="text-2xl md:text-3xl font-semibold section-title mb-8">🌸 About Me 🌸</h2>
        <div class="about-me-container">
            <div class="about-me-text text-gray-300 text-base md:text-lg space-y-3">
                <p>🎓 B.Tech IT Final Year Student at MKCE, Karur.</p>
                <p>⚡ Passionate about the convergence of <strong>Data Science</strong>, intuitive <strong>UI/UX Design</strong>, and robust <strong>Java Full Stack Development</strong>.</p>
                <p>🧠 Exploring and excited by: <strong>React, Spring Boot, Python (Machine Learning & Deep Learning), Streamlit, and Generative AI</strong>.</p>
                <p>🎯 Dedicated to crafting solutions that harmoniously blend <strong>analytical logic, aesthetic design, and user empathy</strong>.</p>
                <p>💕 I find joy in vibrant colors, insightful dashboards, fluid animations, and transforming data into meaningful narratives.</p>
                <p>📈 On a continuous journey to evolve into a <strong>Creative Data Engineer & versatile Full Stack Developer</strong>.</p>
                <p class="mt-6">
                    Discover more about my projects and journey:
                    <br>
                    <a href="https://harinii2415.github.io/" target="_blank" class="portfolio-button">
                        ✨ Visit My Portfolio Website ✨
                    </a>
                </p>
            </div>
            <img src="https://media.giphy.com/media/USV0ym3bVWQJJmNu3N/giphy.gif" alt="Thinking Developer GIF" class="about-me-gif"/>
        </div>
    </section>

    <hr class="custom-hr">

    <!-- Tech Playground Section -->
    <section id="tech-playground" class="mb-12 md:mb-16">
        <h2 class="text-2xl md:text-3xl font-semibold section-title mb-8">🛠️ My Tech Playground 🎨</h2>
        <div class="text-center mb-6 tech-icon-container">
            <img src="https://skillicons.dev/icons?i=python,java,react,spring,html,css,js,figma,azure,bootstrap,github,git,mysql,vscode,idea,postman,maven,docker,tailwind,nodejs,express,mongodb,firebase,pytorch,tensorflow,kubernetes,nextjs,fastapi,grafana&theme=light&perline=11" alt="Tech Skills Icons" class="mx-auto"/>
        </div>
        <div class="flex flex-wrap justify-center gap-3 md:gap-4">
            <img src="https://img.shields.io/badge/-Machine%20Learning-FF69B4?style=for-the-badge&logo=tensorflow&logoColor=white" alt="Machine Learning Badge" class="badge"/>
            <img src="https://img.shields.io/badge/-Deep%20Learning-FF69B4?style=for-the-badge&logo=pytorch&logoColor=white" alt="Deep Learning Badge" class="badge"/>
            <img src="https://img.shields.io/badge/-Streamlit%20Apps-FF9A8B?style=for-the-badge&logo=streamlit&logoColor=white" alt="Streamlit Apps Badge" class="badge"/> <!-- Changed color for variety -->
            <img src="https://img.shields.io/badge/-PowerBI%20Analytics-FFC0CB?style=for-the-badge&logo=powerbi&logoColor=black" alt="PowerBI Analytics Badge" class="badge"/>
            <img src="https://img.shields.io/badge/-Full%20Stack%20Dev-FF69B4?style=for-the-badge&logo=javascript&logoColor=white" alt="Full Stack Developer Badge" class="badge"/>
            <img src="https://img.shields.io/badge/-Cloud%20Native-87CEFA?style=for-the-badge&logo=kubernetes&logoColor=white" alt="Cloud Native Badge" class="badge"/> <!-- Changed color -->
            <img src="https://img.shields.io/badge/-Problem%20Solver-FF69B4?style=for-the-badge&logo=hackerrank&logoColor=white" alt="Problem Solver Badge" class="badge"/>
            <img src="https://img.shields.io/badge/-Team%20Player-FFC0CB?style=for-the-badge&logoColor=black" alt="Team Player Badge" class="badge"/>
        </div>
    </section>

    <hr class="custom-hr">

    <!-- Projects Section -->
    <section id="projects" class="mb-12 md:mb-16">
        <h2 class="text-2xl md:text-3xl font-semibold section-title mb-10">✨ Projects That Spark 🔥</h2>
        <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8 md:gap-10">
            <!-- Project Card 1 -->
            <div class="project-card">
                <div class="project-card-content">
                    <h3>🌿 Skin Cancer Risk Detector</h3>
                    <p class="tech-stack">Python, Scikit-learn, Streamlit, TensorFlow/Keras</p>
                    <p class="description">An intuitive web application that predicts skin cancer risk using image analysis (CNNs) and clinical data inputs.</p>
                </div>
                <div class="project-links">
                    <a href="YOUR_REPO_LINK_HERE_SKIN" target="_blank"><i class="fab fa-github"></i> GitHub Repo</a>
                    <a href="YOUR_DEMO_LINK_HERE_SKIN" target="_blank"><i class="fas fa-external-link-alt"></i> Live App</a>
                </div>
            </div>
            <!-- Project Card 2 -->
            <div class="project-card">
                 <div class="project-card-content">
                    <h3>🌦️ WeatherMate Real-Time Forecaster</h3>
                    <p class="tech-stack">React, Spring Boot, OpenWeatherAPI, RESTful APIs</p>
                    <p class="description">A dynamic application delivering real-time weather forecasts and conditions globally, using the OpenWeatherMap API.</p>
                </div>
                <div class="project-links">
                    <a href="YOUR_REPO_LINK_HERE_WEATHER" target="_blank"><i class="fab fa-github"></i> GitHub Repo</a>
                    <a href="YOUR_DEMO_LINK_HERE_WEATHER" target="_blank"><i class="fas fa-external-link-alt"></i> Live App</a>
                </div>
            </div>
            <!-- Project Card 3 -->
            <div class="project-card">
                <div class="project-card-content">
                    <h3>🎶 Elegant Music Player UI</h3>
                    <p class="tech-stack">React, Tailwind CSS, Figma (for design)</p>
                    <p class="description">A sleek, responsive, and visually appealing front-end user interface designed for a modern music player application.</p>
                </div>
                <div class="project-links">
                    <a href="YOUR_REPO_LINK_HERE_MUSIC" target="_blank"><i class="fab fa-github"></i> GitHub Repo</a>
                    <a href="YOUR_DEMO_LINK_HERE_MUSIC" target="_blank"><i class="fas fa-external-link-alt"></i> Live Demo</a>
                </div>
            </div>
            <!-- Project Card 4 -->
            <div class="project-card">
                <div class="project-card-content">
                    <h3>🧬 HbA1c Diabetes Prediction System</h3>
                    <p class="tech-stack">Python, Pandas, Scikit-learn, Streamlit</p>
                    <p class="description">A health analytics web application to predict diabetes risk based on HbA1c levels and other patient correlational data.</p>
                </div>
                <div class="project-links">
                    <a href="YOUR_REPO_LINK_HERE_DIABETES" target="_blank"><i class="fab fa-github"></i> GitHub Repo</a>
                    <a href="YOUR_DEMO_LINK_HERE_DIABETES" target="_blank"><i class="fas fa-external-link-alt"></i> Live App</a>
                </div>
            </div>
            <!-- Project Card 5 (Example) -->
            <div class="project-card">
                <div class="project-card-content">
                    <h3>🛍️ Full-Stack E-Commerce Platform</h3>
                    <p class="tech-stack">Java, Spring Boot, React, MySQL, Docker</p>
                    <p class="description">A comprehensive online shopping website with features like product catalog, user authentication, and order management.</p>
                </div>
                <div class="project-links">
                    <a href="YOUR_REPO_LINK_HERE_ECOMMERCE" target="_blank"><i class="fab fa-github"></i> GitHub Repo</a>
                    <a href="YOUR_DEMO_LINK_HERE_ECOMMERCE" target="_blank"><i class="fas fa-external-link-alt"></i> Live Demo</a>
                </div>
            </div>
             <!-- Project Card 6 (New Example) -->
            <div class="project-card">
                <div class="project-card-content">
                    <h3>📝 AI-Powered Content Summarizer</h3>
                    <p class="tech-stack">Python, FastAPI, Hugging Face Transformers, Next.js</p>
                    <p class="description">A web service that leverages pre-trained NLP models to generate concise summaries of long texts or articles.</p>
                </div>
                <div class="project-links">
                    <a href="YOUR_REPO_LINK_HERE_SUMMARIZER" target="_blank"><i class="fab fa-github"></i> GitHub Repo</a>
                    <a href="YOUR_DEMO_LINK_HERE_SUMMARIZER" target="_blank"><i class="fas fa-external-link-alt"></i> Live API</a>
                </div>
            </div>
        </div>
    </section>

    <hr class="custom-hr">

    <!-- GitHub Snapshot Section -->
    <section id="github-snapshot" class="mb-12 md:mb-16">
        <h2 class="text-2xl md:text-3xl font-semibold section-title mb-8">📊 GitHub Snapshot 🚀</h2>
        <div class="github-stats-container text-center">
             <div class="flex flex-wrap justify-center items-start gap-6">
                <img src="https://github-readme-stats.vercel.app/api?username=HARINII2415&show_icons=true&theme=radical&title_color=FF69B4&icon_color=FF69B4&text_color=ffffff&bg_color=0d1117&border_radius=10&hide_border=true&cache_seconds=1800&count_private=true&hide=issues" alt="Harini's GitHub Stats" class="github-stats-img"/>
                <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=HARINII2415&layout=compact&theme=radical&title_color=FF69B4&text_color=ffffff&bg_color=0d1117&border_radius=10&hide_border=true&langs_count=10&cache_seconds=1800&hide=jupyter%20notebook" alt="Harini's Top Languages" class="github-stats-img"/>
            </div>
            <img src="https://github-readme-streak-stats.herokuapp.com?user=HARINII2415&theme=radical&ring=FF69B4&fire=FF69B4&currStreakLabel=FF69B4&border_radius=10&hide_border=true&cache_seconds=1800&date_format=M%20j%5B%2C%20Y%5D" alt="Harini's GitHub Streak" class="mt-6 mx-auto github-stats-img" style="max-width: 90%;"/>
        </div>
    </section>

    <hr class="custom-hr">

    <!-- Contribution Heatmap Section -->
    <section id="contribution-heatmap" class="mb-12 md:mb-16">
        <h2 class="text-2xl md:text-3xl font-semibold section-title mb-8">🪄 Contribution Activity 🗓️</h2>
        <div class="text-center p-2 bg-gray-800/30 rounded-lg">
            <img src="https://github-readme-activity-graph.vercel.app/graph?username=HARINII2415&theme=react-dark&bg_color=0d1117&color=ff69b4&line=ff69b4&point=ffc0cb&area=true&hide_border=true&area_color=ff69b4" alt="Harini's Contribution Graph" class="mx-auto github-activity-img"/>
        </div>
    </section>

    <hr class="custom-hr">

    <!-- Connect Section -->
    <section id="connect" class="mb-12 md:mb-16 text-center">
        <h2 class="text-2xl md:text-3xl font-semibold section-title mb-8">💬 Let’s Connect & Collaborate! 🤝</h2>
        <div class="flex justify-center items-center gap-4 md:gap-6">
            <a href="mailto:harinii2415@gmail.com" class="connect-link" title="Email Me"><img src="https://img.shields.io/badge/Gmail-D14836?style=for-the-badge&logo=gmail&logoColor=white" alt="Gmail"/></a>
            <a href="https://www.linkedin.com/in/harini-a-9a014925a/" class="connect-link" title="LinkedIn Profile"><img src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn"/></a>
            <a href="https://harinii2415.github.io" class="connect-link" title="My Portfolio"><img src="https://img.shields.io/badge/Portfolio-FF69B4?style=for-the-badge&logo=github&logoColor=white" alt="Portfolio"/></a>
            <a href="https://github.com/HARINII2415" class="connect-link" title="My GitHub Profile"><img src="https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white" alt="GitHub Profile"/></a>
        </div>
    </section>

    <!-- Footer Wave -->
    <footer class="mt-12 md:mt-16">
        <img src="https://capsule-render.vercel.app/api?type=waving&color=ff69b4&height=120&section=footer&width=100%" alt="Waving Footer Animation" class="wave-footer"/>
    </footer>

    <!-- 
    JavaScript Note for GitHub READMEs:
    Complex client-side JavaScript for dynamic interactions is generally not supported in GitHub READMEs for security reasons.
    The "JS" aspect here is primarily through:
    1. SVGs with built-in animations (like the typing intro).
    2. CSS animations and transitions for visual feedback.
    This README uses Tailwind CSS (loaded via CDN) for styling and responsiveness. FontAwesome is used for icons.
    -->
</body>
</html>
