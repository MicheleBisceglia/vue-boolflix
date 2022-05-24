<template>
  <div class="search_bar mt-3">
    <input class="m-3" type="text" v-model="searchKey">
    <button @click="$emit('searchClick', 'searchKey')" >Clicca qui
    </button>
  </div>
</template>

<script>
export default {
  name: "HelloWorld",
  data() {
    return {
      searchKey: "",
    }
  }
};
</script>

<style scoped lang="scss">
  .search_bar {
    height: 80px;
    width: 400px;
    margin: 0 auto;
  }
</style>
