<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Chemistry Team</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background: #f4f4f4;
      margin: 0;
      padding: 0;
    }
    header {
      background: #222;
      color: white;
      padding: 20px;
      text-align: center;
    }
    header img {
      width: 100px;
      height: auto;
      margin-bottom: 10px;
    }
    .container {
      padding: 20px;
      max-width: 900px;
      margin: auto;
    }
    .video-card {
      background: white;
      border-radius: 8px;
      box-shadow: 0 2px 5px rgba(0,0,0,0.1);
      margin-bottom: 20px;
      padding: 15px;
    }
    .video-card h3 {
      margin-top: 0;
    }
    video {
      width: 100%;
      border-radius: 6px;
    }
    .login-container {
      max-width: 400px;
      margin: 100px auto;
      background: white;
      padding: 30px;
      border-radius: 10px;
      box-shadow: 0 4px 10px rgba(0,0,0,0.1);
    }
    .login-container h2 {
      text-align: center;
    }
    .login-container input[type="text"],
    .login-container input[type="password"] {
      width: 100%;
      padding: 10px;
      margin: 10px 0;
      border: 1px solid #ccc;
      border-radius: 5px;
    }
    .login-container input[type="submit"] {
      width: 100%;
      padding: 10px;
      background: #222;
      color: white;
      border: none;
      border-radius: 5px;
      cursor: pointer;
    }
    .welcome-message {
      text-align: center;
      font-size: 1.2em;
      margin: 20px 0;
      color: #333;
    }
  </style>
  <script>
    function login(event) {
      event.preventDefault();
      const username = document.getElementById("username").value;
      const password = document.getElementById("password").value;
      if (username === "team" && password === "1234") {
        document.getElementById("loginPage").style.display = "none";
        document.getElementById("mainContent").style.display = "block";
        document.getElementById("welcomeUser").textContent =
          "Welcome, " + username + "!";
      } else {
        alert("Incorrect username or password.");
      }
    }
  </script>
</head>
<body>
  <!-- صفحة تسجيل الدخول -->
  <div id="loginPage" class="login-container">
    <h2>Login to Chemistry Team</h2>
    <form onsubmit="login(event)">
      <input type="text" id="username" placeholder="Username" required />
      <input type="password" id="password" placeholder="Password" required />
      <input type="submit" value="Log In" />
    </form>
  </div>

  <!-- الصفحة الرئيسية بعد تسجيل الدخول -->
  <div id="mainContent" style="display: none">
    <header>
      <!-- الصورة المضافة -->
      <img src="data:image/png;base64,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" alt="Logo" />

      <h1>🧪 Chemistry Team</h1>
      <p>Watch all shared content in one place</p>
    </header>

    <div class="container">
      <div class="welcome-message" id="welcomeUser"></div>

      <!-- فيديو تجريبي -->
      <div class="video-card">
        <h3>Team Intro Video</h3>
        <video controls>
          <source src="https://www.w3schools.com/html/mov_bbb.mp4" type="video/mp4" />
          Your browser does not support the video tag.
        </video>
      </div>
    </div>
  </div>
</body>
</html>
