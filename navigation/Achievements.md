---
layout: page
title: Achievements
permalink: /Achievements/
comments: true
---

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Dice Roller</title>
  <style>
    body {
      font-family: sans-serif;
      text-align: center;
      margin-top: 50px;
    }
    .dice {
      font-size: 100px;
      margin: 20px;
    }
    button {
      padding: 10px 20px;
      font-size: 18px;
      cursor: pointer;
    }
  </style>
</head>
<body>
  <h1>🎲 Roll the Dice!</h1>
  <div class="dice" id="dice">🎲</div>
  <button onclick="rollDice()">Roll</button>

  <script>
    const diceFaces = ['⚀', '⚁', '⚂', '⚃', '⚄', '⚅'];

    function rollDice() {
      const randomIndex = Math.floor(Math.random() * 6);
      document.getElementById('dice').textContent = diceFaces[randomIndex];
    }
  </script>
</body>
</html>




