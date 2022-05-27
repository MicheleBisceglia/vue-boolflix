<template>
  <div>
    <header>
      <!-- Logo header -->
      <h1 class="title">Boolflix</h1>
  
      <!-- header list -->
      <ul class="header_list">
        <li>Home</li>
        <li>Serie TV</li>
        <li>Film</li>
        <li>Nuovi e popolari</li>
        <li>La mia lista</li>
      </ul>
      <!-- /header list -->

      <!-- search bar -->
      <div class="search_bar">
        <button @click="$emit('searchClick', searchKey)">
          <input placeholder="Cerca qui Film o Serie TV" type="text" v-model="searchKey">
          <i class="fas fa-search pt-2"></i>
        </button>
        <img 
          class="user_img"
          src="https://fs-prod-cdn.nintendo-europe.com/media/images/10_share_images/support_9/H2x1_Support_Nintendo_Account.jpg" alt="">
        <i class="fa-solid fa-bell pt-2"></i>
      </div>
      <!-- search bar -->
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
@import "../style/query.scss";
.title {
  padding-left: 5%;
}
.header_list {
  list-style: none;
  display: flex;
  justify-content: flex-start;
  align-items: center;
  width: 50%;
  color: white;
  font-size: 80%;
  margin-top: 15px;
    li {
      padding-left: 15px;
    }
}
.search_bar {
  display: flex;
  justify-content: flex-end;
  color: white;
  width: 25%;
  }
button {
  color: white;
  border: none;
  background-color: #141414;
  padding-right: 20px;
  display: flex;
  }
input {
    display: none;
  }
button:hover input{
    display: inline;
    background-color: #141414;
    border-style: none;
    color: white;
    border-radius: 5px;
}
.user_img {
  height: 30px;
  width: 30px;
  object-fit: cover;
  margin-right: 15px;
}
</style>