# A-cute-love-page-for-Ilham
A cute valentine webpage from yuu for Ilham 💖
index.html
<!DOCTYPE html>
<html lang="id">
<head>
<meta charset="UTF-8">
<title>Be My Valentine</title>

<style>
body {
  margin: 0;
  height: 100vh;
  background: linear-gradient(135deg, #ff9a9e, #fad0c4);
  display: flex;
  justify-content: center;
  align-items: center;
  font-family: 'Arial', sans-serif;
  overflow: hidden;
}

.container {
  text-align: center;
  background: white;
  padding: 40px;
  border-radius: 20px;
  box-shadow: 0 0 25px rgba(0,0,0,0.25);
  max-width: 400px;
}

h1 {
  color: #ff4d6d;
}

button {
  padding: 12px 25px;
  font-size: 18px;
  border: none;
  border-radius: 12px;
  cursor: pointer;
  margin: 10px;
}

#yes {
  background: #ff4d6d;
  color: white;
}

#no {
  background: #ccc;
  position: absolute;
}

/* hearts animation */
.heart {
  position: fixed;
  bottom: -10px;
  color: pink;
  font-size: 20px;
  animation: floatUp 5s linear infinite;
}

@keyframes floatUp {
  0% {
    transform: translateY(0);
    opacity: 1;
  }
  100% {
    transform: translateY(-100vh);
    opacity: 0;
  }
}
</style>
</head>

<body>

<!-- MUSIC -->
<audio autoplay loop>
  <source src="https://cdn.pixabay.com/download/audio/2022/10/03/audio_8f7a3f78cc.mp3?filename=perfect-piano-cover-121684.mp3" type="audio/mpeg">
</audio>

<div class="container" id="mainBox">
  <h1>ddy ❤️</h1>
  <h2>Mau jadi Valentine aku?</h2>
  <button id="yes">YA</button>
  <button id="no">TIDAK</button>
</div>

<script>
const noBtn = document.getElementById("no");
const yesBtn = document.getElementById("yes");

noBtn.addEventListener("mouseover", () => {
  const x = Math.random() * (window.innerWidth - 100);
  const y = Math.random() * (window.innerHeight - 50);
  noBtn.style.left = x + "px";
  noBtn.style.top = y + "px";
});

yesBtn.addEventListener("click", () => {
  document.body.innerHTML = `
  <div style="
    background: white;
    padding: 40px;
    border-radius: 20px;
    text-align: center;
    max-width: 500px;
    margin: auto;
    margin-top: 15vh;
    box-shadow: 0 0 25px rgba(0,0,0,0.3);
  ">
    <h1 style="color:#ff4d6d;">Yeay! 💖</h1>
    <p style="font-size:18px;">
      Hai suamiku tersayang ddy ❤️  
      <br><br>
      Makasih ya udah jadi rumah paling nyaman buat aku.  
      Makasih udah sabar sama aku yang kadang random, drama,  
      lapar, ngambek, tapi tetep kamu peluk 😆  
      <br><br>
      Aku jatuh cinta sama kamu…  
      setiap hari…  
      tanpa expired.  
      <br><br>
      Kamu itu favorit aku,  
      doa aku,  
      dan masa depan aku.  
      <br><br>
      Love you forever ♾️
    </p>
  </div>
  `;
});

// hearts generator
setInterval(() => {
  const heart = document.createElement("div");
  heart.className = "heart";
  heart.innerHTML = "💖";
  heart.style.left = Math.random() * 100 + "vw";
  heart.style.fontSize = Math.random() * 20 + 15 + "px";
  document.body.appendChild(heart);

  setTimeout(() => {
    heart.remove();
  }, 5000);
}, 300);
</script>

</body>
</html>
