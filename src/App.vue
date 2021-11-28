<template>
  <RandomVinyl />
</template>

<script>
import RandomVinyl from './components/RandomVinyl.vue'

export default {
  name: 'App',
  components: {
    RandomVinyl
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
  position: fixed;
  top: 50%;
  left: 50%;
  /* bring your own prefixes */
  transform: translate(-50%, -50%);
}

</style>
