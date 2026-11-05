<!DOCTYPE html>
<html lang="en">
<head> 
    <meta charset="UTF-8"> 
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>My Portfolio</title> 
    <style>
        :root {
            --bg-color: #ffffff;
            --text-color: #333333;
            --primary-color: #2563eb;
            --card-bg: #f8fafc;
            --border-color: #e2e8f0;
        }

        [data-theme="dark"] {
            --bg-color: #0f172a;
            --text-color: #f8fafc;
            --primary-color: #38bdf8;
            --card-bg: #1e293b;
            --border-color: #334155;
        }

        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
            transition: background-color 0.3s, color 0.3s;
        }

        body {
            font-family: system-ui, -apple-system, sans-serif;
            background-color: var(--bg-color);
            color: var(--text-color);
            line-height: 1.6;
            padding: 2rem 1rem;
        }

        .container {
            max-width: 800px;
            margin: 0 auto;
        }

        header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding-bottom: 2rem;
            border-bottom: 2px solid var(--border-color);
        }

        .theme-btn {
            background: var(--primary-color);
            color: #fff;
            border: none;
            padding: 0.5rem 1rem;
            border-radius: 5px;
            cursor: pointer;
            font-weight: bold;
        }

        section {
            padding: 3rem 0;
            border-bottom: 1px solid var(--border-color);
        }

        h2 {
            margin-bottom: 1.5rem;
            color: var(--primary-color);
        }

        .job, .project {
            background-color: var(--card-bg);
            padding: 1.5rem;
            border-radius: 8px;
            margin-bottom: 1.5rem;
            border: 1px solid var(--border-color);
        }

        .job-title, .project-title {
            font-weight: bold;
            font-size: 1.2rem;
        }

        .company, .date {
            font-style: italic;
            color: #64748b;
            margin-bottom: 0.5rem;
        }

        .contact-info p {
            margin-bottom: 0.5rem;
        }

        .project-link {
            display: inline-block;
            margin-top: 1rem;
            color: var(--primary-color);
            text-decoration: none;
            font-weight: bold;
        }

        .project-link:hover {
            text-decoration: underline;
        }
    </style>
</head>
<body>

    <div class="container">
        <!-- Header Section -->
        <header>
            <div>
                <h1>Your Name Here</h1>
                <p>Your Profession / Job Title</p>
            </div>
            <button class="theme-btn" id="themeToggle">Toggle Mode</button>
        </header>

        <!-- About Me Section -->
        <section id="about">
            <h2>About Me</h2>
            <p>Write a brief summary about yourself here. Detail your professional passions, what drives you, your core technical skillset, and the type of problems you enjoy solving for businesses or users.</p>
        </section>

        <!-- Experience Section -->
        <section id="experience">
            <h2>Previous Experience</h2>
            
            <div class="job">
                <div class="job-title">Senior Role / Title</div>
                <div class="company">Company Name Name | 2024 - Present</div>
                <p>Describe your core accomplishments here. Focus on the impact you made, technologies you implemented, and metrics achieved during your tenure.</p>
            </div>

            <div class="job">
                <div class="job-title">Junior Role / Title</div>
                <div class="company">Previous Company | 2022 - 2024</div>
                <p>Summarize your responsibilities and growth in this role. Detail how you collaborated with teams and expanded your core knowledge base.</p>
            </div>
        </section>

        <!-- Projects Section -->
        <section id="projects">
            <h2>Featured Projects</h2>
            
            <div class="project">
                <div class="project-title">Project Name One</div>
                <p>A brief explanation of what this application does, the specific problem it addresses, and the technology stack utilized to build it.</p>
                <a href="#" class="project-link">View Project &rarr;</a>
            </div>

            <div class="project">
                <div class="project-title">Project Name Two</div>
                <p>A description of your second key project highlighting your structural layout, optimization efforts, and final features.</p>
                <a href="#" class="project-link">View Project &rarr;</a>
            </div>
        </section>

        <!-- Contact Section -->
        <section id="contact">
            <h2>Contact Details</h2>
            <div class="contact-info">
                <p><strong>Phone:</strong> +1 (555) 019-2834</p>
                <p><strong>Email:</strong> your.email@example.com</p>
                <p><strong>LinkedIn:</strong> ://linkedin.com</p>
            </div>
        </section>
    </div>

    <!-- JavaScript for Theme Toggle Interactivity -->
    <script>
        const themeToggle = document.getElementById('themeToggle');
        
        themeToggle.addEventListener('click', () => {
            const currentTheme = document.documentElement.getAttribute('data-theme');
            if (currentTheme === 'dark') {
                document.documentElement.removeAttribute('data-theme');
            } else {
                document.documentElement.setAttribute('data-theme', 'dark');
            }
        });
    </script>
</body>
</html>
