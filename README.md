[Uploading t<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Forgive Me</title>
  <style>
    body {
      background: linear-gradient(45deg, #ff7eb3, #ff00a3, #ff007f);
      height: 100vh;
      margin: 0;
      display: flex;
      justify-content: center;
      align-items: center;
      font-family: Arial, sans-serif;
    }
    .game-container {
      text-align: center;
      padding: 20px;
      border-radius: 20px;
      background-color: #fff;
      box-shadow: 0 8px 16px rgba(0, 0, 0, 0.2);
    }
    h1 {
      color: #ff007f;
    }
    p {
      color: #333;
      font-size: 18px;
      margin-bottom: 15px;
    }
    button {
      padding: 10px 20px;
      font-size: 16px;
      background-color: #ff007f;
      color: #fff;
      border: none;
      border-radius: 5px;
      cursor: pointer;
    }
    button:hover {
      background-color: #ff0055;
    }
    .hidden {
      display: none;
    }
    .heart {
      font-size: 50px;
      color: red;
    }
  </style>
</head>
<body>
  <div class="game-container" id="part1">
    <h1>Apology Adventure</h1>
    <p>Dear Love, I've set up a game for you!</p>
    <p>Click the button below to start the quest to forgiveness.</p>
    <button onclick="startGame()">Begin the Adventure</button>
  </div>

  <div class="game-container hidden" id="part2">
    <h1>Level 1: Puzzling Apology</h1>
    <p>Unscramble the letters to reveal the message:</p>
    <p id="scrambledMessage">I'm yBUs o!rry</p>
    <input type="text" id="inputBox">
    <button onclick="checkAnswer()">Submit Answer</button>
    <p id="feedback"></p>
  </div>

  <div class="game-container hidden" id="part3">
    <h1>Level 2: Memory Lane</h1>
    <p>Memorize the sequence of numbers:</p>
    <p id="memorySequence">5, 8, 2, 4</p>
    <input type="text" id="inputSequence">
    <button onclick="checkSequence()">Submit Sequence</button>
    <p id="sequenceFeedback"></p>
  </div>

  <div class="game-container hidden" id="part4">
    <h1>Final Level: True Forgiveness</h1>
    <p>Can you forgive me, my love?</p>
    <button onclick="showHeart()">Yes, I forgive you</button>
  </div>

  <div class="game-container hidden" id="part5">
    <h1>Final Message</h1>
    <p class="heart">&#10084;</p>
    <p>I love you infinity BOU</p>
  </div>

  <script>
    let correctAnswer = "I'm sorry, my love";
    let correctSequence = "5824";

    function startGame() {
      document.getElementById('part1').classList.add('hidden');
      document.getElementById('part2').classList.remove('hidden');
    }

    function checkAnswer() {
      let userAnswer = document.getElementById('inputBox').value.toLowerCase();
      if (userAnswer === correctAnswer.toLowerCase()) {
        document.getElementById('feedback').innerText = "Well done! Proceed to the next level.";
        document.getElementById('part2').classList.add('hidden');
        document.getElementById('part3').classList.remove('hidden');
      } else {
        document.getElementById('feedback').innerText = "Try again!";
      }
    }

    function checkSequence() {
      let userSequence = document.getElementById('inputSequence').value;
      if (userSequence === correctSequence) {
        document.getElementById('sequenceFeedback').innerText = "Impressive! One more level to go.";
        document.getElementById('part3').classList.add('hidden');
        document.getElementById('part4').classList.remove('hidden');
      } else {
        document.getElementById('sequenceFeedback').innerText = "Not quite right. Give it another shot!";
      }
    }

    function showHeart() {
      document.getElementById('part4').classList.add('hidden');
      document.getElementById('part5').classList.remove('hidden');
    }
  </script>
</body>
</html>
ahiyaLive.html…]()
