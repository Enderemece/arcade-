# arcade-

<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <title>Jugar DOOM</title>
  <script src="https://js-dos.com/6.22/current/js-dos.js"></script>
  <style>
    html, body {
      margin: 0;
      padding: 0;
      background-color: #000;
      height: 100%;
      display: flex;
      justify-content: center;
      align-items: center;
    }
    #dosbox {
      width: 100vw;
      height: 100vh;
    }
  </style>
</head>
<body>
  <div id="dosbox"></div>
  <script>
    Dos(document.getElementById("dosbox")).ready((fs, main) => {
      fs.extract("doom.zip").then(() => {
        main(["doom.exe"]);
      });
    });
  </script>
</body>
</html>
