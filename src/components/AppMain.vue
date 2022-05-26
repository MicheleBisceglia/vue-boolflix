<template>
    <div>
        <div class="ms_container">
            <h1>Film</h1>
            <div class="container">
                <div class="row row-cols-3 row-cols-md-4 row-cols-lg-4 ">
                    <AppCard v-for="item in movies" :key="item.index" :movie="item" class="gy-3 gx-1"/>
                </div>
            </div>
        </div>
        <div class="ms_container">
            <h1>SerieTv</h1>
            <div class="container">
                <div class="row row-cols-2 row-cols-md-2 row-cols-lg-2">
                    <AppCard v-for="item in series" :key="item.index" :movie="item" class="gy-3 gx-1"/>
                </div>
            </div>
        </div>
    </div>
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
</style>