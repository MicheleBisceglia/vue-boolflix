<template>
    <div>
        <AppSearch @searchClick="search"/>
        <div class="container">
            <div class="row row-cols-3 row-cols-md-4 row-cols-lg-6 gy-4">
                <AppCard class="appCard"/>
                <AppCard class="appCard"/>
                <AppCard class="appCard"/>
                <AppCard class="appCard"/>
                <AppCard class="appCard"/>
                <AppCard class="appCard"/>
                <AppCard class="appCard"/>
                <AppCard class="appCard"/>
                <AppCard class="appCard"/>
                <AppCard class="appCard"/>
                <AppCard class="appCard"/>
                <AppCard class="appCard"/>
            </div>
        </div>
    </div>
</template>

<script>
import AppSearch from './AppSearch.vue';
import AppCard from './AppCard.vue'
export default {
  name: "AppMain",
    components: {
       AppSearch ,
       AppCard
       },
    methods: {
    search (searchKey) {
      console.log('search', searchKey);
    }
  }
};
</script>

<style lang="scss" scoped>
@import "../style/common.scss";
</style>