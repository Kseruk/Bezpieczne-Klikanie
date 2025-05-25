# Bezpieczne-Klikanie
Edukacja Cyfrowa
<!DOCTYPE html>
<html lang="pl">
<head>
  <meta charset="UTF-8">
  <title>Wygrałeś nagrodę!</title>
  <style>
    body {
      font-family: 'Arial', sans-serif;
      background-color: #f0f0f0;
      text-align: center;
      padding: 50px;
    }

    #jumpscare, #edukacja {
      display: none;
    }

    #jumpscare {
      position: fixed;
      top: 0; left: 0;
      width: 100vw;
      height: 100vh;
      background-color: black;
      display: flex;
      align-items: center;
      justify-content: center;
      z-index: 1000;
    }

    #jumpscare img {
      width: 100vw;
      height: 100vh;
      object-fit: cover;
    }

    #edukacja {
      margin-top: 40px;
      background-color: #fff;
      padding: 30px;
      border-radius: 12px;
      box-shadow: 0 0 10px rgba(0,0,0,0.2);
    }

    .btn {
      background-color: #007bff;
      color: white;
      padding: 15px 30px;
      font-size: 18px;
      border: none;
      border-radius: 8px;
      cursor: pointer;
      transition: background-color 0.3s;
    }

    .btn:hover {
      background-color: #0056b3;
    }

    ul {
      text-align: left;
      max-width: 600px;
      margin: 20px auto;
    }
  </style>
</head>
<body>

  <h1>🎁 Gratulacje! Wygrałeś iPhone'a 15!</h1>
  <p>Aby odebrać nagrodę, kliknij poniższy przycisk:</p>
  <button class="btn" onclick="uruchomJumpscare()">Odbierz nagrodę</button>

  <div id="jumpscare">
    <img src="https://i.imgur.com/6KJ1vPp.jpg" alt="Straszak!">
    <audio id="audio" src="https://www.myinstants.com/media/sounds/movie_1.mp3" autoplay></audio>
  </div>

  <div id="edukacja">
    <h2>⚠️ Uważaj na podejrzane linki!</h2>
    <p>To był test edukacyjny pokazujący, dlaczego nie warto klikać w podejrzane wiadomości i strony.</p>
    <h3>Jak się chronić?</h3>
    <ul>
      <li>Nie klikaj w linki z nieznanych źródeł</li>
      <li>Nie podawaj danych osobowych w podejrzanych formularzach</li>
      <li>Sprawdzaj adres strony – czy to naprawdę oficjalna domena?</li>
      <li>Zgłaszaj podejrzane wiadomości nauczycielowi lub rodzicowi</li>
    </ul>
    <p><strong>Pamiętaj:</strong> Prawdziwe nagrody nie przychodzą bez powodu!</p>
  </div>

  <script>
    function uruchomJumpscare() {
      document.getElementById('jumpscare').style.display = 'flex';
      document.getElementById('audio').play();

      setTimeout(() => {
        document.getElementById('jumpscare').style.display = 'none';
        document.getElementById('edukacja').style.display = 'block';
      }, 3000); // po 3 sekundach pokazuje część edukacyjną
    }
  </script>

</body>
</html>
