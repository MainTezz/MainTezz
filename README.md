<html>
<head>
  <title>Login Form</title>
  <style>
    .form-container {
      width: 300px;
      margin: 0 auto;
      display: flex;
      flex-direction: column;
      align-items: center;
    }
    input[type="email"], input[type="password"], input[type="text"] {
      width: 80%;
      padding: 10px;
      margin-bottom: 10px;
      border: 1px solid #ccc;
      border-radius: 4px;
      box-sizing: border-box;
    }
    input[type="submit"] {
      width: 80%;
      padding: 10px;
      background-color: #4CAF50;
      color: white;
      border: none;
      border-radius: 4px;
      cursor: pointer;
    }
    input[type="submit"]:hover {
      background-color: #3e8e41;
    }
  </style>
</head>
<body>
  <div class="form-container">
    <h2>Login Form</h2>
    <form id="login-form">
      <label for="email">Email:</label>
      <input type="email" id="email" name="email" required>

      <label for="password">Password:</label>
      <input type="password" id="password" name="password" required>

      <input type="submit" value="Log In">
    </form>
    <p>Don't have an account? <a href="#" id="create-account">Create one here</a></p>
  </div>

  <div id="nickname-container" style="display:none;">
    <h2>Create Nickname</h2>
    <form id="nickname-form">
      <label for="nickname">Choose a nickname:</label>
      <input type="text" id="nickname" name="nickname" required>

      <input type="submit" value="Create Nickname">
    </form>
  </div>

  <div id="home-container" style="display:none;">
    <h2>Welcome to the Home Page!</h2>
    <p>Your nickname is: <span id="nickname-display"></span></p>
    <p><a href="#" id="logout">Log Out</a></p>
  </div>

  <script>
    const loginForm = document.getElementById('login-form');
    const nicknameContainer = document.getElementById('nickname-container');
    const homeContainer = document.getElementById('home-container');
    const nicknameDisplay = document.getElementById('nickname-display');
    const logout = document.getElementById('logout');

    loginForm.addEventListener('submit', (e) => {
      e.preventDefault();
      const email = loginForm.email.value;
      const password = loginForm.password.value;

      // Here you would typically check if the email and password are correct
      // If they are, you can show the nickname container
      nicknameContainer.style.display = 'block';
    });

    const nicknameForm = document.getElementById('nickname-form');
    nicknameForm.addEventListener('submit', (e) => {
      e.preventDefault();
      const nickname = nicknameForm.nickname.value;

      // Here you would typically save the nickname to the server
      // If the nickname is saved successfully, you can show the home container
      homeContainer.style.display = 'block';
      nicknameDisplay.textContent = nickname;
    });

    logout.addEventListener('click', () => {
      // Here you would typically log out the user
      // If the user is logged out, you can show the login form again
      nicknameContainer.style.display = 'none';
      homeContainer.style.display = 'none';
      loginForm.style.display = 'block';
    });
  </script>
</body>
</html>
