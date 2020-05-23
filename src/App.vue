<template>
  <div id="app">
    <topBar></topBar>
  </div>
</template>

<script>
  import topBar from "./components/header.vue";

  export default {
    name: "App",
    components: {
      topBar,
    },
  };
</script>

<style lang="scss">
  * {
    box-sizing: border-box;
  }
  body {
    margin: 0;
  }
</style>
