<template>
  <div>
    <h1 class="main-heading"><span style="margin-left: 20px;">Home Appliances Menu</span><button @click="fetchData">Load Menu >>>></button></h1>
    <p>Click on load menu to view products</p>
    <product-list v-if="details.length" :details="details"></product-list>
  </div>
</template>

<script>
import ProductList from './ProductList.vue';
import axios from 'axios';

export default {
  components: {
    ProductList,
  },
  data() {
    return {
      details: [],
    };
  },
  methods: {
    fetchData() {
      axios.get('https://backend-node-sui5.onrender.com/api')
        .then(response => {
          this.details = response.data.homeapplainces;
        })
        .catch(error => {
          console.error('Error fetching data:', error);
        });
    },
  },
};
</script>

<style scoped>
div {
  text-align: center;
}

button {
  float: right !important;
  margin-right: 20px !important;
  background-color: white;
  color: blueviolet;
  border: solid 2px blueviolet;
  padding-right: 30px;
  padding-left: 30px;
  font-size: 20px;
  padding-top: 6px;
  padding-bottom: 6px;
  border-radius: 20px;
  cursor: pointer;
  font-weight: bold;
}

.main-heading{
  background-color: blueviolet;
  color: white;
  font-size: 30px;
  padding-top: 20px;
  padding-bottom: 20px;
  border-radius: 20px;
  text-align: left !important;
}
</style>
