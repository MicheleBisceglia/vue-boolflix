<template>
    <div class="container">
      <div class="ms_container">
        <h2>{{ movie.title}}</h2>
        <h3>{{ movie.original_title }} </h3>
        <p>{{ movie.original_language }}</p>
        <div>{{ movie.vote_average }}</div>
      </div>
    </div>
</template>

<script>
   export default {
    name: "AppHeader",
   props: {
       movie: Object
   }
   }
</script>

<style lang="scss" scoped>
.ms_container {
    background-color: white;
    border: solid 1px black;
    text-align: center;
    min-height: 200px;
}
h2 {
    font-size: 80%;
    padding-top: 30%;
}
h3 {
    font-size: 80%}

</style>
