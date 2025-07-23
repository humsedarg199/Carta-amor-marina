# Carta-amor-marinalet open = false;
function openLetter(){
  const flap = document.querySelector('.flap');
  const msg = document.getElementById('message');
  if(!open){
    flap.style.transform = 'rotateX(-180deg)';
    setTimeout(() => msg.style.opacity = 1, 600);
  } else {
    flap.style.transform = '';
    msg.style.opacity = 0;
  }
  open = !open;
}body { display:flex; height:100vh; align-items:center; justify-content:center; background:#fce4ec; }
.envelope { position:relative; width:300px; height:200px; cursor:pointer; }
.flap { position:absolute; width:100%; height:50%; background:#d32f2f; border-bottom:4px solid #b71c1c; transition: transform .6s; transform-origin:top; }
.card { position:absolute; top:50%; width:100%; height:50%; background:#fff; overflow:hidden;}
#message { opacity:0; padding:20px; text-align:center; transition: opacity 1s; }
#message h1 { color:#d32f2f; animation: float 3s ease-in-out infinite; }
@keyframes float { 0%,100%{transform:translateY(0)} 50%{transform:translateY(-10px)} }<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <title>Carta de Amor Animada</title>
  <link rel="stylesheet" href="styles.css">
</head>
<body>
  <div class="envelope" onclick="openLetter()">
    <div class="flap"></div>
    <div class="card">
      <div id="message">
        <h1>Mi amor…</h1>
        <p>Eres la razón de mi sonrisa cada día. Te amo con todo mi corazón.</p>
        <p>– Siempre tuyo/a</p>
      </div>
    </div>
  </div>
  <script src="script.js"></script>
</body>
</html>
