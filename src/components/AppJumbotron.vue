<template>
  <div>
    <!-- jumbotron -->
    <div class="jumbotron">
      <h1>Demon Slayer</h1>
      <p>It is the Taisho Period in Japan. Tanjiro, a kindhearted boy who sells charcoal for a living, finds his family slaughtered by a demon. To make matters worse, his younger sister Nezuko, the sole survivor, has been transformed into a demon herself. Though devastated by this grim reality, Tanjiro resolves to become a “demon slayer” so that he can turn his sister back into a human, and kill the demon that massacred his family</p>
      <button>
        <i class="fas fa-play"></i>
        Riproduci
      </button>
      <button class="bg-dark text-white">
        <i class="fa-solid fa-circle-info"></i>
        Altre info
      </button>
    </div>
    <!-- /jumbotron -->
  </div>
</template>

<script>
export default {
  name: "AppJumbotron"
}
</script>

<style lang="scss" scoped>
@import "../style/common.scss";
@import "../style/query.scss";
  .jumbotron {
    background-image: url(https://wallpaperaccess.com/full/7807768.png);
    width: 100%;
    height: 500px;
    background-size: cover;
    background-position: bottom;
    padding-left: 30px;
    h1{
        font-size: 2rem;
        padding-top: 270px;
    }
    p {
        max-width: 50%;
        font-size: 80%;
    }
    button {
        margin-left: 2rem;
        background-color: white;
        color: black;
        border-radius: 5px;
        border-style: none;
        width: 7rem;

    }
  }
</style>