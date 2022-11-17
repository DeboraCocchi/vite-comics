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
  
  <div class="container d-flex">
    <div class="title"><h2>CURRENT SERIES</h2></div>
    <AppThumb v-for="(product, index) in products" :key="index" :comic="product"/>
    <div class="btn-load"><button>Load More</button></div>
  </div>

</main>
  
</template>


<style lang="scss" scoped>
  @use '../style/partials/variables' as *;
  @use '../style/partials/mixin' as *;
  main{
    background-color: $primary-black;
    padding-bottom:20px;
    .jumbo{
    width:100%;
    height:400px;
    background-image: url('../assets/jumbotron.jpg');
    }
    .title{
      margin:0 auto;
      width:100%;
      h2{
        font-size:1.5rem;
        display:inline-block;
        padding:8px 12px;
        background-color: $primary-blue;
        text-align:center;
        position:relative;
        top:-22px;
    }
    }
    
    .container{
      display: flex;
      flex-wrap: wrap;
      padding:50px auto;
      background-color: $primary-black;
      .btn-load{
        margin:0 auto;
        margin-top:20px;
        button{
          background-color: $primary-blue;
          text-transform: uppercase;
          padding:5px 8px;
          font-size:90%;
          color:white;
          border:none;
          &:hover{
            cursor:pointer;
          }
        }
      }
  }
  }
  
</style>