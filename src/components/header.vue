<template>
  <header>
    <v-app-bar>
      <img
        class="logo-image"
        src="../assets/yt_logo_rgb_dark.png"
        alt="YouTube logo"
        srcset=""
      />
      <v-spacer></v-spacer>
      <v-btn icon>
        <v-icon>mdi-cast</v-icon>
      </v-btn>
      <v-btn icon>
        <v-icon>mdi-video</v-icon>
      </v-btn>
      <v-btn icon>
        <v-icon>mdi-magnify</v-icon>
      </v-btn>
      <v-btn icon>
        <v-avatar height="25" width="25">
          <img
            src="https://cdn.iconscout.com/icon/free/png-256/avatar-370-456322.png"
            alt="Xavi"
          />
        </v-avatar>
      </v-btn>
    </v-app-bar>
  </header>
</template>
<script>
  export default {
    name: "topBar",
  };
</script>
<style lang="scss">
  @import "../scss/variables.scss";
  .logo-image {
    height: 20px;
  }
</style>
