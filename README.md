<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Happy Birthday ❤️</title>

  <style>
    body {
      margin: 0;
      height: 100vh;
      background: linear-gradient(135deg, #ff9a9e, #fad0c4);
      display: flex;
      justify-content: center;
      align-items: center;
      font-family: 'Poppins', sans-serif;
      color: white;
      text-align: center;
      overflow: hidden;
    }

    .card {
      padding: 20px;
      animation: fadeIn 2s ease;
    }

    h1 {
      font-size: 2.2rem;
      animation: slideDown 1.5s ease;
    }

    p {
      font-size: 1.1rem;
      margin-top: 10px;
      animation: fadeIn 3s ease;
    }

    button {
      margin-top: 20px;
      padding: 12px 24px;
      border: none;
      border-radius: 30px;
      background: white;
      color: #ff5e78;
      font-size: 1rem;
      cursor: pointer;
    }

    .hearts span {
      position: absolute;
      bottom: -10px;
      animation: float 6s infinite;
      font-size: 20px;
    }

    @keyframes float {
      0% { transform: translateY(0); opacity: 1; }
      100% { transform: translateY(-800px); opacity: 0; }
    }

    @keyframes fadeIn {
      from { opacity: 0; }
      to { opacity: 1; }
    }

    @keyframes slideDown {
      from { transform: translateY(-50px); opacity: 0; }
      to { transform: translateY(0); opacity: 1; }
    }
  </style>
</head>
<body>

  <div class="card">
    <h1>Happy Birthday, <br> ❤️ Ayesha ❤️</h1>
    <p>
      You’re not just special today,  
      you’re special every single day 💫  
      Thank you for being YOU.
    </p>
    <button onclick="showLove()">Tap for a surprise 🎁</button>
  </div>

  <div class="hearts" id="hearts"></div>

  <script>
    function showLove() {
      for (let i = 0; i < 30; i++) {
        let heart = document.createElement("span");
        heart.innerHTML = "❤️";
        heart.style.left = Math.random() * 100 + "vw";
        heart.style.animationDuration = (Math.random() * 3 + 3) + "s";
        document.getElementById("hearts").appendChild(heart);

        setTimeout(() => heart.remove(), 6000);
      }
    }
  </script>

</body>
</html>
