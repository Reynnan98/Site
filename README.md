<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Login</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <div class="login-container">
    <h1>Login</h1>
    <form id="login-form">
      <input type="text" id="username" placeholder="Usuário" required>
      <input type="password" id="password" placeholder="Senha" required>
      <button type="submit">Entrar</button>
    </form>
    <p id="error-message"></p>
  </div>
  <script src="script.js"></script>
</body>
</html>
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Animes</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <div class="anime-container">
    <h1>Bem-vindo, Teste1!</h1>
    <h2>Lista de Animes</h2>
    <ul>
      <li>Naruto</li>
      <li>One Piece</li>
      <li>Attack on Titan</li>
      <li>Dragon Ball Z</li>
      <li>Demon Slayer</li>
    </ul>
  </div>
</body>
</html>
body {
  font-family: Arial, sans-serif;
  background-color: #f0f0f0;
  margin: 0;
  padding: 0;
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
}

.login-container, .anime-container {
  background: white;
  padding: 20px;
  border-radius: 10px;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
  text-align: center;
}

input {
  display: block;
  margin: 10px auto;
  padding: 10px;
  width: 80%;
  border: 1px solid #ccc;
  border-radius: 5px;
}

button {
  padding: 10px 20px;
  background-color: #4CAF50;
  color: white;
  border: none;
  border-radius: 5px;
  cursor: pointer;
}

button:hover {
  background-color: #45a049;
}

#error-message {
  color: red;
  font-size: 14px;
}
// Script para validar login
document.getElementById('login-form').addEventListener('submit', function (e) {
  e.preventDefault();

  const username = document.getElementById('username').value;
  const password = document.getElementById('password').value;
  const errorMessage = document.getElementById('error-message');

  if (username === "Teste1" && password === "12345") {
    // Redirecionar para a página de animes
    window.location.href = "anime.html";
  } else {
    // Exibir mensagem de erro
    errorMessage.textContent = "Usuário ou senha incorretos.";
  }
});
