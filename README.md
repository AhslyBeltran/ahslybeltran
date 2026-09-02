```html
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">

  <title>Ahsly Valentina | Portafolio</title>

  <!-- Google Fonts -->
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&family=Orbitron:wght@400;500;600;700;800&display=swap" rel="stylesheet">

  <!-- Font Awesome -->
  <link rel="stylesheet"
        href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.2/css/all.min.css">

  <style>

    /* =========================================================
       VARIABLES
    ========================================================= */

    :root {
      --bg: #03030b;
      --bg2: #070719;
      --card: rgba(12, 13, 35, 0.72);

      --primary: #8b5cf6;
      --secondary: #22d3ee;
      --pink: #ec4899;

      --text: #f8fafc;
      --muted: #a5acc4;

      --border: rgba(139, 92, 246, 0.25);

      --glow:
        0 0 20px rgba(139, 92, 246, 0.35),
        0 0 60px rgba(34, 211, 238, 0.08);
    }

    /* =========================================================
       RESET
    ========================================================= */

    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    html {
      scroll-behavior: smooth;
    }

    body {
      background: var(--bg);
      color: var(--text);
      font-family: "Inter", sans-serif;
      overflow-x: hidden;
    }

    a {
      color: inherit;
      text-decoration: none;
    }

    /* =========================================================
       SPACE BACKGROUND
    ========================================================= */

    .space {
      position: fixed;
      inset: 0;
      z-index: -10;
      overflow: hidden;
      background:
        radial-gradient(
          circle at 20% 20%,
          rgba(91, 33, 182, 0.16),
          transparent 30%
        ),
        radial-gradient(
          circle at 80% 70%,
          rgba(8, 145, 178, 0.12),
          transparent 28%
        ),
        #03030b;
    }

    .nebula {
      position: absolute;
      border-radius: 50%;
      filter: blur(90px);
      opacity: 0.25;
      animation: nebulaMove 15s ease-in-out infinite alternate;
    }

    .nebula.one {
      width: 500px;
      height: 500px;
      background: #6d28d9;
      top: -200px;
      left: -150px;
    }

    .nebula.two {
      width: 400px;
      height: 400px;
      background: #0891b2;
      right: -150px;
      bottom: 5%;
      animation-delay: 3s;
    }

    .nebula.three {
      width: 300px;
      height: 300px;
      background: #db2777;
      left: 45%;
      top: 45%;
      opacity: 0.12;
      animation-delay: 6s;
    }

    @keyframes nebulaMove {
      from {
        transform: translate(0, 0) scale(1);
      }

      to {
        transform: translate(60px, -40px) scale(1.15);
      }
    }

    /* =========================================================
       STARS
    ========================================================= */

    .stars,
    .stars2,
    .stars3 {
      position: absolute;
      inset: 0;
      background-repeat: repeat;
    }

    .stars {
      background-image:
        radial-gradient(1px 1px at 10% 20%, white, transparent),
        radial-gradient(1px 1px at 30% 70%, white, transparent),
        radial-gradient(1px 1px at 50% 40%, white, transparent),
        radial-gradient(1px 1px at 80% 10%, white, transparent),
        radial-gradient(1px 1px at 90% 80%, white, transparent),
        radial-gradient(1px 1px at 15% 90%, white, transparent);

      background-size: 250px 250px;
      opacity: 0.7;
      animation: starsMove 100s linear infinite;
    }

    .stars2 {
      background-image:
        radial-gradient(2px 2px at 20% 30%, #c4b5fd, transparent),
        radial-gradient(2px 2px at 70% 50%, #67e8f9, transparent),
        radial-gradient(1px 1px at 40% 80%, white, transparent);

      background-size: 350px 350px;
      opacity: 0.5;
      animation: starsMove 150s linear infinite reverse;
    }

    .stars3 {
      background-image:
        radial-gradient(1px 1px at 25% 65%, #f9a8d4, transparent),
        radial-gradient(1px 1px at 65% 25%, #a5f3fc, transparent);

      background-size: 500px 500px;
      opacity: 0.5;
    }

    @keyframes starsMove {
      from {
        transform: translateY(0);
      }

      to {
        transform: translateY(250px);
      }
    }

    /* =========================================================
       NAVBAR
    ========================================================= */

    header {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      z-index: 1000;
      padding: 20px 6%;
      background: rgba(3, 3, 11, 0.55);
      backdrop-filter: blur(18px);
      border-bottom: 1px solid rgba(255,255,255,0.05);
    }

    nav {
      max-width: 1200px;
      margin: auto;
      display: flex;
      align-items: center;
      justify-content: space-between;
    }

    .logo {
      font-family: "Orbitron", sans-serif;
      font-weight: 700;
      font-size: 1.1rem;
      letter-spacing: 2px;
    }

    .logo span {
      color: var(--secondary);
    }

    .nav-links {
      display: flex;
      gap: 30px;
      list-style: none;
    }

    .nav-links a {
      color: var(--muted);
      font-size: 0.9rem;
      transition: 0.3s;
    }

    .nav-links a:hover {
      color: white;
      text-shadow: 0 0 15px var(--secondary);
    }

    .menu {
      display: none;
      font-size: 1.4rem;
      cursor: pointer;
    }

    /* =========================================================
       GENERAL
    ========================================================= */

    section {
      min-height: 100vh;
      padding: 120px 7%;
      display: flex;
      align-items: center;
    }

    .container {
      width: 100%;
      max-width: 1150px;
      margin: auto;
    }

    .section-title {
      margin-bottom: 50px;
    }

    .section-title .mini {
      color: var(--secondary);
      font-family: "Orbitron", sans-serif;
      font-size: 0.75rem;
      letter-spacing: 4px;
      margin-bottom: 12px;
      display: block;
    }

    .section-title h2 {
      font-family: "Orbitron", sans-serif;
      font-size: clamp(2rem, 5vw, 3.5rem);
    }

    .section-title p {
      color: var(--muted);
      max-width: 650px;
      margin-top: 15px;
      line-height: 1.8;
    }

    /* =========================================================
       HERO
    ========================================================= */

    #inicio {
      position: relative;
      overflow: hidden;
    }

    .hero {
      max-width: 1150px;
      width: 100%;
      margin: auto;
      display: grid;
      grid-template-columns: 1.2fr 0.8fr;
      align-items: center;
      gap: 50px;
    }

    .status {
      display: inline-flex;
      align-items: center;
      gap: 10px;
      padding: 8px 15px;
      border: 1px solid var(--border);
      background: rgba(139, 92, 246, 0.08);
      border-radius: 50px;
      color: #c4b5fd;
      font-size: 0.8rem;
      margin-bottom: 25px;
    }

    .status-dot {
      width: 8px;
      height: 8px;
      border-radius: 50%;
      background: #22c55e;
      box-shadow: 0 0 15px #22c55e;
      animation: pulse 2s infinite;
    }

    @keyframes pulse {
      50% {
        opacity: 0.3;
      }
    }

    .hero h1 {
      font-family: "Orbitron", sans-serif;
      font-size: clamp(3rem, 8vw, 6rem);
      line-height: 1;
      margin-bottom: 20px;
    }

    .hero h1 span {
      background: linear-gradient(
        90deg,
        #ffffff,
        #a78bfa,
        #22d3ee
      );
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
    }

    .hero h2 {
      font-size: clamp(1.1rem, 2vw, 1.5rem);
      color: var(--secondary);
      margin-bottom: 20px;
      font-weight: 400;
    }

    .hero p {
      color: var(--muted);
      line-height: 1.8;
      max-width: 600px;
      margin-bottom: 35px;
    }

    .buttons {
      display: flex;
      flex-wrap: wrap;
      gap: 15px;
    }

    .btn {
      padding: 14px 22px;
      border-radius: 12px;
      border: 1px solid var(--border);
      font-weight: 600;
      font-size: 0.9rem;
      transition: 0.3s;
      display: inline-flex;
      align-items: center;
      gap: 10px;
    }

    .btn.primary {
      background: linear-gradient(
        135deg,
        var(--primary),
        #6d28d9
      );
      box-shadow: var(--glow);
    }

    .btn.secondary {
      background: rgba(255,255,255,0.03);
    }

    .btn:hover {
      transform: translateY(-4px);
      box-shadow:
        0 10px 30px rgba(139, 92, 246, 0.25);
    }

    /* =========================================================
       PLANET
    ========================================================= */

    .planet-container {
      position: relative;
      width: 380px;
      height: 380px;
      margin: auto;
    }

    .planet {
      position: absolute;
      width: 260px;
      height: 260px;
      border-radius: 50%;
      top: 60px;
      left: 60px;

      background:
        radial-gradient(
          circle at 35% 30%,
          #e0e7ff,
          #8b5cf6 20%,
          #4c1d95 50%,
          #111827 80%
        );

      box-shadow:
        inset -35px -25px 60px rgba(0,0,0,0.7),
        0 0 50px rgba(139,92,246,0.4),
        0 0 120px rgba(34,211,238,0.12);

      animation: planetFloat 6s ease-in-out infinite;
    }

    .planet::before {
      content: "";
      position: absolute;
      width: 340px;
      height: 80px;
      border: 2px solid rgba(103,232,249,0.35);
      border-radius: 50%;
      left: -40px;
      top: 95px;
      transform: rotate(-20deg);
    }

    .planet::after {
      content: "";
      position: absolute;
      width: 330px;
      height: 75px;
      border: 1px solid rgba(196,181,253,0.25);
      border-radius: 50%;
      left: -35px;
      top: 100px;
      transform: rotate(-20deg);
    }

    @keyframes planetFloat {
      50% {
        transform: translateY(-18px) rotate(3deg);
      }
    }

    .orbit {
      position: absolute;
      width: 360px;
      height: 130px;
      border: 1px solid rgba(34,211,238,0.15);
      border-radius: 50%;
      top: 125px;
      left: 10px;
      transform: rotate(-20deg);
    }

    /* =========================================================
       ABOUT
    ========================================================= */

    .about-grid {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 60px;
      align-items: center;
    }

    .about-text {
      color: var(--muted);
      line-height: 1.9;
      font-size: 1rem;
    }

    .about-text strong {
      color: white;
    }

    .stats {
      display: grid;
      grid-template-columns: repeat(2, 1fr);
      gap: 15px;
    }

    .stat {
      padding: 25px;
      border: 1px solid var(--border);
      background: var(--card);
      border-radius: 18px;
      backdrop-filter: blur(10px);
      transition: 0.3s;
    }

    .stat:hover {
      transform: translateY(-5px);
      border-color: var(--secondary);
    }

    .stat i {
      color: var(--secondary);
      font-size: 1.4rem;
      margin-bottom: 15px;
    }

    .stat h3 {
      font-family: "Orbitron", sans-serif;
      font-size: 1.3rem;
      margin-bottom: 5px;
    }

    .stat p {
      color: var(--muted);
      font-size: 0.8rem;
    }

    /* =========================================================
       SKILLS
    ========================================================= */

    .skills-grid {
      display: grid;
      grid-template-columns: repeat(4, 1fr);
      gap: 18px;
    }

    .skill {
      position: relative;
      padding: 30px 20px;
      text-align: center;
      background: var(--card);
      border: 1px solid var(--border);
      border-radius: 18px;
      backdrop-filter: blur(12px);
      transition: 0.4s;
      overflow: hidden;
    }

    .skill::before {
      content: "";
      position: absolute;
      width: 100px;
      height: 100px;
      background: var(--primary);
      filter: blur(60px);
      opacity: 0;
      left: 50%;
      top: 50%;
      transform: translate(-50%, -50%);
      transition: 0.4s;
    }

    .skill:hover {
      transform: translateY(-8px) scale(1.02);
      border-color: var(--secondary);
      box-shadow: var(--glow);
    }

    .skill:hover::before {
      opacity: 0.2;
    }

    .skill i,
    .skill h3 {
      position: relative;
    }

    .skill i {
      font-size: 2.2rem;
      margin-bottom: 15px;
      color: var(--secondary);
    }

    .skill h3 {
      font-family: "Orbitron", sans-serif;
      font-size: 0.9rem;
    }

    /* =========================================================
       PROJECTS
    ========================================================= */

    .projects-grid {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 25px;
    }

    .project {
      background: var(--card);
      border: 1px solid var(--border);
      border-radius: 22px;
      overflow: hidden;
      backdrop-filter: blur(12px);
      transition: 0.4s;
    }

    .project:hover {
      transform: translateY(-10px);
      border-color: rgba(34,211,238,0.5);
      box-shadow: var(--glow);
    }

    .project-image {
      height: 180px;
      position: relative;
      display: flex;
      align-items: center;
      justify-content: center;
      overflow: hidden;

      background:
        radial-gradient(
          circle at center,
          rgba(139,92,246,0.5),
          transparent 50%
        ),
        linear-gradient(
          135deg,
          #08081c,
          #151044,
          #031820
        );
    }

    .project-image i {
      font-size: 4rem;
      color: #c4b5fd;
      filter: drop-shadow(0 0 20px #8b5cf6);
    }

    .project-content {
      padding: 25px;
    }

    .project-number {
      color: var(--secondary);
      font-family: "Orbitron", sans-serif;
      font-size: 0.7rem;
      letter-spacing: 2px;
    }

    .project h3 {
      font-family: "Orbitron", sans-serif;
      margin: 10px 0;
      font-size: 1.2rem;
    }

    .project p {
      color: var(--muted);
      font-size: 0.85rem;
      line-height: 1.7;
      margin-bottom: 18px;
    }

    .tags {
      display: flex;
      flex-wrap: wrap;
      gap: 7px;
      margin-bottom: 20px;
    }

    .tag {
      font-size: 0.7rem;
      padding: 5px 9px;
      border-radius: 20px;
      background: rgba(139,92,246,0.12);
      color: #c4b5fd;
      border: 1px solid rgba(139,92,246,0.2);
    }

    .project-link {
      display: inline-flex;
      align-items: center;
      gap: 8px;
      color: var(--secondary);
      font-size: 0.85rem;
      font-weight: 600;
    }

    /* =========================================================
       TIMELINE
    ========================================================= */

    .timeline {
      position: relative;
      max-width: 850px;
      margin: auto;
    }

    .timeline::before {
      content: "";
      position: absolute;
      left: 20px;
      top: 0;
      bottom: 0;
      width: 1px;
      background: linear-gradient(
        var(--primary),
        var(--secondary),
        transparent
      );
    }

    .timeline-item {
      position: relative;
      padding-left: 70px;
      margin-bottom: 45px;
    }

    .timeline-dot {
      position: absolute;
      left: 12px;
      top: 4px;
      width: 17px;
      height: 17px;
      border-radius: 50%;
      background: var(--secondary);
      box-shadow: 0 0 20px var(--secondary);
    }

    .timeline-item span {
      color: var(--secondary);
      font-family: "Orbitron", sans-serif;
      font-size: 0.7rem;
    }

    .timeline-item h3 {
      margin: 8px 0;
      font-family: "Orbitron", sans-serif;
    }

    .timeline-item p {
      color: var(--muted);
      line-height: 1.7;
      font-size: 0.9rem;
    }

    /* =========================================================
       CONTACT
    ========================================================= */

    .contact-box {
      text-align: center;
      padding: 70px 30px;
      border: 1px solid var(--border);
      border-radius: 30px;
      background:
        radial-gradient(
          circle at center,
          rgba(139,92,246,0.12),
          transparent 60%
        ),
        var(--card);
      backdrop-filter: blur(15px);
      box-shadow: var(--glow);
    }

    .signal {
      font-family: "Orbitron", sans-serif;
      color: var(--secondary);
      letter-spacing: 5px;
      font-size: 0.75rem;
      margin-bottom: 20px;
    }

    .contact-box h2 {
      font-family: "Orbitron", sans-serif;
      font-size: clamp(2rem, 5vw, 3.5rem);
      margin-bottom: 20px;
    }

    .contact-box p {
      color: var(--muted);
      max-width: 600px;
      margin: 0 auto 30px;
      line-height: 1.8;
    }

    .socials {
      display: flex;
      justify-content: center;
      flex-wrap: wrap;
      gap: 12px;
    }

    .social {
      width: 48px;
      height: 48px;
      border: 1px solid var(--border);
      border-radius: 14px;
      display: flex;
      align-items: center;
      justify-content: center;
      transition: 0.3s;
      background: rgba(255,255,255,0.03);
    }

    .social:hover {
      color: var(--secondary);
      border-color: var(--secondary);
      transform: translateY(-5px);
      box-shadow: 0 0 25px rgba(34,211,238,0.2);
    }

    /* =========================================================
       FOOTER
    ========================================================= */

    footer {
      padding: 30px;
      text-align: center;
      border-top: 1px solid rgba(255,255,255,0.05);
      color: var(--muted);
      font-size: 0.8rem;
    }

    footer span {
      color: var(--secondary);
    }

    /* =========================================================
       REVEAL ANIMATION
    ========================================================= */

    .reveal {
      opacity: 0;
      transform: translateY(35px);
      transition: 0.8s ease;
    }

    .reveal.active {
      opacity: 1;
      transform: translateY(0);
    }

    /* =========================================================
       RESPONSIVE
    ========================================================= */

    @media (max-width: 900px) {

      .hero {
        grid-template-columns: 1fr;
        text-align: center;
      }

      .hero p {
        margin-left: auto;
        margin-right: auto;
      }

      .buttons {
        justify-content: center;
      }

      .planet-container {
        transform: scale(0.8);
      }

      .skills-grid {
        grid-template-columns: repeat(2, 1fr);
      }

      .projects-grid {
        grid-template-columns: 1fr;
      }

      .about-grid {
        grid-template-columns: 1fr;
      }
    }

    @media (max-width: 650px) {

      header {
        padding: 18px 5%;
      }

      .nav-links {
        position: absolute;
        top: 70px;
        left: 5%;
        right: 5%;
        display: none;
        flex-direction: column;
        padding: 25px;
        background: rgba(5,5,18,0.95);
        border: 1px solid var(--border);
        border-radius: 18px;
      }

      .nav-links.show {
        display: flex;
      }

      .menu {
        display: block;
      }

      section {
        padding: 100px 5%;
      }

      .hero h1 {
        font-size: 3rem;
      }

      .planet-container {
        transform: scale(0.65);
        margin-top: -30px;
      }

      .skills-grid {
        grid-template-columns: 1fr 1fr;
      }

      .stats {
        grid-template-columns: 1fr;
      }

      .timeline-item {
        padding-left: 55px;
      }
    }

  </style>
</head>

<body>

  <!-- =======================================================
       FONDO ESPACIAL
  ======================================================== -->

  <div class="space">
    <div class="stars"></div>
    <div class="stars2"></div>
    <div class="stars3"></div>

    <div class="nebula one"></div>
    <div class="nebula two"></div>
    <div class="nebula three"></div>
  </div>


  <!-- =======================================================
       NAVBAR
  ======================================================== -->

  <header>

    <nav>

      <a href="#inicio" class="logo">
        AHSLY<span>.</span>
      </a>

      <ul class="nav-links" id="navLinks">

        <li>
          <a href="#inicio">Inicio</a>
        </li>

        <li>
          <a href="#sobre-mi">Sobre mí</a>
        </li>

        <li>
          <a href="#skills">Tecnologías</a>
        </li>

        <li>
          <a href="#proyectos">Proyectos</a>
        </li>

        <li>
          <a href="#viaje">Mi viaje</a>
        </li>

        <li>
          <a href="#contacto">Contacto</a>
        </li>

      </ul>

      <div class="menu" id="menu">
        <i class="fa-solid fa-bars"></i>
      </div>

    </nav>

  </header>


  <!-- =======================================================
       HERO
  ======================================================== -->

  <section id="inicio">

    <div class="hero">

      <div class="hero-text reveal">

        <div class="status">
          <span class="status-dot"></span>
          Disponible para aprender y crear
        </div>

        <h1>
          Ahsly<br>
          <span>Valentina</span>
        </h1>

        <h2>
          Desarrolladora de Software 🚀
        </h2>

        <p>
          Explorando ideas, aprendiendo nuevas tecnologías
          y construyendo soluciones digitales.
          Este es mi pequeño rincón del universo.
        </p>

        <div class="buttons">

          <a href="#proyectos" class="btn primary">
            <i class="fa-solid fa-rocket"></i>
            Ver mis proyectos
          </a>

          <a href="#contacto" class="btn secondary">
            <i class="fa-regular fa-paper-plane"></i>
            Contactarme
          </a>

        </div>

      </div>


      <div class="planet-container reveal">

        <div class="orbit"></div>

        <div class="planet"></div>

      </div>

    </div>

  </section>


  <!-- =======================================================
       SOBRE MÍ
  ======================================================== -->

  <section id="sobre-mi">

    <div class="container">

      <div class="section-title reveal">

        <span class="mini">
          01 // IDENTIDAD
        </span>

        <h2>
          Conoce a la exploradora
        </h2>

      </div>


      <div class="about-grid">

        <div class="about-text reveal">

          <p>
            Soy <strong>Ahsly Valentina</strong>,
            estudiante de Análisis y Desarrollo de Software.
          </p>

          <br>

          <p>
            Me interesa el mundo de la programación,
            el desarrollo web y la creación de proyectos
            que combinen funcionalidad con una experiencia
            visual atractiva.
          </p>

          <br>

          <p>
            Actualmente estoy construyendo mi camino como
            desarrolladora, aprendiendo constantemente y
            convirtiendo cada proyecto en una nueva misión.
          </p>

        </div>


        <div class="stats reveal">

          <div class="stat">
            <i class="fa-solid fa-user-astronaut"></i>
            <h3>ADSO</h3>
            <p>Análisis y Desarrollo de Software</p>
          </div>

          <div class="stat">
            <i class="fa-solid fa-code"></i>
            <h3>Web</h3>
            <p>Desarrollo de aplicaciones web</p>
          </div>

          <div class="stat">
            <i class="fa-solid fa-lightbulb"></i>
            <h3>Creatividad</h3>
            <p>Ideas convertidas en proyectos</p>
          </div>

          <div class="stat">
            <i class="fa-solid fa-rocket"></i>
            <h3>Futuro</h3>
            <p>Siempre aprendiendo algo nuevo</p>
          </div>

        </div>

      </div>

    </div>

  </section>


  <!-- =======================================================
       TECNOLOGÍAS
  ======================================================== -->

  <section id="skills">

    <div class="container">

      <div class="section-title reveal">

        <span class="mini">
          02 // EQUIPAMIENTO
        </span>

        <h2>
          Tecnologías
        </h2>

        <p>
          Algunas de las herramientas que utilizo
          para construir mis proyectos.
        </p>

      </div>


      <div class="skills-grid">

        <div class="skill reveal">
          <i class="fa-brands fa-html5"></i>
          <h3>HTML5</h3>
        </div>

        <div class="skill reveal">
          <i class="fa-brands fa-css3-alt"></i>
          <h3>CSS3</h3>
        </div>

        <div class="skill reveal">
          <i class="fa-brands fa-js"></i>
          <h3>JavaScript</h3>
        </div>

        <div class="skill reveal">
          <i class="fa-brands fa-python"></i>
          <h3>Python</h3>
        </div>

        <div class="skill reveal">
          <i class="fa-brands fa-php"></i>
          <h3>PHP</h3>
        </div>

        <div class="skill reveal">
          <i class="fa-solid fa-database"></i>
          <h3>SQL</h3>
        </div>

        <div class="skill reveal">
          <i class="fa-brands fa-git-alt"></i>
          <h3>Git</h3>
        </div>

        <div class="skill reveal">
          <i class="fa-brands fa-github"></i>
          <h3>GitHub</h3>
        </div>

      </div>

    </div>

  </section>


  <!-- =======================================================
       PROYECTOS
  ======================================================== -->

  <section id="proyectos">

    <div class="container">

      <div class="section-title reveal">

        <span class="mini">
          03 // MISSION CONTROL
        </span>

        <h2>
          Mis proyectos
        </h2>

        <p>
          Cada proyecto representa una misión,
          un problema y una oportunidad para aprender.
        </p>

      </div>


      <div class="projects-grid">


        <!-- PROYECTO 1 -->

        <article class="project reveal">

          <div class="project-image">

            <i class="fa-solid fa-calendar-check"></i>

          </div>

          <div class="project-content">

            <span class="project-number">
              MISSION 001
            </span>

            <h3>
              Reserva Restaurante
            </h3>

            <p>
              Aplicación web para gestionar reservas
              y facilitar la administración de un restaurante.
            </p>

            <div class="tags">

              <span class="tag">HTML</span>
              <span class="tag">CSS</span>
              <span class="tag">JavaScript</span>

            </div>

            <a href="#" class="project-link">
              Ver proyecto
              <i class="fa-solid fa-arrow-right"></i>
            </a>

          </div>

        </article>


        <!-- PROYECTO 2 -->

        <article class="project reveal">

          <div class="project-image">

            <i class="fa-solid fa-chart-line"></i>

          </div>

          <div class="project-content">

            <span class="project-number">
              MISSION 002
            </span>

            <h3>
              Finanzas Personales
            </h3>

            <p>
              Aplicación para registrar, organizar
              y analizar ingresos y gastos personales.
            </p>

            <div class="tags">

              <span class="tag">Python</span>
              <span class="tag">HTML</span>
              <span class="tag">CSS</span>
              <span class="tag">JavaScript</span>

            </div>

            <a href="#" class="project-link">
              Ver proyecto
              <i class="fa-solid fa-arrow-right"></i>
            </a>

          </div>

        </article>


        <!-- PROYECTO 3 -->

        <article class="project reveal">

          <div class="project-image">

            <i class="fa-solid fa-rocket"></i>

          </div>

          <div class="project-content">

            <span class="project-number">
              MISSION 003
            </span>

            <h3>
              Pentasoft
            </h3>

            <p>
              Sistema para gestionar eventos,
              participantes, inscripciones y actividades.
            </p>

            <div class="tags">

              <span class="tag">HTML</span>
              <span class="tag">CSS</span>
              <span class="tag">PHP</span>
              <span class="tag">SQL</span>

            </div>

            <a href="#" class="project-link">
              Ver proyecto
              <i class="fa-solid fa-arrow-right"></i>
            </a>

          </div>

        </article>

      </div>

    </div>

  </section>


  <!-- =======================================================
       MI VIAJE
  ======================================================== -->

  <section id="viaje">

    <div class="container">

      <div class="section-title reveal">

        <span class="mini">
          04 // FLIGHT LOG
        </span>

        <h2>
          Mi viaje
        </h2>

        <p>
          El camino que estoy recorriendo para convertirme
          en una gran desarrolladora.
        </p>

      </div>


      <div class="timeline">


        <div class="timeline-item reveal">

          <div class="timeline-dot"></div>

          <span>START</span>

          <h3>
            Descubrí el desarrollo
          </h3>

          <p>
            Comencé a conocer el mundo de la programación
            y descubrí que podía crear cosas desde cero.
          </p>

        </div>


        <div class="timeline-item reveal">

          <div class="timeline-dot"></div>

          <span>MISSION 01</span>

          <h3>
            Desarrollo Web
          </h3>

          <p>
            Aprendí HTML, CSS y JavaScript para construir
            mis primeras páginas y aplicaciones.
          </p>

        </div>


        <div class="timeline-item reveal">

          <div class="timeline-dot"></div>

          <span>MISSION 02</span>

          <h3>
            Programación
          </h3>

          <p>
            Empecé a trabajar con Python, PHP,
            bases de datos y lógica de programación.
          </p>

        </div>


        <div class="timeline-item reveal">

          <div class="timeline-dot"></div>

          <span>MISSION 03</span>

          <h3>
            Git & GitHub
          </h3>

          <p>
            Aprendí a gestionar proyectos y compartir
            mi código utilizando Git y GitHub.
          </p>

        </div>


        <div class="timeline-item reveal">

          <div class="timeline-dot"></div>

          <span>NEXT DESTINATION</span>

          <h3>
            Construyendo mi futuro 🚀
          </h3>

          <p>
            Seguir aprendiendo, crear proyectos cada vez
            mejores y convertir la programación en mi profesión.
          </p>

        </div>

      </div>

    </div>

  </section>


  <!-- =======================================================
       CONTACTO
  ======================================================== -->

  <section id="contacto">

    <div class="container">

      <div class="contact-box reveal">

        <div class="signal">
          TRANSMISIÓN DE SEÑAL
        </div>

        <h2>
          ¿Trabajamos juntos?
        </h2>

        <p>
          Si tienes una idea, un proyecto o simplemente
          quieres conocer mi trabajo, puedes encontrarme
          en las siguientes coordenadas.
        </p>

        <div class="socials">

          <!-- CAMBIA ESTOS # POR TUS ENLACES -->

          <a href="#" class="social" title="GitHub">
            <i class="fa-brands fa-github"></i>
          </a>

          <a href="#" class="social" title="LinkedIn">
            <i class="fa-brands fa-linkedin-in"></i>
          </a>

          <a href="mailto:tu-correo@gmail.com"
             class="social"
             title="Correo">
            <i class="fa-solid fa-envelope"></i>
          </a>

        </div>

      </div>

    </div>

  </section>


  <!-- =======================================================
       FOOTER
  ======================================================== -->

  <footer>

    <p>
      © 2026 Ahsly Valentina ·
      Made with curiosity & code <span>🚀</span>
    </p>

  </footer>


  <!-- =======================================================
       JAVASCRIPT
  ======================================================== -->

  <script>

    /* ==========================================
       MENÚ MOBILE
    ========================================== */

    const menu = document.getElementById("menu");
    const navLinks = document.getElementById("navLinks");

    menu.addEventListener("click", () => {

      navLinks.classList.toggle("show");

    });


    /* ==========================================
       CERRAR MENÚ AL HACER CLICK
    ========================================== */

    document.querySelectorAll(".nav-links a").forEach(link => {

      link.addEventListener("click", () => {

        navLinks.classList.remove("show");

      });

    });


    /* ==========================================
       ANIMACIÓN AL HACER SCROLL
    ========================================== */

    const reveals = document.querySelectorAll(".reveal");

    const observer = new IntersectionObserver(

      entries => {

        entries.forEach(entry => {

          if (entry.isIntersecting) {

            entry.target.classList.add("active");

          }

        });

      },

      {
        threshold: 0.12
      }

    );


    reveals.forEach(element => {

      observer.observe(element);

    });


    /* ==========================================
       EFECTO DE MOVIMIENTO DEL PLANETA
    ========================================== */

    const planet = document.querySelector(".planet");

    document.addEventListener("mousemove", event => {

      const x = (window.innerWidth / 2 - event.clientX) / 80;
      const y = (window.innerHeight / 2 - event.clientY) / 80;

      planet.style.transform =
        `translate(${x}px, ${y}px)`;

    });


    /* ==========================================
       AÑO AUTOMÁTICO
    ========================================== */

    const footerYear = document.querySelector("footer");

    footerYear.innerHTML = `
      <p>
        © ${new Date().getFullYear()} Ahsly Valentina ·
        Made with curiosity & code <span>🚀</span>
      </p>
    `;

  </script>

</body>
</html>
```
