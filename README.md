<!DOCTYPE html>
<html>
<head>
  <title>Temperature Converter</title>
  <style>
    body {
      font-family: Arial, sans-serif;
    }

    h1 {
      text-align: center;
    }

    .container {
      max-width: 400px;
      margin: 0 auto;
    }

    label {
      display: block;
      margin-bottom: 5px;
    }

    input[type="number"] {
      width: 100%;
      padding: 8px;
      box-sizing: border-box;
      margin-bottom: 10px;
    }

    .btn {
      background-color: #4CAF50;
      color: white;
      padding: 10px;
      border: none;
      cursor: pointer;
      width: 100%;
    }

    .result {
      font-weight: bold;
      margin-top: 10px;
    }
  </style>
</head>
<body>
  <div class="container">
    <h1>Temperature Converter</h1>
    <label>Enter temperature in Celsius:</label>
    <input type="number" id="celsiusInput" placeholder="Celsius" step="0.01">
    <label>Enter temperature in Fahrenheit:</label>
    <input type="number" id="fahrenheitInput" placeholder="Fahrenheit" step="0.01">
    <button class="btn" onclick="convertToCelsius()">Convert to Celsius</button>
    <button class="btn" onclick="convertToFahrenheit()">Convert to Fahrenheit</button>
    <p class="result" id="result"></p>
  </div>

  <script>
    function convertToCelsius() {
      var fahrenheitInput = document.getElementById('fahrenheitInput').value;
      var celsius = (parseFloat(fahrenheitInput) - 32) * 5 / 9;
      document.getElementById('result').textContent = celsius.toFixed(2) + ' °C';
    }

    function convertToFahrenheit() {
      var celsiusInput = document.getElementById('celsiusInput').value;
      var fahrenheit = (parseFloat(celsiusInput) * 9 / 5) + 32;
      document.getElementById('result').textContent = fahrenheit.toFixed(2) + ' °F';
    }
  </script>
</body>
</html>


