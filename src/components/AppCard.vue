<template>
    <div class="container">
      <div class="ms_container">
        <h2>Titolo: {{ movie.title}}</h2>
        <h3>Titolo Originale: {{ movie.original_title }} </h3>
        <div>Valutazione: {{ movie.vote_average }}</div>
        <span>Lingua: </span>
        <img v-if="flags.includes(movie.original_language)" :src='"../assets/img/flag-" + movie.original_language +".png"' alt="lenguage">
        <span class="language bg-primary" v-else>{{ movie.original_language}}</span>
      </div>
    </div>
</template>

<script>
   export default {
    name: "AppHeader",
   props: {
       movie: Object
   },
   data() {
       return {
           flags: ["it", "en", "fr", "de"],
       }
   },
   }
</script>

<style lang="scss" scoped>
.ms_container {
    background-color: white;
    border: solid 1px black;
    text-align: left;
    min-height: 200px;
    padding-left: 20%;
}
h2 {
    font-size: 80%;
    padding-top: 30%;
}
h3 {
    font-size: 80%
    }
img {
    height: 15px;
    width: 15px;
    border-radius: 50%;
}
.language {
    color: white;
    border-radius: 100%;
    height: 15px;
    width: 15px;
    text-transform: uppercase;
    font-size: 70%;
}
    

</style>
