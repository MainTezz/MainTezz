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
</head>
<body>
    <div class="login">
        <form id="login" method="get" action="login.php">
            <h2>Login Page</h2>
            <label><b>User Name</b></label><br>
            <input type="text" name="Uname" id="Uname" placeholder="Username"><br><br>
            <label><b>Password</b></label><br>
            <input type="Password" name="Pass" id="Pass" placeholder="Password"><br><br>
            <input type="button" name="log" id="log" value="Log In Here"><br><br>
            <input type="checkbox" id="check">
            <span>Remember me</span><br><br>
            Forgot <a href="#">Password</a><br>
        </form>
    </div>
</body>
</html>
