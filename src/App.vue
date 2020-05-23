<template>
  <v-app>
    <topbar></topbar>
    <v-content> </v-content>
  </v-app>
</template>

<script>
  import topbar from "./components/header";

  export default {
    name: "App",

    components: {
      topbar,
    },

    data: () => ({
      //
    }),
  };
</script>
