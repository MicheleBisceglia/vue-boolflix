<template>
    <div class="container">
      <div class="ms_container">
        <h2>Titolo: {{ movie.title ? movie.title : movie.name }}</h2>
        <h3>Titolo Originale: {{ movie.original_title ? movie.original_title : movie.original_name}} </h3>
        <span>Lingua: </span>
        <img v-if="flags.includes(movie.original_language)" :src='"../assets/img/flag-" + movie.original_language +".png"' alt="lenguage">
        <span class="language bg-primary" v-else>{{ movie.original_language}}</span>
        <div>Valutazione: {{ movie.vote_average }}</div>
      </div>
    </div>
</template>

<script>
   export default {
    name: "AppCard",
   props: {
       movie: Object,
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
    padding-left: 15%;
    font-size: .8rem;
}
h2 {
    padding-top: 30%;
    font-size: .8rem;
}
h3 {
    font-size: .8rem
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
