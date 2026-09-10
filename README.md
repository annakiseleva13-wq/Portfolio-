# Portfolio-
index.html
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>Anna Kiseleva — Portfolio</title>

<style>

@import url('https://fonts.googleapis.com/css2?family=DM+Sans:wght@400;500;600;700&family=Playfair+Display:ital,wght@0,500;1,500&display=swap');

* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

html {
    scroll-behavior: smooth;
}

body {
    font-family: "DM Sans", sans-serif;
    background: #f7f6f2;
    color: #171717;
    overflow-x: hidden;
}

/* =====================
   BACKGROUND
===================== */

body::before {
    content: "";
    position: fixed;
    width: 500px;
    height: 500px;
    background: #dcd6ff;
    border-radius: 50%;
    filter: blur(100px);
    opacity: .45;
    top: -200px;
    right: -150px;
    z-index: -1;
}

body::after {
    content: "";
    position: fixed;
    width: 400px;
    height: 400px;
    background: #ffd9df;
    border-radius: 50%;
    filter: blur(100px);
    opacity: .35;
    bottom: -150px;
    left: -150px;
    z-index: -1;
}

/* =====================
   NAVIGATION
===================== */

nav {
    position: fixed;
    top: 20px;
    left: 50%;
    transform: translateX(-50%);
    width: min(1100px, 92%);
    padding: 14px 22px;

    background: rgba(255,255,255,.65);
    backdrop-filter: blur(20px);

    border: 1px solid rgba(0,0,0,.07);
    border-radius: 100px;

    display: flex;
    justify-content: space-between;
    align-items: center;

    z-index: 1000;
}

.logo {
    font-weight: 700;
    font-size: 18px;
}

nav a {
    text-decoration: none;
    color: #333;
    margin-left: 25px;
    font-size: 14px;
}

nav a:hover {
    opacity: .5;
}

/* =====================
   HERO
===================== */

.hero {
    min-height: 100vh;
    max-width: 1100px;
    margin: auto;

    display: flex;
    align-items: center;
    justify-content: space-between;

    padding: 120px 30px 70px;
    gap: 50px;
}

.hero-text {
    max-width: 650px;
}

.small-title {
    font-size: 13px;
    letter-spacing: 2px;
    text-transform: uppercase;
    opacity: .55;
    margin-bottom: 20px;
}

h1 {
    font-size: clamp(60px, 9vw, 115px);
    line-height: .9;
    letter-spacing: -6px;
}

h1 span {
    font-family: "Playfair Display", serif;
    font-style: italic;
    font-weight: 500;
}

.hero-description {
    margin-top: 35px;
    font-size: 19px;
    line-height: 1.6;
    max-width: 550px;
    color: #555;
}

.buttons {
    margin-top: 35px;
    display: flex;
    gap: 12px;
}

.btn {
    display: inline-block;
    padding: 14px 23px;
    border-radius: 50px;
    text-decoration: none;
    font-size: 14px;
    transition: .3s;
}

.btn-dark {
    background: #171717;
    color: white;
}

.btn-light {
    border: 1px solid #ccc;
    color: #171717;
}

.btn:hover {
    transform: translateY(-3px);
}

/* =====================
   PHOTO
===================== */

.photo-wrapper {
    width: 310px;
    height: 390px;
    position: relative;
    flex-shrink: 0;
}

.photo-wrapper::before {
    content: "";
    position: absolute;
    width: 100%;
    height: 100%;
    background: #ddd5ff;
    border-radius: 150px 150px 25px 25px;
    transform: rotate(7deg);
}

.photo {
    position: relative;
    width: 100%;
    height: 100%;
    object-fit: cover;

    border-radius: 150px 150px 25px 25px;

    border: 8px solid #f7f6f2;

    box-shadow: 0 30px 70px rgba(0,0,0,.15);
}

/* =====================
   SECTIONS
===================== */

section {
    max-width: 1100px;
    margin: auto;
    padding: 120px 30px;
}

.section-label {
    text-transform: uppercase;
    font-size: 12px;
    letter-spacing: 2px;
    opacity: .45;
    margin-bottom: 20px;
}

.section-title {
    font-size: clamp(40px, 6vw, 75px);
    line-height: 1;
    letter-spacing: -3px;
    margin-bottom: 60px;
}

/* =====================
   ABOUT
===================== */

.about {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 70px;
}

.about p {
    font-size: 20px;
    line-height: 1.65;
    color: #555;
}

.highlight {
    color: #171717;
    font-weight: 600;
}

/* =====================
   PROJECTS
===================== */

.projects {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    gap: 20px;
}

.project {
    background: white;
    border-radius: 30px;
    padding: 35px;
    min-height: 300px;

    border: 1px solid #eee;

    transition: .4s;
}

.project:hover {
    transform: translateY(-8px);
    box-shadow: 0 25px 60px rgba(0,0,0,.08);
}

.project-number {
    font-size: 12px;
    opacity: .4;
}

.project h3 {
    margin-top: 80px;
    font-size: 28px;
    letter-spacing: -1px;
}

.project p {
    margin-top: 15px;
    line-height: 1.6;
    color: #666;
}

.project-tag {
    display: inline-block;
    margin-top: 20px;
    padding: 7px 12px;
    border-radius: 50px;
    background: #f1f1f1;
    font-size: 12px;
}

/* =====================
   JOURNEY
===================== */

.timeline {
    border-left: 1px solid #ccc;
    margin-left: 10px;
}

.timeline-item {
    position: relative;
    padding: 0 0 60px 40px;
}

.timeline-item::before {
    content: "";
    position: absolute;
    left: -6px;
    top: 5px;

    width: 11px;
    height: 11px;

    background: #171717;
    border-radius: 50%;
}

.timeline-year {
    font-size: 12px;
    letter-spacing: 1px;
    opacity: .4;
}

.timeline h3 {
    font-size: 25px;
    margin: 8px 0;
}

.timeline p {
    color: #666;
    line-height: 1.6;
}

/* =====================
   SKILLS
===================== */

.skills {
    display: flex;
    flex-wrap: wrap;
    gap: 12px;
}

.skill {
    padding: 14px 20px;
    border: 1px solid #ccc;
    border-radius: 50px;
    background: rgba(255,255,255,.5);
}

/* =====================
   CONTACT
===================== */

.contact {
    text-align: center;
    padding-bottom: 150px;
}

.contact h2 {
    font-size: clamp(50px, 8vw, 100px);
    letter-spacing: -5px;
    line-height: .95;
}

.contact p {
    margin: 30px auto;
    max-width: 500px;
    color: #666;
    font-size: 18px;
}

/* =====================
   ANIMATION
===================== */

.fade {
    opacity: 0;
    transform: translateY(30px);
    animation: appear 1s forwards;
}

@keyframes appear {
    to {
        opacity: 1;
        transform: translateY(0);
    }
}

/* =====================
   MOBILE
===================== */

@media(max-width: 800px) {

    nav {
        padding: 12px 16px;
    }

    nav div:last-child {
        display: none;
    }

    .hero {
        flex-direction: column;
        align-items: flex-start;
        padding-top: 150px;
    }

    .photo-wrapper {
        width: 230px;
        height: 290px;
        margin-top: 20px;
    }

    h1 {
        letter-spacing: -4px;
    }

    .about {
        grid-template-columns: 1fr;
    }

    .projects {
        grid-template-columns: 1fr;
    }

    section {
        padding: 90px 25px;
    }
}

</style>
</head>

<body>

<!-- NAVIGATION -->

<nav>

    <div class="logo">
        AK.
    </div>

    <div>
        <a href="#about">About</a>
        <a href="#work">Work</a>
        <a href="#journey">Journey</a>
        <a href="#contact">Contact</a>
    </div>

</nav>


<!-- HERO -->

<header class="hero">

    <div class="hero-text fade">

        <div class="small-title">
            Portfolio · 2026
        </div>

        <h1>
            Anna<br>
            <span>Kiseleva</span>
        </h1>

        <p class="hero-description">
            I connect business, technology and people —
            turning ideas into projects, communities and
            meaningful products.
        </p>

        <div class="buttons">

            <a href="#work" class="btn btn-dark">
                Explore my work
            </a>

            <a href="#contact" class="btn btn-light">
                Let's connect
            </a>

        </div>

    </div>


    <!-- YOUR PHOTO -->

    <div class="photo-wrapper fade">

        <img
            src="anna.jpg"
            class="photo"
            alt="Anna Kiseleva"
        >

    </div>

</header>


<!-- ABOUT -->

<section id="about">

    <div class="section-label">
        01 — About
    </div>

    <div class="section-title">
        More than<br>
        <i>one role.</i>
    </div>

    <div class="about">

        <p>
            My background sits at the intersection of
            <span class="highlight">
            business, technology and communication.
            </span>
        </p>

        <p>
            I started in HR and management, moved into
            Developer Relations and technology communities,
            and later focused on product-oriented initiatives
            and cross-functional projects.
        </p>

        <p>
            Today I am looking for opportunities in
            <span class="highlight">
            Business Development, Business Analysis,
            Project Management and Product Management.
            </span>
        </p>

        <p>
            I enjoy understanding complex problems,
            bringing people together and turning ideas
            into structured, measurable outcomes.
        </p>

    </div>

</section>


<!-- WORK -->

<section id="work">

    <div class="section-label">
        02 — Selected Work
    </div>

    <div class="section-title">
        Things I've<br>
        <i>built & explored.</i>
    </div>


    <div class="projects">


        <div class="project">

            <div class="project-number">
                01 / COMMUNITY
            </div>

            <h3>
                Agile & Product Owners Guild
            </h3>

            <p>
                Designed and structured an internal community
                connecting Product Owners, PMs and specialists
                during a company-wide product transformation.
            </p>

            <span class="project-tag">
                Product · Community · Strategy
            </span>

        </div>


        <div class="project">

            <div class="project-number">
                02 / TECHNOLOGY
            </div>

            <h3>
                Developer Relations
            </h3>

            <p>
                Worked with technology communities, speakers,
                conferences and educational initiatives in
                the developer ecosystem.
            </p>

            <span class="project-tag">
                Tech · Events · Communication
            </span>

        </div>


        <div class="project">

            <div class="project-number">
                03 / RESEARCH
            </div>

            <h3>
                Corporate Culture Research
            </h3>

            <p>
                Analysed corporate culture in digital ecosystems
                using CVF, Hofstede and Schein frameworks.
            </p>

            <span class="project-tag">
                Research · Strategy · Analytics
            </span>

        </div>


        <div class="project">

            <div class="project-number">
                04 / PEOPLE
            </div>

            <h3>
                Intern Experience
            </h3>

            <p>
                Worked on onboarding and intern experience,
                helping improve satisfaction and communication
                within the corporate university environment.
            </p>

            <span class="project-tag">
                HR · People · Operations
            </span>

        </div>


    </div>

</section>


<!-- JOURNEY -->

<section id="journey">

    <div class="section-label">
        03 — Journey
    </div>

    <div class="section-title">
        A non-linear<br>
        <i>career path.</i>
    </div>


    <div class="timeline">


        <div class="timeline-item">

            <div class="timeline-year">
                2020 — 2024
            </div>

            <h3>
                Lomonosov Moscow State University
            </h3>

            <p>
                Bachelor's degree in Management.
                Focus on management, HR and organisational processes.
            </p>

        </div>


        <div class="timeline-item">

            <div class="timeline-year">
                2023
            </div>

            <h3>
                Yandex
            </h3>

            <p>
                Developer Relations Intern.
                Technology events, speakers and community initiatives.
            </p>

        </div>


        <div class="timeline-item">

            <div class="timeline-year">
                2023 — 2024
            </div>

            <h3>
                Ingosstrakh
            </h3>

            <p>
                HR & Corporate University.
                Employee onboarding and intern experience.
            </p>

        </div>


        <div class="timeline-item">

            <div class="timeline-year">
                2025 — 2026
            </div>

            <h3>
                MTS Web Services
            </h3>

            <p>
                Developer Relations → Product & Agile initiatives.
                Technology communities, conferences and cross-functional projects.
            </p>

        </div>


        <div class="timeline-item">

            <div class="timeline-year">
                2026
            </div>

            <h3>
                International Business
            </h3>

            <p>
                Master's studies focused on international business
                and global professional development.
            </p>

        </div>


    </div>

</section>


<!-- SKILLS -->

<section>

    <div class="section-label">
        04 — Toolkit
    </div>

    <div class="section-title">
        What I<br>
        <i>bring with me.</i>
    </div>


    <div class="skills">

        <div class="skill">Business Development</div>
        <div class="skill">Project Management</div>
        <div class="skill">Product Thinking</div>
        <div class="skill">Business Analysis</div>
        <div class="skill">Community Building</div>
        <div class="skill">Research</div>
        <div class="skill">Stakeholder Management</div>
        <div class="skill">Public Speaking</div>
        <div class="skill">Figma</div>
        <div class="skill">Notion</div>
        <div class="skill">Excel</div>
        <div class="skill">AI Tools</div>
    </div>

</section>


<!-- CONTACT -->

<section id="contact" class="contact">

    <div class="section-label">
        05 — Contact
    </div>

    <h2>
        Let's build<br>
        <i>something.</i>
    </h2>

    <p>
        I'm open to internships, junior roles and
        international opportunities in Business,
        Product and Project Management.
    </p>

    <div class="buttons" style="justify-content:center;">

        <a
            href="mailto:YOUR_EMAIL@example.com"
            class="btn btn-dark"
        >
            Email me
        </a>

        <a
            href="https://www.linkedin.com/"
            class="btn btn-light"
            target="_blank"
        >
            LinkedIn
        </a>

    </div>

</section>


</body>
</html>