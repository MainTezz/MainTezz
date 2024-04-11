<!DOCTYPE html>
<html>
<head>
    <title>Calculator</title>
    <style>
        body {
            background-color: #6abadeba;
            font-family: 'Arial';
        }
        .calculator {
            width: 300px;
            overflow: hidden;
            margin: 20px auto;
            padding: 30px;
            background-color: white;
            border-radius: 15px;
        }
        input[type="text"], input[type="button"] {
            width: 300px;
            height: 30px;
            border: none;
            border-radius: 3px;
            padding-left: 8px;
        }
        button {
            width: 50px;
            height: 50px;
            border: none;
            border-radius: 25px;
            color: white;
            background-color: #08ffd1;
            font-size: 20px;
            cursor: pointer;
        }
    </style>
    <script>
        function calculate(op, a, b) {
            if (op === "+") {
                return a + b;
            } else if (op === "-") {
                return a - b;
            } else if (op === "*") {
                return a * b;
            } else if (op === "/") {
                return a / b;
            }
        }
        function solve() {
            var a = parseFloat(document.getElementById("A").value);
            var b = parseFloat(document.getElementById("B").value);
            var op = document.getElementById("Op").value;
            var result = calculate(op, a, b);
            document.getElementById("Result").value = result;
        }
    </script>
</head>
<body>
    <div class="calculator">
        <h2>Calculator</h2>
        <input type="text" id="A" placeholder="Enter first number"><br><br>
        <input type="text" id="B" placeholder="Enter second number"><br><br>
        <select id="Op">
            <option value="+">+</option>
            <option value="-">-</option>
            <option value="*">*</option>
            <option value="/">/</option>
        </select><br><br>
        <input type="button" value="Calculate" onclick="solve()"><br><br>
        <input type="text" id="Result" readonly><br><br>
    </div>
</body>
</html>
