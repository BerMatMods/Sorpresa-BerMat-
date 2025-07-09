<!DOCTYPE html><html lang="es">
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
      overflow-x: hidden;
    }.container {
  text-align: center;
  padding: 30px;
}

.titulo {
  font-family: 'Dancing Script', cursive;
  font-size: 48px;
  color: #ad1457;
  text-shadow: 0 0 10px #f48fb1;
}

.contador {
  margin-top: 10px;
  font-size: 20px;
  color: #880e4f;
}

.btn {
  margin: 30px auto;
  padding: 20px 40px;
  font-size: 24px;
  background: linear-gradient(45deg, #f06292, #ec407a);
  border: none;
  color: white;
  border-radius: 30px;
  cursor: pointer;
  font-family: 'Pacifico', cursive;
  box-shadow: 0 0 15px #f48fb1;
}

.mensaje, .galeria-container {
  display: none;
  animation: fadeIn 1.5s forwards;
}

@keyframes fadeIn {
  from { opacity: 0; transform: translateY(30px); }
  to { opacity: 1; transform: translateY(0); }
}

.mensaje {
  background: #fce4ec;
  padding: 20px;
  border-radius: 20px;
  box-shadow: 0 0 20px #f8bbd0;
  font-size: 24px;
  margin-top: 20px;
  font-family: 'Great Vibes', cursive;
  color: #ad1457;
}

.imagen-extra img {
  margin-top: 20px;
  max-width: 90%;
  border-radius: 20px;
  box-shadow: 0 0 20px #f48fb1;
}

.galeria-container {
  position: relative;
  background: #fff0f6;
  padding: 30px 15px;
  border-radius: 20px;
  margin: 40px auto;
  box-shadow: 0 0 25px #f8bbd0;
}

.galeria-fotos {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  gap: 20px;
}

.galeria-fotos img {
  width: 180px;
  height: 180px;
  object-fit: cover;
  border-radius: 15px;
  box-shadow: 0 0 15px #ec407a;
}

.corazon {
  position: fixed;
  top: -50px;
  width: 30px;
  height: 30px;
  background: url('https://i.postimg.cc/9f2tCtFg/corazon.png') no-repeat center/contain;
  animation: lluvia 5s linear infinite;
  z-index: 9999;
  opacity: 0.8;
}

@keyframes lluvia {
  0% { transform: translateY(0); }
  100% { transform: translateY(120vh); }
}

.footer {
  text-align: center;
  font-family: 'Raleway', sans-serif;
  color: #6a1b9a;
  padding: 20px;
  margin-top: 40px;
  font-style: italic;
}

  </style>
</head>
<body>
  <div class="container">
    <div class="titulo">💖 Feliz Aniversario Mi Amor 💖</div>
    <div class="contador" id="contador"></div><button class="btn" onclick="mostrarMensaje()">TOCA AQUÍ MI REINA</button>

<div class="mensaje" id="mensaje">
  ¡Feliz 1 año y 8 meses, mi reina Briyidth! Gracias por cada momento. 💘
  <div class="imagen-extra">
    <img src="https://i.postimg.cc/pXWvCFsC/IMG-20240924-WA0182.jpg" alt="Foto juntos">
  </div>
</div>

<button class="btn" onclick="mostrarGaleria()">Ver nuestra galería 📸</button>

<div class="galeria-container" id="galeria">
  <div class="galeria-fotos">
    <img src="https://i.postimg.cc/HkxS5Yjs/1742316301125-2.jpg" alt="Foto 1">
    <img src="https://i.postimg.cc/8PkwQpRB/Screenshot-20250427-213138.jpg" alt="Foto 2">
    <img src="https://i.postimg.cc/VNsb5vND/received-1162848851410899.jpg" alt="Foto 3">
    <img src="https://i.postimg.cc/RVRShRnx/PSX-20250530-060357.jpg" alt="Foto 4">
    <img src="https://i.postimg.cc/59KpJcnh/IMG-20241228-231305-817-3.jpg" alt="Foto 5">
  </div>
</div>

<div class="footer">
  Creado con amor por <strong>Anth'Zz Berrocal</strong> 💻<br>
  Proyecto <strong>BerMatModZ</strong> ❤️<br>
  Andahuaylas | Software & IA personalizada
</div>

  </div>  <script>
    const inicio = new Date("2023-11-10T00:00:00");
    function actualizarContador() {
      const ahora = new Date();
      let diff = ahora - inicio;
      let segundos = Math.floor(diff / 1000) % 60;
      let minutos = Math.floor(diff / (1000 * 60)) % 60;
      let horas = Math.floor(diff / (1000 * 60 * 60)) % 24;
      let dias = Math.floor(diff / (1000 * 60 * 60 * 24));
      let meses = Math.floor(dias / 30);
      dias = dias % 30;
      document.getElementById("contador").innerHTML = `💞 Llevamos juntos: ${meses} meses, ${dias} días, ${horas}h ${minutos}m ${segundos}s 💞`;
    }
    setInterval(actualizarContador, 1000);

    function mostrarMensaje() {
      document.getElementById("mensaje").style.display = "block";
    }

    function mostrarGaleria() {
      document.getElementById("galeria").style.display = "block";
      for (let i = 0; i < 20; i++) {
        let corazon = document.createElement("div");
        corazon.className = "corazon";
        corazon.style.left = Math.random() * 100 + "vw";
        corazon.style.animationDuration = (Math.random() * 3 + 3) + "s";
        document.body.appendChild(corazon);
        setTimeout(() => corazon.remove(), 5000);
      }
    }
  </script></body>
</html>
