<template>
  <v-card class="video" :tile="true">
    <v-img :src="getVideoUrl(video.video)">
      <v-card-text class="video-duration pa-0 pl-1 pr-1">{{
        video.duration
      }}</v-card-text>
    </v-img>
    <div class="pa-2 d-inline-flex video-footer">
      <v-avatar height="30" width="30" min-width="30" class="mr-2">
        <img :src="getAvatarUrl(video.userAvatar)" :alt="video.userName" />
      </v-avatar>
      <div class="video-main-info">
        <v-card-title class="pt-0 pl-0 subtitle-2"
          >{{ video.videoName }}
        </v-card-title>
        <v-card-subtitle class="pl-0 pb-2 caption"
          >{{ video.userName }} · {{ video.visualizations }} visualizations ·
          {{ video.uploadDate }}
        </v-card-subtitle>
      </div>
      <div class="video-dropdown">
        <v-menu left bottom>
          <template v-slot:activator="{ on }">
            <v-btn icon v-on="on">
              <v-icon>mdi-dots-vertical</v-icon>
            </v-btn>
          </template>

          <v-list>
            <v-list-item
              v-for="(option, index) in listOptions"
              :key="index"
              @click="() => {}"
            >
              <v-list-item-title>{{ option }}</v-list-item-title>
            </v-list-item>
          </v-list>
        </v-menu>
      </div>
    </div>
  </v-card>
</template>
<script>
  export default {
    name: "ytVideo",
    props: ["video"],
    data() {
      return {
        listOptions: ["Save to wath later", "Save to playlist", "Share"],
      };
    },
    methods: {
      getVideoUrl(fileName) {
        return require(`../assets/videos/miniatures/${fileName}.webp`);
      },
      getAvatarUrl(fileName) {
        return require(`../assets/videos/avatars/${fileName}.jpg`);
      },
    },
  };
</script>
<style lang="scss" scoped>
  .video {
    background-color: #272727;
    border-bottom: 1.5px solid lighten(#272727, 15%);
  }
  .video-container:last-child > .video {
    border-bottom-color: transparent;
  }
  .video-footer {
    width: 100%;
  }
  .video-duration {
    position: absolute !important;
    bottom: 5px;
    right: 5px;

    width: auto !important;
    height: auto !important;

    border-radius: 5px;
    background-color: black;
  }
  .video-dropdown {
    margin-left: auto;
  }
</style>
