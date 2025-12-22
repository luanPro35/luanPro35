<!DOCTYPE html>
<html lang="vi">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Luan - Full-Stack Developer 🎄</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: linear-gradient(135deg, #1a472a 0%, #0d2818 50%, #2d5a3d 100%);
            color: #fff;
            overflow-x: hidden;
            position: relative;
            min-height: 100vh;
        }

        /* Snowflakes */
        .snowflake {
            position: fixed;
            top: -10px;
            z-index: 1;
            color: #fff;
            font-size: 1em;
            animation: fall linear infinite;
            opacity: 0.8;
        }

        @keyframes fall {
            to {
                transform: translateY(100vh);
            }
        }

        /* Christmas lights */
        .lights {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 8px;
            display: flex;
            justify-content: space-around;
            z-index: 100;
        }

        .light {
            width: 12px;
            height: 12px;
            border-radius: 50%;
            animation: blink 1s infinite;
        }

        .light:nth-child(1) { background: #ff0000; animation-delay: 0s; }
        .light:nth-child(2) { background: #00ff00; animation-delay: 0.2s; }
        .light:nth-child(3) { background: #0000ff; animation-delay: 0.4s; }
        .light:nth-child(4) { background: #ffff00; animation-delay: 0.6s; }
        .light:nth-child(5) { background: #ff00ff; animation-delay: 0.8s; }

        @keyframes blink {
            0%, 100% { opacity: 1; box-shadow: 0 0 20px currentColor; }
            50% { opacity: 0.3; }
        }

        /* Santa */
        .santa {
            position: fixed;
            bottom: 20px;
            right: -200px;
            width: 150px;
            height: 150px;
            animation: santaFly 20s linear infinite;
            z-index: 50;
            font-size: 80px;
        }

        @keyframes santaFly {
            0% { right: -200px; }
            100% { right: 110%; }
        }

        /* Christmas tree decoration */
        .tree-decoration {
            position: fixed;
            bottom: 20px;
            left: 20px;
            font-size: 100px;
            animation: treeGlow 2s ease-in-out infinite;
            z-index: 2;
        }

        @keyframes treeGlow {
            0%, 100% { filter: brightness(1) drop-shadow(0 0 10px #00ff00); }
            50% { filter: brightness(1.3) drop-shadow(0 0 20px #ff0000); }
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 40px 20px;
            position: relative;
            z-index: 10;
        }

        .header {
            text-align: center;
            margin-bottom: 40px;
            padding: 30px;
            background: rgba(255, 255, 255, 0.1);
            backdrop-filter: blur(10px);
            border-radius: 20px;
            border: 2px solid rgba(255, 255, 255, 0.2);
            box-shadow: 0 8px 32px rgba(0, 0, 0, 0.3);
        }

        .header h1 {
            font-size: 3em;
            margin-bottom: 20px;
            background: linear-gradient(45deg, #ff6b6b, #4ecdc4, #45b7d1);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            animation: gradientShift 3s ease infinite;
        }

        @keyframes gradientShift {
            0%, 100% { filter: hue-rotate(0deg); }
            50% { filter: hue-rotate(45deg); }
        }

        .typing-animation {
            font-size: 1.3em;
            color: #6AD3F7;
            margin: 20px 0;
        }

        .gif-container {
            margin: 30px 0;
        }

        .gif-container img {
            max-width: 350px;
            border-radius: 20px;
            box-shadow: 0 10px 40px rgba(106, 211, 247, 0.3);
        }

        .section {
            background: rgba(255, 255, 255, 0.1);
            backdrop-filter: blur(10px);
            padding: 30px;
            margin: 30px 0;
            border-radius: 20px;
            border: 2px solid rgba(255, 255, 255, 0.2);
            box-shadow: 0 8px 32px rgba(0, 0, 0, 0.3);
        }

        .section h2 {
            font-size: 2em;
            margin-bottom: 25px;
            color: #6AD3F7;
            text-align: center;
        }

        .section h3 {
            font-size: 1.5em;
            margin: 25px 0 15px 0;
            text-align: center;
        }

        .tech-category {
            margin: 30px 0;
        }

        .badges {
            display: flex;
            flex-wrap: wrap;
            gap: 15px;
            justify-content: center;
            margin: 20px 0;
        }

        .badge {
            display: inline-block;
            transition: all 0.3s;
        }

        .badge img {
            height: 28px;
            transition: transform 0.3s;
        }

        .badge:hover img {
            transform: translateY(-5px) scale(1.1);
        }

        .connect-section {
            text-align: center;
        }

        .connect-buttons {
            display: flex;
            gap: 20px;
            justify-content: center;
            flex-wrap: wrap;
            margin: 30px 0;
        }

        .connect-btn {
            display: inline-block;
            transition: all 0.3s;
        }

        .connect-btn img {
            height: 28px;
            transition: transform 0.3s;
        }

        .connect-btn:hover img {
            transform: translateY(-5px) scale(1.1);
        }

        .opportunities {
            margin-top: 30px;
            padding: 20px;
            background: rgba(255, 255, 255, 0.05);
            border-radius: 15px;
            border-left: 4px solid #6AD3F7;
        }

        .opportunities h3 {
            color: #6AD3F7;
            margin-bottom: 15px;
        }

        .opportunities p {
            font-size: 1.1em;
            line-height: 1.8;
        }

        .quote {
            text-align: center;
            font-size: 1.3em;
            font-style: italic;
            margin: 40px 0;
            padding: 25px;
            background: rgba(255, 255, 255, 0.05);
            border-radius: 15px;
            border-left: 5px solid #6AD3F7;
        }

        .footer {
            text-align: center;
            margin-top: 50px;
            padding: 30px;
            background: rgba(255, 255, 255, 0.05);
            border-radius: 20px;
        }

        .profile-views {
            margin-top: 20px;
        }

        .profile-views img {
            height: 20px;
        }

        @media (max-width: 768px) {
            .header h1 { font-size: 2em; }
            .typing-animation { font-size: 1em; }
            .gif-container img { max-width: 250px; }
            .connect-buttons { flex-direction: column; align-items: center; }
        }
    </style>
</head>
<body>
    <div class="lights">
        <div class="light"></div>
        <div class="light"></div>
        <div class="light"></div>
        <div class="light"></div>
        <div class="light"></div>
        <div class="light"></div>
        <div class="light"></div>
        <div class="light"></div>
        <div class="light"></div>
        <div class="light"></div>
    </div>

    <div class="santa">🎅🛷</div>

    <div class="tree-decoration">🎄</div>

    <div class="container">
        <div class="header">
            <h1>👋 Xin chào, mình là Luan 🎄✨</h1>
            <div class="typing-animation">
                Full-Stack Web Developer • Always Learning New Technologies • Building Amazing Web Applications
            </div>
            <div class="gif-container">
                <img src="https://media.giphy.com/media/qgQUggAC3Pfv687qPC/giphy.gif" alt="Coding GIF">
            </div>
        </div>

        <div class="section">
            <h2>🛡️ Tech Arsenal</h2>
            
            <div class="tech-category">
                <h3 style="color: #ff6b6b;">🎨 Frontend Mastery</h3>
                <div class="badges">
                    <a href="https://developer.mozilla.org/en-US/docs/Web/HTML" class="badge">
                        <img src="https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white&labelColor=E34F26" alt="HTML5">
                    </a>
                    <a href="https://developer.mozilla.org/en-US/docs/Web/CSS" class="badge">
                        <img src="https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white&labelColor=1572B6" alt="CSS3">
                    </a>
                    <a href="https://javascript.info/" class="badge">
                        <img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black&labelColor=F7DF1E" alt="JavaScript">
                    </a>
                    <a href="https://reactjs.org/" class="badge">
                        <img src="https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB&labelColor=20232A" alt="React">
                    </a>
                    <a href="https://tailwindcss.com/" class="badge">
                        <img src="https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=for-the-badge&logo=tailwind-css&logoColor=white&labelColor=38B2AC" alt="TailwindCSS">
                    </a>
                </div>
            </div>

            <div class="tech-category">
                <h3 style="color: #4ecdc4;">⚙️ Backend Power</h3>
                <div class="badges">
                    <a href="https://nodejs.org/" class="badge">
                        <img src="https://img.shields.io/badge/Node.js-43853D?style=for-the-badge&logo=node.js&logoColor=white&labelColor=43853D" alt="Node.js">
                    </a>
                    <a href="https://expressjs.com/" class="badge">
                        <img src="https://img.shields.io/badge/Express.js-404D59?style=for-the-badge&logo=express&logoColor=white&labelColor=404D59" alt="Express.js">
                    </a>
                    <a href="https://www.mysql.com/" class="badge">
                        <img src="https://img.shields.io/badge/MySQL-00000F?style=for-the-badge&logo=mysql&logoColor=white&labelColor=00000F" alt="MySQL">
                    </a>
                    <a href="https://www.mongodb.com/" class="badge">
                        <img src="https://img.shields.io/badge/MongoDB-4EA94B?style=for-the-badge&logo=mongodb&logoColor=white&labelColor=4EA94B" alt="MongoDB">
                    </a>
                </div>
            </div>

            <div class="tech-category">
                <h3 style="color: #45b7d1;">🛠️ DevTools & Workflow</h3>
                <div class="badges">
                    <a href="https://code.visualstudio.com/" class="badge">
                        <img src="https://img.shields.io/badge/Visual_Studio_Code-0078D4?style=for-the-badge&logo=visual%20studio%20code&logoColor=white&labelColor=0078D4" alt="VS Code">
                    </a>
                    <a href="https://git-scm.com/" class="badge">
                        <img src="https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white&labelColor=F05032" alt="Git">
                    </a>
                    <a href="https://github.com/" class="badge">
                        <img src="https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white&labelColor=100000" alt="GitHub">
                    </a>
                    <a href="https://www.figma.com/" class="badge">
                        <img src="https://img.shields.io/badge/Figma-F24E1E?style=for-the-badge&logo=figma&logoColor=white&labelColor=F24E1E" alt="Figma">
                    </a>
                </div>
            </div>
        </div>

        <div class="section connect-section">
            <h2>📫 Let's Connect & Collaborate</h2>
            <div class="connect-buttons">
                <a href="https://www.facebook.com/luan.le.355745" class="connect-btn">
                    <img src="https://img.shields.io/badge/Facebook-1877F2?style=for-the-badge&logo=facebook&logoColor=white&labelColor=1877F2" alt="Facebook">
                </a>
                <a href="mailto:quangluan03052000@gmail.com" class="connect-btn">
                    <img src="https://img.shields.io/badge/Gmail-D14836?style=for-the-badge&logo=gmail&logoColor=white&labelColor=D14836" alt="Gmail">
                </a>
                <a href="https://github.com/luanPro35" class="connect-btn">
                    <img src="https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white&labelColor=100000" alt="GitHub">
                </a>
                <a href="#" class="connect-btn">
                    <img src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white&labelColor=0077B5" alt="LinkedIn">
                </a>
            </div>
            
            <div class="opportunities">
                <h3>💬 Open for opportunities in:</h3>
                <p>
                    <code>Frontend Development</code> • 
                    <code>Backend Development</code> • 
                    <code>Full-Stack Projects</code> • 
                    <code>Code Review</code> • 
                    <code>Tech Mentoring</code>
                </p>
            </div>
        </div>

        <div class="quote">
            💡 "Code is like humor. When you have to explain it, it's bad." - Cory House
        </div>

        <div class="footer">
            <h2 style="margin-bottom: 20px; color: #6AD3F7;">🎄 Merry Christmas & Happy Coding! 🎅</h2>
            <p style="font-size: 1.2em; margin-bottom: 20px;">Thanks for visiting! ⭐</p>
            <div class="profile-views">
                <img src="https://komarev.com/ghpvc/?username=luanPro35&label=Profile+Views&color=6AD3F7&style=flat-square" alt="Profile Views">
            </div>
        </div>
    </div>

    <script>
        function createSnowflake() {
            const snowflake = document.createElement('div');
            snowflake.classList.add('snowflake');
            snowflake.innerHTML = '❄';
            snowflake.style.left = Math.random() * 100 + '%';
            snowflake.style.animationDuration = Math.random() * 3 + 2 + 's';
            snowflake.style.opacity = Math.random();
            snowflake.style.fontSize = Math.random() * 10 + 10 + 'px';
            document.body.appendChild(snowflake);

            setTimeout(() => {
                snowflake.remove();
            }, 5000);
        }

        setInterval(createSnowflake, 200);
    </script>
</body>
</html>
