<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Happy Birthday Javeria!</title>
  <style>
    body {
      margin: 0;
      font-family: 'Georgia', serif;
      background: linear-gradient(135deg, #fff6f0 0%, #fdf0ff 100%);
      background-image:
        radial-gradient(circle at 20% 20%, #ffd1dc 2%, transparent 3%),
        radial-gradient(circle at 80% 30%, #c1e1ff 2%, transparent 3%),
        radial-gradient(circle at 50% 80%, #e0ffe1 2%, transparent 3%);
      background-size: 150px 150px;
      background-repeat: repeat;
      color: #4b3b2a;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      transition: all 0.5s ease;
    }

    .page {
      display: none;
      text-align: center;
      max-width: 600px;
      padding: 30px;
      box-shadow: 0 10px 30px rgba(0,0,0,0.1);
      border-radius: 20px;
      background: rgba(255, 248, 240, 0.95);
      border: 2px solid #d4c2a9;
    }

    .active {
      display: block;
    }

    h1 {
      font-size: 2.5rem;
      margin-bottom: 10px;
    }

    .cake {
      margin: 20px 0;
      font-size: 6rem;
    }

    button {
      padding: 10px 20px;
      font-size: 1rem;
      background-color: #7f675b;
      color: white;
      border: none;
      border-radius: 10px;
      cursor: pointer;
      transition: background-color 0.3s ease;
    }

    button:hover {
      background-color: #5f4e45;
    }

    input {
      padding: 10px;
      font-size: 1rem;
      width: 80%;
      margin-top: 15px;
      border: 1px solid #c8b6a6;
      border-radius: 8px;
    }

    .message {
      margin-top: 20px;
      font-style: italic;
      color: #6e5849;
    }

    .final-wish {
      margin-top: 30px;
      font-size: 1rem;
      color: #3f3224;
      border-top: 1px dashed #b6a28b;
      padding-top: 20px;
    }
  </style>
</head>
<body>
  <audio autoplay loop>
    <source src="https://www.fesliyanstudios.com/play-mp3/387" type="audio/mpeg">
    Your browser does not support the audio element.
  </audio>

  <div id="page1" class="page active">
    <h1>Happy 19th Birthday, Javeria!</h1>
    <div class="cake">🎂</div>
    <p>Wishing you a day as lovely and timeless as you are.</p>
    <button onclick="goToPage2()">Make a Wish</button>
  </div>

  <div id="page2" class="page">
    <h1>Make a Wish ✨</h1>
    <input type="text" id="wishInput" placeholder="Type your wish here..." />
    <br />
    <button onclick="submitWish()">Take Wish</button>
    <div id="notedMessage" class="message"></div>
    <div class="final-wish">
      <strong>From me to you:</strong><br/>
      Whatever you may ask, may you receive. Whatever you may seek, may you find.  
      Whatever you wish, may it be fulfilled—on your birthday and always.  
      <br/>💖 Happy Birthday!
    </div>
  </div>

  <script>
    function goToPage2() {
      document.getElementById('page1').classList.remove('active');
      document.getElementById('page2').classList.add('active');
    }

    function submitWish() {
      const wish = document.getElementById('wishInput').value.trim();
      const message = document.getElementById('notedMessage');
      if (wish) {
        message.textContent = `"${wish}" – Your wish is noted, Javeria! 🎈`;
      } else {
        message.textContent = "Please type a wish before submitting.";
      }
    }
  </script>
</body>
</html>
