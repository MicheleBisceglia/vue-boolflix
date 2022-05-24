<template>
  <div id="app">
    <body>
      <AppHeader @searchClick="search"/>
      <AppMain :movies="moviesList"/>
    </body>
  </div>
</template>

<script>
import AppMain from "./components/AppMain.vue";
import AppHeader from "./components/AppHeader.vue"
import axios from "axios";

export default {
  name: "App",
  components: {
    AppMain,
    AppHeader
  },
    data() {
        return {
        moviesList : [],
           }
  },
  methods: {
    search: function(searchKey) {
      axios.get("https://api.themoviedb.org/3/search/movie", {
          params: {
              api_key: "296d9c89fe4c7798ffeb669f21665ae2",
              query: searchKey
          }
      })
      .then((resp) => {
          this.moviesList = resp.data.results;
      })
    }
  }
};
</script>

<style lang="scss">
@import "./style/common.scss";
</style>
