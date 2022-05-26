<template>
    <main>
        <div class="ms_container">
            <div>   
                <h1 v-if="movies.length != 0">Film</h1>
                <div v-else class="jumbotron">
                  <div>
                    <h1>Demon Slayer</h1>
                    <p>It is the Taisho Period in Japan. Tanjiro, a kindhearted boy who sells charcoal for a living, finds his family slaughtered by a demon. To make matters worse, his younger sister Nezuko, the sole survivor, has been transformed into a demon herself. Though devastated by this grim reality, Tanjiro resolves to become a “demon slayer” so that he can turn his sister back into a human, and kill the demon that massacred his family</p>
                    <button>
                        <i class="fas fa-play"></i>
                        Riproduci</button>
                    <button class="bg-dark text-white">
                        <i class="fa-solid fa-circle-info"></i>
                        Altre info</button>
                  </div>
                </div>                  
            </div>
            <section class="section_1 my_scroll">
              <div class="container">
                <div class="row row-cols-3 row-cols-md-4 row-cols-lg-6 ">
                    <AppCard v-for="item in movies" :key="item.index" :movie="item" class="g-1"/>
                </div>
              </div>
            </section>
        </div>
        <div class="ms_container">
            <h1 v-if="movies.length != 0" >SerieTv</h1>
            <h1 v-else></h1>
            <div class="container">
                <div class="row row-cols-3 row-cols-md-4 row-cols-lg-5">
                    <AppCard v-for="item in series" :key="item.index" :movie="item" class="gy-3 gx-1"/>
                </div>
            </div>
        </div>
    </main>
</template>

<script>
import AppCard from './AppCard.vue'

export default {
  name: "AppMain",
    components: {
       AppCard,
       },
    props: {
        movies: Array,
        series: Array,
    },
};
</script>

<style lang="scss" scoped>
@import "../style/common.scss";
.ms_container {
    width: 85%;
    margin: 0 auto;
}
.section_1 {
    width: 85%;
    height: 400px;
    overflow-y: auto ;
    overflow-x: hidden ;
    margin: 0 auto;
}
.jumbotron {
    background-image: url(https://wallpaperaccess.com/full/7807768.png);
    width: 100%;
    height: 500px;
    background-size: cover;
    background-position: bottom;
    padding-left: 30px;
    h1{
        font-size: 5rem;
        padding-top: 150px;
    }
    p {
        max-width: 50%;
    }
    button {
        margin-left: 2rem;
        background-color: white;
        color: black;
        border-radius: 5px;
        border-style: none;
        width: 7rem;

    }
}
</style>