```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">

  <title>VÉRA — Interior Studio</title>

  <style>
    @import url('https://fonts.googleapis.com/css2?family=DM+Sans:wght@400;500;600&family=Playfair+Display:wght@500;600&display=swap');

    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    :root {
      --black: #11110f;
      --cream: #f3efe7;
      --white: #ffffff;
      --gold: #b59b72;
      --gray: #77736b;
      --line: rgba(17, 17, 15, 0.15);
    }

    html {
      scroll-behavior: smooth;
    }

    body {
      background: var(--cream);
      color: var(--black);
      font-family: "DM Sans", sans-serif;
    }

    /* NAVBAR */

    nav {
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      padding: 30px 6%;
      display: flex;
      align-items: center;
      justify-content: space-between;
      z-index: 10;
    }

    .logo {
      font-family: "Playfair Display", serif;
      font-size: 28px;
      letter-spacing: 4px;
    }

    nav ul {
      display: flex;
      list-style: none;
      gap: 35px;
    }

    nav a {
      color: var(--white);
      text-decoration: none;
      font-size: 13px;
      letter-spacing: 1px;
      transition: 0.3s;
    }

    nav a:hover {
      color: var(--gold);
    }

    .nav-btn {
      border: 1px solid rgba(255,255,255,.5);
      padding: 12px 20px;
    }

    /* HERO */

    .hero {
      height: 100vh;
      min-height: 700px;
      position: relative;
      display: flex;
      align-items: center;
      overflow: hidden;

      background:
        linear-gradient(
          90deg,
          rgba(0,0,0,.72),
          rgba(0,0,0,.25)
        ),
        url("https://images.unsplash.com/photo-1600210492486-724fe5c67fb0?auto=format&fit=crop&w=2000&q=90")
        center/cover;
    }

    .hero-content {
      width: 90%;
      max-width: 1250px;
      margin: auto;
      color: white;
    }

    .small-title {
      text-transform: uppercase;
      letter-spacing: 5px;
      font-size: 12px;
      color: #ddd;
      margin-bottom: 25px;
    }

    .hero h1 {
      font-family: "Playfair Display", serif;
      font-size: clamp(55px, 8vw, 115px);
      line-height: .92;
      font-weight: 500;
      max-width: 850px;
    }

    .hero h1 span {
      color: #d1b88d;
      font-style: italic;
    }

    .hero-text {
      max-width: 480px;
      margin-top: 35px;
      color: #ddd;
      line-height: 1.7;
      font-size: 15px;
    }

    .hero-button {
      display: inline-block;
      margin-top: 35px;
      padding: 16px 30px;
      background: white;
      color: var(--black);
      text-decoration: none;
      font-size: 13px;
      letter-spacing: 1px;
      transition: .3s;
    }

    .hero-button:hover {
      background: var(--gold);
      color: white;
      transform: translateY(-3px);
    }

    .scroll {
      position: absolute;
      bottom: 35px;
      left: 6%;
      color: white;
      font-size: 11px;
      letter-spacing: 3px;
      writing-mode: vertical-rl;
      opacity: .7;
    }

    /* INTRO */

    .intro {
      padding: 150px 7%;
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 100px;
      align-items: center;
    }

    .section-number {
      color: var(--gold);
      font-size: 13px;
      letter-spacing: 3px;
      margin-bottom: 20px;
    }

    .intro h2 {
      font-family: "Playfair Display", serif;
      font-size: clamp(42px, 5vw, 72px);
      line-height: 1;
      font-weight: 500;
    }

    .intro h2 em {
      color: var(--gold);
    }

    .intro p {
      color: var(--gray);
      line-height: 1.9;
      font-size: 15px;
      margin-bottom: 25px;
    }

    .learn {
      color: var(--black);
      text-decoration: none;
      border-bottom: 1px solid var(--black);
      padding-bottom: 7px;
      font-size: 13px;
    }

    /* PROJECTS */

    .projects {
      background: var(--black);
      color: white;
      padding: 130px 7%;
    }

    .projects-header {
      display: flex;
      justify-content: space-between;
      align-items: end;
      margin-bottom: 70px;
    }

    .projects h2 {
      font-family: "Playfair Display", serif;
      font-size: clamp(45px, 6vw, 80px);
      font-weight: 500;
    }

    .projects-header p {
      color: #aaa;
      max-width: 300px;
      line-height: 1.7;
      font-size: 14px;
    }

    .project-grid {
      display: grid;
      grid-template-columns: 1.2fr .8fr;
      gap: 25px;
    }

    .project {
      position: relative;
      overflow: hidden;
      cursor: pointer;
    }

    .project.large {
      height: 650px;
    }

    .project.small {
      height: 310px;
    }

    .project img {
      width: 100%;
      height: 100%;
      object-fit: cover;
      transition: transform .8s ease;
    }

    .project:hover img {
      transform: scale(1.06);
    }

    .project-info {
      position: absolute;
      bottom: 0;
      left: 0;
      right: 0;
      padding: 35px;
      background: linear-gradient(transparent, rgba(0,0,0,.8));
      padding-top: 100px;
    }

    .project-info h3 {
      font-family: "Playfair Display", serif;
      font-size: 28px;
      font-weight: 500;
    }

    .project-info span {
      font-size: 11px;
      color: #ccc;
      letter-spacing: 2px;
    }

    .side-projects {
      display: grid;
      gap: 25px;
    }

    /* SERVICES */

    .services {
      padding: 140px 7%;
    }

    .services h2 {
      font-family: "Playfair Display", serif;
      font-size: clamp(45px, 6vw, 80px);
      font-weight: 500;
      margin-bottom: 70px;
    }

    .service {
      border-top: 1px solid var(--line);
      padding: 35px 0;
      display: grid;
      grid-template-columns: 80px 1fr 1fr;
      align-items: center;
      transition: .3s;
    }

    .service:last-child {
      border-bottom: 1px solid var(--line);
    }

    .service:hover {
      padding-left: 15px;
    }

    .service-number {
      color: var(--gold);
    }

    .service h3 {
      font-family: "Playfair Display", serif;
      font-size: 30px;
      font-weight: 500;
    }

    .service p {
      color: var(--gray);
      line-height: 1.7;
      font-size: 14px;
      max-width: 450px;
    }

    /* CTA */

    .cta {
      min-height: 500px;
      background:
        linear-gradient(rgba(0,0,0,.55), rgba(0,0,0,.65)),
        url("https://images.unsplash.com/photo-1600607687939-ce8a6c25118c?auto=format&fit=crop&w=2000&q=90")
        center/cover;

      display: flex;
      justify-content: center;
      align-items: center;
      text-align: center;
      color: white;
      padding: 60px 20px;
    }

    .cta h2 {
      font-family: "Playfair Display", serif;
      font-size: clamp(50px, 7vw, 95px);
      font-weight: 500;
      line-height: .95;
    }

    .cta p {
      margin: 30px auto;
      max-width: 500px;
      color: #ddd;
      line-height: 1.7;
    }

    .cta a {
      display: inline-block;
      padding: 16px 32px;
      background: white;
      color: var(--black);
      text-decoration: none;
      font-size: 13px;
      transition: .3s;
    }

    .cta a:hover {
      background: var(--gold);
      color: white;
    }

    /* FOOTER */

    footer {
      background: var(--black);
      color: white;
      padding: 60px 7%;
      display: flex;
      justify-content: space-between;
      align-items: center;
    }

    footer .logo {
      font-size: 24px;
    }

    footer p {
      color: #777;
      font-size: 12px;
    }

    /* RESPONSIVE */

    @media (max-width: 800px) {

      nav ul {
        display: none;
      }

      .hero {
        min-height: 650px;
      }

      .intro {
        grid-template-columns: 1fr;
        gap: 40px;
        padding: 100px 7%;
      }

      .projects {
        padding: 100px 7%;
      }

      .projects-header {
        display: block;
      }

      .projects-header p {
        margin-top: 25px;
      }

      .project-grid {
        grid-template-columns: 1fr;
      }

      .project.large {
        height: 500px;
      }

      .project.small {
        height: 350px;
      }

      .service {
        grid-template-columns: 50px 1fr;
        gap: 15px;
      }

      .service p {
        grid-column: 2;
      }

      footer {
        flex-direction: column;
        gap: 20px;
        text-align: center;
      }
    }
  </style>
</head>

<body>

  <!-- NAVIGATION -->

  <nav>
    <div class="logo">VÉRA</div>

    <ul>
      <li><a href="#home">HOME</a></li>
      <li><a href="#about">ABOUT</a></li>
      <li><a href="#projects">PROJECTS</a></li>
      <li><a href="#services">SERVICES</a></li>
    </ul>

    <a href="#contact" class="nav-btn">CONTACT</a>
  </nav>


  <!-- HERO -->

  <section class="hero" id="home">

    <div class="hero-content">

      <div class="small-title">
        Interior Architecture Studio
      </div>

      <h1>
        Spaces<br>
        with <span>meaning.</span>
      </h1>

      <p class="hero-text">
        We create timeless interiors where architecture,
        materials and everyday life come together.
      </p>

      <a href="#projects" class="hero-button">
        EXPLORE OUR WORK →
      </a>

    </div>

    <div class="scroll">
      SCROLL TO EXPLORE
    </div>

  </section>


  <!-- INTRODUCTION -->

  <section class="intro" id="about">

    <div>
      <div class="section-number">01 — ABOUT US</div>

      <h2>
        Designing<br>
        <em>how you live.</em>
      </h2>
    </div>

    <div>
      <p>
        VÉRA is an independent interior architecture studio
        focused on creating spaces that feel natural, refined
        and deeply personal.
      </p>

      <p>
        From private residences to hospitality spaces,
        we combine architectural thinking with a sensitivity
        for materials, light and proportion.
      </p>

      <a href="#" class="learn">
        DISCOVER OUR STUDIO →
      </a>
    </div>

  </section>


  <!-- PROJECTS -->

  <section class="projects" id="projects">

    <div class="projects-header">

      <div>
        <div class="section-number">02 — SELECTED WORK</div>
        <h2>Our Projects</h2>
      </div>

      <p>
        A collection of spaces designed around
        light, texture and human experience.
      </p>

    </div>


    <div class="project-grid">

      <div class="project large">

        <img
          src="https://images.unsplash.com/photo-1600210491892-03d54c0aaf87?auto=format&fit=crop&w=1400&q=90"
          alt="Luxury living room">

        <div class="project-info">
          <span>RESIDENTIAL · 2025</span>
          <h3>Casa Terra</h3>
        </div>

      </div>


      <div class="side-projects">

        <div class="project small">

          <img
            src="https://images.unsplash.com/photo-1618221195710-dd6b41faaea6?auto=format&fit=crop&w=1200&q=90"
            alt="Minimal bedroom">

          <div class="project-info">
            <span>RESIDENTIAL · 2024</span>
            <h3>Soft Minimal</h3>
          </div>

        </div>


        <div class="project small">

          <img
            src="https://images.unsplash.com/photo-1600566753190-17f0baa2a6c3?auto=format&fit=crop&w=1200&q=90"
            alt="Modern interior">

          <div class="project-info">
            <span>HOSPITALITY · 2025</span>
            <h3>Atelier 09</h3>
          </div>

        </div>

      </div>

    </div>

  </section>


  <!-- SERVICES -->

  <section class="services" id="services">

    <div class="section-number">03 — WHAT WE DO</div>

    <h2>Our Expertise</h2>


    <div class="service">

      <div class="service-number">01</div>

      <h3>Interior Design</h3>

      <p>
        Complete interior concepts from spatial planning
        to furniture, lighting and final styling.
      </p>

    </div>


    <div class="service">

      <div class="service-number">02</div>

      <h3>Architecture</h3>

      <p>
        Thoughtful architectural solutions that connect
        structure, natural light and human experience.
      </p>

    </div>


    <div class="service">

      <div class="service-number">03</div>

      <h3>Material & Styling</h3>

      <p>
        Carefully selected materials, textures, colors
        and objects that give every space its identity.
      </p>

    </div>

  </section>


  <!-- CONTACT CTA -->

  <section class="cta" id="contact">

    <div>

      <div class="section-number">
        LET'S CREATE SOMETHING BEAUTIFUL
      </div>

      <h2>
        Your space.<br>
        Your story.
      </h2>

      <p>
        Have a project in mind? Let's turn your ideas
        into a space that feels uniquely yours.
      </p>

      <a href="mailto:hello@vera-studio.com">
        START A PROJECT →
      </a>

    </div>

  </section>


  <!-- FOOTER -->

  <footer>

    <div class="logo">VÉRA</div>

    <p>
      © 2026 VÉRA Interior Architecture Studio
    </p>

  </footer>

</body>
</html>
```

