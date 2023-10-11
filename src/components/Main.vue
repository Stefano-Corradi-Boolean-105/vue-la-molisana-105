<script>

import ProductCard from './partials/ProductCard.vue';
import products from '../data/products'

export default {
  name: 'Main',
  components:{
    ProductCard
  },
  data(){
    return{
      products
    }
  }
}
</script>

<template>
  <main>
    <h1>I miei prodotti</h1>

    <div class="cards-wrapper container">

      <ProductCard
        v-for="product in products"
        :key="product.id"
        :img="product.src"
        :productName="product.titolo"
      />

    </div>
  

  </main>
  
</template>

<style lang="scss" scoped>

main{
  min-height: 400px;
  padding: 50px;
  background-image: url('../assets/img/bg-prods.jpg');
  margin-bottom: 50px;
  h1{
    text-align: center;
  }
  .cards-wrapper{
    display: flex;
    flex-wrap: wrap;
    padding: 50px 0;
  }
}


</style>