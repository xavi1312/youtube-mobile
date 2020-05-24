<template>
  <v-app>
    <topbar></topbar>
    <v-content>
      <categories></categories>
      <videoList></videoList>
    </v-content>
  </v-app>
</template>

<script>
  import topbar from "./components/header";
  import categories from "./components/categories";
  import videoList from "./components/video-list";

  export default {
    name: "App",

    components: {
      topbar,
      categories,
      videoList,
    },

    data: () => ({
      //
    }),
  };
</script>
