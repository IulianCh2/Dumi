
<html>
<head>
  <meta charset="UTF-8">
  <title>Esti pr</title>

  <style>
    body {
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      height: 100vh;
      background: pink;
      font-family: sans-serif;
      text-align: center;
      overflow: hidden;
    }

    h1 {
      color: red;
      margin-bottom: 40px;
    }

    #container {
      position: relative;
      width: 300px;
      height: 150px;
    }

    button {
      position: absolute;
      font-size: 20px;
      padding: 14px 28px;
      border: none;
      border-radius: 12px;
      cursor: pointer;
      transition: all 0.4s ease;
    }

    #yes {
      background-color: #ff4d6d;
      color: white;
      left: 30px;
      top: 40px;
      z-index: 1;
    }

    #no {
      background-color: white;
      color: #ff4d6d;
      border: 2px solid #ff4d6d;
      right: 30px;
      top: 40px;
      z-index: 2;
    }
  </style>
</head>

<body>

  <h1>Esti pr sora mea ❤️</h1>

  <div id="container">
    <button id="yes">YES</button>
    <button id="no">NO</button>
  </div>

  <script>
    let yesScale = 1;
    let noScale = 1;

    const yesBtn = document.getElementById("yes");
    const noBtn = document.getElementById("no");

    noBtn.onclick = function () {

      yesScale += 0.35;
      noScale -= 0.25;

      if (noScale < 0.15) noScale = 0.15;

      // Mărire YES
      yesBtn.style.transform = `scale(${yesScale})`;

      // Micșorare NO
      noBtn.style.transform = `scale(${noScale})`;

      // Mutare YES peste NO
      yesBtn.style.left = noBtn.offsetLeft + "px";
      yesBtn.style.top = noBtn.offsetTop + "px";
    };

    yesBtn.onclick = function () {
      document.body.innerHTML = `
        <div style="text-align:center;">
          <h1 style="color:red;font-size:50px;">
            Am știut eu! nu ma poti minti ❤️❤️
          </h1>
          <p style="font-size:26px;">
            
          </p>
        </div>
      `;
    };
  </script>

</body>
</html>
>
