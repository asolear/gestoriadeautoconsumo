---
hide:
  - footer
  - navigation
  - toc
---

![](https://github.com/asolear/assets/blob/master/imgs/cabecerag.png?raw=true)
#
</br>
</br>
</br>
<p style="font-size: 33px; color: white;font-family: 'Roboto Condensed', sans-serif;font-weight: bold;">Explorando un Futuro Sostenible: Descubriendo las Energías Renovables</p>

<p style="font-size: 22px; color: white;font-family: Roboto Condensed;">

La <strong>Gestoría de Autoconsumo</strong> es un espacio de información y asesoramiento con la perspectiva de un equipo de ingenieros e instaladores especializados, con vocación de apoyar a los consumidores (particulares, comercios y empresas) que deseen optar por una instalación de autoconsumo para abrir la puerta a una energía justa, limpia y accesible.

</p>
</br>
</br>
</br>
</br>
</br>
</br>
<div class="collage">
    <a href="mailto:m.bluth@example.com"><img src="https://github.com/asolear/assets/blob/master/imgs/satelite_con_placas.png?raw=true" alt="Imagen 2"></a></li>
    <a href="mailto:m.bluth@example.com"><img src="https://github.com/asolear/assets/blob/master/imgs/rvindustrial.jpg?raw=true" alt="Imagen 1">></a></li>
    <a href="mailto:m.bluth@example.com"><img src="https://github.com/asolear/assets/blob/master/imgs/casa.jpg?raw=true" alt="Imagen 1"></a></li>
    <a href="mailto:m.bluth@example.com"><img src="https://github.com/asolear/assets/blob/master/imgs/ev.jpg?raw=true" alt="Imagen 2"></a></li>


<a class="contact-button" href="https://api.whatsapp.com/send?phone=34600366211">
    <img src="https://github.com/asolear/assets/blob/master/imgs/whatsapp.png?raw=true" alt="WhatsApp">
</a>



</div>
</br>
</br>
</br>
</br>
</br>
</br>


<style> 
body { 
  background-image: url('https://github.com/asolear/assets/blob/master/imgs/fondo3.jpg?raw=true'); 
  background-repeat: no-repeat; 
  background-attachment: fixed; /* background-size: cover; */ 
  background-size: 100% 100%;
   } 

.collage {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    grid-gap: 10px;
}
.collage img {
    max-width: 100%;
    height: auto;
    transform: rotate(0deg);
    /* Rotar la imagen 15 grados */
    transition: transform 0.3s ease;
    /* Agregar una transición suave */
}
.collage img:hover {
    transform: scale(1.1) rotate(10deg);
    /* Escalar la imagen al 110% y volver a la rotación original en el hover */
}
/* Estilos para el enlace */
.contact-button {
    position: fixed;
    top: 100px;
    right: 50px;
}
/* Estilos adicionales (opcional) */
.contact-button img {
    width: 77px; /* Tamaño de la imagen */
    height: 77px; /* Tamaño de la imagen */
    border-radius: 50%; /* Hace que la imagen sea redonda */
}
</style> 

<script>
    const images = document.querySelectorAll('.collage img');
    images.forEach(img => {
        img.style.transform = `rotate(${getRandomRotation()}deg) scale(${getRandomScale()})`;
    });
    function getRandomRotation() {
        return Math.floor(Math.random() * 31) - 15; // Valores de rotación aleatorios entre -15 y 15 grados
    }
    function getRandomScale() {
       return 0.8 + Math.random() * 0.4; // Valores de escala aleatorios entre 0.8 y 1.2
    }
</script>






