<template> 
  <div class="throne-and-liberty-container">
    <div class="background-image"></div>
    <div class="content">
      <h2>¿Quiénes somos en Throne and Liberty?</h2>
      <p>
        Throne and liberty es un juego MMORPG donde te puedes desarrollar con diversos roles y explorar un amplio mundo abierto, mazmorras y abisales que puedes adentrarte con tus amigos o un gremio. 
        Contamos con aventureros donde cuentan sus historias en este universo Zunheo. Aun falta historias que mencionar, asi que sigue con nosotros para mas novedades.
      </p>
      <div class="fotos">
        <!-- Imágenes de miembros de la comunidad de Throne and Liberty -->
        <img v-for="n in 3" :key="n" :src="`/images/tl${n}.png`" :alt="'Miembro ' + n" />
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'ThroneAndLiberty',
};
</script>

<style scoped>
.throne-and-liberty-container {
  position: relative;
  width: 100%;
  height: 100vh; /* Ocupa toda la pantalla */
  overflow: hidden; /* Evita que el contenido adicional desborde */
}

.background-image {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-image: url('/images/throneAndLibertyBackground.png'); /* Imagen de fondo */
  background-size: cover; /* Asegura que la imagen cubra todo el área */
  background-position: center; /* Centra la imagen */
  z-index: 1; /* Envía la imagen al fondo */
}

.content {
  position: relative;
  z-index: 2; /* Asegura que el contenido esté encima de la imagen */
  color: white; /* Cambiar texto a color blanco */
  text-align: center; /* Centrar texto horizontalmente */
  padding: 10px;
}

h2 {
  font-size: 2em;
  margin-bottom: 15px;
  color: white; /* Cambiar texto a blanco */
}

p {
  font-size: 1.2em;
  margin-bottom: 20px;
  color: white; /* Cambiar texto a blanco */
}

.fotos {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
}

.fotos img {
  width: 400px; /* Tamaño aumentado para fotos más grandes */
  height: auto;
  margin: 15px;
  border-radius: 12px;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
}
</style>
