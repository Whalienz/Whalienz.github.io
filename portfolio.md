---
title: Chutima Selakhun - Portfolio
description: Frontend Developer portfolio showcasing projects and skills
author: Chutima Selakhun
---

<!DOCTYPE html>
<html lang="th">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Chutima Selakhun - Portfolio</title>
    <link rel="stylesheet" href="styles.css">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
</head>
<body>

<!-- Navigation -->
<nav class="navbar">
    <div class="container">
        <div class="nav-brand">CS</div>
        <ul class="nav-menu">
            <li><a href="#home">Home</a></li>
            <li><a href="#projects">Projects</a></li>
            <li><a href="#skills">Skills</a></li>
            <li><a href="#about">About</a></li>
            <li><a href="#contact">Contact</a></li>
        </ul>
    </div>
</nav>

<!-- Hero Section -->
<section id="home" class="hero">
    <div class="hero-content">
        <div class="hero-text">
            <p class="hero-subtitle">Frontend Developer</p>
            <p class="hero-description">
                Welcome to my digital space where creativity meets technology
            </p>
            <div class="hero-buttons">
                <a href="#contact" class="btn btn-primary">Get In Touch</a>
                <a href="#projects" class="btn btn-secondary">View My Work</a>
            </div>
        </div>
        <div class="hero-image">
            <div class="profile-card">
                <div class="profile-img-wrapper">
                    <img src="images/ICat.gif" alt="Profile" class="profile-img">
                </div>
            </div>
        </div>
    </div>
    <div class="scroll-indicator">
        <i class="fas fa-chevron-down"></i>
    </div>
</section>

<!-- Projects Section -->
<section id="projects" class="projects">
    <div class="container">
        <h2 class="section-title">My Projects</h2>
        <div class="projects-grid">

            <!-- Project 1 -->
            <div class="project-card">
                <div class="project-image">
                    <img src="https://images.unsplash.com/photo-1517694712202-14dd9538aa97?w=600&h=400&fit=crop" alt="Submission 1">
                    <div class="project-overlay">
                        <div class="project-links">
                            <a href="#" class="project-link"><i class="fab fa-github"></i></a>
                            <a href="/dynamic-routing" class="project-link"><i class="fas fa-external-link-alt"></i></a>
                        </div>
                    </div>
                </div>
                <div class="project-content">
                    <h3>Submission 1</h3>
                    <p>A beautiful web application with modern design and smooth animations</p>
                    <div class="project-tags">
                        <span class="tag">HTML</span>
                        <span class="tag">CSS</span>
                        <span class="tag">JavaScript</span>
                    </div>
                </div>
            </div>

            <!-- Project 2 -->
            <div class="project-card">
                <div class="project-image">
                    <img src="https://images.unsplash.com/photo-1551650975-87deedd944c3?w=600&h=400&fit=crop" alt="Submission 2">
                    <div class="project-overlay">
                        <div class="project-links">
                            <a href="#" class="project-link"><i class="fab fa-github"></i></a>
                            <a href="/madman-mib" class="project-link"><i class="fas fa-external-link-alt"></i></a>
                        </div>
                    </div>
                </div>
                <div class="project-content">
                    <h3>Submission 2</h3>
                    <p>An innovative solution to everyday problems using cutting-edge technology</p>
                    <div class="project-tags">
                        <span class="tag">React</span>
                        <span class="tag">Node.js</span>
                        <span class="tag">MongoDB</span>
                    </div>
                </div>
            </div>

            <!-- Project 3 -->
            <div class="project-card">
                <div class="project-image">
                    <img src="https://images.unsplash.com/photo-1498050108023-c5249f4df085?w=600&h=400&fit=crop" alt="Submission 3">
                    <div class="project-overlay">
                        <div class="project-links">
                            <a href="#" class="project-link"><i class="fab fa-github"></i></a>
                            <a href="/node" class="project-link"><i class="fas fa-external-link-alt"></i></a>
                        </div>
                    </div>
                </div>
                <div class="project-content">
                    <h3>Submission 3</h3>
                    <p>A creative project showcasing design and development skills</p>
                    <div class="project-tags">
                        <span class="tag">Python</span>
                        <span class="tag">Django</span>
                        <span class="tag">PostgreSQL</span>
                    </div>
                </div>
            </div>

        </div>
    </div>
</section>

<!-- Skills Section -->
<section id="skills" class="skills">
    <div class="container">
        <h2 class="section-title">Skills & Technologies</h2>
        <div class="skills-grid">
            <div class="skill-category">
                <h3><i class="fas fa-code"></i> Frontend</h3>
                <div class="skill-tags">
                    <span class="skill-tag">HTML5</span>
                    <span class="skill-tag">CSS3</span>
                    <span class="skill-tag">JavaScript</span>
                    <span class="skill-tag">React</span>
                    <span class="skill-tag">Vue.js</span>
                </div>
            </div>
            <div class="skill-category">
                <h3><i class="fas fa-server"></i> Backend</h3>
                <div class="skill-tags">
                    <span class="skill-tag">Node.js</span>
                    <span class="skill-tag">Python</span>
                    <span class="skill-tag">Django</span>
                    <span class="skill-tag">Express</span>
                </div>
            </div>
            <div class="skill-category">
                <h3><i class="fas fa-database"></i> Database</h3>
                <div class="skill-tags">
                    <span class="skill-tag">MongoDB</span>
                    <span class="skill-tag">PostgreSQL</span>
                    <span class="skill-tag">MySQL</span>
                </div>
            </div>
            <div class="skill-category">
                <h3><i class="fas fa-tools"></i> Tools</h3>
                <div class="skill-tags">
                    <span class="skill-tag">Git</span>
                    <span class="skill-tag">Docker</span>
                    <span class="skill-tag">VS Code</span>
                    <span class="skill-tag">Figma</span>
                </div>
            </div>
        </div>
    </div>
</section>

<!-- About Section -->
<section id="about" class="about">
    <div class="container">
        <h2 class="section-title">About Me</h2>
        <div class="about-content">
            <div class="about-text">
                <p class="about-description">
                    Nice to meet you! I'm Chutima Selakhun, a passionate developer who loves creating new things and solving problems with technology.
                </p>
                <p class="about-description">
                    I enjoy learning new technologies and applying them to various projects to create the best possible experience for users.
                </p>
                <div class="about-stats">
                    <div class="stat-item">
                        <i class="fas fa-code"></i>
                        <h3>Projects</h3>
                        <p>10+</p>
                    </div>
                    <div class="stat-item">
                        <i class="fas fa-coffee"></i>
                        <h3>Coffee Cups</h3>
                        <p>∞</p>
                    </div>
                    <div class="stat-item">
                        <i class="fas fa-lightbulb"></i>
                        <h3>Ideas</h3>
                        <p>100+</p>
                    </div>
                </div>
            </div>
        </div>
    </div>
</section>

<!-- Contact Section -->
<section id="contact" class="contact">
    <div class="container">
        <h2 class="section-title">Get In Touch</h2>
        <p class="contact-description">Feel free to reach out for collaborations or just a friendly hello</p>
        <div class="contact-grid">
            <a href="mailto:chutimasalakhun@gmail.com" class="contact-item">
                <i class="fas fa-envelope"></i>
                <h3>Email</h3>
                <p>chutimasalakhun@gmail.com</p>
            </a>
            <a href="tel:063-4650650" class="contact-item">
                <i class="fas fa-phone"></i>
                <h3>Phone</h3>
                <p>063-4650650</p>
            </a>
            <a href="#" class="contact-item">
                <i class="fas fa-map-marker-alt"></i>
                <h3>Location</h3>
                <p>Thailand</p>
            </a>
        </div>
        <div class="social-links">
            <a href="https://github.com/Whalienz" class="social-link" target="_blank">
                <i class="fab fa-github"></i>
            </a>
            <a href="#" class="social-link" target="_blank">
                <i class="fab fa-linkedin"></i>
            </a>
            <a href="#" class="social-link" target="_blank">
                <i class="fab fa-twitter"></i>
            </a>
            <a href="#" class="social-link" target="_blank">
                <i class="fab fa-facebook"></i>
            </a>
        </div>
    </div>
</section>

<!-- Footer -->
<footer class="footer">
    <div class="container">
        <p>&copy; 2024 Chutima Selakhun. Made with ❤️</p>
    </div>
</footer>

<script src="script.js"></script>
</body>
</html>
