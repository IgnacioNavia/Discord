<template>
  <div class="discord">
    <!-- Enlace al servidor de Discord -->
    <h2>Únete a nuestro Discord</h2>
    <p>
      ¡Conéctate con nuestra comunidad en Discord! Haz clic en el enlace para unirte: 
      <a href="https://discord.gg/G5UeY9aKp9" target="_blank">https://discord.gg/G5UeY9aKp9</a>
    </p>

    <!-- Listado de miembros importantes -->
    <div class="miembros">
      <h3>Venga Lulos</h3>
      <div class="miembro" v-for="(miembro, index) in miembros" :key="index">
        <img :src="miembro.foto" :alt="miembro.nombre" />
        <h4>{{ miembro.nombre }}</h4>
        <p>{{ miembro.descripcion }}</p>
        <a v-if="miembro.link" :href="miembro.link" target="_blank">Ver en Twitch</a>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Discord",
  data() {
    return {
      miembros: [
        {
          foto: "/images/Miembro1.png",
          nombre: "El Malaya",
          descripcion: "Coordinador principal y estratega del grupo.",
          link: "https://www.twitch.tv/anakindo01", // Enlace de Twitch
        },
        {
          foto: "/images/Miembro3.png",
          nombre: "Cornalita Rabiosa",
          descripcion: "Creadora de contenido visual y multimedia.",
          link: "https://www.twitch.tv/yasua_frustrada", // Enlace de Twitch
        },
        {
          foto: "/images/Miembro2.png",
          nombre: "El Lolicon",
          descripcion: "Encargado de mantener el orden en la comunidad.",
          link: "https://www.twitch.tv/nekoshiki89", // Enlace de Twitch
        },
        {
          foto: "/images/Miembro4.png",
          nombre: "El LuloToxico",
          descripcion: "Soporte técnico y experto en configuraciones.",
          link: "https://www.twitch.tv/gbozn", // Enlace de Twitch
        },
      ],
    };
  },
};
</script>

<style scoped>
.discord {
  padding: 20px;
  text-align: center;
  background-color: #f0f0f0;
  border-radius: 10px;
  max-width: 800px;
  margin: auto;
}

h2 {
  font-size: 2em;
  margin-bottom: 10px;
}

p {
  font-size: 1.2em;
  margin-bottom: 20px;
}

a {
  color: #007bff;
  text-decoration: none;
}

a:hover {
  text-decoration: underline;
}

.miembros {
  margin-top: 20px;
}

.miembro {
  display: inline-block;
  text-align: center;
  margin: 10px;
}

.miembro img {
  width: 250px;
  height: 250px;
  object-fit: cover;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
  margin-bottom: 10px;
}

.miembro h4 {
  font-size: 1.5em;
  margin-bottom: 5px;
}

.miembro p {
  font-size: 1em;
  color: #666;
}

.miembro a {
  display: block;
  margin-top: 10px;
  font-size: 1em;
  color: #007bff;
  text-decoration: none;
}

.miembro a:hover {
  text-decoration: underline;
}
</style>
