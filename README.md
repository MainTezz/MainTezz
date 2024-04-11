<!DOCTYPE html>
<html>
<head>
    <title>Login Form</title>
    <style>
        body {
            background-color: #6abadeba;
            font-family: 'Arial';
        }
        .login {
            width: 382px;
            overflow: hidden;
            margin: 20px auto;
            padding: 80px;
            background-color: white;
            border-radius: 15px;
            transition: opacity 0.5s ease-in-out;
            opacity: 1;
        }
        h2 {
            text-align: center;
            color: #277582;
            padding: 20px;
        }
        label {
            color: #08ffd1;
            font-size: 17px;
        }
        input[type="text"], input[type="password"], input[type="button"] {
            width: 300px;
            height: 30px;
            border: none;
            border-radius: 3px;
            padding-left: 8px;
        }
        #log {
            width: 300px;
            height: 30px;
            border: none;
            border-radius: 17px;
            padding-left: 7px;
            color: blue;
        }
        span {
            color: white;
            font-size: 17px;
        }
        a {
            float: right;
            background-color: grey;
        }
    </style>
    <script>
        function validateForm() {
            var username = document.getElementById("Uname").value;
            var password = document.getElementById("Pass").value;
            if (username == "" || password == "") {
                alert("Please enter your username and password.");
                return false;
            }
            document.getElementById("login").style.opacity = "0";
            setTimeout(function() {
                window.location.href = "calculator.html";
            }, 500);
            return true;
        }
    </script>
</head>
<body>
    <div class="login" id="login">
        <form id="loginForm" method="post" action="login.php" onsubmit="return validateForm()">
            <h2>Login Page</h2>
            <label><b>User Name</b></label><br>
            <input type="text" name="Uname" id="Uname" placeholder="Username" required><br><br>
            <label><b>Password</b></label><br>
            <input type="Password" name="Pass" id="Pass" placeholder="Password" required><br><br>
            <input type="submit" name="log" id="log" value="Log In Here">
            <br><br>
            <input type="checkbox" id="check">
            <span>Remember me</span><br><br>
            Forgot <a href="#">Password</a><br>
        </form>
    </div>
</body>
</html>
