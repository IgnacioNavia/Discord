<template>
  <div class="black-desert-container">
    <div class="background-image"></div>
    <div class="content">
      <h2>¿Quiénes somos en Black Desert?</h2>
      <p>
        Somo un gremio de chill de cojones del cual apoyamos a los aventureros nuevos con buen gs contacto a anakinignacio, zunheo.
      </p>
      <div class="fotos">
        <!-- Rutas de las fotos numeradas 1 a 10 en formato PNG -->
        <img v-for="n in 11" :key="n" :src="`/images/${n}.png`" :alt="'Miembro ' + n" />
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'BlackDesert',
};
</script>

<style scoped>
.black-desert-container {
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
  background-image: url('/images/blackDesertBackground.png'); /* Imagen de fondo */
  background-size: cover; /* Asegura que la imagen cubra todo el área */
  background-position: center; /* Centra la imagen */
  z-index: 1; /* Envía la imagen al fondo */
}

.content {
  position: relative;
  z-index: 2; /* Asegura que el contenido esté encima de la imagen */
  color: #ffd700; /* Texto en dorado amarillo */
  text-align: center;
  padding: 10px;
}

h2 {
  font-size: 2em;
  margin-bottom: 15px;
  color: #ffd700; /* Texto en dorado amarillo */
}

p {
  font-size: 1.2em;
  margin-bottom: 20px;
  color: #ffd700; /* Texto en dorado amarillo */
}

.fotos {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
}

.fotos img {
  width: 300px;
  height: auto;
  margin: 10px;
  border-radius: 8px;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
}
</style>
