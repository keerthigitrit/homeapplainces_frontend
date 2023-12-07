<template>
  <div id="app">
    <product-manager></product-manager>
  </div>
</template>

<script>
import ProductManager from './components/ProductManager.vue';

export default {
  components: {
    ProductManager,
  },
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  text-align: center;
  color: #0a0a0a;
  margin: 50px;
}
</style>
