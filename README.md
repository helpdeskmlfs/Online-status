<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Toggle Status Website</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <style>
    body {
      font-family: Arial, sans-serif;
      text-align: center;
      padding: 40px;
      background-color: #f9f9f9;
    }

    h1 {
      color: #333;
    }

    #status {
      font-size: 24px;
      font-weight: bold;
      margin: 20px 0;
    }

    .online {
      color: green;
    }

    .offline {
      color: red;
    }

    button {
      padding: 12px 24px;
      font-size: 16px;
      cursor: pointer;
      border: none;
      border-radius: 8px;
      background-color: #007bff;
      color: white;
      transition: background-color 0.3s;
    }

    button:hover {
      background-color: #0056b3;
    }

    footer {
      margin-top: 50px;
      font-size: 14px;
      color: #888;
    }
  </style>
</head>
<body>

  <h1>Employee Online Status</h1>
  <div id="status" class="offline">Status: Offline</div>
  <button onclick="toggleStatus()">Go Online</button>

  <footer>Built for team use</footer>

  <script>
    let isOnline = false;

    function toggleStatus() {
      isOnline = !isOnline;
      const statusEl = document.getElementById("status");
      const buttonEl = document.querySelector("button");

      if (isOnline) {
        statusEl.textContent = "Status: Online";
        statusEl.className = "online";
        buttonEl.textContent = "Go Offline";
      } else {
        statusEl.textContent = "Status: Offline";
        statusEl.className = "offline";
        buttonEl.textContent = "Go Online";
      }
    }
  </script>

</body>
</html>
