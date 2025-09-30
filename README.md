<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Riya Prashant Pandaokar - Portfolio</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: #fff;
            min-height: 100vh;
            padding: 40px 20px;
            overflow-x: hidden;
        }

        .container {
            max-width: 900px;
            margin: 0 auto;
        }

        h1 {
            text-align: center;
            font-size: 3em;
            margin-bottom: 10px;
            animation: fadeInDown 1s ease-out;
        }

        .wave {
            display: inline-block;
            animation: wave 2s ease-in-out infinite;
            transform-origin: 70% 70%;
        }

        @keyframes wave {
            0%, 100% { transform: rotate(0deg); }
            10%, 30% { transform: rotate(14deg); }
            20% { transform: rotate(-8deg); }
            40% { transform: rotate(-4deg); }
            50% { transform: rotate(10deg); }
        }

        h3 {
            text-align: center;
            font-size: 1.5em;
            margin-bottom: 40px;
            opacity: 0;
            animation: fadeIn 1s ease-out 0.5s forwards;
        }

        .info-section {
            background: rgba(255, 255, 255, 0.1);
            backdrop-filter: blur(10px);
            border-radius: 15px;
            padding: 30px;
            margin-bottom: 30px;
            box-shadow: 0 8px 32px rgba(0, 0, 0, 0.1);
            opacity: 0;
            transform: translateY(30px);
            animation: slideUp 0.8s ease-out 1s forwards;
        }

        .info-item {
            margin: 20px 0;
            padding: 15px;
            background: rgba(255, 255, 255, 0.05);
            border-radius: 10px;
            border-left: 4px solid #fff;
            transition: all 0.3s ease;
        }

        .info-item:hover {
            transform: translateX(10px);
            background: rgba(255, 255, 255, 0.15);
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.2);
        }

        .section-title {
            font-size: 1.8em;
            margin-bottom: 20px;
            text-align: center;
            position: relative;
            display: inline-block;
            width: 100%;
        }

        .section-title::after {
            content: '';
            display: block;
            width: 100px;
            height: 3px;
            background: #fff;
            margin: 10px auto;
            animation: expandWidth 1s ease-out;
        }

        @keyframes expandWidth {
            from { width: 0; }
            to { width: 100px; }
        }

        .social-links {
            display: flex;
            justify-content: center;
            gap: 30px;
            margin: 30px 0;
        }

        .social-link {
            width: 60px;
            height: 60px;
            background: rgba(255, 255, 255, 0.2);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            text-decoration: none;
            color: #fff;
            font-size: 24px;
            transition: all 0.3s ease;
            animation: bounceIn 0.6s ease-out;
        }

        .social-link:nth-child(1) { animation-delay: 1.2s; opacity: 0; animation-fill-mode: forwards; }
        .social-link:nth-child(2) { animation-delay: 1.4s; opacity: 0; animation-fill-mode: forwards; }

        .social-link:hover {
            transform: translateY(-10px) scale(1.1);
            background: rgba(255, 255, 255, 0.4);
            box-shadow: 0 10px 25px rgba(0, 0, 0, 0.3);
        }

        .tools-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(100px, 1fr));
            gap: 20px;
            margin-top: 30px;
        }

        .tool-item {
            background: rgba(255, 255, 255, 0.1);
            padding: 20px;
            border-radius: 10px;
            text-align: center;
            transition: all 0.3s ease;
            opacity: 0;
            animation: fadeInScale 0.5s ease-out forwards;
        }

        .tool-item:nth-child(1) { animation-delay: 1.5s; }
        .tool-item:nth-child(2) { animation-delay: 1.6s; }
        .tool-item:nth-child(3) { animation-delay: 1.7s; }
        .tool-item:nth-child(4) { animation-delay: 1.8s; }
        .tool-item:nth-child(5) { animation-delay: 1.9s; }
        .tool-item:nth-child(6) { animation-delay: 2s; }
        .tool-item:nth-child(7) { animation-delay: 2.1s; }
        .tool-item:nth-child(8) { animation-delay: 2.2s; }

        .tool-item:hover {
            transform: translateY(-10px) rotate(5deg);
            background: rgba(255, 255, 255, 0.25);
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.3);
        }

        @keyframes fadeInDown {
            from {
                opacity: 0;
                transform: translateY(-30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        @keyframes fadeIn {
            from { opacity: 0; }
            to { opacity: 1; }
        }

        @keyframes slideUp {
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        @keyframes bounceIn {
            0% {
                opacity: 0;
                transform: scale(0.3);
            }
            50% {
                transform: scale(1.05);
            }
            70% {
                transform: scale(0.9);
            }
            100% {
                opacity: 1;
                transform: scale(1);
            }
        }

        @keyframes fadeInScale {
            from {
                opacity: 0;
                transform: scale(0.8);
            }
            to {
                opacity: 1;
                transform: scale(1);
            }
        }

        .email-link {
            color: #fff;
            text-decoration: none;
            border-bottom: 2px solid transparent;
            transition: border-color 0.3s ease;
        }

        .email-link:hover {
            border-bottom-color: #fff;
        }

        .resume-link {
            display: inline-block;
            color: #fff;
            text-decoration: none;
            padding: 10px 20px;
            background: rgba(255, 255, 255, 0.2);
            border-radius: 25px;
            transition: all 0.3s ease;
            margin-top: 10px;
        }

        .resume-link:hover {
            background: rgba(255, 255, 255, 0.3);
            transform: scale(1.05);
        }

        @media (max-width: 768px) {
            h1 { font-size: 2em; }
            h3 { font-size: 1.2em; }
            .tools-grid { grid-template-columns: repeat(auto-fit, minmax(80px, 1fr)); }
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>Hi <span class="wave">👋</span>, I'm Riya Prashant Pandaokar</h1>
        <h3>A passionate frontend developer from Nashik (India)</h3>

        <div class="info-section">
            <div class="info-item">
                🔭 I'm currently working on <strong>Mess Food Rating App</strong>
            </div>
            <div class="info-item">
                🌱 I'm currently learning <strong>Flutter, Android Studio</strong>
            </div>
            <div class="info-item">
                📫 How to reach me: <a href="mailto:riyapandaokar@gmail.com" class="email-link">riyapandaokar@gmail.com</a>
            </div>
            <div class="info-item">
                📄 <a href="https://docs.google.com/document/d/1GdRj0LE7WRLEBGST4vmM6l4tGGj9LARm3zR39NO8llM/edit?usp=drive_link" target="_blank" class="resume-link">View My Resume</a>
            </div>
        </div>

        <div class="info-section">
            <h2 class="section-title">Connect with me</h2>
            <div class="social-links">
                <a href="https://linkedin.com/in/riya pandaokar" target="_blank" class="social-link" title="LinkedIn">
                    💼
                </a>
                <a href="https://instagram.com/the_bornartist" target="_blank" class="social-link" title="Instagram">
                    📷
                </a>
            </div>
        </div>

        <div class="info-section">
            <h2 class="section-title">Languages & Tools</h2>
            <div class="tools-grid">
                <div class="tool-item">Android</div>
                <div class="tool-item">Angular</div>
                <div class="tool-item">Flutter</div>
                <div class="tool-item">React</div>
                <div class="tool-item">Python</div>
                <div class="tool-item">Java</div>
                <div class="tool-item">JavaScript</div>
                <div class="tool-item">C++</div>
                <div class="tool-item">Kotlin</div>
                <div class="tool-item">Dart</div>
                <div class="tool-item">Django</div>
                <div class="tool-item">Firebase</div>
                <div class="tool-item">MongoDB</div>
                <div class="tool-item">MySQL</div>
                <div class="tool-item">PostgreSQL</div>
                <div class="tool-item">Git</div>
                <div class="tool-item">AWS</div>
                <div class="tool-item">GCP</div>
                <div class="tool-item">Figma</div>
                <div class="tool-item">Unity</div>
            </div>
        </div>
    </div>
</body>
</html>
