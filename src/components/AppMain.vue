<template>
    <main>
        <!-- Main -->
        <div class="ms_container">
            <div>   
                <h1 v-if="movies.length != 0">Film</h1>
            <!-- Jumbotron/pagina iniziale ( se il campo di ricerca è ancora vuoto)-->
                <AppJumbotron v-else class="AppJumbotron"/>

            <!-- Film section -->          
                <section v-if="movies.length != 0" class="section my_scroll">
                    <div class="container">
                        <div class="row row-cols-3 row-cols-md-4 row-cols-lg-6 ">
                            <AppCard v-for="item in movies" :key="item.index" :movie="item" class="g-1"/>
                        </div>
                    </div>
                </section>
            <!-- /Film section -->
            </div>
        </div>
            <!-- Serie TV section -->
        <div class="ms_container">
            <h1 class="pt-5" v-if="movies.length != 0" >SerieTv</h1>
            <h1 v-else></h1>
            <div class="container">
                <div class="row row-cols-3 row-cols-md-4 row-cols-lg-5">
                    <AppCard v-for="item in series" :key="item.index" :movie="item" class="gy-3 gx-1"/>
                </div>
            </div>
        </div>
            <!-- /Serie TV section -->
    </main>
    <!-- /main -->
</template>

<script>
import AppCard from './AppCard.vue'
import AppJumbotron from './AppJumbotron.vue'

export default {
  name: "AppMain",
    components: {
       AppCard,
       AppJumbotron
       },
    props: {
        movies: Array,
        series: Array,
    },
};
</script>

<style lang="scss" scoped>
@import "../style/common.scss";
@import "../style/scrollBar.scss";
@import "../style/query.scss";
.ms_container {
    width: 85%;
    margin: 0 auto;
}
.section {
    width: 85%;
    height: 400px;
    overflow-y: auto ;
    overflow-x: hidden ;
    margin: 0 auto;
}
</style>