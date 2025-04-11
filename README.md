<!DOCTYPE html>
<html>
<head>
<title>Basic Calculator</title>
</head>
<body>

<div style="width: 250px; border: 1px solid black; padding: 10px; border-radius: 5px; background-color: #f0f0f0;">
  <input type="text" id="display" style="width: 95%; margin-bottom: 10px; padding: 10px; font-size: 18px; text-align: right; border: 1px solid #ccc; border-radius: 3px;">

  <div style="display: grid; grid-template-columns: repeat(4, 1fr); grid-gap: 5px;">
    <button onclick="clearDisplay()" style="padding: 15px; font-size: 16px; background-color: #e0e0e0; border: none; border-radius: 3px; cursor: pointer;">C</button>
    <button onclick="appendToDisplay('/')" style="padding: 15px; font-size: 16px; background-color: #e0e0e0; border: none; border-radius: 3px; cursor: pointer;">/</button>
    <button onclick="appendToDisplay('*')" style="padding: 15px; font-size: 16px; background-color: #e0e0e0; border: none; border-radius: 3px; cursor: pointer;">*</button>
    <button onclick="appendToDisplay('-')" style="padding: 15px; font-size: 16px; background-color: #e0e0e0; border: none; border-radius: 3px; cursor: pointer;">-</button>

    <button onclick="appendToDisplay('7')" style="padding: 15px; font-size: 16px; background-color: #f9f9f9; border: none; border-radius: 3px; cursor: pointer;">7</button>
    <button onclick="appendToDisplay('8')" style="padding: 15px; font-size: 16px; background-color: #f9f9f9; border: none; border-radius: 3px; cursor: pointer;">8</button>
    <button onclick="appendToDisplay('9')" style="padding: 15px; font-size: 16px; background-color: #f9f9f9; border: none; border-radius: 3px; cursor: pointer;">9</button>
    <button onclick="appendToDisplay('+')" style="padding: 15px; font-size: 16px; background-color: #e0e0e0; border: none; border-radius: 3px; cursor: pointer;">+</button>

    <button onclick="appendToDisplay('4')" style="padding: 15px; font-size: 16px; background-color: #f9f9f9; border: none; border-radius: 3px; cursor: pointer;">4</button>
    <button onclick="appendToDisplay('5')" style="padding: 15px; font-size: 16px; background-color: #f9f9f9; border: none; border-radius: 3px; cursor: pointer;">5</button>
    <button onclick="appendToDisplay('6')" style="padding: 15px; font-size: 16px; background-color: #f9f9f9; border: none; border-radius: 3px; cursor: pointer;">6</button>
    <button onclick="calculate()" style="padding: 15px; font-size: 16px; background-color: #4CAF50; color: white; border: none; border-radius: 3px; cursor: pointer;">=</button>

    <button onclick="appendToDisplay('1')" style="padding: 15px; font-size: 16px; background-color: #f9f9f9; border: none; border-radius: 3px; cursor: pointer;">1</button>
    <button onclick="appendToDisplay('2')" style="padding: 15px; font-size: 16px; background-color: #f9f9f9; border: none; border-radius: 3px; cursor: pointer;">2</button>
    <button onclick="appendToDisplay('3')" style="padding: 15px; font-size: 16px; background-color: #f9f9f9; border: none; border-radius: 3px; cursor: pointer;">3</button>
    <button></button> <button onclick="appendToDisplay('0')" style="padding: 15px; font-size: 16px; background-color: #f9f9f9; border: none; border-radius: 3px; cursor: pointer; grid-column: 1 / span 2;">0</button>
    <button onclick="appendToDisplay('.')" style="padding: 15px; font-size: 16px; background-color: #f9f9f9; border: none; border-radius: 3px; cursor: pointer;">.</button>
  </div>
</div>

<script>
  let display = document.getElementById('display');

  function appendToDisplay(value) {
    display.value += value;
  }

  function clearDisplay() {
    display.value = '';
  }

  function calculate() {
    try {
      display.value = eval(display.value);
    } catch (error) {
      display.value = 'Error';
    }
  }
</script>

</body>
</html>
