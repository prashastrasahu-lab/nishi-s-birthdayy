# nishi-s-birthdayy
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Happy Birthday My Love 🎉</title>
  <style>
    body {
      margin: 0;
      padding: 0;
      font-family: 'Poppins', sans-serif;
      background: linear-gradient(to bottom right, #fbc2eb, #a6c1ee);
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      min-height: 100vh;
      text-align: center;
      overflow-x: hidden;
    }
    h1 {
      font-size: 3rem;
      color: #d63384;
      text-shadow: 2px 2px 5px rgba(0,0,0,0.2);
      animation: popIn 1s ease forwards;
    }
    p {
      font-size: 1.2rem;
      color: #333;
      max-width: 600px;
      margin-top: 20px;
      line-height: 1.6;
      opacity: 0;
      animation: fadeIn 2s ease forwards;
      animation-delay: 1s;
    }
    .cards {
      display: flex;
      gap: 20px;
      margin-top: 50px;
      opacity: 0;
      animation: fadeIn 2s ease forwards;
      animation-delay: 2s;
      flex-wrap: wrap;
      justify-content: center;
    }
    .card {
      background: white;
      padding: 20px;
      border-radius: 20px;
      box-shadow: 0 5px 15px rgba(0,0,0,0.1);
      transition: transform 0.3s;
    }
    .card:hover {
      transform: scale(1.1);
    }
    .note {
      margin-top: 50px;
      font-size: 1.3rem;
      font-weight: bold;
      color: #b5179e;
      opacity: 0;
      animation: fadeIn 2s ease forwards;
      animation-delay: 3s;
    }
    @keyframes popIn {
      from {transform: scale(0); opacity: 0;}
      to {transform: scale(1); opacity: 1;}
    }
    @keyframes fadeIn {
      from {opacity: 0; transform: translateY(30px);}
      to {opacity: 1; transform: translateY(0);}
    }
  </style>
  <script src="https://cdn.jsdelivr.net/npm/canvas-confetti@1.9.2/dist/confetti.browser.min.js"></script>
</head>
<body>

  <h1>🎉 Happy Birthday My Love 🎉</h1>
  <p>
    Wishing the happiest birthday to the most special person in my life 💕<br>
    You make my world brighter every single day. I’m so lucky to have you 💖
  </p>

  <div class="cards">
    <div class="card">🎂 Cake for You</div>
    <div class="card">🎁 A Gift of Love</div>
    <div class="card">❤️ Endless Love</div>
  </div>

  <div class="note">🎶 Play this while thinking of me 💕</div>
  <audio controls autoplay loop style="margin-top:20px;">
    <source src="song.mp3" type="audio/mpeg">
  </audio>

  <script>
    // Confetti animation
    const duration = 5 * 1000;
    const end = Date.now() + duration;

    (function frame() {
      confetti({
        particleCount: 5,
        angle: 60,
        spread: 55,
        origin: { x: 0 }
      });
      confetti({
        particleCount: 5,
        angle: 120,
        spread: 55,
        origin: { x: 1 }
      });

      if (Date.now() < end) {
        requestAnimationFrame(frame);
      }
    }());
  </script>

</body>
</html>
