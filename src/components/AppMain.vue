<script>
import products from '../data/products'
import AppThumb from './AppThumb.vue'

export default {
  name:'AppMain',
  components:{
    AppThumb
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
  <div class="jumbo"></div>
  <h2>CURRENT SERIES</h2>
  <div class="container d-flex">
    <AppThumb v-for="(product, index) in products" :key="index" :comic="product"/>
  </div>

</main>
  
</template>


<style lang="scss" scoped>
  @use '../style/partials/variables' as *;
  @use '../style/partials/mixin' as *;
  main{
    background-color: $primary-black;
    .jumbo{
    width:100%;
    height:400px;
    background-image: url('../assets/jumbotron.jpg');
    }
    h2{
        font-size:1.5rem;
        display:inline-block;
        padding:8px 12px;
        background-color: $primary-blue;
        text-align:center;
        position:relative;
        top:-22px;
        left:248px;
    }
    .container{
      display: flex;
      flex-wrap: wrap;
      margin:30px auto;
      
  }
  }
  
</style>