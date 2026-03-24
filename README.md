<html>
<head>
  <title>Happy Birthday Sister Samra 🎉</title>
  <link href="https://fonts.googleapis.com/css2?family=Great+Vibes&display=swap" rel="stylesheet">
  <style>
    body {
      margin: 0;
      padding: 0;
      font-family: 'Great Vibes', cursive;
      overflow: hidden;
      text-align: center;
      background: #000;
      color: #fff;
    }

    #intro {
      position: absolute;
      top: 50%;
      left: 50%;
      transform: translate(-50%, -50%);
    }

    #intro button {
      padding: 20px 40px;
      font-size: 30px;
      font-weight: bold;
      background: #ff69b4;
      color: white;
      border: none;
      border-radius: 15px;
      cursor: pointer;
      box-shadow: 2px 2px 10px rgba(0,0,0,0.5);
      transition: 0.3s;
    }

    #intro button:hover {
      transform: scale(1.1);
      box-shadow: 2px 2px 20px rgba(0,0,0,0.7);
    }

    #birthday {
      display: none;
      width: 100%;
      height: 100vh;
      position: relative;
      background: url('https://i.pinimg.com/736x/b6/8c/d2/b68cd2c21df95e1f2d445c0d2f997e8b.jpg') no-repeat center center fixed;
      background-size: cover;
    }

    h1 {
      margin-top: 15%;
      font-size: 80px;
      font-weight: bold;
      color: #ff69b4;
      text-shadow: 2px 2px 12px #fff, 0 0 20px #ff69b4;
      animation: fadeIn 3s ease-in-out;
    }

    p {
      font-size: 28px;
      margin-top: 20px;
      text-shadow: 1px 1px 5px rgba(0,0,0,0.5);
      animation: fadeIn 4s ease-in-out;
    }

    @keyframes fadeIn {
      from {opacity: 0;}
      to {opacity: 1;}
    }

    .flower {
      position: absolute;
      animation: fall linear infinite;
      opacity: 0.9;
      pointer-events: none;
    }

    @keyframes fall {
      0% {top: -10%; transform: rotate(0deg);}
      100% {top: 110%; transform: rotate(360deg);}
    }

  </style>
</head>
<body>

<div id="intro">
  <button onclick="showBirthday()">Open your surprise 🎉</button>
</div>

<div id="birthday">
  <h1>Sister Samra</h1>
  <p>Wishing you a day full of love, joy, and endless happiness! 🎉<br>
  May Allah bless you with health, success, and all the smiles in the world! 💖</p>
  
  <audio autoplay loop>
    <source src="https://www.bensound.com/bensound-music/bensound-buddy.mp3" type="audio/mpeg">
  </audio>
</div>

<script>
function showBirthday() {
  document.getElementById('intro').style.display = 'none';
  document.getElementById('birthday').style.display = 'block';
}

// Pink & white flowers images (use transparent PNGs)
const flowerImages = [
  "https://i.ibb.co/qC9dQYf/pink-flower.png",
  "https://i.ibb.co/7JcDgHf/white-flower.png"
];

for(let i=0; i<50; i++){
  let flower = document.createElement("img");
  flower.src = flowerImages[Math.floor(Math.random()*flowerImages.length)];
  flower.className = "flower";
  flower.style.left = Math.random()*100 + "vw";
  flower.style.width = (30 + Math.random()*40) + "px";
  flower.style.animationDuration = (Math.random()*5 + 5) + "s";
  document.getElementById('birthday').appendChild(flower);
}
</script>

</body>
</html>
