<template>
    <div>
      <header>
        <h1 class="title">Boolflix</h1>
      </header>
      <div class="search_bar mt-3">
    <input placeholder="Inizia la ricerca" class="m-3" type="text" v-model="searchKey">
    <button @click="$emit('searchClick', searchKey)" >Clicca qui
    </button>
  </div>
    </div>
    
</template>

<script>
export default {
  name: "AppHeader",
  data() {
    return {
      searchKey: "",
    }
  }
};
</script>

<style lang="scss" scoped>
@import "../style/common.scss";
.search_bar {
    display: flex;
    justify-content: center;
    align-items: center;
  }
</style>