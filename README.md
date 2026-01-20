# Overlay-
overlay/ │ ├── index.html ├── style.css ├── car.png ├── xsuit.png
index html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>AATMA GAMING RGB Overlay</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>

  <!-- RGB CHANNEL NAME -->
  <div class="channel-name">
    <span>AATMA GAMING</span>
  </div>

  <!-- GAMEPLAY BOX -->
  <div class="gameplay"></div>

  <!-- X-SUIT -->
  <div class="xsuit-box">
    <img src="xsuit.png" class="xsuit">
  </div>

  <!-- CAR -->
  <div class="car-box">
    <img src="car.png" class="car">
  </div>

</body>
</html>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  width: 1920px;
  height: 1080px;
  background: transparent;
  overflow: hidden;
  font-family: Arial, sans-serif;
}

/* RGB CHANNEL NAME */
.channel-name {
  position: absolute;
  top: 10px;
  left: -500px;
  font-size: 52px;
  font-weight: 900;
  animation: moveText 10s linear infinite;
}

.channel-name span {
  background: linear-gradient(
    270deg,
    #ff0000,
    #ff00ff,
    #0000ff,
    #00ffff,
    #00ff00,
    #ffff00,
    #ff0000
  );
  background-size: 400% 400%;
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  animation: rgbGlow 2.5s linear infinite, blink 1.2s infinite alternate;
  text-shadow: 0 0 25px rgba(255,255,255,0.6);
}

/* GAMEPLAY BOX */
.gameplay {
  position: absolute;
  left: 30px;
  top: 90px;
  width: 1400px;
  height: 800px;
  background: rgba(0,0,0,0.88);
  border-radius: 18px;
  border: 4px solid rgba(120,0,255,0.9);
  box-shadow: 0 0 45px #00bfff;
}

/* X-SUIT */
.xsuit-box {
  position: absolute;
  right: 30px;
  top: 110px;
  width: 420px;
}

.xsuit {
  width: 100%;
  animation: gunRecoil 2s ease-in-out infinite;
  filter: drop-shadow(0 0 35px #7f00ff);
}

/* CAR */
.car-box {
  position: absolute;
  bottom: 10px;
  width: 100%;
  display: flex;
  justify-content: center;
}

.car {
  width: 600px;
  animation: carMove 8s linear infinite;
  filter: drop-shadow(0 0 40px #00bfff);
}

/* ANIMATIONS */
@keyframes carMove {
  0%   { transform: translateX(-140px); }
  50%  { transform: translateX(140px); }
  100% { transform: translateX(-140px); }
}

@keyframes gunRecoil {
  0%   { transform: translateX(0); }
  50%  { transform: translateX(10px); }
  100% { transform: translateX(0); }
}

@keyframes moveText {
  0%   { left: -500px; }
  100% { left: 1920px; }
}

@keyframes blink {
  0% { opacity: 1; }
  100% { opacity: 0.45; }
}

@keyframes rgbGlow {
  0% { background-position: 0% 50%; }
  100% { background-position: 100% 50%; }
}
