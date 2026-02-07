<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<title>Mi carta de amor ❤️</title>
<style>
body {
  margin: 0;
  font-family: 'Arial', sans-serif;
  background: linear-gradient(180deg, #ffb6c1, #ff69b4);
  overflow: hidden;
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
  color: white;
  text-align: center;
}

.card {
  background: rgba(255, 255, 255, 0.15);
  padding: 30px;
  border-radius: 20px;
  max-width: 500px;
  animation: fade 1s ease;
}

h1 {
  font-size: 26px;
}

button {
  margin: 10px;
  padding: 12px 22px;
  border: none;
  border-radius: 25px;
  font-size: 16px;
  cursor: pointer;
  background: #ff1744;
  color: white;
  transition: transform 0.2s;
}

button:hover {
  transform: scale(1.1);
}

@keyframes fade {
  from { opacity: 0; transform: scale(0.9); }
  to { opacity: 1; transform: scale(1); }
}

/* corazones */
.heart {
  position: fixed;
  bottom: -20px;
  font-size: 24px;
  animation: float 6s linear infinite;
  color: red;
}

@keyframes float {
  from { transform: translateY(0); opacity: 1; }
  to { transform: translateY(-110vh); opacity: 0; }
}
</style>
</head>

<body>

<div class="card" id="content"></div>

<script>
let step = 0;
const content = document.getElementById("content");

const steps = [
  `
  <h1>¿Dianelly Leturia quieres ser<br>mi San Valentín? ❤️</h1>
  <button onclick="next()">Segura</button>
  <button onclick="next()">Muy segura</button>
  <button onclick="next()">Segurita ❤️</button>
  `,
  `
  <h1>¿Muy segurita señorita Leturia<br>que quiere ser mi San Valentín? 🥺😍</h1>
  <button onclick="next()">Sí</button>
  <button onclick="next()">Claro</button>
  <button onclick="next()">Acepto ❤️</button>
  `,
  `
  <h1>¿Aceptas mi amor? 💍😍💘</h1>
  <button onclick="next()">Sí, acepto ❤️</button>
  `,
  `
  <h1>Eres la persona con la que quiero construir un futuro ❤️</h1>
  <p>Cada día a tu lado me confirma que mi lugar es contigo.</p>
  <p><br>Si llegaste hasta aquí, es porque tu corazón ya sabía la respuesta…</p>
  <p>Quiero que sepas que<br><strong>te amooo muchísimo ❤️</strong></p>
  `
];

function next() {
  step++;
  content.innerHTML = steps[step];
}

content.innerHTML = steps[0];

// corazones infinitos
setInterval(() => {
  const heart = document.createElement("div");
  heart.className = "heart";
  heart.innerHTML = "❤️";
  heart.style.left = Math.random() * 100 + "vw";
  heart.style.animationDuration = (Math.random() * 3 + 4) + "s";
  document.body.appendChild(heart);
  setTimeout(() => heart.remove(), 6000);
}, 300);
</script>

</body>
</html>

