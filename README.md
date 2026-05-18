<!-- Botones ocultos -->
<div class="editarR">r</div>
<div class="editarC">c</div>
<div class="editarE">e</div>

<style>
  .editarR, .editarC, .editarE {
    position: fixed;
    bottom: 10px;
    font-size: 12px;
    color: #ccc;
    cursor: pointer;
    opacity: 0.5;
  }
  .editarR { right: 10px; }
  .editarC { right: 30px; }
  .editarE { right: 50px; }
</style>

<script>
  function activarEdicion(tipo){
    let pass = prompt("Ingrese contraseña:");
    if(pass === "4325"){
      if(tipo === "R"){
        alert("Modo edición de productos activado");
        // Aquí habilitas edición de precios, imágenes, descripciones
      }
      if(tipo === "C"){
        alert("Acceso a datos de clientes activado");
        // Aquí habilitas acceso a pedidos y formularios
      }
      if(tipo === "E"){
        alert("Edición general de la página activada");
        // Aquí habilitas cambios de logo, banners, reseñas, audio, etc.
      }
    } else {
      alert("Contraseña incorrecta");
    }
  }

  document.querySelector('.editarR').addEventListener('click', ()=>activarEdicion("R"));
  document.querySelector('.editarC').addEventListener('click', ()=>activarEdicion("C"));
  document.querySelector('.editarE').addEventListener('click', ()=>activarEdicion("E"));
</script>
