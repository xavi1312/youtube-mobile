<template>
  <v-container class="pa-0">
    <v-app-bar>
      <v-toolbar-title>Vídeos populares</v-toolbar-title>
    </v-app-bar>
    <v-row :no-gutters="true">
      <v-col
        v-for="(video, index) in videos"
        :key="index"
        cols="12"
        class="video-container"
      >
        <ytVideo :video="video"></ytVideo>
      </v-col>
    </v-row>
  </v-container>
</template>
<script>
  import ytVideo from "./video";
  export default {
    name: "videoList",
    components: {
      ytVideo,
    },
    data: function() {
      return {
        videos: [
          {
            video: "lady-gaga-rain-on-me",
            videoName:
              "Lady Gaga, Ariana Grande - Rain On Me (Official Music Video)",
            userName: "Lady Gaga",
            duration: "3:09",
            visualizations: "23M",
            uploadDate: "1 day ago",
            userAvatar: "lady-gaga",
          },
          {
            video: "vox-espana-caravana",
            videoName: "🔴 Directo | Caravana #FaseLibertad",
            userName: "Vox España",
            duration: "1:12:34",
            visualizations: "327K",
            uploadDate: "1 day ago",
            userAvatar: "vox",
          },
          {
            video: "morad-he-visto",
            videoName: "Morad - He Visto [VIDEO OFICIAL]",
            userName: "M.D.L.R",
            duration: "4:49",
            visualizations: "854K",
            uploadDate: "1 day ago",
            userAvatar: "m-d-l-r",
          },
          {
            video: "myke-towers-michael-myers",
            videoName: "Myke Towers - Michael Myers (Video Oficial)",
            userName: "Myke Towers",
            duration: "4:12",
            visualizations: "3M",
            uploadDate: "1 day ago",
            userAvatar: "myke-towers",
          },
          {
            video: "agust-d",
            videoName: "Agust D '대취타' MV",
            userName: "Big Hit Labels",
            duration: "4:29",
            visualizations: "37M",
            uploadDate: "2 days ago",
            userAvatar: "big-hit",
          },
          {
            video: "asi-le-hemos-cambiado-el-dia",
            videoName: "ASÍ LE HEMOS CAMBIADO EL DÍA A ESTE HOMBRE...😊",
            userName: "BROO'S TV",
            duration: "9:17",
            visualizations: "3M",
            uploadDate: "1 day ago",
            userAvatar: "broos-tv",
          },
        ],
      };
    },
  };
</script>
