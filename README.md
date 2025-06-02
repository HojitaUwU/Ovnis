# Ovnis
Sitio que informa el avistamientos de ovnis en las diferentes partes del mundo
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Avistamientos OVNI en EE.UU.</title>
  <style>
    body {
      margin: 0;
      padding: 0;
      background-image: url('imagenes/Fondo Ovni.jpg');
      background-size: cover;
      background-attachment: fixed;
      background-position: center;
      font-family: Arial, sans-serif;
      color: white;
      text-shadow: 1px 1px 2px black;
    }

    .container {
      background-color: rgba(0, 0, 0, 0.75);
      margin: 2rem auto;
      padding: 2rem;
      max-width: 1000px;
      border-radius: 15px;
    }

    h1, h2 {
      text-align: center;
      margin-bottom: 1rem;
    }

    p {
      font-size: 1.1rem;
      line-height: 1.6;
      text-align: justify;
    }

    img {
      display: block;
      max-width: 90%;
      margin: 2rem auto;
      border: 4px solid white;
      border-radius: 10px;
      box-shadow: 0 0 10px black;
      width: 100%;
      height: auto;
    }

    .quote {
      font-style: italic;
      text-align: center;
      margin-top: 1rem;
    }

    nav {
      text-align: center;
      margin-top: 1rem;
    }

    nav a {
      margin: 0 1rem;
      color: lightgreen;
      font-weight: bold;
      text-decoration: none;
    }

    .galeria-evidencias img {
      max-width: 100%;
      margin: 1rem auto;
      cursor: pointer;
      transition: transform 0.3s;
    }

    .galeria-evidencias img:hover {
      transform: scale(1.03);
    }

    #lightbox {
      display: none;
      position: fixed;
      z-index: 999;
      top: 0; left: 0;
      width: 100%;
      height: 100%;
      background: rgba(0,0,0,0.8);
    }

    #lightbox img {
      display: block;
      max-width: 90%;
      max-height: 80%;
      margin: 5% auto;
      border: 4px solid white;
      border-radius: 10px;
      box-shadow: 0 0 20px black;
    }

    #lightbox:target {
      display: block;
    }
  </style>
</head>
<body>

  <!-- 🎵 Música ambiental -->
  <audio id="bg-music" loop preload="auto">
    <source src="imagenes/Rick and Morty Theme Song [HD].mp3" type="audio/mpeg">
    Tu navegador no soporta la reproducción de audio.
  </audio>

  <script>
    document.body.addEventListener('click', function() {
      var audio = document.getElementById('bg-music');
      if (audio.paused) {
        audio.volume = 0.3;
        audio.play();
      }
    });
  </script>

  <div class="container">
    <h1>🌌 Avistamientos de OVNIs en Estados Unidos</h1>

    <nav>
      <a href="#evidencia">📂 Ver Evidencia de Trabajo</a>
    </nav>

    <p>
      Este sitio presenta una visualización de datos basada en reportes de objetos voladores no identificados (OVNIs) observados en Estados Unidos. Se utilizaron herramientas estadísticas para entender patrones comunes.
    </p>

    <h2>📊 Formas Comunes de OVNIs</h2>
    <img src="imagenes/Imagen grafico Formas comunes de Ovnis.png" alt="Formas de OVNI">

    <h2>📈 Avistamientos por Año en EE.UU.</h2>
    <img src="imagenes/Imagen grafico de Ovnis por años en EEUU.png" alt="Ovnis por año">

    <h2>🗺️ Top 10 Estados con más Reportes</h2>
    <img src="imagenes/Imagen grafico top 10 estados .png" alt="Top 10 estados con más reportes">

    <h2>👤 Autor</h2>
    <p>
      Proyecto desarrollado por <strong>Benjamín Alejandro Fierro Guzmán</strong> como parte de un trabajo de análisis de datos con enfoque visual.
    </p>
    <p class="quote">_"La verdad está ahí afuera... pero los datos están aquí."_</p>
  </div>

  <!-- Sección de Evidencia de Trabajo -->
  <div class="container" id="evidencia">
    <h2>📂 Evidencia de Trabajo</h2>
    <p>A continuación se muestran capturas del desarrollo del proyecto:</p>
    <div class="galeria-evidencias" id="galeria-evidencias"></div>
  </div>

  <!-- Lightbox para ampliar imágenes -->
  <div id="lightbox">
    <img id="lightbox-img" src="" alt="Vista ampliada">
  </div>

  <script>
    const evidencias = [
      "Captura desde 2025-05-27 11-45-34.png",
      "Captura desde 2025-05-27 11-46-51.png",
      "Captura desde 2025-05-28 18-46-36.png",
      "Captura desde 2025-05-28 18-46-51.png",
      "Captura desde 2025-05-28 19-12-13.png",
      "Captura desde 2025-05-31 12-21-03.png",
      "Captura desde 2025-05-31 12-21-26.png",
      "Captura desde 2025-05-31 12-22-55.png",
      "Captura desde 2025-05-31 12-23-04.png",
      "Captura desde 2025-05-31 12-25-19.png",
      "Captura desde 2025-05-31 12-26-22.png",
      "Captura desde 2025-05-31 12-26-46.png"
    ];

    const galeria = document.getElementById("galeria-evidencias");
    const lightbox = document.getElementById("lightbox");
    const lightboxImg = document.getElementById("lightbox-img");

    evidencias.forEach(nombre => {
      const img = document.createElement("img");
      img.src = "imagenes/" + nombre;
      img.alt = nombre;
      img.addEventListener("click", () => {
        lightbox.style.display = "block";
        lightboxImg.src = img.src;
      });
      galeria.appendChild(img);
    });

    lightbox.addEventListener("click", () => {
      lightbox.style.display = "none";
    });
  </script>

</body>
</html>
