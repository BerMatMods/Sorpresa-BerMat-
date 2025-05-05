<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <title>Sorpresa para Briyidth</title>
  <link href="https://fonts.googleapis.com/css2?family=Great+Vibes&family=Playfair+Display:wght@700&family=Quicksand:wght@500&display=swap" rel="stylesheet">
  <style>
    body {
      margin: 0;
      background: linear-gradient(to top, #ffe0e9, #ffcad4);
      font-family: 'Quicksand', sans-serif;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      min-height: 100vh;
      overflow-x: hidden;
      color: #c90076;
    }

    .inicio {
      text-align: center;
      margin-top: 60px;
    }

    .titulo-sorpresa {
      font-size: 2.8rem;
      font-family: 'Playfair Display', serif;
      color: #d6006e;
      text-shadow: 0 0 8px #ffc0cb;
      margin-bottom: 30px;
    }

    .boton-sorpresa {
      font-size: 1.6rem;
      background: radial-gradient(circle, #ff69b4, #ff1493);
      color: white;
      padding: 15px 35px;
      border: none;
      border-radius: 40px;
      cursor: pointer;
      box-shadow: 0 0 18px #ffb6c1;
      font-family: 'Playfair Display', serif;
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
      font-family: 'Great Vibes', cursive;
      font-size: 3.5rem;
      margin-bottom: 20px;
      color: #d6006e;
      text-shadow: 0 0 10px #ffc0cb;
    }

    .mensaje p {
      font-size: 1.4rem;
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

    footer {
      margin-top: 50px;
      font-size: 0.9rem;
      color: #a0005e;
    }
  </style>
</head>
<body>

  <div class="inicio" id="inicio">
    <div class="titulo-sorpresa">TE TENGO UNA SORPRESA MI AMOR</div>
    <button class="boton-sorpresa" onclick="mostrarMensaje()">Haz clic aquí mi amor</button>
  </div>

  <div class="mensaje" id="mensaje">
    <img src="https://i.pinimg.com/originals/e9/b3/8f/e9b38f9996ffb31b8cc28ed2cb0c9ed7.png" alt="Flor" class="flor" />
    <h1>Para Mi Reina el amor de mi vida </h1>
    <p>Desde que llegaste a mi vida, todo tiene más color, más sentido y más amor.</p>
    <p>Gracias por ser mi sol, mi paz, mi todo. Eres lo mejor que tengo, y te elijo una y otra vez.</p>
    <p>¡Te amo muchísimo mi mami  hermosa!</p>
    <div class="corazones">❤️‍🔥💗💫💘🌸🌷🌹✨💖💞</div>
    <p style="font-family: 'Great Vibes', cursive; font-size: 2rem;">By: Anth'Zz Berrocal</p>

    <div class="tarjeta">
      <strong>Información del creador:</strong>
      <p><strong>Alias:</strong> BerMatModZ</p>
      <p><strong>Nombre:</strong> Anth'Zz Berrocal</p>
      <p><strong>Especialidad:</strong> Bots, IA, Ciberseguridad</p>
      <p><strong>Ubicación:</strong> Andahuaylas, Perú</p>
    </div>
  </div>

  <footer>
    © 2025 Hecho con todo el amor del mundo para Briyidth  de By: BerMatModZ 
  </footer>

  <script>
    function mostrarMensaje() {
      document.getElementById('inicio').style.display = 'none';
      document.getElementById('mensaje').style.display = 'block';
    }
  </script>

</body>
</html>
