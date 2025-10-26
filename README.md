<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Duxo | Home</title>
  <style>
    :root {
      --main: #3399ff;
      --secondary: #ff9933;
    }

    body {
      font-family: Arial, sans-serif;
      background: var(--main);
      color: white;
      margin: 0;
      text-align: center;
    }

    header {
      background: var(--secondary);
      padding: 1rem;
      font-size: 2rem;
      font-weight: bold;
    }

    .wrap {
      margin: 2rem auto;
      max-width: 900px;
      background: rgba(255, 255, 255, 0.1);
      border-radius: 20px;
      padding: 2rem;
      box-shadow: 0 0 20px rgba(0,0,0,0.3);
    }

    h1 {
      color: white;
    }

    /* Sub Race Button */
    .subrace-button {
      position: fixed;
      top: 20px;
      right: 20px;
      background: var(--secondary);
      color: white;
      padding: 12px 24px;
      border-radius: 50px;
      font-weight: bold;
      font-size: 1.2rem;
      cursor: pointer;
      box-shadow: 0 0 20px rgba(255,153,51,0.6);
      animation: flash 1.2s infinite alternate, bounce 2s infinite ease-in-out;
      z-index: 999;
      transition: transform 0.3s;
      user-select: none;
    }

    .subrace-button:hover {
      transform: scale(1.1);
    }

    @keyframes flash {
      0% { background-color: var(--secondary); color: white; box-shadow: 0 0 10px rgba(255,153,51,0.5); }
      100% { background-color: white; color: var(--secondary); box-shadow: 0 0 25px rgba(255,153,51,1); }
    }

    @keyframes bounce {
      0%, 100% { transform: translateY(0); }
      50% { transform: translateY(-6px); }
    }

    iframe {
      border-radius: 12px;
      width: 100%;
      height: 500px;
      border: none;
      margin-top: 20px;
    }
  </style>
</head>
<body>
  <header>Duxo Channel</header>

  <!-- Flashy SUB RACE Button -->
  <div class="subrace-button" id="subrace-btn">SUB RACE!!</div>

  <div class="wrap">
    <h1>Welcome to Duxo’s Official Homepage!</h1>
    <p>Check out my latest YouTube video below 👇</p>

    <!-- YouTube Embed -->
    <iframe 
      src="https://www.youtube.com/embed?listType=user_uploads&list=Duxo._.W" 
      allowfullscreen>
    </iframe>
  </div>

  <script>
    // Redirect to subrace.html when the button is clicked
    document.getElementById('subrace-btn').addEventListener('click', () => {
      window.location.href = "subrace.html";
    });
  </script>
</body>
</html>
