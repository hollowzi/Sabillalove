<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>Untuk Kamu ❤️</title>
  <style>
    body {
      margin: 0;
      padding: 0;
      background: linear-gradient(to bottom, #fff0f5, #ffe6e6);
      font-family: 'Segoe UI', sans-serif;
      text-align: center;
      overflow: hidden;
    }

    h1 {
      margin-top: 60px;
      font-size: 3em;
      color: #e60073;
      animation: fadeIn 2s ease-out;
    }

    p {
      font-size: 1.3em;
      margin: 20px;
      color: #333;
      animation: fadeIn 3s ease-out;
    }

    button {
      margin-top: 30px;
      padding: 15px 25px;
      font-size: 1.1em;
      background-color: #ff6699;
      border: none;
      border-radius: 10px;
      color: white;
      cursor: pointer;
      transition: 0.3s;
    }

    button:hover {
      background-color: #cc3366;
    }

    #response {
      margin-top: 30px;
      font-size: 1.5em;
      color: #cc0052;
      animation: pop 0.6s ease-in-out;
    }

    @keyframes fadeIn {
      from { opacity: 0; transform: translateY(-30px); }
      to { opacity: 1; transform: translateY(0); }
    }

    @keyframes pop {
      0% { transform: scale(0.5); opacity: 0; }
      100% { transform: scale(1); opacity: 1; }
    }

    .flower {
      position: absolute;
      width: 20px;
      height: 20px;
      background: pink;
      border-radius: 50%;
      animation: fall linear infinite;
      opacity: 0.7;
    }

    @keyframes fall {
      0% { transform: translateY(-50px) rotate(0deg); }
      100% { transform: translateY(100vh) rotate(360deg); }
    }
  </style>
</head>
<body>
  <h1>❤️ Aku Cinta Kamu ❤️</h1>
  <p>Aku sudah lama ingin mengatakan ini...</p>
  <p>Kamu sangat istimewa bagiku, dan aku ingin kita jadi lebih dari sekadar teman.</p>
  <p>Maukah kamu menjadi orang yang selalu ada di sisiku?</p>

  <button onclick="showLove()">Aku Juga Suka Kamu ❤️</button>
  <div id="response"></div>

  <!-- Musik otomatis -->
  <audio autoplay loop>
    <source src="https://www.bensound.com/bensound-music/bensound-love.mp3" type="audio/mp3">
    Browser kamu tidak mendukung audio.
  </audio>

  <script>
    function showLove() {
      const res = document.getElementById("response");
      res.innerHTML = "🥰 Aku juga sayang kamu! Terima kasih sudah membalas cintaku 💖";
    }

    // Efek bunga jatuh
    function createFlower() {
      const flower = document.createElement("div");
      flower.classList.add("flower");
      flower.style.left = Math.random() * 100 + "vw";
      flower.style.animationDuration = 3 + Math.random() * 5 + "s";
      document.body.appendChild(flower);
      setTimeout(() => flower.remove(), 8000);
    }

    setInterval(createFlower, 300);
  </script>
</body>
</html>
