<template>
  <v-container tag="nav" class="categories-container">
    <v-row>
      <v-col
        class="pa-2 column"
        cols="6"
        v-for="(category, index) in categories"
        :key="index"
      >
        <v-btn
          class="category-button pa-6"
          width="100%"
          v-bind:style="{
            'background-image': 'url(' + category.background + ')',
          }"
        >
          <v-icon left dense size="x-large" class="mr-2">{{
            category.icon
          }}</v-icon>
          {{ category.name }}
        </v-btn>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
  export default {
    name: "categories",
    data: function() {
      return {
        categories: [
          {
            name: "Tendencias",
            background:
              "https://cdn.pixabay.com/photo/2016/05/01/21/20/earth-1365995_960_720.jpg",
            icon: "mdi-fire",
          },
          {
            name: "Música",
            background:
              "https://cdn.pixabay.com/photo/2015/03/26/09/58/headphones-690685_960_720.jpg",
            icon: "mdi-music",
          },
          {
            name: "Videojuagos",
            background:
              "https://cdn.pixabay.com/photo/2017/08/10/04/54/playstation-2618338_960_720.jpg",
            icon: "mdi-youtube-gaming",
          },
          {
            name: "Noticias",
            background:
              "https://cdn.pixabay.com/photo/2012/12/20/10/12/article-71342_960_720.jpg",
            icon: "mdi-newspaper",
          },
          {
            name: "Películas",
            background:
              "https://cdn.pixabay.com/photo/2019/05/19/10/40/cinema-4213751_960_720.jpg",
            icon: "mdi-filmstrip-box",
          },
          {
            name: "Aprendizaje",
            background:
              "https://cdn.pixabay.com/photo/2016/06/29/08/50/pencil-1486278_960_720.jpg",
            icon: "mdi-lightbulb",
          },
        ],
      };
    },
  };
</script>
<style lang="scss" scoped>
  .category-button {
    text-align: left;
    justify-content: flex-start;
    background-size: cover;
    background-position: center center;
  }
</style>
