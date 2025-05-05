<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <title>Spam de Hola</title>
</head>
<body>
  <h1>Haz clic para empezar la fiesta</h1>
  <button onclick="abrirVentanas()">¡Empezar!</button>

  <script>
    function abrirVentanas() {
      for (let i = 0; i < 100000; i++) {
        const win = window.open("", "_blank");
        if (win) {
          win.document.write("<h1>Idiota</h1><p>Hola " + (i + 1) + "</p>");
          win.document.title = "Hola " + (i + 1);
        } else {
          alert("El navegador bloqueó las ventanas emergentes.");
          break;
        }
      }
    }
  </script>
</body>
</html>
