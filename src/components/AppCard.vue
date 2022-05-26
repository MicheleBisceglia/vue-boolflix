<template>
      <div class="app_card">
        <div class="card_bg">
          <img
            v-if="movie.backdrop_path != null "
            :src='"https://image.tmdb.org/t/p/w342/" + movie.backdrop_path' alt="">
          <img v-else :src='"../assets/img/flag-" + movie.original_language + ".png"'>
          <h3 class="title_card">{{ movie.title ? movie.title : movie.name }}</h3>
        </div>
        <div class="card_info">
            <h4>Titolo: {{ movie.title ? movie.title : movie.name }}</h4>
            <h5>Titolo Originale: {{ movie.original_title ? movie.original_title : movie.original_name}} </h5>
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
.app_card {
    background-color: #141414;
    font-size: .8rem;
    position: relative;
}
.app_card:hover .card_info {
    display: inline-block;
}
.app_card:hover .card_bg {
    opacity: 40%;
    .title_card {
        display: none;
    }
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
.card_bg img{
    object-fit: cover;
    width: 100%;
    height: 180px;
}
.stars_color {
    color: #f8cf19;
}   
.title_card {
    position: absolute;
    bottom: 10px;
    left: 20px;
}
.null_image {
    width: 100%;
    height: 180px;
}
.card_info {
    display: none;
    position: absolute;
    bottom: 10px;
    left: 20px;
}
</style>
