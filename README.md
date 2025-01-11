# fun-web
A simple website for fun..
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Mini Game: Guess the Number</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      text-align: center;
      background-color: #f0f8ff;
      margin: 0;
      padding: 20px;
    }
    h1 {
      color: #333;
    }
    input {
      padding: 10px;
      font-size: 16px;
      margin: 10px;
    }
    button {
      padding: 10px 20px;
      font-size: 16px;
      background-color: #4caf50;
      color: white;
      border: none;
      border-radius: 5px;
      cursor: pointer;
    }
    button:hover {
      background-color: #45a049;
    }
    #result {
      margin-top: 20px;
      font-size: 18px;
      color: #555;
    }
  </style>
</head>
<body>
  <h1>Guess the Number Game</h1>
  <p>I'm thinking of a number between 1 and 100. Can you guess it?</p>
  <input type="number" id="guessInput" placeholder="Enter your guess" />
  <button onclick="checkGuess()">Submit Guess</button>
  <div id="result"></div>

  <script>
    // Generate a random number between 1 and 100
    const randomNumber = Math.floor(Math.random() * 100) + 1;

    function checkGuess() {
      const guess = document.getElementById('guessInput').value;
      const result = document.getElementById('result');

      if (guess == randomNumber) {
        result.textContent = '🎉 Correct! You guessed the number!';
        result.style.color = 'green';
      } else if (guess < randomNumber) {
        result.textContent = '📉 Too low! Try again.';
        result.style.color = 'orange';
      } else {
        result.textContent = '📈 Too high! Try again.';
        result.style.color = 'orange';
      }
    }
  </script>
</body>
</html>