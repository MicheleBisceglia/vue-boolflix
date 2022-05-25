<template>
    <div class="container">
      <div class="ms_container">
        <img class="card_bg pt-3" 
          v-if="movie.backdrop_path != null "
          :src='"https://image.tmdb.org/t/p/w200/" + movie.backdrop_path' alt="">
        <img class="card_bg pt-3"
          v-else src="https://image.tmdb.org/t/p/w342/wwemzKWzjKYJFfCeiB57q3r4Bcm.png " alt="netflix">
        <h2>Titolo: {{ movie.title ? movie.title : movie.name }}</h2>
        <h3>Titolo Originale: {{ movie.original_title ? movie.original_title : movie.original_name}} </h3>
        <span>Lingua: </span>
        <img class="flag_circle" 
          v-if="flags.includes(movie.original_language)" :src='"../assets/img/flag-" + movie.original_language +".png"' alt="lenguage">
        <span class="language bg-primary" 
          v-else>{{ movie.original_language}}</span>
        <div>
          <i v-for="n in 5" :key="n" class="fa-star stars_color" :class="n <= stars ? 'fas' : 'd-none '"></i>
        </div>
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
   computed: {
       stars() {
           return Math.ceil(this.movie.vote_average / 2);
       }
       
   }
   }
</script>

<style lang="scss" scoped>
@import '~@fortawesome/fontawesome-free/css/all.min.css';
.ms_container {
    background-color: white;
    border: solid 1px black;
    text-align: center;
    min-height: 260px;
    font-size: .8rem;
}
h2 {
    padding-top: 10%;
    font-size: .8rem;
}
h3 {
    font-size: .8rem
    }
.flag_circle {
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
.card_bg {
    object-fit: contain;
    width: 90%;
    height: 100px;
}
.stars_color {
    color: #f8cf19;
}    

</style>
