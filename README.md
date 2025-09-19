<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Deepak Nigam - GitHub Profile</title>
    <style>
        body {
            font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Helvetica, Arial, sans-serif;
            background: linear-gradient(135deg, #0d1117 0%, #161b22 100%);
            color: #e6edf3;
            margin: 0;
            padding: 20px;
            line-height: 1.6;
        }
        .container {
            max-width: 1000px;
            margin: 0 auto;
            background: #0d1117;
            border-radius: 16px;
            padding: 40px;
            box-shadow: 0 16px 32px rgba(0, 0, 0, 0.4);
            border: 1px solid #30363d;
        }
        .header {
            text-align: center;
            margin-bottom: 40px;
        }
        
        .header h1 {
            font-size: 3rem;
            background: linear-gradient(45deg, #36BCF7, #9945FF);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            margin-bottom: 20px;
            animation: glow 2s ease-in-out infinite alternate;
        }
        
        @keyframes glow {
            from { filter: drop-shadow(0 0 10px #36BCF7); }
            to { filter: drop-shadow(0 0 20px #9945FF); }
        }
        
        .typing-animation {
            background: linear-gradient(45deg, #36BCF7, #FF6B6B, #4ECDC4, #45B7D1);
            background-size: 400% 400%;
            animation: gradient 4s ease infinite;
            padding: 15px 25px;
            border-radius: 25px;
            font-size: 1.2rem;
            font-weight: bold;
            margin: 20px 0;
            text-align: center;
            overflow: hidden;
            white-space: nowrap;
            border-right: 3px solid;
            animation: typing 4s steps(40) infinite, gradient 4s ease infinite;
        }
        
        @keyframes typing {
            0%, 90% { width: 100%; }
            95%, 100% { width: 0; }
        }
        
        @keyframes gradient {
            0% { background-position: 0% 50%; }
            50% { background-position: 100% 50%; }
            100% { background-position: 0% 50%; }
        }
        
        .badges {
            display: flex;
            justify-content: center;
            gap: 15px;
            margin: 20px 0;
            flex-wrap: wrap;
        }
        
        .badge {
            background: linear-gradient(45deg, #28a745, #20c997);
            color: white;
            padding: 8px 16px;
            border-radius: 20px;
            font-size: 0.9rem;
            font-weight: bold;
            text-decoration: none;
            transition: all 0.3s ease;
            border: 2px solid transparent;
        }
        
        .badge:hover {
            transform: translateY(-3px);
            box-shadow: 0 10px 25px rgba(40, 167, 69, 0.4);
            border-color: #28a745;
        }
        
        .section {
            margin: 50px 0;
            padding: 30px;
            background: rgba(22, 27, 34, 0.8);
            border-radius: 16px;
            border-left: 4px solid #36BCF7;
            backdrop-filter: blur(10px);
        }
        
        .section h2 {
            color: #36BCF7;
            font-size: 2rem;
            margin-bottom: 20px;
            display: flex;
            align-items: center;
            gap: 10px;
        }
        
        .about-section {
            display: grid;
            grid-template-columns: 1fr 300px;
            gap: 30px;
            align-items: start;
        }
        
        .coding-gif {
            width: 300px;
            height: auto;
            border-radius: 15px;
            box-shadow: 0 10px 30px rgba(54, 188, 247, 0.3);
            animation: float 3s ease-in-out infinite;
        }
        
        @keyframes float {
            0%, 100% { transform: translateY(0px); }
            50% { transform: translateY(-10px); }
        }
        
        .tech-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
            margin: 30px 0;
        }
        
        .tech-category {
            background: rgba(30, 35, 42, 0.9);
            padding: 25px;
            border-radius: 12px;
            border: 1px solid #30363d;
            transition: all 0.3s ease;
        }
        
        .tech-category:hover {
            transform: translateY(-5px);
            box-shadow: 0 15px 35px rgba(54, 188, 247, 0.2);
            border-color: #36BCF7;
        }
        
        .tech-category h3 {
            color: #36BCF7;
            margin-bottom: 15px;
            font-size: 1.3rem;
        }
        
        .tech-badges {
            display: flex;
            flex-wrap: wrap;
            gap: 8px;
        }
        
        .tech-badge {
            background: linear-gradient(45deg, #FF6B6B, #4ECDC4);
            color: white;
            padding: 6px 12px;
            border-radius: 15px;
            font-size: 0.8rem;
            font-weight: bold;
            transition: all 0.3s ease;
            cursor: pointer;
        }
        
        .tech-badge:hover {
            transform: scale(1.1);
            box-shadow: 0 5px 15px rgba(255, 107, 107, 0.4);
        }
        
        .stats-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(400px, 1fr));
            gap: 20px;
            margin: 30px 0;
        }
        
        .stat-card {
            background: rgba(22, 27, 34, 0.9);
            border: 1px solid #30363d;
            border-radius: 12px;
            padding: 20px;
            text-align: center;
            transition: all 0.3s ease;
            position: relative;
            overflow: hidden;
        }
        
        .stat-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: linear-gradient(90deg, transparent, rgba(54, 188, 247, 0.1), transparent);
            transition: left 0.5s;
        }
        
        .stat-card:hover::before {
            left: 100%;
        }
        
        .stat-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 15px 35px rgba(54, 188, 247, 0.2);
            border-color: #36BCF7;
        }
        
        .stat-image {
            width: 100%;
            height: auto;
            border-radius: 8px;
            background: rgba(30, 35, 42, 0.8);
            padding: 10px;
        }
        
        .trophy-section {
            text-align: center;
            background: linear-gradient(135deg, rgba(255, 215, 0, 0.1), rgba(255, 140, 0, 0.1));
            border: 1px solid rgba(255, 215, 0, 0.3);
            border-radius: 15px;
            padding: 30px;
            margin: 30px 0;
        }
        
        .trophy-image {
            width: 100%;
            height: auto;
            filter: drop-shadow(0 5px 15px rgba(255, 215, 0, 0.3));
        }
        
        .connect-section {
            text-align: center;
        }
        
        .social-links {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin: 20px 0;
            flex-wrap: wrap;
        }
        
        .social-badge {
            background: linear-gradient(45deg, #0077B5, #00A0DC);
            color: white;
            padding: 12px 24px;
            border-radius: 25px;
            text-decoration: none;
            font-weight: bold;
            transition: all 0.3s ease;
            display: flex;
            align-items: center;
            gap: 8px;
        }
        
        .social-badge:hover {
            transform: translateY(-3px) scale(1.05);
            box-shadow: 0 10px 25px rgba(0, 119, 181, 0.4);
        }
        
        .footer {
            text-align: center;
            margin-top: 50px;
            padding: 30px;
            background: linear-gradient(45deg, #36BCF7, #9945FF);
            border-radius: 15px;
            position: relative;
            overflow: hidden;
        }
        
        .footer::before {
            content: '';
            position: absolute;
            top: -50%;
            left: -50%;
            width: 200%;
            height: 200%;
            background: repeating-linear-gradient(
                45deg,
                transparent,
                transparent 10px,
                rgba(255, 255, 255, 0.1) 10px,
                rgba(255, 255, 255, 0.1) 20px
            );
            animation: slide 3s linear infinite;
        }
        
        @keyframes slide {
            0% { transform: translate(-50%, -50%); }
            100% { transform: translate(-30%, -30%); }
        }
        
        .footer h3 {
            position: relative;
            z-index: 1;
            color: white;
            font-size: 1.5rem;
            margin: 0;
        }
        
        .emoji {
            font-size: 1.5em;
            animation: bounce 2s infinite;
        }
        
        @keyframes bounce {
            0%, 20%, 50%, 80%, 100% { transform: translateY(0); }
            40% { transform: translateY(-10px); }
            60% { transform: translateY(-5px); }
        }
        
        @media (max-width: 768px) {
            .about-section {
                grid-template-columns: 1fr;
                text-align: center;
            }
            
            .coding-gif {
                width: 250px;
            }
            
            .stats-grid {
                grid-template-columns: 1fr;
            }
            
            .header h1 {
                font-size: 2rem;
            }
        }
        
        .pulse {
            animation: pulse 2s infinite;
        }
        
        @keyframes pulse {
            0% { opacity: 1; }
            50% { opacity: 0.7; }
            100% { opacity: 1; }
        }
    </style>
</head>
<body>
    <div class="container">
        <!-- Header Section -->
        <div class="header">
            <h1><span class="emoji">👋</span> Hi there, I'm Deepak Nigam!</h1>
            
            <div class="typing-animation">
                Full Stack Developer • Software Engineer • Problem Solver • Code Enthusiast
            </div>
            
            <div class="badges">
                <span class="badge">Profile Views: 1,234</span>
                <span class="badge">Followers: 156</span>
            </div>
        </div>

        <!-- About Section -->
        <div class="section">
            <h2><span class="emoji">🚀</span> About Me</h2>
            <div class="about-section">
                <div>
                    <p><strong>🎯 Passionate Software Developer</strong> from India 🇮🇳</p>
                    <p><strong>🔭 Currently working on:</strong> Full-stack web applications and mobile development</p>
                    <p><strong>🌱 Learning:</strong> Advanced React, Cloud Technologies, and System Design</p>
                    <p><strong>👨‍💻 Experience:</strong> Building scalable applications with modern tech stack</p>
                    <p><strong>💡 Interests:</strong> Problem solving, competitive programming, and open source</p>
                    <p><strong>📫 Reach me:</strong> deepaknigam2004@gmail.com</p>
                    <p><strong>⚡ Fun fact:</strong> I debug code faster than I debug my life! 😄</p>
                </div>
                <div>
                    <img src="https://media.giphy.com/media/SWoSkN6DxTszqIKEqv/giphy.gif" alt="Coding" class="coding-gif">
                </div>
            </div>
        </div>

        <!-- Tech Stack Section -->
        <div class="section">
            <h2><span class="emoji">🛠️</span> Tech Stack & Tools</h2>
            <div class="tech-grid">
                <div class="tech-category">
                    <h3>Languages</h3>
                    <div class="tech-badges">
                        <span class="tech-badge">C</span>
                        <span class="tech-badge">C++</span>
                        <span class="tech-badge">Java</span>
                        <span class="tech-badge">Python</span>
                        <span class="tech-badge">JavaScript</span>
                        <span class="tech-badge">Dart</span>
                        <span class="tech-badge">PHP</span>
                    </div>
                </div>
                
                <div class="tech-category">
                    <h3>Frontend</h3>
                    <div class="tech-badges">
                        <span class="tech-badge">HTML5</span>
                        <span class="tech-badge">CSS3</span>
                        <span class="tech-badge">React</span>
                        <span class="tech-badge">Flutter</span>
                    </div>
                </div>
                
                <div class="tech-category">
                    <h3>Backend & Database</h3>
                    <div class="tech-badges">
                        <span class="tech-badge">Node.js</span>
                        <span class="tech-badge">Spring</span>
                        <span class="tech-badge">MySQL</span>
                        <span class="tech-badge">PostgreSQL</span>
                        <span class="tech-badge">MongoDB</span>
                        <span class="tech-badge">SQLite</span>
                    </div>
                </div>
                
                <div class="tech-category">
                    <h3>Tools & Technologies</h3>
                    <div class="tech-badges">
                        <span class="tech-badge">Git</span>
                        <span class="tech-badge">Docker</span>
                        <span class="tech-badge">Firebase</span>
                        <span class="tech-badge">Postman</span>
                        <span class="tech-badge">Linux</span>
                        <span class="tech-badge">Illustrator</span>
                    </div>
                </div>
            </div>
        </div>

        <!-- Trophies Section -->
        <div class="trophy-section">
            <h2><span class="emoji">🏆</span> GitHub Trophies</h2>
            <div style="background: rgba(0,0,0,0.3); padding: 20px; border-radius: 10px; color: #FFD700;">
                <div style="display: flex; justify-content: center; gap: 20px; flex-wrap: wrap;">
                    <div style="text-align: center;">
                        <div style="font-size: 2rem;">🥇</div>
                        <div>MultiLanguage</div>
                    </div>
                    <div style="text-align: center;">
                        <div style="font-size: 2rem;">🥈</div>
                        <div>Commits</div>
                    </div>
                    <div style="text-align: center;">
                        <div style="font-size: 2rem;">🥉</div>
                        <div>Repositories</div>
                    </div>
                    <div style="text-align: center;">
                        <div style="font-size: 2rem;">⭐</div>
                        <div>Stars</div>
                    </div>
                    <div style="text-align: center;">
                        <div style="font-size: 2rem;">🔥</div>
                        <div>Streak</div>
                    </div>
                </div>
            </div>
        </div>

        <!-- GitHub Stats Section -->
        <div class="section">
            <h2><span class="emoji">📊</span> GitHub Statistics</h2>
            <div class="stats-grid">
                <div class="stat-card">
                    <h3>GitHub Stats</h3>
                    <div style="background: linear-gradient(45deg, #1a1b27, #2d3748); padding: 20px; border-radius: 10px;">
                        <div style="color: #36BCF7; font-size: 1.5rem; margin: 10px 0;">⭐ 234 Total Stars</div>
                        <div style="color: #4ECDC4; font-size: 1.5rem; margin: 10px 0;">📦 45 Public Repos</div>
                        <div style="color: #FF6B6B; font-size: 1.5rem; margin: 10px 0;">🔥 156 Contributions</div>
                    </div>
                </div>
                
                <div class="stat-card">
                    <h3>Most Used Languages</h3>
                    <div style="background: linear-gradient(45deg, #1a1b27, #2d3748); padding: 20px; border-radius: 10px;">
                        <div style="margin: 10px 0; display: flex; justify-content: space-between;">
                            <span>JavaScript</span>
                            <span style="color: #F7DF1E;">32.5%</span>
                        </div>
                        <div style="margin: 10px 0; display: flex; justify-content: space-between;">
                            <span>Python</span>
                            <span style="color: #3776AB;">28.1%</span>
                        </div>
                        <div style="margin: 10px 0; display: flex; justify-content: space-between;">
                            <span>Java</span>
                            <span style="color: #ED8B00;">21.3%</span>
                        </div>
                        <div style="margin: 10px 0; display: flex; justify-content: space-between;">
                            <span>C++</span>
                            <span style="color: #00599C;">18.1%</span>
                        </div>
                    </div>
                </div>
            </div>
        </div>

        <!-- Coding Profiles Section -->
        <div class="section">
            <h2><span class="emoji">💻</span> Coding Profiles</h2>
            <div class="social-links">
                <a href="#" class="social-badge" style="background: linear-gradient(45deg, #FFA116, #FF8C00);">
                    <span>🟨</span> LeetCode
                </a>
                <a href="#" class="social-badge" style="background: linear-gradient(45deg, #5B4638, #8B4513);">
                    <span>👨‍🍳</span> CodeChef
                </a>
            </div>
        </div>

        <!-- Connect Section -->
        <div class="section connect-section">
            <h2><span class="emoji">🤝</span> Connect With Me</h2>
            <div class="social-links">
                <a href="#" class="social-badge">
                    <span>💼</span> LinkedIn
                </a>
                <a href="#" class="social-badge" style="background: linear-gradient(45deg, #D14836, #EA4335);">
                    <span>📧</span> Gmail
                </a>
                <a href="#" class="social-badge" style="background: linear-gradient(45deg, #333, #24292e);">
                    <span>🐙</span> GitHub
                </a>
            </div>
        </div>

        <!-- Quote Section -->
        <div class="section" style="text-align: center;">
            <h2><span class="emoji">🎨</span> Random Dev Quote</h2>
            <div style="background: rgba(54, 188, 247, 0.1); border: 2px solid #36BCF7; border-radius: 15px; padding: 25px; font-style: italic; font-size: 1.2rem;">
                "The only way to learn a new programming language is by writing programs in it." - Dennis Ritchie
            </div>
        </div>

        <!-- Footer -->
        <div class="footer">
            <h3><span class="emoji">🙏</span> Thanks for visiting! Happy coding! <span class="emoji">💻</span></h3>
            <p style="margin: 10px 0; position: relative; z-index: 1;">⭐ Star my repositories if you like them!</p>
        </div>
    </div>

    <script>
        // Add some interactive effects
        document.addEventListener('DOMContentLoaded', function() {
            // Animate tech badges on hover
            const techBadges = document.querySelectorAll('.tech-badge');
            techBadges.forEach(badge => {
                badge.addEventListener('mouseenter', function() {
                    this.style.transform = 'scale(1.1) rotate(5deg)';
                });
                
                badge.addEventListener('mouseleave', function() {
                    this.style.transform = 'scale(1) rotate(0deg)';
                });
            });
            
            // Add sparkle effect to trophies
            const trophySection = document.querySelector('.trophy-section');
            setInterval(() => {
                const sparkle = document.createElement('div');
                sparkle.innerHTML = '✨';
                sparkle.style.position = 'absolute';
                sparkle.style.fontSize = '1rem';
                sparkle.style.animation = 'sparkle 2s ease-out forwards';
                sparkle.style.left = Math.random() * 100 + '%';
                sparkle.style.top = Math.random() * 100 + '%';
                sparkle.style.pointerEvents = 'none';
                
                const style = document.createElement('style');
                style.textContent = `
                    @keyframes sparkle {
                        0% { opacity: 1; transform: scale(0) rotate(0deg); }
                        50% { opacity: 1; transform: scale(1) rotate(180deg); }
                        100% { opacity: 0; transform: scale(0) rotate(360deg); }
                    }
                `;
                document.head.appendChild(style);
                
                trophySection.appendChild(sparkle);
                setTimeout(() => sparkle.remove(), 2000);
            }, 3000);
        });
    </script>
</body>
</html>
