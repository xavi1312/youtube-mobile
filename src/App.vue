<template>
  <v-app>
    <topbar></topbar>
    <v-content>
      <categories></categories>
    </v-content>
  </v-app>
</template>

<script>
  import topbar from "./components/header";
  import categories from "./components/categories";

  export default {
    name: "App",

    components: {
      topbar,
      categories,
    },

    data: () => ({
      //
    }),
  };
</script>
