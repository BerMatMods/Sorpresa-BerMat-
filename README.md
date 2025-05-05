<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Sorpresa para Briyidth</title>
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
      margin-top: 80px;
      padding: 30px;
      border-radius: 20px;
      background: rgba(255, 255, 255, 0.85);
      box-shadow: 0 0 30px rgba(192, 112, 255, 0.6);
      width: 90%;
      max-width: 600px;
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
  </style>
</head>
<body>
  <div class="container">
    <div class="titulo">TE TENGO UNA SORPRESA MI AMOR</div>
    <button class="btn" onclick="mostrarMensaje()">Haz clic aquí</button>

    <div id="mensaje" class="mensaje">
      <div class="flor"></div>
      <p style="font-family:'Pacifico', cursive; font-size: 22px;">
        Te amo mucho mi amor, mi reina hermosa.<br>
        Te doy gracias por llegar a mi vida.<br>
        Eres lo más valioso que tengo y tengo miedo a perderte.<br>
        Siempre te voy a amar, en las buenas y en las malas.<br>
        Y sé que juntos vamos a salir adelante.<br><br>
        <strong>Te amo muchísimo, mi mami.</strong>
      </p>
      <div class="imagen-extra">
        <img src="https://i.postimg.cc/pXWvCFsC/IMG-20240924-WA0182.jpg" alt="Foto dedicada a Briyidth" />
      </div>
    </div>
  </div>

  <div class="footer">
    Creado con amor por Anth'Zz Berrocal | Proyecto BerMatModZ
  </div>

  <script>
    function mostrarMensaje() {
      document.getElementById("mensaje").style.display = "block";
    }
  </script>
</body>
</html>
