<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <title>Para Dianelly ❤️</title>
  <style>
    body {
      margin: 0;
      padding: 0;
      background: #fff0f5;
      font-family: 'Arial', sans-serif;
      overflow: hidden;
      text-align: center;
    }

    .page {
      display: none;
      height: 100vh;
      padding: 40px 20px;
      box-sizing: border-box;
    }

    .page.active {
      display: block;
      animation: fade 0.8s ease;
    }

    h1 {
      color: #e60073;
    }

    .options button {
      display: block;
      margin: 15px auto;
      padding: 12px 20px;
      font-size: 18px;
      border: none;
      border-radius: 25px;
      background: #ff4d6d;
      color: white;
      cursor: pointer;
      width: 260px;
    }

    .options button:hover {
      background: #e60073;
    }

    @keyframes fade {
      from { opacity: 0; transform: translateY(20px); }
      to { opacity: 1; transform: translateY(0); }
    }

    /* Corazones */
    .heart {
      position: fixed;
      bottom: -20px;
      font-size: 22px;
      animation: float 6s linear infinite;
      z-index: 1;
    }

    @keyframes float {
      to {
        transform: translateY(-110vh);
        opacity: 0;
      }
    }

    /* Hello Kitty */
    .hello-kitty {
      position: fixed;
      bottom: 10px;
      right: 10px;
      width: 130px;
      z-index: 2;
      animation: kitty 3s ease-in-out infinite;
    }

    @keyframes kitty {
      0% { transform: translateY(0); }
      50% { transform: translateY(-8px); }
      100% { transform: translateY(0); }
    }

    p {
      font-size: 18px;
      color: #444;
      max-width: 500px;
      margin: auto;
    }
  </style>
</head>
<body>

<!-- PÁGINA 1 -->
<div class="page active">
  <h1>¿Dianelly Leturia quieres ser<br>Mi San Valentín? 💖</h1>
  <div class="options">
    <button onclick="sendWA('Segura ❤️')">Segura</button>
    <button onclick="sendWA('Muy segura 😍')">Muy segura</button>
    <button onclick="sendWA('Segurita ❤️')">Segurita ❤️</button>
  </div>
  <button onclick="nextPage()">➡️</button>
</div>

<!-- PÁGINA 2 -->
<div class="page">
  <h1>Muy segurita señorita Leturia<br>que quiere ser mi San Valentín? 🥺😍</h1>
  <div class="options">
    <button onclick="sendWA('Sí mi amor ❤️')">Sí</button>
    <button onclick="sendWA('Claro 😍')">Claro</button>
    <button onclick="sendWA('Acepto ❤️ ser tu San Valentín')">Acepto ❤️</button>
  </div>
  <button onclick="nextPage()">➡️</button>
</div>

<!-- PÁGINA 3 -->
<div class="page">
  <h1>¿Aceptas mi amor? 💍😍💘</h1>
  <div class="options">
    <button onclick="sendWA('Sí acepto ❤️💍')">Sí acepto ❤️</button>
  </div>
  <button onclick="nextPage()">➡️</button>
</div>

<!-- PÁGINA FINAL -->
<div class="page">
  <h1>💖 Mi Reina 💖</h1>
  <p>
    Eres la persona con la que quiero construir un futuro.<br>
    Cada día a tu lado me confirma que mi lugar es contigo ❤️<br><br>

    Si llegaste hasta aquí, es porque tal vez sí aceptaste,  
    y tu corazón ya sabía la respuesta…<br><br>

    Quiero que sepas que<br>
    <strong>te amooo muchísimo ❤️</strong><br><br>

    🐱💖 Hello Kitty 💖🐱
  </p>
</div>

<img src="hellokitty.png" class="hello-kitty" alt="Hello Kitty abrazándose">

<script>
  let current = 0;
  const pages = document.querySelectorAll('.page');

  function nextPage() {
    pages[current].classList.remove('active');
    current++;
    if (current < pages.length) {
      pages[current].classList.add('active');
    }
  }

  function sendWA(msg) {
    const text = encodeURIComponent(msg);
    window.open("https://wa.me/18093192007?text=" + text, "_blank");
  }

  function createHeart() {
    const heart = document.createElement('div');
    heart.className = 'heart';
    heart.innerHTML = '❤️';
    heart.style.left = Math.random() * 100 + 'vw';
    heart.style.animationDuration = (3 + Math.random() * 4) + 's';
    document.body.appendChild(heart);
    setTimeout(() => heart.remove(), 6000);
  }

  setInterval(createHeart, 250);
</script>

</body>
</html>
<img width="225" height="225" alt="hello kitty" src="https://github.com/user-attachments/assets/d651f6a6-da4c-45f4-af14-69bee9afcb1c" />
