

  

  
<!DOCTYPE html>
<html lang="pl">
<head>
  <meta charset="UTF-8">
  <title>Odliczanie do ślubu</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background: linear-gradient(to right, #f8e1e7, #e1f0f8);
      text-align: center;
      padding: 50px;
      color: #333;
    }

    h1 {
      font-size: 2.2em;
      margin-bottom: 30px;
    }

    #countdown {
      font-size: 2em;
      font-weight: bold;
      background: white;
      display: inline-block;
      padding: 20px 40px;
      border-radius: 15px;
      box-shadow: 0 0 15px rgba(0,0,0,0.1);
    }
  </style>
</head>
<body>

  <h1>Do ślubu i wesela Patrycji i Krzysztofa pozostało:</h1>
  <div id="countdown">Ładowanie...</div>

  <script>
    const weddingDate = new Date("April 17, 2027 14:00:00").getTime();

    const countdownFunction = setInterval(function() {
      const now = new Date().getTime();
      const distance = weddingDate - now;

      if (distance < 0) {
        clearInterval(countdownFunction);
        document.getElementById("countdown").innerHTML = "To już dziś! ❤️";
        return;
      }

      const days = Math.floor(distance / (1000 * 60 * 60 * 24));
      const hours = Math.floor((distance / (1000 * 60 * 60)) % 24);
      const minutes = Math.floor((distance / (1000 * 60)) % 60);
      const seconds = Math.floor((distance / 1000) % 60);

      document.getElementById("countdown").innerHTML =
        days + " dni " +
        hours + " godz. " +
        minutes + " min " +
        seconds + " sek";
    }, 1000);
  </script>

</body>
</html>
