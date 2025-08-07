<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>BerMa_Mods</title>
  <link href="https://fonts.googleapis.com/css2?family=Dancing+Script&family=Pacifico&family=Great+Vibes&family=Raleway:wght@400;700&display=swap" rel="stylesheet">
  <style>
    body {
      margin: 0;
      padding: 0;
      background: linear-gradient(135deg, #fce4ec, #f8bbd0);
      font-family: 'Raleway', sans-serif;
      display: flex;
      flex-direction: column;
      align-items: center;
      position: relative;
      min-height: 100vh;
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
      text-align: center;
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
      padding: 10px 25px;
      font-size: 22px;
      background: linear-gradient(45deg, #f06292, #ec407a);
      color: white;
      border: none;
      border-radius: 30px;
      font-family: 'Pacifico', cursive;
      box-shadow: 0 0 20px #ec407a;
      cursor: pointer;
    }

    #stitch {
      border: 5px dashed #f06292;
      border-radius: 25px;
      padding: 15px;
      background: #fff0f6;
      box-shadow: 0 0 20px #f8bbd0;
      margin-top: 20px;
      display: inline-block;
    }

    #stitch img {
      width: 220px;
      border-radius: 20px;
      box-shadow: 0 0 15px #ec407a;
    }

    #infoSeguridad {
      margin-top: 25px;
      color: #ad1457;
      font-family: 'Pacifico', cursive;
      font-size: 20px;
      text-shadow: 0 0 5px #ec407a;
    }

    #contenidoPrincipal {
      display: none;
    }

    /* Resto de tu contenido principal como estaba */

    .container {
      text-align: center;
      margin-top: 60px;
      padding: 30px;
      border-radius: 25px;
      background: rgba(255, 255, 255, 0.95);
      box-shadow: 0 0 40px rgba(219, 112, 147, 0.7);
      width: 90%;
      max-width: 700px;
      z-index: 2;
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
      margin: 30px auto 0;
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
      display: inline-block;
    }

    .btn:hover {
      transform: scale(1.05);
      box-shadow: 0 0 40px #f50057;
    }

    .mensaje {
      margin-top: 30px;
      padding: 30px 25px;
      background-color: #fce4ec;
      border-radius: 20px;
      font-size: 24px;
      color: #ad1457;
      box-shadow: 0 0 30px #f48fb1;
      font-family: 'Great Vibes', cursive;
      text-shadow: 0 0 5px #ec407a;
      display: none;
      animation: aparecer 1.8s ease-out forwards;
    }

    .imagen-extra {
      margin-top: 25px;
      display: none;
      animation: aparecer 1.8s ease-out forwards;
    }

    .imagen-extra img {
      max-width: 90%;
      border-radius: 25px;
      box-shadow: 0 0 35px #f48fb1;
      border: 5px solid #ec407a;
      user-select: none;
    }

    @keyframes aparecer {
      0% { opacity: 0; transform: translateY(25px); }
      100% { opacity: 1; transform: translateY(0); }
    }

    .muñequitos {
      position: fixed;
      bottom: 0;
      left: 0;
      width: 100%;
      text-align: center;
      padding: 15px 0;
      background: rgba(255, 228, 241, 0.7);
      font-size: 40px;
      animation: rebote 2.5s infinite ease-in-out;
      z-index: 1;
    }

    @keyframes rebote {
      0%, 100% { transform: translateY(0); }
      50% { transform: translateY(-15px); }
    }

    .muñequitos .cuadro {
      display: inline-block;
      background: #fff0f6;
      border: 3px solid #f48fb1;
      border-radius: 20px;
      padding: 15px;
      margin: 0 15px;
      box-shadow: 0 0 15px #f8bbd0;
    }

    .muñequitos img {
      width: 85px;
      height: 85px;
      animation: muñequito-bailando 2.5s infinite;
      user-select: none;
    }

    @keyframes muñequito-bailando {
      0% { transform: translateY(0); }
      50% { transform: translateY(-15px); }
      100% { transform: translateY(0); }
    }

    #btnGaleria {
      margin-top: 20px;
      background: linear-gradient(45deg, #ba68c8, #ab47bc);
      border: 3px solid #8e24aa;
      color: white;
      border-radius: 30px;
      padding: 15px 30px;
      font-size: 20px;
      font-family: 'Pacifico', cursive;
      cursor: pointer;
      box-shadow: 0 0 20px #ce93d8;
      transition: transform 0.3s ease;
    }

    #btnGaleria:hover {
      transform: scale(1.05);
      box-shadow: 0 0 30px #9c27b0;
    }

    #galeria {
      display: none;
      margin-top: 25px;
      max-width: 700px;
      text-align: center;
    }

    #galeria .cuadro-foto {
      display: inline-block;
      margin: 10px;
      border: 3px solid #ce93d8;
      border-radius: 15px;
      overflow: hidden;
      box-shadow: 0 0 15px #ba68c8;
      background: white;
      transition: transform 0.3s ease;
      cursor: pointer;
      width: 150px;
      height: 150px;
    }

    #galeria img {
      width: 100%;
      height: 100%;
      object-fit: cover;
    }
  </style>
</head>
<body>
  <!-- Pantalla de acceso -->
  <div id="pantallaClave">
    <h2>🔒 Código para acceder</h2>
    <input type="text" id="claveInput" placeholder="10/11/23" maxlength="8" readonly>
    <div id="teclado"></div>
    <button id="accederBtn">Acceder</button>

    <div id="stitch">
      <img src="https://media0.giphy.com/media/v1.Y2lkPTZjMDliOTUydXRucTZibGt3cDRhdTA1NXQzOG04ejZ6NGVtbXNzMjAxemp3ZnZjOSZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9cw/huXuyCODzzCQLy3T05/giphy.gif" alt="Stitch Amoroso">
    </div>

    <div id="infoSeguridad">
      By: <b>Anth'Zz Berrocal</b><br>👽 Líder de <strong>BERMATMODS</strong> 👽
    </div>
  </div>

  <!-- Contenido principal -->
  <div id="contenidoPrincipal">
    <div class="container">
      <div class="titulo">💖 Feliz Aniversario Mi Amor 💖</div>
      <div class="contador" id="contador">Calculando el tiempo... ⏳</div>

      <button class="btn" id="btnSorpresa">TOCA AQUÍ MI REINA</button>

      <div id="mensaje" class="mensaje">
        <p>🎉 ¡Feliz 1 año y 8 meses, mi reina Briyidth! 🎉</p>
        <p>Hoy Cumplimos un mes mi amor, y vamos por más.</p>
        <p>Gracias por regalarme tu vida, tu risa y tu ternura.</p>
        <p>Siempre contigo, hasta el fin del mundo. 💘</p>
      </div>

      <div class="imagen-extra" id="imagenExtra">
        <img src="https://i.postimg.cc/pXWvCFsC/IMG-20240924-WA0182.jpg" alt="Foto de nosotros" />
      </div>

      <button id="btnGaleria">Ver nuestra galería 📸</button>

      <div id="galeria">
        <div class="cuadro-foto"><img src="https://i.postimg.cc/HkxS5Yjs/1742316301125-2.jpg" /></div>
        <div class="cuadro-foto"><img src="https://i.postimg.cc/8PkwQpRB/Screenshot-20250427-213138.jpg" /></div>
        <div class="cuadro-foto"><img src="https://i.postimg.cc/VNsb5vND/received-1162848851410899.jpg" /></div>
        <div class="cuadro-foto"><img src="https://i.postimg.cc/RVRShRnx/PSX-20250530-060357.jpg" /></div>
        <div class="cuadro-foto"><img src="https://i.postimg.cc/59KpJcnh/IMG-20241228-231305-817-3.jpg" /></div>
      </div>
    </div>

    <div class="muñequitos">
      <div class="cuadro"><img src="https://media0.giphy.com/media/yN5xPFm8klwMddZVKi/giphy.gif" /></div>
      <div class="cuadro"><img src="https://media2.giphy.com/media/5dkb3UXNiRU5qwNrzL/giphy.gif" /></div>
      <div class="cuadro"><img src="https://media0.giphy.com/media/yN5xPFm8klwMddZVKi/giphy.gif" /></div>
    </div>
  </div>

  <script>
    const input = document.getElementById('claveInput');
    const teclado = document.getElementById('teclado');
    const accederBtn = document.getElementById('accederBtn');
    const claveCorrecta = '10/11/23';

    const numeros = ['1','2','3','4','5','6','7','8','9','0','B','/'];
    numeros.forEach(n => {
      const tecla = document.createElement('div');
      tecla.className = 'tecla';
      tecla.textContent = n;
      tecla.onclick = () => {
        if(n === 'B') input.value = input.value.slice(0, -1);
        else if(input.value.length < 8) input.value += n;
      };
      teclado.appendChild(tecla);
    });

    accederBtn.addEventListener('click', () => {
      if(input.value === claveCorrecta) {
        document.getElementById('pantallaClave').style.display = 'none';
        document.getElementById('contenidoPrincipal').style.display = 'block';
      } else {
        alert('Código incorrecto ❌');
      }
    });

    const inicio = new Date("2023-11-10T00:00:00");
    const contador = document.getElementById("contador");
    const btnSorpresa = document.getElementById("btnSorpresa");
    const mensaje = document.getElementById("mensaje");
    const imagenExtra = document.getElementById("imagenExtra");
    const btnGaleria = document.getElementById("btnGaleria");
    const galeria = document.getElementById("galeria");

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

      contador.innerHTML = `💞 𝐘𝐀 𝐕𝐀𝐌𝐎𝐒: ${anos} AÑOS, ${meses} MESES, ${dias} DÍAS, ${horas}h ${minutos}m ${segundos}s 💞`;
    }

    setInterval(actualizarContador, 1000);

    btnSorpresa.addEventListener("click", () => {
      mensaje.style.display = "block";
      imagenExtra.style.display = "block";
      btnSorpresa.disabled = true;
      btnSorpresa.style.cursor = "not-allowed";
    });

    btnGaleria.addEventListener("click", () => {
      if (galeria.style.display === "none" || galeria.style.display === "") {
        galeria.style.display = "block";
        btnGaleria.textContent = "Ocultar galería 📸";
      } else {
        galeria.style.display = "none";
        btnGaleria.textContent = "Ver nuestra galería 📸";
      }
    });
  </script>
</body>
</html>
