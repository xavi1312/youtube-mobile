<template>
  <header>
    <img
      class="logo-image"
      src="../assets/yt_logo_rgb_dark.png"
      alt="YouTube logo"
      srcset=""
    />
    <div class="icons">
      <font-awesome-icon :icon="['fab', 'chromecast']" />
      <font-awesome-icon icon="video" />
      <font-awesome-icon icon="search" />
      <img
        class="user-profile-image"
        src="https://yt3.ggpht.com/-7GJNRWiWh_c/AAAAAAAAAAI/AAAAAAAAAAA/Ef1w4FgIQ_0/s108-c-k-c0x00ffffff-no-rj-mo/photo.jpg"
        alt="User profile image"
      />
    </div>
  </header>
</template>
<script>
  export default {
    name: "topBar",
  };
</script>
<style lang="scss">
  @import "../scss/variables.scss";
  header {
    display: flex;
    padding: 1em;
    background-color: $light-black;
  }
  .logo-image {
    height: 20px;
  }
  .icons {
    display: flex;
    align-items: center;
    margin-left: auto;
    & > * {
      font-size: 1.25em;
      margin-left: 30px;
      color: #fff;
    }
  }
  .user-profile-image {
    border-radius: 50%;
    height: 25px;
  }
</style>
