<template>
  <div id="app" class="app-container">
    <!-- Barra de navegación de juegos -->
    <div class="tabs">
      <button
        :class="{ active: activeTab === 'blackDesert' }"
        @click="activeTab = 'blackDesert'"
      >
        Black Desert
      </button>
      <button
        :class="{ active: activeTab === 'valorant' }"
        @click="activeTab = 'valorant'"
      >
        Valorant
      </button>
      <button
        :class="{ active: activeTab === 'throneAndLiberty' }"
        @click="activeTab = 'throneAndLiberty'"
      >
        Throne and Liberty
      </button>
      <button
        :class="{ active: activeTab === 'discord' }"
        @click="activeTab = 'discord'"
      >
        Discord
      </button>
    </div>

    <!-- Contenido dinámico -->
    <div
      v-if="activeTab === 'blackDesert'"
      class="game-content"
      :style="{ backgroundImage: 'url(/images/black-desert-background.png)' }"
    >
      <BlackDesert />
    </div>
    <div v-if="activeTab === 'valorant'">
      <Valorant />
    </div>
    <div v-if="activeTab === 'throneAndLiberty'">
      <ThroneAndLiberty />
    </div>
    <div v-if="activeTab === 'discord'">
      <Discord />
    </div>
  </div>
</template>

<script>
// Importa los componentes de los juegos y Discord
import BlackDesert from './components/BlackDesert.vue';
import Valorant from './components/Valorant.vue';
import ThroneAndLiberty from './components/ThroneAndLiberty.vue';
import Discord from './components/Discord.vue';

export default {
  components: {
    BlackDesert,
    Valorant,
    ThroneAndLiberty,
    Discord, // Agregar el componente de Discord
  },
  data() {
    return {
      activeTab: 'blackDesert', // Pestaña activa por defecto
    };
  },
};
</script>

<style scoped>
/* Estilos generales */
.app-container {
  background-color: #87CEEB; /* Fondo azul */
  font-family: Arial, sans-serif;
  padding: 20px;
  min-height: 100vh; /* Asegura que ocupe toda la pantalla */
  margin: 0; /* Elimina márgenes */
}

/* Barra de navegación */
.tabs {
  display: flex;
  margin-bottom: 20px;
}

.tabs button {
  background-color: #f0f0f0;
  padding: 10px;
  border: 1px solid #ccc;
  cursor: pointer;
  margin-right: 10px;
  transition: background-color 0.3s ease;
}

.tabs button.active {
  background-color: #007bff;
  color: white;
}

.tabs button:hover {
  background-color: #e0e0e0;
}

/* Contenido de las pestañas */
.game-content {
  background-size: cover; /* Asegura que la imagen cubra todo el espacio */
  background-position: center; /* Centra la imagen */
  padding: 0; /* Elimina el padding para usar toda la pantalla */
  margin: 0;
  height: 100vh; /* Hace que el contenedor ocupe toda la altura de la ventana */
  display: flex;
  align-items: center; /* Centra el contenido verticalmente */
  justify-content: center; /* Centra el contenido horizontalmente */
}
</style>
