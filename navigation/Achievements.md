---
layout: page
title: Rock Paper Scissors
permalink: /Achievements/
comments: true
---

<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <style>
    body {
      font-family: Arial, sans-serif;
      text-align: center;
      background: #CB4325;
      padding-top: 50px;
    }
    h1 {
      color: #CB4325;
    }
    .options {
      margin: 20px;
    }
    button {
      font-size: 20px;
      margin: 10px;
      padding: 10px 20px;
      cursor: pointer;
    }
    .result {
      font-size: 24px;
      margin-top: 30px;
      font-weight: bold;
    }
  </style>
</head>
<body>
  <h1>Rock Paper Scissors</h1>
  <div class="option">
    <button onclick="play('rock')">🪨 Rock</button>
    <button onclick="play('paper')">📄 Paper</button>
    <button onclick="play('scissors')">✂️ Scissors</button>
  </div>
  <div class="result" id="result"></div>

  <script>
    function play(playerChoice) {
      const options = ['rock', 'paper', 'scissors'];
      const computerChoice = options[Math.floor(Math.random() * options.length)];
      
      let result = '';
      if (playerChoice === computerChoice) {
        result = "It's a tie!";
      } else if (
        (playerChoice === 'rock' && computerChoice === 'scissors') ||
        (playerChoice === 'scissors' && computerChoice === 'paper') ||
        (playerChoice === 'paper' && computerChoice === 'rock')
      ) {
        result = `You Win! ${playerChoice} beats ${computerChoice}`;
      } else {
        result = `You Lose! ${computerChoice} beats ${playerChoice}`;
      }

      document.getElementById('result').textContent = result;
    }
  </script>
</body>
</html>





