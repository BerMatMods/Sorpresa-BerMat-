<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>💍 Aniversario con Briyidth 💖</title>
  <link href="https://fonts.googleapis.com/css2?family=Pacifico&family=Great+Vibes&family=Raleway:wght@400;700&display=swap" rel="stylesheet">
  <style>
    body {
      margin: 0;
      padding: 0;
      background: linear-gradient(135deg, #f8e4ff, #f3c1f7);
      font-family: 'Raleway', sans-serif;
      display: flex;
      flex-direction: column;
      align-items: center;
    }

    .container {
      text-align: center;
      margin-top: 60px;
      padding: 30px;
      border-radius: 20px;
      background: rgba(255, 255, 255, 0.85);
      box-shadow: 0 0 30px rgba(192, 112, 255, 0.6);
      width: 90%;
      max-width: 650px;
    }

    .titulo {
      font-family: 'Great Vibes', cursive;
      font-size: 40px;
      color: #ba00ff;
      text-shadow: 0 0 10px #ff00f2;
      animation: parpadeo 2s infinite;
    }

    @keyframes parpadeo {
      0%, 100% { opacity: 1; }
      50% { opacity: 0.5; }
    }

    .btn {
      margin-top: 20px;
      padding: 15px 25px;
      font-size: 18px;
      background: linear-gradient(to right, #ff99cc, #cc66ff);
      border: none;
      color: white;
      border-radius: 30px;
      cursor: pointer;
      box-shadow: 0 0 15px #d66fff;
      font-family: 'Pacifico', cursive;
    }

    .mensaje {
      margin-top: 30px;
      padding: 25px;
      background-color: #ffe6ff;
      border-radius: 15px;
      font-size: 20px;
      color: #aa00aa;
      box-shadow: 0 0 15px #f0b3ff;
      display: none;
      animation: aparecer 1.5s ease-out forwards;
    }

    @keyframes aparecer {
      0% {
        opacity: 0;
        transform: translateY(20px);
      }
      100% {
        opacity: 1;
        transform: translateY(0);
      }
    }

    .flor {
      width: 60px;
      height: 60px;
      background: radial-gradient(circle at center, #ff99cc 0%, #cc66ff 80%);
      border-radius: 50%;
      animation: crecer 3s ease-out forwards;
      margin: 30px auto;
    }

    @keyframes crecer {
      from {
        transform: scale(0);
        opacity: 0;
      }
      to {
        transform: scale(1);
        opacity: 1;
      }
    }

    .imagen-extra {
      margin-top: 30px;
    }

    .imagen-extra img {
      max-width: 100%;
      border-radius: 15px;
      box-shadow: 0 0 20px #d9b3ff;
    }

    .footer {
      margin-top: 40px;
      padding: 10px;
      background: rgba(255, 255, 255, 0.7);
      border-radius: 10px;
      font-size: 13px;
      color: #6d00a3;
      font-style: italic;
      box-shadow: 0 0 10px #e0b3ff;
      text-align: center;
      width: 90%;
      max-width: 300px;
    }

    .destacado {
      font-family: 'Pacifico', cursive;
      font-size: 22px;
      color: #d100d1;
      text-shadow: 0 0 5px #ff99ff;
    }

    .contador {
      font-size: 18px;
      color: #9900cc;
      font-weight: bold;
      margin-top: 15px;
    }

    audio {
      margin-top: 20px;
    }
  </style>
</head>
<body>
  <div class="container">
    <div class="titulo">💖 FELIZ ANIVERSARIO MI AMOR 💖</div>
    <div class="contador" id="contador">Calculando el tiempo... ⏳</div>
    <button class="btn" onclick="mostrarMensaje()">Haz clic aquí, mi reina 👑</button>

    <div id="mensaje" class="mensaje">
      <div class="flor"></div>
      <p class="destacado">
        Te amo mucho mi amor, mi reina hermosa Briyidth Jhorgina. 💗<br><br>
        Hoy celebramos 1 año y 8 meses de amor verdadero, de historias únicas, sonrisas, lágrimas y sueños juntos.<br>
        Gracias por existir en mi vida. Eres mi bendición. 💫<br>
        Siempre te voy a amar, en las buenas y en las malas. 💍<br><br>
        <strong>Te amo muchísimo, mi mami, mi reina, mi todo. 💘</strong>
      </p>
      <div class="imagen-extra">
        <img src="https://i.postimg.cc/pXWvCFsC/IMG-20240924-WA0182.jpg" alt="Foto dedicada a Briyidth" />
      </div>
      <audio controls autoplay loop>
        <!-- 🎵 Reemplaza este enlace con el audio real de Cosculluela si lo tienes -->
        <source src="TU_LINK_DE_AUDIO_AQUI.mp3" type="audio/mpeg">
        Tu navegador no soporta audio.
      </audio>
    </div>
  </div>

  <div class="footer">
    Creado con amor por Anth'Zz Berrocal 💻 | Proyecto BerMatModZ ❤️
  </div>

  <script>
    function mostrarMensaje() {
      document.getElementById("mensaje").style.display = "block";
    }

    // 🕓 Contador desde el 10 noviembre 2023
    const inicio = new Date("2023-11-10T00:00:00");
    const contador = document.getElementById("contador");

    function actualizarContador() {
      const ahora = new Date();
      let diferencia = ahora - inicio;

      const segundos = Math.floor(diferencia / 1000) % 60;
      const minutos = Math.floor(diferencia / 1000 / 60) % 60;
      const horas = Math.floor(diferencia / (1000 * 60 * 60)) % 24;
      const diasTotales = Math.floor(diferencia / (1000 * 60 * 60 * 24));
      const meses = Math.floor(diasTotales / 30);
      const dias = diasTotales % 30;

      contador.innerHTML = `💞 Llevamos juntos: ${meses} meses, ${dias} días, ${horas}h ${minutos}m ${segundos}s 💞`;
    }

    setInterval(actualizarContador, 1000);
  </script>
</body>
</html></body>
</html>
