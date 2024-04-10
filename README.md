<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Login</title>
    <style>
        #calculator {
            display: none;
        }

        #login-form {
            display: block;
        }

        #login-success {
            display: none;
        }

        #calculator-success {
            display: none;
        }
    </style>
</head>
<body>
    <header>
        <h1>Login</h1>
    </header>
    <main>
        <section id="login-form">
            <h2>Enter your credentials</h2>
            <form action="#" method="post" onsubmit="return login();">
                <label for="username">Username:</label>
                <input type="text" id="username" name="username" required>

                <label for="password">Password:</label>
                <input type="password" id="password" name="password" required>

                <button type="submit">Login</button>
            </form>
        </section>
        <section id="login-success">
            <h2>Successfully logged in!</h2>
            <button onclick="showCalculator();">Go to Calculator</button>
        </section>
        <section id="calculator">
            <h2>Enter an expression to calculate</h2>
            <input type="text" id="calculator-input" oninput="calculate();">
            <p id="calculator-result"></p>
        </section>
    </main>
    <footer>
        <p>Copyright © 2023 Simple Login and Calculator. All rights reserved.</p>
    </footer>
    <script>
        function login() {
            const username = document.getElementById("username").value;
            const password = document.getElementById("password").value;

            // Replace this with your actual authentication logic
            if (username === "admin" && password === "password") {
                document.getElementById("login-form").style.display = "none";
                document.getElementById("login-success").style.display = "block";
                return false;
            } else {
                alert("Invalid credentials");
                return false;
            }
        }

        function showCalculator() {
            document.getElementById("login-success").style.display = "none";
            document.getElementById("calculator").style.display = "block";
        }

        function calculate() {
            const input = document.getElementById("calculator-input").value;
            const result = eval(input);
            document.getElementById("calculator-result").innerText = "Result: " + result;
        }
    </script>
</body>
</html>
