# byleco-max.github.io
data:text/html;charset=utf-8,
<!DOCTYPE html>
<html lang="pl">
<head>
<meta charset="UTF-8">
<title>Do Ślubu 💍</title>
<style>
body {
  margin:0;
  height:100vh;
  display:flex;
  flex-direction:column;
  justify-content:center;
  align-items:center;
  font-family: 'Segoe UI', sans-serif;
  background: linear-gradient(135deg, #fce4ec, #f8bbd0);
  color:#880e4f;
  text-align:center;
}
h1 {
  font-size:28px;
  max-width:90%;
}
#countdown {
  font-size:40px;
  margin-top:20px;
  background:white;
  padding:20px 30px;
  border-radius:20px;
  box-shadow:0 10px 25px rgba(0,0,0,0.1);
}
</style>
</head>
<body>

<h1>💍 Do Ślubu i wesela Krzysia i Patrycji pozostało:</h1>
<div id="countdown"></div>

<script>
const targetDate = new Date("2027-04-17T14:00:00").getTime();

setInterval(() => {
  const now = new Date().getTime();
  const distance = targetDate - now;

  if (distance < 0) {
    document.getElementById("countdown").innerHTML = "💖 To już dziś!";
    return;
  }

  const days = Math.floor(distance / (1000*60*60*24));
  const hours = Math.floor((distance / (1000*60*60)) % 24);
  const minutes = Math.floor((distance / (1000*60)) % 60);
  const seconds = Math.floor((distance / 1000) % 60);

  document.getElementById("countdown").innerHTML =
    days + " dni " + hours + " godz " + minutes + " min " + seconds + " sek";
}, 1000);
</script>

</body>
</html>

  
