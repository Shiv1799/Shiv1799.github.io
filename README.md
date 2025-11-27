
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Om Tiwari | AI & Robotics Portfolio</title>
    <link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css" rel="stylesheet">
    <style>
        :root {
            /* Modern Professional Color Palette */
            --primary: #2563eb;       /* Royal Blue */
            --secondary: #0f172a;     /* Dark Slate */
            --accent: #10b981;        /* Emerald Green for success/thesis */
            --bg: #f8fafc;            /* Light Gray Background */
            --card-bg: #ffffff;       /* White */
            --text-main: #334155;     /* Slate Gray */
            --text-light: #64748b;    /* Lighter Gray */
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            margin: 0;
            padding: 0;
            background-color: var(--bg);
            color: var(--text-main);
            line-height: 1.6;
        }

        /* --- Navigation --- */
        nav {
            background-color: rgba(255, 255, 255, 0.95);
            backdrop-filter: blur(10px);
            box-shadow: 0 1px 3px rgba(0,0,0,0.1);
            position: sticky;
            top: 0;
            z-index: 1000;
            padding: 1rem 5%;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .nav-brand {
            font-size: 1.5rem;
            font-weight: 700;
            color: var(--primary);
        }

        .nav-links a {
            text-decoration: none;
            color: var(--secondary);
            margin-left: 25px;
            font-weight: 500;
            transition: 0.3s;
            font-size: 0.95rem;
        }

        .nav-links a:hover {
            color: var(--primary);
        }

        /* --- Hero Section --- */
        .hero {
            display: flex;
            flex-direction: column;
            align-items: center;
            text-align: center;
            padding: 5rem 2rem;
            background: linear-gradient(135deg, #e0f2fe 0%, #ffffff 100%);
        }

        .profile-img {
            width: 180px;
            height: 180px;
            border-radius: 50%;
            object-fit: cover;
            border: 4px solid var(--primary);
            margin-bottom: 1.5rem;
            box-shadow: 0 10px 15px -3px rgba(0, 0, 0, 0.1);
        }

        .hero h1 {
            font-size: 2.5rem;
            color: var(--secondary);
            margin: 0.5rem 0;
        }

        .hero-subtitle {
            font-size: 1.25rem;
            color: var(--text-light);
            margin-bottom: 1.5rem;
        }

        .social-icons a {
            font-size: 1.8rem;
            margin: 0 12px;
            color: var(--secondary);
            transition: transform 0.2s;
            display: inline-block;
        }

        .social-icons a:hover {
            color: var(--primary);
            transform: translateY(-3px);
        }

        /* --- General Layout --- */
        section {
            padding: 4rem 10%;
            max-width: 1100px;
            margin: 0 auto;
        }

        h2 {
            font-size: 2rem;
            color: var(--secondary);
            margin-bottom: 2.5rem;
            position: relative;
            display: inline-block;
        }

        h2::after {
            content: '';
            display: block;
            width: 60%;
            height: 4px;
            background: var(--primary);
            margin-top: 8px;
            border-radius: 2px;
        }

        /* --- Experience & Thesis Cards --- */
        .timeline-card {
            background: var(--card-bg);
            padding: 2rem;
            border-radius: 12px;
            box-shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.1);
            margin-bottom: 2rem;
            border-left: 6px solid var(--primary);
            transition: transform 0.2s;
        }

        .timeline-card:hover {
            transform: translateX(5px);
        }

        .timeline-header {
            display: flex;
            justify-content: space-between;
            flex-wrap: wrap;
            margin-bottom: 1rem;
        }

        .role {
            font-size: 1.2rem;
            font-weight: 700;
            color: var(--secondary);
        }

        .company {
            color: var(--primary);
            font-weight: 600;
        }

        .date-location {
            color: var(--text-light);
            font-size: 0.9rem;
            font-style: italic;
        }

        .timeline-card ul {
            margin: 0;
            padding-left: 1.2rem;
        }

        .timeline-card li {
            margin-bottom: 0.5rem;
        }

        /* --- Thesis Specific --- */
        .thesis-card {
            border-left-color: var(--accent);
            background: #f0fdf4; /* Very light green tint */
        }
        
        /* --- Projects Grid --- */
        .projects-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
            gap: 2rem;
        }

        .project-card {
            background: var(--card-bg);
            border-radius: 12px;
            overflow: hidden;
            box-shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.1);
            transition: transform 0.3s, box-shadow 0.3s;
            display: flex;
            flex-direction: column;
        }

        .project-card:hover {
            transform: translateY(-8px);
            box-shadow: 0 20px 25px -5px rgba(0, 0, 0, 0.1);
        }

        .project-content {
            padding: 1.5rem;
            flex-grow: 1;
        }

        .project-tags {
            margin-bottom: 1rem;
        }

        .tag {
            background-color: #e0f2fe;
            color: var(--primary);
            padding: 4px 10px;
            border-radius: 20px;
            font-size: 0.75rem;
            font-weight: 700;
            margin-right: 5px;
            text-transform: uppercase;
        }

        .tag.genai { background-color: #f3e8ff; color: #7e22ce; } /* Purple for AI */
        .tag.robotics { background-color: #ffedd5; color: #c2410c; } /* Orange for Robotics */

        .project-card h3 {
            margin: 0.5rem 0;
            color: var(--secondary);
        }

        .btn-link {
            display: inline-block;
            margin-top: auto;
            padding: 1.5rem;
            background-color: #f8fafc;
            color: var(--primary);
            font-weight: 600;
            text-decoration: none;
            text-align: center;
            border-top: 1px solid #e2e8f0;
            transition: background 0.2s;
        }

        .btn-link:hover {
            background-color: #e0f2fe;
        }

        /* --- Skills Section --- */
        .skills-container {
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
        }
        
        .skill-badge {
            background: white;
            border: 1px solid #e2e8f0;
            padding: 8px 16px;
            border-radius: 6px;
            font-weight: 500;
            font-size: 0.9rem;
        }

        /* --- Footer --- */
        footer {
            background-color: var(--secondary);
            color: #94a3b8;
            text-align: center;
            padding: 3rem;
            margin-top: 4rem;
        }

        /* Mobile Responsive */
        @media (max-width: 768px) {
            .nav-links { display: none; } /* Simple hide for mobile for now */
            section { padding: 3rem 5%; }
            .hero h1 { font-size: 2rem; }
        }
    </style>
</head>
<body>

    <nav>
        <div class="nav-brand">Om Tiwari</div>
        <div class="nav-links">
            <a href="#about">About</a>
            <a href="#skills">Skills</a>
            <a href="#experience">Experience</a>
            <a href="#thesis">Thesis</a>
            <a href="#projects">Projects</a>
        </div>
    </nav>

    <section id="about" class="hero">
        <img src="profile.jpg" alt="Om Tiwari" class="profile-img" onerror="this.src='https://github.githubassets.com/images/modules/logos_page/GitHub-Mark.png'">
        
        <h1>Om Tiwari</h1>
        <div class="hero-subtitle">M.Sc. Computer Science @ RPTU | Robotics & AI Researcher</div>
        
        <p style="max-width: 600px; margin-bottom: 20px;">
            Specializing in Generative AI, Robotics (ROS2), and 3D Object Detection. 
            Passionate about merging machine learning algorithms with precision control systems.
        </p>

        <div class="social-icons">
            <a href="https://github.com/Shiv1799" target="_blank" title="GitHub"><i class="fab fa-github"></i></a>
            <a href="https://www.linkedin.com/in/om-tiwari-960246193/" target="_blank" title="LinkedIn"><i class="fab fa-linkedin"></i></a>
            <a href="mailto:tiwari@rptu.de" title="Email"><i class="fas fa-envelope"></i></a>
        </div>
    </section>

    <section id="skills">
        <h2>Technical Skills</h2>
        <div class="skills-container">
            <span class="skill-badge"><i class="fab fa-python"></i> Python</span>
            <span class="skill-badge"><i class="fas fa-code"></i> C/C++</span>
            <span class="skill-badge"><i class="fas fa-robot"></i> ROS / ROS2</span>
            <span class="skill-badge"><i class="fas fa-brain"></i> PyTorch / TensorFlow</span>
            <span class="skill-badge"><i class="fas fa-cube"></i> Docker</span>
            <span class="skill-badge"><i class="fas fa-laptop-code"></i> Linux / Ubuntu</span>
            <span class="skill-badge">Computer Vision</span>
            <span class="skill-badge">Generative AI</span>
            <span class="skill-badge">SLAM</span>
        </div>
    </section>

    <section id="experience">
        <h2>Work Experience</h2>

        <div class="timeline-card">
            <div class="timeline-header">
                <div>
                    <div class="role">Intern - Robotics & AI</div>
                    <div class="company">BOSCH</div>
                </div>
                <div class="date-location">
                    01/2024 - 06/2024<br>
                    Renningen, Germany
                </div>
            </div>
            <ul>
                <li>Spearheaded system integration to embed foundational models into the Franka Panda robot.</li>
                <li>Merged machine learning algorithms with precision control systems for robotic manipulation.</li>
                <li>Used MoveIt and FlexBE for collision-free motion planning; refined rope manipulation using MuJoCo and Stable Baselines3 (RL).</li>
            </ul>
        </div>

        <div class="timeline-card">
            <div class="timeline-header">
                <div>
                    <div class="role">Research Assistant</div>
                    <div class="company">DFKI (German Research Center for AI)</div>
                </div>
                <div class="date-location">
                    06/2021 - 06/2023<br>
                    Kaiserslautern, Germany
                </div>
            </div>
            <ul>
                <li>Generated synthetic data using NVIDIA Deep Learning Data Synthesizer to improve object detection accuracy by 5.1% mAP.</li>
                <li>Enhanced YOLOv4 algorithm performance through hyperparameter tuning and data augmentation.</li>
                <li> devised strategies for message transfer between robots and external computers via MQTT protocol.</li>
            </ul>
        </div>

        <div class="timeline-card">
            <div class="timeline-header">
                <div>
                    <div class="role">Autonomous Navigation Intern</div>
                    <div class="company">Kaiserslautern Racing Team (Formula Student)</div>
                </div>
                <div class="date-location">
                    11/2021 - 11/2022<br>
                    Kaiserslautern, Germany
                </div>
            </div>
            <ul>
                <li>Integrated Tiny YOLO, SFA3D, and PointNet on Nvidia Jetson for Formula E student car.</li>
                <li>Leveraged GNSS, LiDARs, and stereo vision for precise Visual SLAM-based localization.</li>
                <li>Achieved a 10% improvement in detection and depth prediction.</li>
            </ul>
        </div>
    </section>

    <section id="thesis">
        <h2>Master's Thesis</h2>
        <div class="timeline-card thesis-card">
            <div class="timeline-header">
                <div>
                    <div class="role">Master Thesis: 3D Object Detection Pipeline</div>
                    <div class="company">Hitachi Astemo</div>
                </div>
                <div class="date-location">
                    01/2025 - 08/2025<br>
                    Munich, Germany
                </div>
            </div>
            <p><strong>Focus:</strong> Robust Pseudo-LiDAR System in ROS2</p>
            <ul>
                <li>Integrated a 3D object detection pipeline in ROS2 using multi-camera and LiDAR sensors.</li>
                <li>Developed an end-to-end pseudo-LiDAR system using stereo vision within a Docker-based environment.</li>
                <li>Conducted Software-in-the-Loop (SiL) tests using CARLA simulator to validate performance under various weather and lighting conditions.</li>
                <li>Reduced false positives by 30% through statistical evaluation and parameter fine-tuning.</li>
            </ul>
        </div>
    </section>

    <section id="projects">
        <h2>Projects</h2>
        
        <h3>Generative AI Focus</h3>
        <div class="projects-grid">
            
            <div class="project-card">
                <div class="project-content">
                    <div class="project-tags">
                        <span class="tag genai">Generative AI</span>
                        <span class="tag genai">Computer Vision</span>
                    </div>
                    <h3>Fashion Style Analyzer</h3>
                    <p>An advanced AI tool analyzing fashion trends and styles using generative models. Helps users identify and generate style recommendations.</p>
                </div>
                <a href="https://github.com/Shiv1799/Fashion-Style-Analyzer" class="btn-link" target="_blank">View on GitHub <i class="fas fa-arrow-right"></i></a>
            </div>

            <div class="project-card">
                <div class="project-content">
                    <div class="project-tags">
                        <span class="tag genai">Generative AI</span>
                        <span class="tag genai">NLP</span>
                    </div>
                    <h3>AI Meeting Assistant</h3>
                    <p>Intelligent assistant for transcribing, summarizing, and extracting actionable insights from meetings to boost productivity.</p>
                </div>
                <a href="https://github.com/Shiv1799/AI-Meeting-Assistant" class="btn-link" target="_blank">View on GitHub <i class="fas fa-arrow-right"></i></a>
            </div>
        </div>

        <h3 style="margin-top: 3rem;">Robotics & Systems</h3>
        <div class="projects-grid">
            
            <div class="project-card">
                <div class="project-content">
                    <div class="project-tags">
                        <span class="tag robotics">ROS 2</span>
                        <span class="tag robotics">Safety</span>
                    </div>
                    <h3>DBA for Autonomous Vehicles</h3>
                    <p>Designed safety-engineered behavior modules in ROS 2 with fail-safe logic for real-time obstacle detection and command arbitration.</p>
                </div>
                <a href="https://github.com/Shiv1799" class="btn-link" target="_blank">View on GitHub <i class="fas fa-arrow-right"></i></a>
            </div>

             <div class="project-card">
                <div class="project-content">
                    <div class="project-tags">
                        <span class="tag robotics">SLAM</span>
                        <span class="tag robotics">C++</span>
                    </div>
                    <h3>OV2SLAM Optimization</h3>
                    <p>Erasmus Mundus Challenge: Ported OV2SLAM to ROS 2, achieving a 30% increase in processing speed and optimizing thread execution.</p>
                </div>
                <a href="https://github.com/Shiv1799" class="btn-link" target="_blank">View on GitHub <i class="fas fa-arrow-right"></i></a>
            </div>

        </div>
    </section>

    <section id="publications">
        <h2>Publications</h2>
        <ul>
            <li>
                <strong>Automated Weed Detection:</strong> An experimental setup for utilizing CNNs (IEEE, 2023).
            </li>
            <li>
                <strong>Skin Cancer Detection:</strong> Intelligent application using CNNs (JARDCS, Vol 11).
            </li>
        </ul>
    </section>

    <footer>
        <p>&copy; 2025 Om Tiwari. Hosted on GitHub Pages.</p>
        <div class="social-icons" style="margin-top: 1rem;">
            <a href="https://github.com/Shiv1799"><i class="fab fa-github"></i></a>
            <a href="https://www.linkedin.com/in/om-tiwari-960246193/"><i class="fab fa-linkedin"></i></a>
        </div>
    </footer>

</body>
</html>
