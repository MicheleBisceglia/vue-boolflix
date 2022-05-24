<template>
    <div>
        <AppHeader />
        <div class="container">
            <div class="row row-cols-3 row-cols-md-4 row-cols-lg-6 gy-5">
                <AppCard v-for="item in movies" :key="item.index" :movie="item" class="appCard"/>
            </div>
        </div>
    </div>
</template>

<script>
import AppCard from './AppCard.vue'

export default {
  name: "AppMain",
    components: {
       AppCard
       },
    props: {
        movies: Array
    },
};
</script>

<style lang="scss" scoped>
@import "../style/common.scss";
</style>