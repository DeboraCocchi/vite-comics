<script>
export default {
  name:'AppThumb',
  props:{
    comic:Object
  }
}


</script>


<template>
  <div class="card">
    <div class="card-img">{{product.thumb}}</div>
    <div class="card-body">{{product.series}}</div>
  </div>
</template>


<style scoped lang="scss">
  .card{
    width:205px;
    height:250px;
    background-color: aqua;
    margin:10px;
    padding:5px;
    display:flex;
    flex-direction: column;
    align-items: center;
      .card-img{
        height:185px;
        width:185px;
      }
      .card-body{
        text-transform: uppercase;
      }
  }
</style>