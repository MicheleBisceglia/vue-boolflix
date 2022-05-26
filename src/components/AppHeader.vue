<template>
    <div>
      <header>
        <h1 class="title">Boolflix</h1>
        <div class="search_bar mt-3">
        <button @click="$emit('searchClick', searchKey)">
          <input placeholder="Inizia la ricerca" class="m-3" type="text" v-model="searchKey">
          <i class="fas fa-search"></i>
        </button>
      </div>
      </header>
      
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
    justify-content: flex-end;
    align-items: center;
    width: 80%;
    color: white;
  }
  button {
    color: white;
    border: none;
    background-color: #141414;
  }
  input {
    display: none;
  }
  button:hover input{
    display: inline;
}
</style>