<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Login</title>
    <style>
        #calculator {
            opacity: 0;
            transition: opacity 0.5s ease-in-out;
            display: none;
        }

        #login-form {
            display: block;
        }

        #login-success {
            display: none;
        }

        #signup {
            display: none;
        }

        #login-success.visible,
        #calculator.visible,
        #signup.visible {
            opacity: 1;
            display: block;
        }

        #login-form,
        #signup {
            transition: opacity 0.5s ease-in-out;
            opacity: 1;
        }

        #login-form.fade-out,
        #signup.fade-out {
            opacity: 0;
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
        <section id="login-success" class="visible">
            <h2>Successfully logged in!</h2>
            <button onclick="showCalculator();">Go to Calculator</button>
            <button onclick="showSignup();">Sign Up</button>
        </section>
        <section id="calculator">
            <h2>Enter an expression to calculate</h2>
            <input type="text" id="calculator-input" oninput="calculate();">
            <p id="calculator-result"></p>
        </section>
        <section id="signup" class="visible">
            <h2>Sign Up</h2>
            <form action="#" method="post" onsubmit="return signup();">
                <label for="new-username">Username:</label>
                <input type="text" id="new-username" name="new-username" required>

                <label for="new-password">Password:</label>
                <input type="password" id="new-password" name="new-password" required>

                <button type="submit">Sign Up</button>
            </form>
            <button onclick="showLogin();">Back to Login</button>
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
                document.getElementById("login-form").classList.add("fade-out");
                document.getElementById("login-success").classList.add("visible");
                document.getElementById("signup").classList.add("visible");
                return false;
            } else {
                alert("Invalid credentials");
                return false;
            }
        }

        function showCalculator() {
            document.getElementById("login-success").classList.remove("visible");
            document.getElementById("calculator").classList.add("visible");
            document.getElementById("signup").classList.add("visible");
document.getElementById("login-form").classList.add("fade-out");
        }

        function calculate() {
            const input = document.getElementById("calculator-input").value;
            const result = eval(input);
            document.getElementById("calculator-result").innerText = "Result: " + result;
        }

        function showSignup() {
            document.getElementById("login-success").classList.remove("visible");
            document.getElementById("signup").classList.add("visible");
            document.getElementById("login-form").classList.add("fade-out");
        }

        function showLogin() {
            document.getElementById("login-form").classList.remove("fade-out");
            document.getElementById("signup").classList.remove("visible");
            document.getElementById("calculator").classList.remove("visible");
            document.getElementById("login-success").classList.remove("visible");
        }

        function signup() {
            const newUsername = document.getElementById("new-username").value;
            const newPassword = document.getElementById("new-password").value;

            // Replace this with your actual signup logic
            if (newUsername !== "admin" && newPassword !== "password") {
                alert("Sign up successful!");
                document.getElementById("signup").classList.remove("visible");
                document.getElementById("login-form").classList.remove("fade-out");
                return false;
            } else {
                alert("Sign up failed. Please choose a different username and password.");
                return false;
            }
        }
    </script>
</body>
</html>
