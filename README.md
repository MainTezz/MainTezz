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
            <h2>Successfully logged in!</h
