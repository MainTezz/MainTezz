<!DOCTYPE html>
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
    input[type="email"], input[type="password"] {
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
    <h2>Facebook</h2>
    <p>Hjelper deg med å holde kontakten og dele opplevelser med menneskene i livet ditt.</p>
    <form>
      <label for="email">E-postadresse eller telefonnummer</label>
      <input type="email" id="email" name="email" required>

      <label for="password">Passord</label>
      <input type="password" id="password" name="password" required>

      <input type="submit" value="Logg inn">
    </form>
    <p>Glemt passordet?</p>
    <p>Opprett ny konto</p>
    <p>Opprett en side for en kjendis, et merke eller en bedrift.</p>
  </div>
</body>
</html>
