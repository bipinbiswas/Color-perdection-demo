# Color-perdection-demo
<!DOCTYPE html>
<html>
<head>
  <title>Color Prediction Demo</title>
  <style>
    body { text-align: center; font-family: sans-serif; padding: 30px; }
    button { padding: 10px 20px; margin: 10px; font-size: 18px; border-radius: 10px; }
    #result { margin-top: 30px; font-size: 28px; font-weight: bold; }
  </style>
</head>
<body>
  <h1>Color Prediction Demo</h1>
  <p>Pick your color prediction:</p>
  <button onclick="predict('Green')" style="background:green;color:white;">Green</button>
  <button onclick="predict('Red')" style="background:red;color:white;">Red</button>
  <button onclick="predict('Violet')" style="background:purple;color:white;">Violet</button>

  <div id="result"></div>

  <script>
    function predict(choice) {
      const colors = ['Green', 'Red', 'Violet'];
      const result = colors[Math.floor(Math.random() * colors.length)];
      let message = `Your Prediction: ${choice}<br>Result: ${result}<br>`;
      if(choice === result) {
        message += "<span style='color:green;'>You Win!</span>";
      } else {
        message += "<span style='color:red;'>You Lose!</span>";
      }
      document.getElementById('result').innerHTML = message;
    }
  </script>
</body>
</html>
