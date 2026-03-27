<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <title>Mi Portafolio de Luis Pro</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0">

  <!-- Fuente -->
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;500;700&display=swap" rel="stylesheet">

  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      font-family: 'Poppins', sans-serif;
    }

    body {
      background: linear-gradient(135deg, #000000, #020a1f, #000000);
      color: white;
      overflow-x: hidden;
    }

    header {
      text-align: center;
      padding: 80px 20px;
      animation: fadeDown 1.5s ease;
    }

    header h1 {
      font-size: 3rem;
      color: #4da6ff;
      text-shadow: 0 0 15px #4da6ff;
    }

    nav {
      display: flex;
      justify-content: center;
      gap: 25px;
      padding: 15px;
      background: rgba(0,0,0,0.8);
      backdrop-filter: blur(10px);
      position: sticky;
      top: 0;
      z-index: 1000;
    }

    nav a {
      color: #4da6ff;
      text-decoration: none;
      transition: 0.3s;
    }

    nav a:hover {
      color: white;
      text-shadow: 0 0 10px #4da6ff;
    }

    section {
      padding: 80px 20px;
      max-width: 900px;
      margin: auto;
      opacity: 0;
      transform: translateY(50px);
      transition: 1s;
    }

    section.visible {
      opacity: 1;
      transform: translateY(0);
    }

    h2 {
      color: #4da6ff;
      margin-bottom: 20px;
    }

    /* Proyectos */
    .proyecto {
      background: #0a0a0a;
      padding: 20px;
      margin: 20px 0;
      border-radius: 10px;
      transition: 0.4s;
      box-shadow: 0 0 10px #000;
    }

    .proyecto:hover {
      transform: translateY(-5px);
      box-shadow: 0 0 20px #4da6ff;
    }

    /* Habilidades */
    .skill {
      margin: 20px 0;
    }

    .bar {
      height: 10px;
      background: #222;
      border-radius: 10px;
      overflow: hidden;
    }

    .progress {
      height: 100%;
      width: 0;
      background: linear-gradient(90deg, #4da6ff, #00c3ff);
      transition: 2s;
    }

    /* Botones */
    button {
      background: #4da6ff;
      border: none;
      padding: 10px 20px;
      margin-top: 10px;
      border-radius: 5px;
      cursor: pointer;
      transition: 0.3s;
    }

    button:hover {
      box-shadow: 0 0 10px #4da6ff;
    }

    /* Redes */
    .redes {
      display: flex;
      gap: 20px;
      margin-top: 20px;
    }

    .redes a {
      color: #4da6ff;
      font-size: 1.5rem;
      transition: 0.3s;
    }

    .redes a:hover {
      color: white;
      text-shadow: 0 0 10px #4da6ff;
    }

    footer {
      text-align: center;
      padding: 20px;
      background: black;
      margin-top: 40px;
    }

    /* Animaciones */
    @keyframes fadeDown {
      from { opacity: 0; transform: translateY(-50px); }
      to { opacity: 1; transform: translateY(0); }
    }
  </style>
</head>

<body>

<header>
  <h1>Tu Nombre Luis Fernando</h1>
  <p>Desarrollador Web</p>
</header>

<nav>
  <a href="#sobre">Sobre mí</a>
  <a href="#proyectos">Proyectos</a>
  <a href="#habilidades">Habilidades</a>
  <a href="#contacto">Contacto</a>
</nav>

<section id="sobre">
  <h2>Sobre mí</h2>
  <p>Soy desarrollador web apasionado por crear experiencias modernas y dinámicas.</p>
</section>

<section id="proyectos">
  <h2>Proyectos</h2>

  <div class="proyecto">
    <h3>Proyecto 1</h3>
    <p>Descripción de tu proyecto.</p>
    <button onclick="alert('Proyecto 1')">Ver</button>
  </div>

  <div class="proyecto">
    <h3>Proyecto 2</h3>
    <p>Descripción de tu proyecto.</p>
    <button onclick="alert('Proyecto 2')">Ver</button>
  </div>

</section>

<section id="habilidades">
  <h2>Habilidades</h2>

  <div class="skill">
    <p>HTML</p>
    <div class="bar"><div class="progress" data-width="90%"></div></div>
  </div>

  <div class="skill">
    <p>CSS</p>
    <div class="bar"><div class="progress" data-width="80%"></div></div>
  </div>

  <div class="skill">
    <p>JavaScript</p>
    <div class="bar"><div class="progress" data-width="75%"></div></div>
  </div>

</section>

<section id="contacto">
  <h2>Contacto</h2>
  <p>Email: luiscalderonllanque@gmail.com</p>

  <div class="redes">
    <a href="#">🌐</a>
    <a href="#">💼</a>
    <a href="#">🐙</a>
  </div>

  <button onclick="alert('Mensaje enviado 🚀')">Enviar mensaje</button>
</section>

<footer>
  <p>© 2026 - Portafolio Pro</p>
</footer>

<script>
  // Scroll animaciones
  const sections = document.querySelectorAll("section");

  window.addEventListener("scroll", () => {
    sections.forEach(sec => {
      const top = sec.getBoundingClientRect().top;
      if (top < window.innerHeight - 100) {
        sec.classList.add("visible");
      }
    });
  });

  // Animación barras
  window.addEventListener("scroll", () => {
    document.querySelectorAll(".progress").forEach(bar => {
      const top = bar.getBoundingClientRect().top;
      if (top < window.innerHeight) {
        bar.style.width = bar.dataset.width;
      }
    });
  });
</script>

</body>
</html>
