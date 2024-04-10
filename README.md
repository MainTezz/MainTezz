<!DOCTYPE html>
<html>
<head>
	<title>Login/Signup Page</title>
	<link rel="stylesheet" type="text/css" href="styles.css">
</head>
<body>
	<div class="container">
		<div id="login">
			<form action="#">
				<h2>Login</h2>
	Here's the HTML code for the login/signup page:

HTML:
```html
<!DOCTYPE html>
<html>
<head>
	<title>Login/Signup Page</title>
	<link rel="stylesheet" type="text/css" href="styles.css">
</head>
<body>
	<div class="container">
		<div id="login">
			<form action="#">
				<h2>Login</h2>
				<input type="text" placeholder="Username" id="username" required>
				<input type="password" placeholder="Password" id="password" required>
				<button type="submit" id="login-btn">Login</button>
			</form>
		</div>
		<div id="signup">
			<form action="#">
				<h2>Signup</h2>
				<input type="text" placeholder="Username" id="signup-username" required>
				<input type="email" placeholder="Email" id="signup-email" required>
				<input type="password" placeholder="Password" id="signup-password" required>
				<button type="submit" id="signup-btn">Signup</button>
			</form>
		</div>
	</div>
	<script src="script.js"></script>
</body>
</html>
CSS:

css
Edit
Full Screen
Copy code
body {
	background-color: #f2f2f2;
	font-family: Arial, sans-serif;
}

.container {
	width: 300px;
	background-color: #fff;
	padding: 20px;
	border-radius: 5px;
	box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.1);
	margin: 50px auto;
}

h2 {
	text-align: center;
	margin-bottom: 20px;
}

input {
	width: 100%;
	padding: 10px;
	margin-bottom: 10px;
	border: 1px solid #ccc;
	border-radius: 5px;
	box-sizing: border-box;
}

button {
	width: 100%;
	padding: 10px;
	background-color: #4CAF50;
	color: #fff;
	border: none;
	border-radius: 5px;
	cursor: pointer;
}

button:hover {
	background-color: #45a049;
}

#signup {
	display: none;
}
