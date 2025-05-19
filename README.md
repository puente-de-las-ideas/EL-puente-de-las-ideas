<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>El Puente de las Ideas</title>
  <!-- Google Fonts -->
  <link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@600&family=Open+Sans&display=swap" rel="stylesheet">
  <!-- Font Awesome para íconos -->
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
  <!-- Librería marked para convertir Markdown a HTML -->
  <script src="https://cdn.jsdelivr.net/npm/marked/marked.min.js"></script>
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      font-family: 'Open Sans', sans-serif;
      background-color: #FFFFFF;
      color: #1C2526;
      line-height: 1.6;
    }

    /* Header */
    header {
      background-color: #1C2526;
      padding: 1.5rem 1rem;
      display: flex;
      align-items: center;
      justify-content: flex-start;
    }

    .header-container {
      display: flex;
      align-items: center;
      max-width: 1200px;
      width: 100%;
    }

    .logo img {
      width: 80px;
      height: auto;
      margin-right: 0.5rem;
    }

    .title-slogan {
      flex: 1;
    }

    .title-slogan h1 {
      font-family: 'Montserrat', sans-serif;
      color: #FFFFFF;
      font-size: 2.2rem;
      margin-bottom: 0.2rem;
      text-shadow: 1px 1px 2px rgba(0, 0, 0, 0.2);
      text-transform: uppercase;
    }

    .title-slogan p {
      color: #FFFFFF;
      font-size: 1rem;
      font-style: italic;
      text-transform: none;
    }

    .title-slogan p::first-letter {
      text-transform: capitalize;
    }

    /* Navegación */
    nav {
      background-color: #2E4F3A;
      padding: 1rem;
      text-align: center;
    }

    nav a {
      font-family: 'Montserrat', sans-serif;
      color: #FFFFFF;
      text-decoration: none;
      margin: 0 1.5rem;
      font-weight: 600;
      transition: color 0.3s ease;
    }

    nav a:hover {
      color: #5A8A6F;
    }

    /* Contenido Principal (Dos Columnas) */
    main {
      max-width: 1200px;
      margin: 0 auto;
      padding: 3rem 2rem;
      display: flex;
      gap: 2rem;
      min-height: calc(100vh - 300px);
    }

    .content-column {
      flex: 2;
    }

    .social-column {
      flex: 1;
      display: flex;
      flex-direction: column;
      gap: 0.75rem;
      align-items: flex-end;
    }

    /* Secciones */
    section {
      display: none;
      margin-bottom: 4rem;
    }

    section.active {
      display: block;
    }

    section h2 {
      font-family: 'Montserrat', sans-serif;
      color: #2E4F3A;
      font-size: 1.8rem;
      margin-bottom: 1rem;
      border-bottom: 2px solid #1C2526;
      padding-bottom: 0.5rem;
      display: flex;
      align-items: center;
    }

    section h2 i {
      margin-right: 0.5rem;
      color: #2E4F3A;
    }

    section .content {
      font-size: 1rem;
      margin-bottom: 1rem;
      text-align: justify;
    }

    /* Recuadros de Redes Sociales */
    .social-box {
      background-color: #2E4F3A;
      color: #FFFFFF;
      padding: 0.5rem;
      text-align: center;
      border-radius: 5px;
      font-family: 'Montserrat', sans-serif;
      font-weight: 600;
      font-size: 0.75rem;
      width: 75%;
      transition: background-color 0.3s ease;
    }

    .social-box:hover {
      background-color: #5A8A6F;
    }

    .social-box i {
      margin-right: 0.3rem;
    }

    /* Footer (Contacto) */
    footer {
      background-color: #1C2526;
      color: #FFFFFF;
      text-align: center;
      padding: 2rem;
      position: relative;
      bottom: 0;
      width: 100%;
    }

    footer h2 {
      font-family: 'Montserrat', sans-serif;
      font-size: 1.5rem;
      margin-bottom: 1rem;
    }

    footer p {
      margin: 0.5rem 0;
    }

    footer a {
      color: #2E4F3A;
      text-decoration: none;
    }

    footer a:hover {
      text-decoration: underline;
    }

    footer i {
      margin-right: 0.5rem;
      color: #2E4F3A;
    }

    /* Responsividad */
    @media (max-width: 768px) {
      .header-container {
        flex-direction: column;
        text-align: center;
      }

      .logo img {
        margin-bottom: 1rem;
      }

      nav-Down {
        display: block;
        margin: 0.5rem 0;
      }

      main {
        flex-direction: column;
        padding: 2rem 1rem;
      }

      .social-column {
        flex-direction: row;
        flex-wrap: wrap;
        justify-content: center;
        align-items: center;
      }

      .social-box {
        flex: 1 1 40%;
        width: 50%;
      }
    }
  </style>
</head>
<body>
  <!-- Header con Logo, Título y Eslogan -->
  <header>
    <div class="header-container">
      <div class="logo">
        <img src="logo.png" alt="Logo El Puente de las Ideas">
      </div>
      <div class="title-slogan">
        <h1>EL PUENTE DE LAS IDEAS</h1>
        <p>Ideas que construyen sentido, desde la mente hasta el mundo.</p>
      </div>
    </div>
  </header>

  <!-- Navegación -->
  <nav>
    <a href="#inicio" onclick="showSection('inicio')">Inicio</a>
    <a href="#noticias" onclick="showSection('noticias')">Noticias</a>
    <a href="#analisis" onclick="showSection('analisis')">Análisis</a>
    <a href="#investigaciones" onclick="showSection('investigaciones')">Investigaciones</a>
    <a href="#sobre-mi" onclick="showSection('sobre-mi')">Sobre Mí</a>
  </nav>

  <!-- Contenido Principal (Dos Columnas) -->
  <main>
    <!-- Columna de Contenido -->
    <div class="content-column">
      <!-- Inicio -->
      <section id="inicio">
        <h2><i class="fas fa-home"></i> Inicio</h2>
        <div class="content" id="inicio-content"></div>
      </section>

      <!-- Noticias -->
      <section id="noticias">
        <h2><i class="fas fa-newspaper"></i> Noticias</h2>
        <div class="content" id="noticias-content"></div>
      </section>

      <!-- Análisis -->
      <section id="analisis">
        <h2><i class="fas fa-search"></i> Análisis</h2>
        <div class="content" id="analisis-content"></div>
      </section>

      <!-- Investigaciones -->
      <section id="investigaciones">
        <h2><i class="fas fa-book"></i> Investigaciones</h2>
        <div class="content" id="investigaciones-content"></div>
      </section>

      <!-- Sobre Mí -->
      <section id="sobre-mi">
        <h2><i class="fas fa-user"></i> Sobre Mí</h2>
        <div class="content" id="sobre-mi-content"></div>
      </section>
    </div>

    <!-- Columna de Redes Sociales -->
    <div class="social-column">
      <div class="social-box">
        <a href="https://www.facebook.com/share/15yJuHGZst/" style="color: #FFFFFF; text-decoration: none;">
          <i class="fab fa-facebook"></i> Facebook
        </a>
      </div>
      <div class="social-box">
        <a href="https://www.instagram.com/cxl_fig?igsh=cm4wcnNoNWE1dW1v" style="color: #FFFFFF; text-decoration: none;">
          <i class="fab fa-instagram"></i> Instagram
        </a>
      </div>
      <div class="social-box">
        <a href="https://x.com/CcFigaro" style="color: #FFFFFF; text-decoration: none;">
          <i class="fab fa-twitter"></i> X (Twitter)
        </a>
      </div>
      <div class="social-box">
        <a href="https://youtube.com/@ektos-mente?si=bknRu47hHvpWBy6W" style="color: #FFFFFF; text-decoration: none;">
          <i class="fab fa-youtube"></i> YouTube
        </a>
      </div>
    </div>
  </main>

  <!-- Footer (Contacto) -->
  <footer>
    <h2>Contacto</h2>
    <p><i class="fas fa-envelope"></i> Email: <a href="mailto:contacto@elpuentedelasideas.com">contacto@elpuentedelasideas.com</a></p>
    <p><i class="fas fa-phone"></i> Teléfono: +1 809-555-1234</p>
    <p>© 2025 El Puente de las Ideas. Todos los derechos reservados.</p>
  </footer>

  <!-- JavaScript para controlar la visibilidad de las secciones y cargar contenido -->
  <script>
    function showSection(sectionId) {
      // Ocultar todas las secciones
      document.querySelectorAll('section').forEach(section => {
        section.classList.remove('active');
      });

      // Mostrar la sección seleccionada
      const selectedSection = document.getElementById(sectionId);
      selectedSection.classList.add('active');

      // Cargar el contenido del archivo Markdown correspondiente
      fetch(`content/${sectionId}.md`)
        .then(response => response.text())
        .then(data => {
          // Extraer el contenido después de los metadatos (ignorar la parte entre ---)
          const content = data.split('---')[2].trim();
          // Convertir Markdown a HTML usando marked
          document.getElementById(`${sectionId}-content`).innerHTML = marked.parse(content);
        })
        .catch(error => {
          console.error('Error al cargar el contenido:', error);
          document.getElementById(`${sectionId}-content`).innerHTML = 'Error al cargar el contenido.';
        });
    }

    // Mostrar la sección "Inicio" por defecto al cargar la página
    document.addEventListener('DOMContentLoaded', () => {
      showSection('inicio');
    });
  </script>
</body>
</html>
