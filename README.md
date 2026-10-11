<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<meta name="theme-color" content="#080d1c">
<meta name="description" content="Bajun Kisku's personal portfolio showcasing web development, website design and digital projects.">

<title>Bajun Kisku | Web Developer Portfolio</title>

<style>
:root {
  --bg: #080d1c;
  --card: #111a35;
  --purple: #a78bfa;
  --bright: #a855f7;
  --text: #f5f7ff;
  --muted: #bbc5df;
  --border: rgba(167,139,250,.28);
}

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  scroll-behavior: smooth;
}

body {
  font-family: Arial, Helvetica, sans-serif;
  background: var(--bg);
  color: var(--text);
  line-height: 1.7;
}

a {
  color: inherit;
  text-decoration: none;
}

header {
  position: sticky;
  top: 0;
  z-index: 1000;
  background: rgba(8,13,28,.96);
  border-bottom: 1px solid var(--border);
  padding: 16px 6%;
}

.navbar {
  display: flex;
  align-items: center;
  justify-content: space-between;
  max-width: 1200px;
  margin: auto;
}

.logo {
  font-size: 27px;
  font-weight: 800;
  color: var(--purple);
}

nav {
  display: flex;
  gap: 25px;
  align-items: center;
}

nav a {
  color: var(--muted);
  font-weight: 600;
  transition: .3s;
}

nav a:hover {
  color: var(--purple);
}

.menu-btn {
  display: none;
  background: transparent;
  color: white;
  border: 1px solid var(--border);
  padding: 7px 13px;
  border-radius: 10px;
  font-size: 24px;
  cursor: pointer;
}

section {
  padding: 90px 6%;
  scroll-margin-top: 75px;
}

.container {
  max-width: 1150px;
  margin: auto;
}

.hero {
  min-height: 85vh;
  display: flex;
  align-items: center;
  background:
    radial-gradient(circle at 85% 25%, #35175b 0, transparent 35%),
    var(--bg);
}

.hero-grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 55px;
  align-items: center;
}

.badge {
  display: inline-block;
  border: 1px solid var(--border);
  color: var(--purple);
  border-radius: 30px;
  padding: 8px 18px;
  margin-bottom: 22px;
  font-weight: 700;
}

h1 {
  font-size: clamp(38px, 5vw, 65px);
  line-height: 1.2;
  margin-bottom: 20px;
}

h2 {
  font-size: clamp(32px, 4vw, 48px);
  text-align: center;
  margin-bottom: 12px;
}

h2 span,
h1 span,
.purple {
  color: var(--purple);
}

.subtitle {
  color: var(--muted);
  text-align: center;
  font-size: 19px;
  margin-bottom: 48px;
}

.hero h3 {
  font-size: 27px;
  margin-bottom: 18px;
}

.hero p,
.card p {
  color: var(--muted);
  font-size: 17px;
}

.buttons {
  display: flex;
  gap: 15px;
  flex-wrap: wrap;
  margin-top: 30px;
}

.btn {
  display: inline-block;
  padding: 13px 22px;
  border-radius: 13px;
  border: 1px solid var(--purple);
  font-weight: 700;
  transition: .3s;
}

.btn-primary {
  background: linear-gradient(120deg, #7c3aed, #a855f7);
  border: none;
}

.btn:hover {
  transform: translateY(-3px);
  box-shadow: 0 8px 25px #7c3aed35;
}

.photo-box {
  max-width: 430px;
  width: 100%;
  margin: auto;
  padding: 12px;
  border: 2px solid #8b5cf6;
  border-radius: 35px;
  background: var(--card);
  box-shadow: 0 0 45px #7c3aed25;
}

.profile-photo {
  display: block;
  width: 100%;
  height: 470px;
  object-fit: cover;
  object-position: center 30%;
  border-radius: 25px;
}

.photo-caption {
  text-align: center;
  padding: 12px;
  color: var(--purple);
  font-weight: bold;
}

.grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 24px;
}

.card {
  background: linear-gradient(145deg, #15203f, #10172e);
  border: 1px solid var(--border);
  border-radius: 27px;
  padding: 30px;
  transition: .3s;
}

.card:hover {
  transform: translateY(-6px);
  border-color: var(--purple);
  box-shadow: 0 12px 30px #0003;
}

.card h3 {
  font-size: 23px;
  color: var(--purple);
  margin: 12px 0;
}

.icon {
  font-size: 43px;
  display: block;
  margin-bottom: 10px;
}

.profile-list {
  list-style: none;
  margin-top: 15px;
}

.profile-list li {
  padding: 12px 0;
  border-bottom: 1px solid var(--border);
  color: var(--muted);
}

.profile-list strong {
  color: var(--text);
}

.project-link {
  display: inline-block;
  margin-top: 22px;
  color: var(--purple);
  font-weight: bold;
  border-bottom: 1px solid var(--purple);
}

.project-status {
  display: inline-block;
  margin-top: 18px;
  padding: 5px 12px;
  border: 1px solid var(--border);
  border-radius: 20px;
  color: var(--purple);
  font-size: 14px;
}

.contact-box {
  max-width: 750px;
  margin: auto;
  text-align: center;
}

.contact-box p {
  color: var(--muted);
  margin: 20px 0;
}

footer {
  border-top: 1px solid var(--border);
  text-align: center;
  padding: 25px 15px;
  color: var(--muted);
}

footer span {
  color: var(--purple);
}

@media (max-width: 850px) {
  .hero-grid {
    grid-template-columns: 1fr;
    text-align: center;
  }

  .hero-grid .buttons {
    justify-content: center;
  }

  .photo-box {
    max-width: 380px;
  }

  .profile-photo {
    height: 430px;
  }

  .grid {
    grid-template-columns: repeat(2, 1fr);
  }

  nav {
    display: none;
    position: absolute;
    top: 100%;
    left: 0;
    width: 100%;
    padding: 22px;
    background: #0e1530;
    border-bottom: 1px solid var(--border);
    flex-direction: column;
    gap: 18px;
  }

  nav.open {
    display: flex;
  }

  .menu-btn {
    display: block;
  }
}

@media (max-width: 550px) {
  header {
    padding: 13px 5%;
  }

  .logo {
    font-size: 24px;
  }

  section {
    padding: 65px 5%;
  }

  .grid {
    grid-template-columns: 1fr;
  }

  .card {
    padding: 25px;
  }

  .profile-photo {
    height: 390px;
  }

  .hero h3 {
    font-size: 23px;
  }

  .subtitle {
    font-size: 17px;
  }
}
</style>
</head>

<body>

<header>
  <div class="navbar">
    <a class="logo" href="#home">BK. Portfolio</a>

    <button class="menu-btn"
      id="menuBtn"
      aria-label="Open navigation"
      aria-expanded="false"
      onclick="toggleMenu()">☰</button>

    <nav id="nav">
      <a href="#home" onclick="closeMenu()">Home</a>
      <a href="#about" onclick="closeMenu()">About</a>
      <a href="#skills" onclick="closeMenu()">Skills</a>
      <a href="#projects" onclick="closeMenu()">Projects</a>
      <a href="#contact" onclick="closeMenu()">Contact</a>
    </nav>
  </div>
</header>

<!-- HOME -->

<section class="hero" id="home">
  <div class="container hero-grid">

    <div>
      <span class="badge">WELCOME TO MY PORTFOLIO</span>

      <h1>
        Hi, I'm <span>Bajun Kisku</span>
      </h1>

      <h3>
        Web Developer in Training
        <span class="purple">& AI Learner</span>
      </h3>

      <p>
        I am learning to build modern websites,
        responsive web applications and useful digital
        experiences. I enjoy exploring new technologies
        and creating projects step by step.
      </p>

      <div class="buttons">
        <a class="btn btn-primary" href="#projects">
          Explore My Work ↗
        </a>

        <a class="btn" href="#contact">
          Contact Me
        </a>
      </div>
    </div>

    <div>
      <div class="photo-box">
        <img
          class="profile-photo"
          src="profile.png"
          alt="Bajun Kisku profile photo"
          onerror="this.style.display='none';
          document.getElementById('photoFallback').style.display='block';">

        <div id="photoFallback"
          style="display:none;text-align:center;padding:100px 10px;">
          <div style="font-size:70px;color:#a78bfa;">BK</div>
          <p style="color:#bbc5df;">Upload profile.png</p>
        </div>

        <div class="photo-caption">
          Bajun Kisku | Web Developer
        </div>
      </div>
    </div>

  </div>
</section>

<!-- ABOUT -->

<section id="about">
  <div class="container">

    <h2>About <span>Me</span></h2>
    <p class="subtitle">A little introduction about myself</p>

    <div class="grid">

      <div class="card">
        <h3>My Introduction</h3>
        <p>
          Hello! My name is Bajun Kisku.
          I am learning web design, website development
          and artificial intelligence.
        </p>
        <br>
        <p>
          My goal is to build useful digital products,
          solve real-world problems and improve my
          technical skills through practical projects.
        </p>
      </div>

      <div class="card">
        <h3>My Profile</h3>

        <ul class="profile-list">
          <li><strong>Name:</strong> Bajun Kisku</li>
          <li><strong>Focus:</strong> Web Development</li>
          <li><strong>Learning:</strong> AI Tools</li>
          <li><strong>Portfolio:</strong> Personal Projects</li>
          <li><strong>Goal:</strong> Skilled Developer</li>
        </ul>
      </div>

      <div class="card">
        <h3>My Mission</h3>
        <p>
          To learn new technologies, design helpful
          websites and create practical digital solutions.
        </p>
        <br>
        <p>
          I believe in learning by doing and improving
          a little every day.
        </p>
      </div>

    </div>
  </div>
</section>

<!-- SKILLS -->

<section id="skills">
  <div class="container">

    <h2>My <span>Skills</span></h2>
    <p class="subtitle">
      Technologies and tools I am learning
    </p>

    <div class="grid">

      <div class="card">
        <span class="icon">🌐</span>
        <h3>HTML</h3>
        <p>Website structure and content.</p>
      </div>

      <div class="card">
        <span class="icon">🎨</span>
        <h3>CSS</h3>
        <p>Website layouts, colours and styling.</p>
      </div>

      <div class="card">
        <span class="icon">⚡</span>
        <h3>JavaScript</h3>
        <p>Interactive website features.</p>
      </div>

      <div class="card">
        <span class="icon">📱</span>
        <h3>Responsive Design</h3>
        <p>Mobile-friendly website layouts.</p>
      </div>

      <div class="card">
        <span class="icon">🐙</span>
        <h3>GitHub</h3>
        <p>Code management and repositories.</p>
      </div>

      <div class="card">
        <span class="icon">🚀</span>
        <h3>Website Publishing</h3>
        <p>Publishing websites using GitHub Pages.</p>
      </div>

      <div class="card">
        <span class="icon">🔌</span>
        <h3>API Integration</h3>
        <p>Learning how websites connect to services.</p>
      </div>

      <div class="card">
        <span class="icon">🤖</span>
        <h3>AI Tools</h3>
        <p>Exploring artificial intelligence tools.</p>
      </div>

      <div class="card">
        <span class="icon">💡</span>
        <h3>Problem Solving</h3>
        <p>Learning through practical experiments.</p>
      </div>

    </div>
  </div>
</section>

<!-- PROJECTS -->

<section id="projects">
  <div class="container">

    <h2>My <span>Projects</span></h2>
    <p class="subtitle">
      My learning projects and experiments
    </p>

    <div class="grid">

      <div class="card">
        <span class="icon">🌐</span>
        <h3>Portfolio Website</h3>
        <p>
          My personal portfolio showcasing my learning
          journey, skills and projects.
        </p>
        <span class="project-status">Current Project</span>
        <br>
        <a class="project-link" href="#home">
          View Portfolio ↗
        </a>
      </div>

      <div class="card">
        <span class="icon">🏫</span>
        <h3>School Website</h3>
        <p>
          A website concept for presenting school
          information, activities and educational resources.
        </p>
        <span class="project-status">Learning Project</span>
      </div>

      <div class="card">
        <span class="icon">📚</span>
        <h3>English Grammar Quiz</h3>
        <p>
          An educational quiz project for practising
          English grammar and improving knowledge.
        </p>
        <span class="project-status">In Development</span>
      </div>

      <div class="card">
        <span class="icon">🛍️</span>
        <h3>Murmu Saree</h3>
        <p>
          An e-commerce learning project for sarees,
          kurtis and children's clothing.
        </p>
        <span class="project-status">In Development</span>
      </div>

      <div class="card">
        <span class="icon">🧠</span>
        <h3>GK Quiz App</h3>
        <p>
          A general knowledge quiz concept for
          practising questions and answers.
        </p>
        <span class="project-status">Learning Project</span>
      </div>

      <div class="card">
        <span class="icon">💻</span>
        <h3>Future Projects</h3>
        <p>
          I plan to build more useful websites and
          applications as my skills improve.
        </p>
        <span class="project-status">Coming Soon</span>
      </div>

    </div>
  </div>
</section>

<!-- CONTACT -->

<section id="contact">
  <div class="container contact-box">

    <h2>Contact <span>Me</span></h2>

    <p class="subtitle">
      Let's connect and build something useful.
    </p>

    <div class="card">
      <span class="icon">🤝</span>

      <h3>Thank You for Visiting!</h3>

      <p>
        Thank you for exploring my portfolio.
        I am continuously learning and improving
        my web development skills.
      </p>

      <p>
        For project enquiries, please contact me
        using your preferred contact method.
      </p>

      <a class="btn btn-primary" href="#home">
        Back to Home ↑
      </a>
    </div>

  </div>
</section>

<footer>
  <p>
    © <span id="year"></span>
    <span>Bajun Kisku</span> |
    Personal Portfolio
  </p>

  <p>Designed with HTML, CSS & JavaScript.</p>
</footer>

<script>
function toggleMenu() {
  const nav = document.getElementById("nav");
  const btn = document.getElementById("menuBtn");

  nav.classList.toggle("open");

  btn.setAttribute(
    "aria-expanded",
    nav.classList.contains("open")
  );
}

function closeMenu() {
  document.getElementById("nav").classList.remove("open");
  document.getElementById("menuBtn")
    .setAttribute("aria-expanded", "false");
}

document.getElementById("year").textContent =
  new Date().getFullYear();
</script>

</body>
</html>
