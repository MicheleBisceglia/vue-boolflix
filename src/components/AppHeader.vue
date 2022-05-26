<template>
    <div>
      <header>
        <h1 class="title">Boolflix</h1>
        <div class="search_bar">
          <button @click="$emit('searchClick', searchKey)">
            <input placeholder="Inizia la ricerca" type="text" v-model="searchKey">
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
    color: white;
    width: 85%;
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