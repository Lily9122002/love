<!DOCTYPE html>
<html lang="zh">
<head>
  <meta charset="UTF-8">
  <title>中秋节快乐 🎑</title>
  <style>
    body {
      margin: 0;
      height: 100vh;
      background: radial-gradient(circle at center, #ffe9b3 0%, #ffcc66 70%);
      overflow: hidden;
      display: flex;
      justify-content: center;
      align-items: center;
      flex-direction: column;
      font-family: "Microsoft YaHei", sans-serif;
    }
    h1 {
      font-size: 3em;
      color: #d6336c;
      text-shadow: 0 0 20px #ff99cc;
      animation: glow 2s infinite alternate;
    }
    @keyframes glow {
      from { text-shadow: 0 0 10px #ff99cc; }
      to { text-shadow: 0 0 30px #ff3366; }
    }
    .heart {
      position: absolute;
      width: 20px;
      height: 20px;
      background-color: #ff4d6d;
      transform: rotate(45deg);
      animation: float 5s infinite ease-in;
    }
    .heart::before,
    .heart::after {
      content: "";
      position: absolute;
      width: 20px;
      height: 20px;
      background-color: #ff4d6d;
      border-radius: 50%;
    }
    .heart::before { top: -10px; left: 0; }
    .heart::after { left: -10px; top: 0; }
    @keyframes float {
      0% { transform: translateY(0) rotate(45deg); opacity: 1; }
      100% { transform: translateY(-100vh) rotate(45deg); opacity: 0; }
    }
  </style>
</head>
<body>
  <h1>中秋节快乐 🎑💕</h1>

  <script>
    function createHeart() {
      const heart = document.createElement('div');
      heart.classList.add('heart');
      heart.style.left = Math.random() * 100 + 'vw';
      heart.style.animationDuration = (2 + Math.random() * 3) + 's';
      document.body.appendChild(heart);
      setTimeout(() => heart.remove(), 5000);
    }
    setInterval(createHeart, 300);
  </script>
</body>
</html>
