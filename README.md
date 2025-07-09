
<html lang="es">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>💍 Aniversario con Briyidth 💖</title>
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
    .btn:disabled {
      background: #f8bbd0;
      border-color: #f48fb1;
      color: #880e4f;
      cursor: not-allowed;
      box-shadow: none;
      transform: none;
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

    @keyframes aparecer {
      0% {
        opacity: 0;
        transform: translateY(25px);
      }
      100% {
        opacity: 1;
        transform: translateY(0);
      }
    }

    .mensaje p {
      margin: 15px 0 0;
      font-size: 28px;
      line-height: 1.4;
      font-weight: 700;
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

    /* Flores grandes en cuadritos decorativos */
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

    /* Botón para galería */
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

    /* Galería fotos */
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

    #galeria .cuadro-foto:hover {
      transform: scale(1.1);
      box-shadow: 0 0 25px #9c27b0;
    }

    #galeria img {
      width: 100%;
      height: 100%;
      object-fit: cover;
      user-select: none;
    }

    /* Video */
    #galeria video {
      width: 100%;
      border-radius: 15px;
      box-shadow: 0 0 20px #ab47bc;
      margin-top: 20px;
    }
  </style>
</head>
<body>
  <div class="container">
    <div class="titulo">💖 Feliz Aniversario Mi Amor 💖</div>
    <div class="contador" id="contador">Calculando el tiempo... ⏳</div>

    <button class="btn" id="btnSorpresa">TOCA AQUÍ MI REINA</button>

    <div id="mensaje" class="mensaje">
      <p>🎉 ¡Feliz 1 año y 8 meses, mi reina Briyidth! 🎉</p>
      <p>Hoy Cumplimos un mes mi amor , y vamos por mas .</p>
      <p>Gracias por regalarme tu vida, tu risa y tu ternura.</p>
      <p>Siempre contigo, hasta el fin del mundo. 💘</p>
    </div>

    <div class="imagen-extra" id="imagenExtra">
      <img src="https://i.postimg.cc/pXWvCFsC/IMG-20240924-WA0182.jpg" alt="Foto de nosotros" />
    </div>

    <button id="btnGaleria">Ver nuestra galería 📸</button>

    <div id="galeria">
      <div class="cuadro-foto">
        <img src="https://i.postimg.cc/HkxS5Yjs/1742316301125-2.jpg" alt="Foto 1" />
      </div>
      <div class="cuadro-foto">
        <img src="https://i.postimg.cc/8PkwQpRB/Screenshot-20250427-213138.jpg" alt="Foto 2" />
      </div>
      <div class="cuadro-foto">
        <img src="https://i.postimg.cc/VNsb5vND/received-1162848851410899.jpg" alt="Foto 3" />
      </div>
      <div class="cuadro-foto">
        <img src="https://i.postimg.cc/RVRShRnx/PSX-20250530-060357.jpg" alt="Foto 4" />
      </div>
      <div class="cuadro-foto">
        <img src="https://i.postimg.cc/59KpJcnh/IMG-20241228-231305-817-3.jpg" alt="Foto 5" />
      </div>

    
    </div>
  </div>

  <div class="footer">
    𝐁𝐲: 𝐀𝐧𝐭𝐡𝐙𝐳 𝐁𝐞𝐫𝐫𝐨𝐜𝐚𝐥 | 𝑳𝒊𝒅𝒆𝒓 👽BERMATMODS👽 
  </div>

  <div class="muñequitos">
    <div class="cuadro">
      <img src="https://i.postimg.cc/6qf6xLNc/pngtree-rose-red-roses-flower-png-image-15133984.png" alt="Flor 1" />
    </div>
    <div class="cuadro">
      <img src="https://i.postimg.cc/nL9HhtJC/40a978855678347ec791ff76c9cad6e0.jpg" alt="Flor 2" />
    </div>
    <div class="cuadro">
      <img src="https://i.postimg.cc/6qf6xLNc/pngtree-rose-red-roses-flower-png-image-15133984.png" alt="Flor 3" />
    </div>
  </div>

  <script>
    const inicio = new Date("2023-11-10T00:00:00");
    const contador = document.getElementById("contador");
    const btnSorpresa = document.getElementById("btnSorpresa");
    const mensaje = document.getElementById("mensaje");
    const imagenExtra = document.getElementById("imagenExtra");
    const btnGaleria = document.getElementById("btnGaleria");
    const galeria = document.getElementById("galeria");

    function actualizarContador() {
      const ahora = new Date();

      let años = ahora.getFullYear() - inicio.getFullYear();
      let meses = ahora.getMonth() - inicio.getMonth();
      let dias = ahora.getDate() - inicio.getDate();
      let horas = ahora.getHours() - inicio.getHours();
      let minutos = ahora.getMinutes() - inicio.getMinutes();
      let segundos = ahora.getSeconds() - inicio.getSeconds();

      if (segundos < 0) {
        segundos += 60;
        minutos--;
      }
      if (minutos < 0) {
        minutos += 60;
        horas--;
      }
      if (horas < 0) {
        horas += 24;
        dias--;
      }
      if (dias < 0) {
        meses--;
        const mesAnterior = new Date(ahora.getFullYear(), ahora.getMonth(), 0);
        dias += mesAnterior.getDate();
      }
      if (meses < 0) {
        meses += 12;
        años--;
      }

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
