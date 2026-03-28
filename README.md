<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Portafolio | Luis Fernando</title>

<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;500;700&display=swap" rel="stylesheet">

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: 'Poppins', sans-serif;
}

body {
  background: radial-gradient(circle at top, #0a0f2c, #000000 60%);
  color: white;
  overflow-x: hidden;
}

/* NAV */
nav {
  display: flex;
  justify-content: center;
  gap: 30px;
  padding: 15px;
  background: rgba(0,0,0,0.7);
  backdrop-filter: blur(10px);
  position: sticky;
  top: 0;
  z-index: 1000;
}

nav a {
  color: #6aa8ff;
  text-decoration: none;
  transition: 0.3s;
}

nav a:hover {
  color: #b57cff;
  text-shadow: 0 0 10px #6aa8ff;
}

/* HEADER */
header {
  text-align: center;
  padding: 100px 20px;
  animation: fadeDown 1.5s ease;
}

header h1 {
  font-size: 3.2rem;
  background: linear-gradient(90deg, #6aa8ff, #b57cff);
  -webkit-background-clip: text;
  color: transparent;
}

header p {
  color: #aaa;
}

/* SECCIONES */
section {
  padding: 80px 20px;
  max-width: 900px;
  margin: auto;
  opacity: 0;
  transform: translateY(40px);
  transition: 1s;
}

section.visible {
  opacity: 1;
  transform: translateY(0);
}

h2 {
  color: #6aa8ff;
  margin-bottom: 20px;
}

/* TARJETAS */
.card {
  background: #0c0c0c;
  padding: 20px;
  margin: 20px 0;
  border-radius: 12px;
  transition: 0.4s;
  box-shadow: 0 0 15px #000;
}

.card:hover {
  transform: translateY(-8px);
  box-shadow: 0 0 25px #6aa8ff;
}

/* HABILIDADES */
.skill {
  margin: 20px 0;
}

.bar {
  height: 12px;
  background: #1a1a1a;
  border-radius: 10px;
  overflow: hidden;
}

.progress {
  height: 100%;
  width: 0;
  background: linear-gradient(90deg, #6aa8ff, #b57cff);
  transition: 2s;
}

/* BOTONES */
button {
  background: linear-gradient(90deg, #6aa8ff, #b57cff);
  border: none;
  padding: 10px 20px;
  border-radius: 6px;
  color: white;
  cursor: pointer;
}

button:hover {
  box-shadow: 0 0 15px #6aa8ff;
}

/* REDES */
.redes {
  display: flex;
  gap: 20px;
  margin-top: 20px;
}

.redes a {
  font-size: 1.6rem;
  color: #6aa8ff;
  transition: 0.3s;
}

.redes a:hover {
  color: #b57cff;
}

/* FOOTER */
footer {
  text-align: center;
  padding: 20px;
  background: black;
  margin-top: 40px;
}

/* ANIMACIONES */
@keyframes fadeDown {
  from {opacity:0; transform:translateY(-50px);}
  to {opacity:1; transform:translateY(0);}
}
</style>
</head>

<body>

<nav>
  <a href="#sobre">Sobre mí</a>
  <a href="#proyectos">Proyectos</a>
  <a href="#habilidades">Habilidades</a>
  <a href="#contacto">Contacto</a>
</nav>

<header>
  <h1>Luis Fernando</h1>
  <p>Estudiante de Ingeniería Estadística e Informática</p>
</header>

<section id="sobre">
  <h2>Sobre mí</h2>
  <p>
    Soy estudiante de Ingeniería Estadística e Informática, apasionado por la tecnología,
    el análisis de datos y el desarrollo web moderno. Busco mejorar continuamente mis habilidades
    y crear proyectos innovadores.
  </p>
</section>

<section id="proyectos">
  <h2>Proyectos</h2>

  <div class="card">
    <h3>Proyecto 1</h3>
    <p>Aplicación web en desarrollo.</p>
    <button onclick="alert('Proyecto en construcción')">Ver</button>
  </div>

  <div class="card">
    <h3>Proyecto 2</h3>
    <p>Análisis de datos y visualización.</p>
    <button onclick="alert('Proyecto en construcción')">Ver</button>
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
    <div class="bar"><div class="progress" data-width="85%"></div></div>
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

  <button onclick="alert('Gracias por contactarme 🚀')">Enviar mensaje</button>
</section>

<footer>
  <p>© 2026 - Luis Fernando</p>
</footer>

<script>
const sections = document.querySelectorAll("section");

window.addEventListener("scroll", () => {
  sections.forEach(sec => {
    if (sec.getBoundingClientRect().top < window.innerHeight - 100) {
      sec.classList.add("visible");
    }
  });

  document.querySelectorAll(".progress").forEach(bar => {
    if (bar.getBoundingClientRect().top < window.innerHeight) {
      bar.style.width = bar.dataset.width;
    }
  });
});
</script>

</body>
</html>
