<script>
export default {
  name: 'ProductCard',
  props:{
    img: String,
    productName: String
  }
}
</script>

<template>

  <div class="card">
    <img :src="img" :alt="productName">
    <h4>{{ productName }}</h4>
  </div>
  
</template>



<style lang="scss" scoped>

@use '../../scss/partials/variabiles' as *;

.card{
  flex-basis: 25%;
  background-color: white;
  text-align: center;
  border: 1px solid lighten($primary-color, 65%);
  h4{
    margin-bottom: 20px;
  }
}
</style>