<template>
  <div id="start">
    <div class="background"></div>
    <div id="logo"></div>
    <!-- WINNER BOARD -->
    <winner-board></winner-board>
  </div>
</template>

<script>
  import WinnerBoard from "./components/winner-board.vue";

  export default {
    name: 'App',
    components: {WinnerBoard},
    data() {
      return {}
    }
  }
</script>

<style scoped>

  .background {
    background: black url(./assets/victory_back.png) center;
    background-size: cover;
    position: fixed;
    left: 0;
    top: 0;
    width: 100vw;
    height: 100vh;
    z-index: -1;
  }

  #logo {
    background: url(./assets/boi-logo.png) no-repeat;
    background-size: contain;
    width: 613px;
    height: 124px;
    margin: 0 auto;
  }

  @media (max-width: 768px) {
    #logo {
      width: 300px;
      height: 61px;
    }
  }

</style>
