<template>
  <div>
    <footer class="text-center text-white">
  <!-- Grid container -->
  <div class="container p-4 pb-0">
    <!-- Section: Social media -->
    <section class="mb-4">
      <!-- Facebook -->
      <a class="btn btn-outline-light btn-floating m-1" href="#!" role="button"
        ><i class="fab fa-facebook-f"></i
      ></a>

      <!-- Twitter -->
      <a class="btn btn-outline-light btn-floating m-1" href="#!" role="button"
        ><i class="fab fa-twitter"></i
      ></a>

      <!-- Google -->
      <a class="btn btn-outline-light btn-floating m-1" href="#!" role="button"
        ><i class="fab fa-google"></i
      ></a>

      <!-- Instagram -->
      <a class="btn btn-outline-light btn-floating m-1" href="#!" role="button"
        ><i class="fab fa-instagram"></i
      ></a>

    </section>
    <!-- /Section: Social media -->
  </div>
  <!-- /Grid container -->

  <!-- Copyright -->
  <div class="text-center p-3 bg-dark">
    © 2022 Copyright:
    <a class="text-white" href="">Boolflix.com</a>
  </div>
  <!-- Copyright -->
</footer>
  </div>
</template>

<script>
export default {
  name: "AppFooter",
}
</script>

<style lang="scss" scoped>
  footer {
    background-color: #141414;
  }
  a {
    border-style: none;
  }
</style>