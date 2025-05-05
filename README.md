<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <title>Sorpresa para Briyidth</title>
  <link href="https://fonts.googleapis.com/css2?family=Pacifico&family=Quicksand:wght@500&display=swap" rel="stylesheet">
  <style>
    body {
      margin: 0;
      background: linear-gradient(to top, #ffdee9, #ffcad4);
      font-family: 'Quicksand', sans-serif;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      min-height: 100vh;
      overflow-x: hidden;
    }

    .inicio {
      text-align: center;
      margin-top: 50px;
    }

    .boton-sorpresa {
      font-size: 2.2rem;
      background: radial-gradient(circle, #ff69b4, #ff1493);
      color: white;
      padding: 20px 45px;
      border: none;
      border-radius: 40px;
      cursor: pointer;
      box-shadow: 0 0 25px #ffb6c1;
      font-family: 'Pacifico', cursive;
      transition: all 0.4s ease;
      animation: parpadeo 1.5s infinite;
    }

    .boton-sorpresa:hover {
      background: radial-gradient(circle, #ff85c1, #db0c8b);
      transform: scale(1.07);
    }

    @keyframes parpadeo {
      0%, 100% { box-shadow: 0 0 20px #ff85c1; }
      50% { box-shadow: 0 0 35px #ff2e9e; }
    }

    .mensaje {
      display: none;
      text-align: center;
      padding: 40px;
      max-width: 700px;
      animation: aparecer 2s ease-in-out forwards;
      color: #c90076;
    }

    @keyframes aparecer {
      from { opacity: 0; transform: translateY(50px); }
      to { opacity: 1; transform: translateY(0); }
    }

    .mensaje h1 {
      font-family: 'Pacifico', cursive;
      font-size: 2.8rem;
      margin-bottom: 20px;
      color: #e60073;
      text-shadow: 0 0 10px #ffc0cb;
    }

    .mensaje p {
      font-size: 1.5rem;
      margin: 10px 0;
      line-height: 1.6;
    }

    .flor {
      width: 120px;
      height: 120px;
      margin: 20px auto;
      animation: crecer 3s ease-out forwards;
    }

    @keyframes crecer {
      0% { transform: scale(0); opacity: 0; }
      100% { transform: scale(1); opacity: 1; }
    }

    .corazones {
      font-size: 2rem;
      animation: latido 1.5s infinite;
    }

    @keyframes latido {
      0%, 100% { transform: scale(1); }
      50% { transform: scale(1.2); }
    }

    .tarjeta {
      background-color: #fff0f5;
      border: 1px solid #ffadd6;
      border-radius: 12px;
      padding: 15px 20px;
      margin-top: 30px;
      box-shadow: 0 0 10px #ffc0cb;
      max-width: 300px;
      font-size: 0.9rem;
      color: #a0005e;
      text-align: left;
    }

    .tarjeta strong {
      display: block;
      margin-bottom: 6px;
    }

    footer {
      margin-top: 50px;
      font-size: 0.9rem;
      color: #a0005e;
    }
  </style>
</head>
<body>

  <div class="inicio">
    <button class="boton-sorpresa" onclick="mostrarMensaje()">TE TENGO UNA SORPRESA MI AMOR</button>
  </div>

  <div class="mensaje" id="mensaje">
    <img src="https://i.pinimg.com/originals/e9/b3/8f/e9b38f9996ffb31b8cc28ed2cb0c9ed7.png" alt="Flor Creciendo" class="flor" />
    <h1>Para Mi Reina BriyidthCha</h1>
    <p>Desde que llegaste a mi vida, todo tiene más color, más sentido y más amor.</p>
    <p>Gracias por ser mi sol, mi paz, mi todo. Eres lo mejor que tengo, y te elijo una y otra vez.</p>
    <p>¡Te amo con toda mi alma, mi reina hermosa!</p>
    <div class="corazones">❤️‍🔥💗💫💘🌸🌷🌹✨💖💞</div>
    <p>Tuyo por siempre: <strong>Anth'Zz Berrocal</strong></p>

    <div class="tarjeta">
      <strong>Información del creador:</strong>
      <p><strong>Alias:</strong> BerMatModZ</p>
      <p><strong>Nombre:</strong> Anth'Zz Berrocal</p>
      <p><strong>Especialidad:</strong> Bots de WhatsApp, IA, ciberseguridad</p>
      <p><strong>Ubicación:</strong> Andahuaylas, Perú</p>
    </div>
  </div>

  <footer>
    © 2025 Hecho con todo el amor del mundo para Briyidth Jhorgina
  </footer>

  <script>
    function mostrarMensaje() {
      document.querySelector('.inicio').style.display = 'none';
      document.getElementById('mensaje').style.display = 'block';
    }
  </script>

</body>
</html>
