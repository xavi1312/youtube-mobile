<template>
  <v-bottom-navigation class="footerMenu">
    <v-btn value="página-principal" class="caption font-regular">
      <span>Home</span>
      <v-icon class="mb-1">mdi-home</v-icon>
    </v-btn>

    <v-btn value="explorar" class="caption font-regular">
      <span>Explore</span>
      <v-icon class="mb-1">mdi-compass</v-icon>
    </v-btn>

    <v-btn value="suscripciones" class="caption font-regular">
      <span>Suscriptions</span>
      <v-badge content="2" color="error" overlap>
        <v-icon class="mb-1">mdi-youtube-subscription</v-icon>
      </v-badge>
    </v-btn>

    <v-btn value="notificaciones" class="caption font-regular">
      <span>Notifications</span>
      <v-icon class="mb-1">mdi-email</v-icon>
    </v-btn>
    <v-btn value="biblioteca" class="caption font-regular">
      <span>Library</span>
      <v-icon class="mb-1">mdi-play-box-multiple</v-icon>
    </v-btn>
  </v-bottom-navigation>
</template>
<script>
  export default {
    name: "footerMenu",
  };
</script>
<style lang="scss" scoped>
  .footerMenu {
    position: fixed;
    bottom: 0;
    border-top: 1.5px solid lighten(#272727, 15%);
  }
</style>
