<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Análisis de Pólizas - Demo</title>
  <style>
    body { font-family: Arial, sans-serif; background:#f8f9fa; margin:40px; }
    h1 { text-align:center; color:#333; }
    textarea { width:100%; height:200px; margin-top:10px; }
    button { background:#007bff; color:white; border:none; padding:10px 20px; border-radius:8px; cursor:pointer; }
    button:hover { background:#0056b3; }
    .resultado { margin-top:20px; background:white; padding:20px; border-radius:8px; box-shadow:0 2px 4px rgba(0,0,0,0.1); }
  </style>
</head>
<body>
  <h1>Análisis de Pólizas</h1>
  <p>Pegá aquí el texto de tu póliza para obtener un resumen del contenido y los riesgos clave.</p>
  <textarea id="textoPoliza" placeholder="Pegá tu póliza aquí..."></textarea><br>
  <button onclick="analizar()">Analizar</button>
  <div id="resultado" class="resultado"></div>

  <script>
    function analizar() {
      const texto = document.getElementById('textoPoliza').value;
      if (!texto.trim()) {
        alert('Pegá primero el texto de la póliza');
        return;
      }
      document.getElementById('resultado').innerHTML = `
        <b>Procesando...</b><br>Esto es una demo. 
        El análisis real se hace con inteligencia artificial (prompt oculto).
      `;
    }
  </script>
</body>
</html>
