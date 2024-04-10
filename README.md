<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Login</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <div class="container">
        <h1>Welcome Back!</h1>
        <form id="login-form">
            <label for="email">Email address</label>
            <input type="email" id="email" name="email" required>

            <label for="password">Password</label>
            <div class="password-container">
                <input type="password" id="password" name="password" required>
                <span class="show-password-btn">Show</span>
            </div>

            <button type="submit">Sign In</button>
        </form>
        <div class="signup-link">
            Don't have an account? <a href="signup.html">Create one</a>
        </div>
    </div>
</body>
</html>
