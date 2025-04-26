# Task-2
Task 2 SkillCraft Technology Internship
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>Simple Calculator</title>
  <style>
    body {
      background: #f0f0f0;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      font-family: 'Poppins', sans-serif;
    }
    .calculator {
      background: #fff;
      padding: 30px;
      border-radius: 10px;
      box-shadow: 0 4px 8px rgba(0,0,0,0.2);
      width: 300px;
    }
    .calculator input {
      width: 100%;
      height: 50px;
      margin-bottom: 20px;
      font-size: 24px;
      text-align: right;
      padding: 10px;
      border: 1px solid #ccc;
      border-radius: 5px;
    }
    .buttons {
      display: grid;
      grid-template-columns: repeat(4, 1fr);
      gap: 10px;
    }
    .buttons button {
      padding: 20px;
      font-size: 18px;
      border: none;
      border-radius: 5px;
      background: #00aced;
      color: #fff;
      cursor: pointer;
      transition: background 0.3s;
    }
    .buttons button:hover {
      background: #007bb5;
    }
  </style>
</head>
<body>

<div class="calculator">
  <input type="text" id="display" readonly>
  <div class="buttons">
    <button onclick="appendNumber('7')">7</button>
    <button onclick="appendNumber('8')">8</button>
    <button onclick="appendNumber('9')">9</button>
    <button onclick="appendOperator('/')">÷</button>

    <button onclick="appendNumber('4')">4</button>
    <button onclick="appendNumber('5')">5</button>
    <button onclick="appendNumber('6')">6</button>
    <button onclick="appendOperator('*')">×</button>

    <button onclick="appendNumber('1')">1</button>
    <button onclick="appendNumber('2')">2</button>
    <button onclick="appendNumber('3')">3</button>
    <button onclick="appendOperator('-')">-</button>

    <button onclick="appendNumber('0')">0</button>
    <button onclick="appendNumber('.')">.</button>
    <button onclick="calculate()">=</button>
    <button onclick="appendOperator('+')">+</button>

    <button onclick="clearDisplay()" style="grid-column: span 4; background: #f44336;">C</button>
  </div>
</div>

<script>
  let display = document.getElementById('display');

  function appendNumber(number) {
    display.value += number;
  }

  function appendOperator(operator) {
    display.value += operator;
  }

  function calculate() {
    try {
      display.value = eval(display.value);
    } catch (error) {
      display.value = 'Error';
    }
  }

  function clearDisplay() {
    display.value = '';
  }
</script>

</body>
</html>
