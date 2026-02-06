
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Be My Valentine 💖</title>
  <style>
    body {
      background: linear-gradient(135deg, #ff9a9e, #fad0c4);
      font-family: 'Comic Sans MS', cursive, sans-serif;
      text-align: center;
      height: 100vh;
      display: flex;
      justify-content: center;
      align-items: center;
    }

    .container {
      background: white;
      padding: 40px;
      border-radius: 20px;
      box-shadow: 0 10px 25px rgba(0,0,0,0.2);
      max-width: 420px;
    }

    img {
      width: 180px;
      margin-bottom: 20px;
    }

    h1 {
      margin-bottom: 15px;
      color: #ff4d6d;
    }

    p {
      font-size: 18px;
      margin-bottom: 25px;
    }

    button {
      font-size: 18px;
      padding: 12px 25px;
      border-radius: 12px;
      border: none;
      cursor: pointer;
      transition: all 0.3s ease;
      margin: 10px;
    }

    #yesBtn {
      background-color: #ff4d6d;
      color: white;
    }

    #noBtn {
      background-color: #ccc;
      color: black;
    }
  </style>
</head>
<body>

  <div class="container">
    <!-- CUTE GIF -->
    <img src="cutie.gif" alt="Cute Cat">

    <h1>💘 Will you be my Valentine? 💘</h1>
    <p id="message">Please say yes 🥺</p>

    <button id="yesBtn" onclick="yesClicked()">Yes 💖</button>
    <button id="noBtn" onclick="noClicked()">No 🙄</button>
  </div>

  <script>
    let noCount = 0;
    let yesSize = 18;

    const messages = [
      "Are you sure? 🥺",
      "Like… REALLY sure? 😭",
      "Come onnnn 😭💔",
      "This is getting painful 😢",
      "Just say yes already 😩❤️",
      "I will cry fr 😭😭"
    ];

    function noClicked() {
      noCount++;

      const msgIndex = Math.min(noCount - 1, messages.length - 1);
      document.getElementById("message").innerText = messages[msgIndex];

      yesSize += 8;
      const yesBtn = document.getElementById("yesBtn");
      yesBtn.style.fontSize = yesSize + "px";
      yesBtn.style.padding =
        (12 + noCount * 2) + "px " + (25 + noCount * 4) + "px";
    }

    function yesClicked() {
      document.querySelector(".container").innerHTML = `
        <img src="cutie.gif" alt="Cute Cat" style="width:200px; margin-bottom:20px;">
        <h1>YAYYYYY 💕💍</h1>
        <p>You just made me the happiest person ever 😍</p>
        <p>Happy Valentine’s Day 💖</p>
      `;
    }
  </script>

</body>
</html>
