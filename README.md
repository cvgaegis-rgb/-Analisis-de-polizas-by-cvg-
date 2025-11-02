<button onclick="mostrarAnalisis()" style="margin-top:20px; padding:14px 28px; background-color:#000; color:#fff; border:none; border-radius:6px; font-size:16px; cursor:pointer;">
  Analizar
</button>

<div id="resultado" style="margin-top:40px; max-width:600px; background:#fff; border:1px solid #eee; border-radius:8px; padding:20px; display:none;">
  <p id="textoAnalisis" style="font-size:16px; color:#333;"></p>
</div>

<script>
function mostrarAnalisis() {
  const boton = event.target;
  const resultado = document.getElementById("resultado");
  const texto = document.getElementById("textoAnalisis");

  boton.disabled = true;
  boton.innerText = "Analizando...";

  texto.innerText = "Leyendo cláusulas de cobertura, detectando exclusiones y condiciones relevantes...";
  resultado.style.display = "block";

  setTimeout(() => {
    texto.innerHTML = `
      <strong>Análisis preliminar:</strong><br><br>
      • Se detecta cobertura completa para daños materiales, pero sin extensión a terceros.<br>
      • Plazo de vigencia: 12 meses.<br>
      • Exclusión destacada: pérdida por mal uso o negligencia.<br><br>
      <em>Recomendación:</em> revisar condiciones de renovación automática y deducibles.
    `;
    boton.disabled = false;
    boton.innerText = "Analizar";
  }, 2500);
}
</script>
<body style="font-family: 'Helvetica Neue', sans-serif; background-color: #fafafa; color: #222; margin: 0; padding: 0;">

  <header style="text-align:center; padding: 60px 20px;">
    <h1 style="font-weight:300; font-size:42px; letter-spacing:-0.5px;">Análisis de Pólizas</h1>
    <p style="font-weight:200; font-size:18px; color:#555; max-width:600px; margin:10px auto;">
      Sube tu póliza y obtén una lectura inteligente de los puntos clave — rápido, claro y confidencial.
    </p>
  </header>

  <main style="display:flex; flex-direction:column; align-items:center; padding: 40px 20px;">
    <textarea placeholder="Pega aquí el texto de tu póliza..." 
      style="width:90%; max-width:600px; height:180px; padding:16px; border:1px solid #ccc; border-radius:8px; font-size:16px; background-color:#fff;">
    </textarea>

    <button style="margin-top:20px; padding:14px 28px; background-color:#000; color:#fff; border:none; border-radius:6px; font-size:16px; cursor:pointer;">
      Analizar
    </button>
  </main>

  <footer style="text-align:center; padding:50px 20px; font-size:14px; color:#666;">
    <p>¿Necesitás ayuda o asesoría personalizada?</p>
    <a href="https://wa.me/50378609460" 
       style="display:inline-block; margin-top:10px; padding:12px 24px; border:1px solid #000; border-radius:6px; text-decoration:none; color:#000; font-weight:500;">
      Contactar por WhatsApp
    </a>
  </footer>

</body>
