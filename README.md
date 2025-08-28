<!DOCTYPE html>
<html>
<head>
  <title>Your IP</title>
</head>
<body>
  Your IP is <span id="ip">loading...</span>

  <script>
    fetch("https://api.ipify.org?format=json")
      .then(response => response.json())
      .then(data => {
        document.getElementById("ip").textContent = data.ip;
        document.title = data.ip;
      });
  </script>
</body>
</html>
