<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>💍 Aniversario con Briyidth 💖</title>
  <link href="https://fonts.googleapis.com/css2?family=Dancing+Script&family=Pacifico&family=Great+Vibes&family=Raleway:wght@400;700&display=swap" rel="stylesheet">
  <style>
    * {
      box-sizing: border-box;
    }
    body {
      margin: 0;
      padding: 0;
      background: linear-gradient(135deg, #fce4ec, #f8bbd0);
      font-family: 'Raleway', sans-serif;
    }

    #pantallaClave {
      position: fixed;
      top: 0; left: 0;
      width: 100%; height: 100%;
      background: linear-gradient(135deg, #fce4ec, #f8bbd0);
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      z-index: 9999;
      padding: 20px;
    }

    #pantallaClave h2 {
      font-size: 30px;
      color: #ad1457;
      font-family: 'Pacifico', cursive;
      margin-bottom: 15px;
      text-shadow: 0 0 5px #ec407a;
    }

    #claveInput {
      font-size: 24px;
      padding: 15px;
      border: 3px solid #ec407a;
      border-radius: 15px;
      text-align: center;
      width: 220px;
      margin-bottom: 15px;
      letter-spacing: 4px;
      color: #880e4f;
      background: #fff0f7;
    }

    #claveInput::placeholder {
      color: #d81b60;
      opacity: 0.5;
    }

    #teclado {
      display: grid;
      grid-template-columns: repeat(3, 70px);
      gap: 15px;
      margin-bottom: 20px;
    }

    .tecla {
      font-size: 24px;
      padding: 15px;
      background: #f8bbd0;
      border: 2px solid #ec407a;
      border-radius: 15px;
      color: #880e4f;
      cursor: pointer;
      box-shadow: 0 0 10px #f48fb1;
      user-select: none;
    }

    .tecla:active {
      transform: scale(0.95);
      background: #f48fb1;
    }

    #accederBtn {
      padding: 12px 30px;
      font-size: 22px;
      background: linear-gradient(45deg, #f06292, #ec407a);
      color: white;
      border: none;
      border-radius: 30px;
      font-family: 'Pacifico', cursive;
      box-shadow: 0 0 20px #ec407a;
      cursor: pointer;
      margin-bottom: 15px;
    }

    .cuadro-stitch {
      border: 5px solid #ec407a;
      padding: 20px;
      border-radius: 25px;
      background: #fff0f7;
      box-shadow: 0 0 30px #f48fb1;
      margin-top: 15px;
    }

    .cuadro-stitch img {
      width: 250px;
      border-radius: 20px;
      box-shadow: 0 0 15px #f8bbd0;
    }

    .info-autor {
      margin-top: 20px;
      font-size: 18px;
      font-weight: bold;
      color: #ad1457;
      text-align: center;
      font-family: 'Dancing Script', cursive;
      text-shadow: 0 0 5px #f48fb1;
    }

    #contenidoPrincipal {
      display: none;
      padding: 20px;
    }

    .container {
      text-align: center;
      margin-top: 60px;
      padding: 30px;
      border-radius: 25px;
      background: rgba(255, 255, 255, 0.95);
      box-shadow: 0 0 40px rgba(219, 112, 147, 0.7);
      max-width: 700px;
      margin: auto;
    }

    .titulo {
      font-family: 'Dancing Script', cursive;
      font-size: 50px;
      color: #ad1457;
      text-shadow: 0 0 15px #f48fb1, 0 0 10px #ec407a;
      animation: parpadeo 2s infinite;
    }

    @keyframes parpadeo {
      0%, 100% { opacity: 1; }
      50% { opacity: 0.6; }
    }

    .contador {
      font-size: 20px;
      color: #880e4f;
      font-weight: 700;
      margin-top: 20px;
    }

    .btn {
      margin-top: 30px;
      padding: 20px 40px;
      font-size: 24px;
      background: linear-gradient(45deg, #f06292, #ec407a);
      border: 3px solid #ad1457;
      color: white;
      border-radius: 35px;
      cursor: pointer;
      box-shadow: 0 0 25px #f48fb1;
      font-family: 'Pacifico', cursive;
      transition: transform 0.3s ease;
      user-select: none;
    }

    .btn:hover {
      transform: scale(1.05);
      box-shadow: 0 0 40px #f50057;
    }

    .mensaje {
      display: none;
      margin-top: 30px;
      font-size: 26px;
      font-family: 'Great Vibes', cursive;
      color: #ad1457;
      background: #fff0f7;
      padding: 25px;
      border-radius: 20px;
      box-shadow: 0 0 20px #f48fb1;
      animation: aparecer 1.5s ease-out forwards;
    }

    .imagen-extra img {
      margin-top: 25px;
      width: 90%;
      border-radius: 25px;
      box-shadow: 0 0 35px #f48fb1;
      border: 5px solid #ec407a;
    }

    @keyframes aparecer {
      0% { opacity: 0; transform: translateY(20px); }
      100% { opacity: 1; transform: translateY(0); }
    }

  </style>
</head>
<body>
  <!-- Pantalla de seguridad -->
  <div id="pantallaClave">
    <h2>🔒 Ingresa el código secreto</h2>
    <input type="text" id="claveInput" placeholder="10/11/23" maxlength="8" readonly>
    <div id="teclado"></div>
    <button id="accederBtn">Acceder</button>

    <div class="cuadro-stitch">
      <img src="https://media0.giphy.com/media/v1.Y2lkPTZjMDliOTUyZjViN2d1M2FyaG14dmsxMzZ2dDVmcDlyNzA4aWhsaGE3Mmt6dG9rayZlcD12MV9naWZzX3NlYXJjaCZjdD1n/11ZSwQNWba4YF2/giphy.gif" alt="Stitch lindo">
    </div>

    <div class="info-autor">
      ❤️ By: AnthZz Berrocal <br> 👑 Líder de BERMATMODS 👽
    </div>
  </div>

  <!-- Contenido principal -->
  <div id="contenidoPrincipal">
    <div class="container">
      <div class="titulo">💖 Feliz Aniversario Mi Amor 💖</div>
      <div class="contador" id="contador">Calculando el tiempo... ⏳</div>
      <button class="btn" id="btnSorpresa">TOCA AQUÍ MI REINA</button>
      <div class="mensaje" id="mensaje">
        🎉 ¡Feliz 1 año y 8 meses, mi reina Briyidth! 🎉<br>
        Hoy Cumplimos un mes más de amor puro 💕<br>
        Gracias por regalarme tu tiempo y tu ternura.<br>
        Siempre contigo hasta el fin del mundo 🌍💘
      </div>
      <div class="imagen-extra" id="imagenExtra">
        <img src="https://i.postimg.cc/pXWvCFsC/IMG-20240924-WA0182.jpg" alt="Foto especial">
      </div>
    </div>
  </div>

  <script>
    const input = document.getElementById('claveInput');
    const teclado = document.getElementById('teclado');
    const accederBtn = document.getElementById('accederBtn');
    const claveCorrecta = '10/11/23';

    const numeros = ['1','2','3','4','5','6','7','8','9','0','/','B'];
    numeros.forEach(n => {
      const tecla = document.createElement('div');
      tecla.className = 'tecla';
      tecla.textContent = n;
      tecla.onclick = () => {
        if(n === 'B') {
          input.value = input.value.slice(0, -1);
        } else if(input.value.length < 8) {
          input.value += n;
        }
      };
      teclado.appendChild(tecla);
    });

    accederBtn.addEventListener('click', () => {
      if(input.value === claveCorrecta) {
        document.getElementById('pantallaClave').style.display = 'none';
        document.getElementById('contenidoPrincipal').style.display = 'block';
      } else {
        alert('❌ Código incorrecto, mi amor');
      }
    });

    // Contador aniversario
    const inicio = new Date("2023-11-10T00:00:00");
    const contador = document.getElementById("contador");

    function actualizarContador() {
      const ahora = new Date();
      let anos = ahora.getFullYear() - inicio.getFullYear();
      let meses = ahora.getMonth() - inicio.getMonth();
      let dias = ahora.getDate() - inicio.getDate();
      let horas = ahora.getHours() - inicio.getHours();
      let minutos = ahora.getMinutes() - inicio.getMinutes();
      let segundos = ahora.getSeconds() - inicio.getSeconds();

      if (segundos < 0) { segundos += 60; minutos--; }
      if (minutos < 0) { minutos += 60; horas--; }
      if (horas < 0) { horas += 24; dias--; }
      if (dias < 0) {
        meses--;
        const mesAnterior = new Date(ahora.getFullYear(), ahora.getMonth(), 0);
        dias += mesAnterior.getDate();
      }
      if (meses < 0) { meses += 12; anos--; }

      contador.innerHTML = `💞 YA VAMOS: ${anos} AÑOS, ${meses} MESES, ${dias} DÍAS, ${horas}h ${minutos}m ${segundos}s 💞`;
    }
    setInterval(actualizarContador, 1000);

    document.getElementById("btnSorpresa").addEventListener("click", () => {
      document.getElementById("mensaje").style.display = "block";
      document.getElementById("imagenExtra").style.display = "block";
    });
  </script>
</body>
</html>
