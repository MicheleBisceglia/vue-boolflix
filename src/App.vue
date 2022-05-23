<template>
  <div id="app">
    <body>
      <header>
       <h1 class="title">Boolflix</h1>
      </header>
      <HelloWorld />
    </body>
  </div>
</template>

<script>
import HelloWorld from "./components/HelloWorld.vue";

export default {
  name: "App",
  components: {
    HelloWorld,
  },
};
</script>

<style lang="scss">
@import "./style/common.scss";
</style>
