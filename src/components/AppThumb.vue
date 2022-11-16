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
    <img class="card-img" :src="comic.thumb" :alt="comic.series">
    <div class="card-body">{{comic.series}}</div>
  </div>
</template>


<style scoped lang="scss">
  .card{
    width:calc(100% / 6);
    padding:4px;
    display:flex;
    flex-direction: column;
    align-items: center;
      .card-img{
        width:calc(100% - 8px);
        object-fit: cover;
        aspect-ratio: 1 / 1;
        object-position: top;
        }
      .card-body{
        margin:3px 0 10px;
        overflow: hidden;
        padding:2px;
        text-transform: uppercase;
        font-size:85%;
        text-overflow:ellipsis;
        width:calc(100% - 12px);
        white-space: nowrap;
        }
  }
</style>