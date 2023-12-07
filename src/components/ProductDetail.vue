<template>
  <div class="list">
    <h2>{{ detail.productName }}</h2>
    <p>Brand : {{ detail.Brand }}</p>
    <p>Current Price : {{ detail.CurrentPrice }}</p>
    <p>Discount : {{ detail.Discount }}</p>
    <p>DeliveryCharges : {{ detail.DeliveryCharges }}</p>
    <p>Ratings : {{ detail.Ratings }}</p>
    <p>Reviews : {{ detail.Reviews }}</p>
    <p>SeriesOfBrand : {{ detail.SeriesOfBrand }}</p>
  </div>
</template>

<script>
export default {
  props: ['detail']
}
</script>

<style scoped>
.list{
  border: solid 2px blueviolet !important;
  border-radius: 20px;
  text-transform: capitalize;
}
</style>
