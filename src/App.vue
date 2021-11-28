<template>
  <RandomVinyl />
</template>

<script>
import RandomVinyl from "./components/RandomVinyl.vue";

export default {
  name: "App",
  components: {
    RandomVinyl,
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #adadad;
  position: fixed;
  position: absolute;
  top: 50;
  left: 25;
  right: 25;
  bottom: 0;
  margin: auto;
}
body{  background-color: #5d5c61;
}
</style>
