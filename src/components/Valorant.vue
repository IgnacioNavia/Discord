<template>
  <div class="valorant-container">
    <!-- Fondo de la página -->
    <div class="background-image"></div>

    <!-- Contenido principal -->
    <div class="valorant-content">
      <h2>¿Quiénes somos en Valorant?</h2>
      <p>Valorant es un juego táctico en línea de disparos en primera persona, donde se enfrentan equipos de 5 contra 5.</p>
      <div class="fotos">
        <!-- Imágenes de miembros de la comunidad de Valorant -->
        <img v-for="n in 3" :key="n" :src="`/images/v${n}.png`" :alt="'Miembro ' + n" />
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Valorant',
};
</script>

<style scoped>
/* Contenedor principal que incluye el fondo */
.valorant-container {
  position: relative;
  width: 100%;
  height: 100vh; /* Asegúrate de que ocupe toda la ventana */
  overflow: hidden;
}

/* Fondo de la página */
.background-image {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-image: url('/images/Valorantbackground.png'); /* Ruta de la imagen */
  background-size: cover; /* Asegura que la imagen cubra todo el área */
  background-position: center; /* Centra la imagen */
  z-index: 1; /* Envía el fondo detrás del contenido */
}

/* Contenido principal */
.valorant-content {
  position: relative;
  z-index: 2; /* Trae el contenido al frente */
  padding: 10px;
  color: white; /* Asegura que el texto sea visible sobre el fondo */
  text-align: center;
}

h2 {
  font-size: 1.8em;
  margin-bottom: 15px;
}

p {
  font-size: 1.2em;
  margin-bottom: 20px;
}

.fotos {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
}

.fotos img {
  width: 250px;
  height: auto;
  margin: 10px;
  border-radius: 8px;
  box-shadow: 0 4px 23px rgba(0, 0, 0, 0.1);
}
</style>
