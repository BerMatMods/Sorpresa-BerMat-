<!DOCTYPE html><html lang="es">
<head>
  <meta charset="UTF-8">
  <title>Sorpresa para Briyidth</title>
  <link href="https://fonts.googleapis.com/css2?family=Great+Vibes&family=Playfair+Display:wght@700&family=Quicksand:wght@500&family=Sacramento&display=swap" rel="stylesheet">
  <style>
    body {
      margin: 0;
      background: linear-gradient(to top left, #f7e1ff, #f5c6ff);
      font-family: 'Quicksand', sans-serif;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      min-height: 100vh;
      overflow-x: hidden;
      color: #9e00b6;
    }.cuadro-principal {
  background: rgba(255, 240, 250, 0.9);
  border: 2px solid #d673ff;
  border-radius: 20px;
  padding: 30px;
  margin: 40px 20px;
  box-shadow: 0 0 25px #e68cff;
  max-width: 90%;
  text-align: center;
  transition: all 0.3s ease;
  animation: parpadeo-cuadro 2s infinite;
}

.titulo-sorpresa {
  font-size: 3rem;
  font-family: 'Playfair Display', serif;
  color: #a000a0;
  text-shadow: 0 0 12px #ffccff;
}

.boton-sorpresa {
  margin-top: 20px;
  font-size: 1.6rem;
  background: radial-gradient(circle, #a84dd1, #7700aa);
  color: white;
  padding: 15px 35px;
  border: none;
  border-radius: 40px;
  cursor: pointer;
  box-shadow: 0 0 18px #da9fff;
  font-family: 'Playfair Display', serif;
  transition: all 0.4s ease;
  animation: parpadeo 1.5s infinite;
}

@keyframes parpadeo {
  0%, 100% { box-shadow: 0 0 20px #cc66ff; }
  50% { box-shadow: 0 0 35px #9900cc; }
}

@keyframes parpadeo-cuadro {
  0%, 100% { box-shadow: 0 0 20px #e8aaff; }
  50% { box-shadow: 0 0 35px #b300d6; }
}

.mensaje {
  display: none;
  animation: aparecer 2s ease-in-out forwards;
}

@keyframes aparecer {
  from { opacity: 0; transform: translateY(50px); }
  to { opacity: 1; transform: translateY(0); }
}

.mensaje .contenido {
  background: #fff0ff;
  padding: 30px;
  border-radius: 25px;
  box-shadow: 0 0 30px #e0b3ff;
  max-width: 800px;
  margin: auto;
}

.mensaje h1 {
  font-family: 'Great Vibes', cursive;
  font-size: 3.5rem;
  margin-bottom: 20px;
  color: #a000d0;
}

.mensaje p {
  font-size: 1.4rem;
  margin: 10px 0;
  line-height: 1.7;
  font-family: 'Sacramento', cursive;
  color: #8800aa;
}

.flor {
  width: 100px;
  height: 100px;
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
  color: #d633ff;
}

@keyframes latido {
  0%, 100% { transform: scale(1); }
  50% { transform: scale(1.2); }
}

.tarjeta-info {
  background-color: #f5dbff;
  border: 1px solid #e599f7;
  border-radius: 12px;
  padding: 15px 20px;
  margin-top: 30px;
  box-shadow: 0 0 10px #e5aaff;
  max-width: 280px;
  font-size: 0.85rem;
  color: #7d0099;
  text-align: left;
  margin: auto;
}

  </style>
</head>
<body>
  <div class="cuadro-principal" id="inicio">
    <div class="titulo-sorpresa">TE TENGO UNA SORPRESA MI AMOR</div>
    <button class="boton-sorpresa" onclick="mostrarMensaje()">Haz clic aquí mi amor</button>
  </div>  <div class="mensaje" id="mensaje">
    <div class="contenido">
      <img src="https://i.pinimg.com/originals/e9/b3/8f/e9b38f9996ffb31b8cc28ed2cb0c9ed7.png" alt="Flor" class="flor" />
      <h1>Para Mi Reina BriyidthCha</h1>
      <p>Desde que llegaste a mi vida, todo tiene más color, más sentido y más amor.</p>
      <p>Gracias por ser mi sol, mi paz, mi todo. Eres lo mejor que tengo, y te elijo una y otra vez.</p>
      <p>¡Te amo con toda mi alma, mi reina hermosa!</p>
      <div class="corazones">💜💖💫🌸🌷🌹💘✨💞</div>
      <p style="font-family: 'Great Vibes', cursive; font-size: 2rem; margin-top: 20px; color: #91009b;">Tuyo por siempre: Anth'Zz Berrocal</p>
      <div class="tarjeta-info">
        <strong>Información del creador:</strong>
        <p><strong>Alias:</strong> BerMatModZ</p>
        <p><strong>Nombre:</strong> Anth'Zz Berrocal</p>
        <p><strong>Especialidad:</strong> Bots, IA, Ciberseguridad</p>
        <p><strong>Ubicación:</strong> Andahuaylas, Perú</p>
      </div>
    </div>
  </div>  <script>
    function mostrarMensaje() {
      document.getElementById('inicio').style.display = 'none';
      document.getElementById('mensaje').style.display = 'block';
    }
  </script></body>
</html>
