<template>
  <v-app>
    <topbar></topbar>
    <v-content class="mb-12">
      <categories></categories>
      <videoList></videoList>
    </v-content>
    <footerMenu></footerMenu>
  </v-app>
</template>

<script>
  import topbar from "./components/header";
  import categories from "./components/categories";
  import videoList from "./components/video-list";
  import footerMenu from "./components/footer";

  export default {
    name: "App",

    components: {
      topbar,
      categories,
      videoList,
      footerMenu,
    },

    data: () => ({
      //
    }),
  };
</script>
