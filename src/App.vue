<template>
  <div id="app">
    <body>
      <AppHeader />
      <AppMain />
    </body>
  </div>
</template>

<script>
import AppMain from "./components/AppMain.vue";
import AppHeader from "./components/AppHeader.vue"

export default {
  name: "App",
  components: {
    AppMain,
    AppHeader
  },
  
};
</script>

<style lang="scss">
@import "./style/common.scss";
</style>
