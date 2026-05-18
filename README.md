<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <title>TROGUI Store</title>
  <style>
    body { font-family: Arial, sans-serif; background: #f9f9f9; margin:0; }
    header { background:#fff; padding:20px; text-align:center; }
    .producto { border:1px solid #ddd; padding:15px; margin:10px; background:#fff; }
    .precio { color:#e60000; font-size:20px; font-weight:bold; }
    .tachado { text-decoration: line-through; color:#777; }
    .temporizador { color:#ff6600; font-weight:bold; }
    .reseña { font-size:14px; margin-top:10px; }
    .carrito { position:fixed; top:20px; right:20px; background:#ff6600; color:#fff; padding:10px; border-radius:5px; }
    .editar { position:fixed; bottom:10px; right:10px; font-size:12px; color:#ccc; cursor:pointer; }
  </style>
</head>
<body>
  <header>
    <h1>TROGUI Store</h1>
    <p>🚚 Envío gratis a toda Colombia | Pago contra entrega</p>
    <a href="https://wa.link/lhneng"><img src="whatsapp_logo.png" alt="WhatsApp" width="40"></a>
    <a href="https://www.instagram.com/store_trog"><img src="instagram_logo.png" alt="Instagram" width="40"></a>
    <a href="https://www.tiktok.com/@trogui_store"><img src="tiktok_logo.png" alt="TikTok" width="40"></a>
  </header>

  <div class="carrito">🛒 Carrito</div>

  <section class="producto">
    <img src="quita_callos.jpg" alt="Quita Callos" width="200">
    <h2>Quita Callos Profesional</h2>
    <p class="tachado">$79,000</p>
    <p class="precio">$49,000</p>
    <p class="temporizador">⏳ Oferta termina en 2 horas</p>
    <p>⭐️⭐️⭐️⭐️☆ (120 reseñas)</p>
    <div class="reseña">Juan Camilo: "Muy bueno, me llegó rápido a Medellín"</div>
    <button>Comprar ahora</button>
  </section>

  <!-- Aquí se agregan más productos con la misma estructura -->

  <div class="editar">r</div>

  <script>
    // Temporizador dinámico
    function iniciarTemporizador(duracion, elemento) {
      let tiempo = duracion;
      setInterval(() => {
        if(tiempo > 0){
          tiempo--;
          elemento.textContent = "⏳ Oferta termina en " + tiempo + " min";
        }
      }, 60000);
    }
    const temporizador = document.querySelector('.temporizador');
    iniciarTemporizador(120, temporizador); // 120 minutos

    // Botón oculto con contraseña
    document.querySelector('.editar').addEventListener('click', () => {
      let pass = prompt("Ingrese contraseña:");
      if(pass === "4325"){
        alert("Modo edición activado");
        // Aquí se habilitan funciones de edición
      }
    });
  </script>
</body>
</html>
