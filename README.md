# CODSOfT
Tech intership
<html>
<head>
    <title>Basic Calculator</title>
    <link rel="stylesheet" href="calculator.css">
</head>
<body>
    <h2>Calculator</h2>
    <div class="calculator">
        <input type="text" class="display" id="display" disabled>
        <div class="buttons">
            <button onclick="clearDisplay()" class="clear">C</button>
            <button onclick="appendToDisplay('7')">7</button>
            <button onclick="appendToDisplay('8')">8</button>
            <button onclick="appendToDisplay('9')">9</button>
            <button onclick="appendToDisplay('/')" class="operator">/</button>
            <button onclick="appendToDisplay('4')">4</button>
            <button onclick="appendToDisplay('5')">5</button>
            <button onclick="appendToDisplay('6')">6</button>
            <button onclick="appendToDisplay('*')" class="operator">*</button>
            <button onclick="appendToDisplay('1')">1</button>
            <button onclick="appendToDisplay('2')">2</button>
            <button onclick="appendToDisplay('3')">3</button>
            <button onclick="appendToDisplay('-')" class="operator">-</button>
            <button onclick="appendToDisplay('0')">0</button>
            <button onclick="appendToDisplay('.')">.</button>
            <button onclick="calculate()" class="equal">=</button>
            <button onclick="appendToDisplay('+')" class="operator">+</button>
        </div>
    </div>

    <script>
        function appendToDisplay(value) {
            document.getElementById('display').value += value;
        }
        function clearDisplay() {
            document.getElementById('display').value = '';
        }
        function calculate() {
            try {
                document.getElementById('display').value = eval(document.getElementById('display').value);
            } catch {
                document.getElementById('display').value = 'Error';
            }
        }
    </script>
</body>
</html>
