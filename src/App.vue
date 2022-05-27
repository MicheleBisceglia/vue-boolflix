<template>
  <div id="app">
    <body>
      <!--catturo dati al click (searchkey)-->
      <AppHeader @searchClick="search"/>
      
      <!--passo gli array in Appmain-->
      <AppMain :movies="moviesList" :series="seriesList"/>

      <AppFooter />
    </body>
  </div>
</template>

<script>
import AppMain from "./components/AppMain.vue";
import AppHeader from "./components/AppHeader.vue"
import AppFooter from "./components/AppFooter.vue"
import axios from "axios";

export default {
  name: "App",
  components: {
    AppMain,
    AppHeader,
    AppFooter
  },
    data() {
      //Creo un array per i film e uno per le serie
      return {
        moviesList : [],
        seriesList : [],
      }
  },
  methods: {
    //Funzione di ricerca nella api
    search: function(searchKey) {
    //lettura api film
      axios.get("https://api.themoviedb.org/3/search/movie", {
        params: {
          api_key: "296d9c89fe4c7798ffeb669f21665ae2",
          query: searchKey
        }
    })
    //invio i dati all'array movieslist
      .then((resp) => {
        this.moviesList = resp.data.results;
    })

    //lettura api Serie TV
    axios.get("https://api.themoviedb.org/3/search/tv", {
      params: {
        api_key: "296d9c89fe4c7798ffeb669f21665ae2",
          query: searchKey
          },
      })
      //invio i dati all'array serieslist
      .then((resp) => {
        this.seriesList = resp.data.results;
      })
    }
  }
};
</script>

<style lang="scss">
@import "./style/common.scss";
</style>