<!DOCTYPE html>
<html>
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Full Stack Developer | React • Next.js • Node.js</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: linear-gradient(135deg, #0f172a, #1e293b);
            color: #e2e8f0;
            line-height: 1.6;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 2rem;
        }

        .header {
            text-align: center;
            padding: 3rem 0;
            background: linear-gradient(135deg, #6366f1, #8b5cf6);
            border-radius: 20px;
            margin-bottom: 3rem;
            position: relative;
            overflow: hidden;
        }

        .header::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: url('data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1000 100" fill="%23ffffff20"><polygon points="0,100 1000,0 1000,100"/></svg>');
            background-size: cover;
        }

        .profile-img {
            width: 150px;
            height: 150px;
            border-radius: 50%;
            border: 4px solid white;
            margin: 0 auto 1rem;
            background: linear-gradient(45deg, #ff6b6b, #4ecdc4);
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 3rem;
            color: white;
        }

        h1 {
            font-size: 3rem;
            margin-bottom: 0.5rem;
            background: linear-gradient(45deg, #fff, #cbd5e1);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }

        .tagline {
            font-size: 1.4rem;
            opacity: 0.9;
            margin-bottom: 1rem;
        }

        .stats {
            display: flex;
            justify-content: center;
            gap: 2rem;
            margin: 1.5rem 0;
        }

        .stat {
            text-align: center;
        }

        .stat-number {
            font-size: 2rem;
            font-weight: bold;
            color: #fbbf24;
        }

        .badges {
            display: flex;
            flex-wrap: wrap;
            gap: 1rem;
            justify-content: center;
            margin: 1rem 0;
        }

        .badge {
            background: rgba(255, 255, 255, 0.1);
            padding: 0.5rem 1rem;
            border-radius: 20px;
            border: 1px solid rgba(255, 255, 255, 0.2);
            backdrop-filter: blur(10px);
        }

        .section {
            background: rgba(30, 41, 59, 0.8);
            padding: 2rem;
            border-radius: 15px;
            margin-bottom: 2rem;
            border: 1px solid rgba(255, 255, 255, 0.1);
            backdrop-filter: blur(10px);
        }

        h2 {
            color: #fbbf24;
            margin-bottom: 1.5rem;
            font-size: 1.8rem;
            border-bottom: 2px solid #fbbf24;
            padding-bottom: 0.5rem;
        }

        .tech-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 1.5rem;
        }

        .tech-category {
            background: rgba(15, 23, 42, 0.6);
            padding: 1.5rem;
            border-radius: 10px;
            border-left: 4px solid #6366f1;
        }

        .tech-list {
            list-style: none;
        }

        .tech-list li {
            padding: 0.5rem 0;
            border-bottom: 1px solid rgba(255, 255, 255, 0.1);
        }

        .tech-list li:last-child {
            border-bottom: none;
        }

        .projects {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
            gap: 2rem;
        }

        .project-card {
            background: rgba(15, 23, 42, 0.6);
            padding: 1.5rem;
            border-radius: 15px;
            border: 1px solid rgba(255, 255, 255, 0.1);
            transition: transform 0.3s ease, border-color 0.3s ease;
        }

        .project-card:hover {
            transform: translateY(-5px);
            border-color: #6366f1;
        }

        .project-title {
            color: #fbbf24;
            font-size: 1.3rem;
            margin-bottom: 1rem;
        }

        .project-tech {
            display: flex;
            flex-wrap: wrap;
            gap: 0.5rem;
            margin: 1rem 0;
        }

        .tech-tag {
            background: #6366f1;
            color: white;
            padding: 0.3rem 0.8rem;
            border-radius: 15px;
            font-size: 0.8rem;
        }

        .contact-links {
            display: flex;
            justify-content: center;
            gap: 1rem;
            flex-wrap: wrap;
        }

        .contact-btn {
            background: linear-gradient(45deg, #6366f1, #8b5cf6);
            color: white;
            padding: 0.8rem 1.5rem;
            border-radius: 25px;
            text-decoration: none;
            transition: transform 0.3s ease;
            display: flex;
            align-items: center;
            gap: 0.5rem;
        }

        .contact-btn:hover {
            transform: scale(1.05);
        }

        .quote {
            text-align: center;
            font-style: italic;
            opacity: 0.8;
            margin: 2rem 0;
            padding: 1rem;
            border-left: 3px solid #fbbf24;
            background: rgba(251, 191, 36, 0.1);
        }

        @media (max-width: 768px) {
            .container {
                padding: 1rem;
            }
            
            h1 {
                font-size: 2rem;
            }
            
            .stats {
                flex-direction: column;
                gap: 1rem;
            }
            
            .tech-grid {
                grid-template-columns: 1fr;
            }
            
            .projects {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <!-- Header Section -->
        <header class="header">
            <div class="profile-img">🚀</div>
            <h1>Your Name</h1>
            <div class="tagline">Full Stack & Vibe Coding Specialist</div>
            <div class="badges">
                <div class="badge">7+ Years Experience</div>
                <div class="badge">100+ Projects</div>
                <div class="badge">React Expert</div>
                <div class="badge">TypeScript</div>
            </div>
            <div class="stats">
                <div class="stat">
                    <div class="stat-number">7+</div>
                    <div>Years</div>
                </div>
                <div class="stat">
                    <div class="stat-number">100+</div>
                    <div>Projects</div>
                </div>
                <div class="stat">
                    <div class="stat-number">50+</div>
                    <div>Clients</div>
                </div>
                <div class="stat">
                    <div class="stat-number">99%</div>
                    <div>Satisfaction</div>
                </div>
            </div>
        </header>

        <!-- About Section -->
        <section class="section">
            <h2>👨‍💻 About Me</h2>
            <p>Dedicated Full Stack Developer with 7+ years of experience specializing in React, Next.js, Node.js, and TypeScript. I deliver scalable and high-performance web applications by combining modern frontend frameworks with powerful backend technologies.</p>
            <div class="quote">
                "Building seamless, maintainable, and efficient full stack solutions tailored to business needs."
            </div>
        </section>

        <!-- Tech Stack Section -->
        <section class="section">
            <h2>🛠 Tech Stack</h2>
            <div class="tech-grid">
                <div class="tech-category">
                    <h3>🎨 Frontend</h3>
                    <ul class="tech-list">
                        <li>React.js ⚛️</li>
                        <li>Next.js 🔥</li>
                        <li>TypeScript 📘</li>
                        <li>Redux 🗳️</li>
                        <li>Tailwind CSS 🎨</li>
                    </ul>
                </div>
                <div class="tech-category">
                    <h3>⚙️ Backend</h3>
                    <ul class="tech-list">
                        <li>Node.js 🟢</li>
                        <li>Express.js 🚂</li>
                        <li>REST APIs 🌐</li>
                        <li>GraphQL 🔷</li>
                        <li>Microservices 🏗️</li>
                    </ul>
                </div>
                <div class="tech-category">
                    <h3>🗄️ Database</h3>
                    <ul class="tech-list">
                        <li>MongoDB 🍃</li>
                        <li>PostgreSQL 🐘</li>
                        <li>MySQL 🐬</li>
                        <li>Firebase 🔥</li>
                        <li>Supabase 🟦</li>
                    </ul>
                </div>
            </div>
        </section>

        <!-- Projects Section -->
        <section class="section">
            <h2>🚀 Featured Projects</h2>
            <div class="projects">
                <div class="project-card">
                    <div class="project-title">E-Commerce Platform</div>
                    <p>Full-stack e-commerce solution with Next.js, TypeScript, and PostgreSQL. Features include payment integration, admin dashboard, and real-time inventory.</p>
                    <div class="project-tech">
                        <span class="tech-tag">Next.js</span>
                        <span class="tech-tag">TypeScript</span>
                        <span class="tech-tag">PostgreSQL</span>
                        <span class="tech-tag">Stripe</span>
                    </div>
                    <div class="stats">
                        <div class="stat">
                            <div class="stat-number">40%</div>
                            <div>Faster Load</div>
                        </div>
                        <div class="stat">
                            <div class="stat-number">20%</div>
                            <div>More Sales</div>
                        </div>
                    </div>
                </div>

                <div class="project-card">
                    <div class="project-title">SaaS Analytics Dashboard</div>
                    <p>Real-time analytics platform with React, Node.js, and MongoDB. Handles data visualization, user management, and automated reporting.</p>
                    <div class="project-tech">
                        <span class="tech-tag">React</span>
                        <span class="tech-tag">Node.js</span>
                        <span class="tech-tag">MongoDB</span>
                        <span class="tech-tag">D3.js</span>
                    </div>
                    <div class="stats">
                        <div class="stat">
                            <div class="stat-number">10k+</div>
                            <div>Users</div>
                        </div>
                        <div class="stat">
                            <div class="stat-number">99.9%</div>
                            <div>Uptime</div>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <!-- Contact Section -->
        <section class="section">
            <h2>📞 Let's Connect</h2>
            <p>Ready to bring your next project to life? Let's discuss how we can work together to create something amazing!</p>
            <div class="contact-links">
                <a href="https://github.com/yourusername" class="contact-btn">
                    <span>GitHub</span>
                </a>
                <a href="https://linkedin.com/in/yourprofile" class="contact-btn">
                    <span>LinkedIn</span>
                </a>
                <a href="mailto:your.email@domain.com" class="contact-btn">
                    <span>Email</span>
                </a>
                <a href="https://yourportfolio.com" class="contact-btn">
                    <span>Portfolio</span>
                </a>
            </div>
        </section>

        <!-- Footer -->
        <footer style="text-align: center; margin-top: 3rem; opacity: 0.7;">
            <p>© 2024 Your Name. Crafted with 💻 and ☕</p>
            <p style="margin-top: 0.5rem;">Available for freelance projects and full-time opportunities</p>
        </footer>
    </div>

    <script>
        // Add some interactive elements
        document.addEventListener('DOMContentLoaded', function() {
            // Animate stats counting
            const stats = document.querySelectorAll('.stat-number');
            stats.forEach(stat => {
                const target = parseInt(stat.textContent);
                let current = 0;
                const increment = target / 50;
                const timer = setInterval(() => {
                    current += increment;
                    if (current >= target) {
                        stat.textContent = target + (stat.textContent.includes('%') ? '%' : '+');
                        clearInterval(timer);
                    } else {
                        stat.textContent = Math.floor(current) + (stat.textContent.includes('%') ? '%' : '+');
                    }
                }, 50);
            });

            // Add hover effects to project cards
            const projectCards = document.querySelectorAll('.project-card');
            projectCards.forEach(card => {
                card.addEventListener('mouseenter', function() {
                    this.style.transform = 'translateY(-10px) scale(1.02)';
                });
                card.addEventListener('mouseleave', function() {
                    this.style.transform = 'translateY(0) scale(1)';
                });
            });
        });
    </script>
</body>
</html>
