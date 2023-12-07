<template>
  <div>
    <!-- <h1>Menu List</h1> -->
    <product-detail v-for="detail in details" :key="detail.id" :detail="detail"></product-detail>
  </div>
</template>

<script>
import ProductDetail from './ProductDetail.vue';

export default {
  components: {
    ProductDetail,
  },
  props: ['details']
}
</script>

<style scoped>
div {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
  gap: 10px;
  justify-content: center;
  align-items: center;
}
h1 {
  text-align: center;
}
</style>
