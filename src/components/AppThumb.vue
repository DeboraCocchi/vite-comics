<script>
export default {
  name:'AppThumb',
  props:{
    comic:Object
  },
  data(){
    return{
      hover: false
    }
  }
}
</script>


<template>
  <div class="card" @mouseenter="hover = true" @mouseleave="hover = false" >
    <div class="card-img">
      <img :src="comic.thumb" :alt="comic.series">
      <div class="cover-thumb" v-if="hover">
          <span>{{comic.price}}</span>
          <a href="#">Acquista Ora</a>
          <a href="#">Maggiori Informazioni</a>
        <span class="info" v-if="info">{{comic.type}}</span>
      </div>
    </div>
    <div class="card-body">{{comic.series}}</div>
    
  </div>
</template>


<style scoped lang="scss">
  @use '../style/partials/variables' as *;
  .card{
    width:calc(100% / 6);
    display:flex;
    padding:6px;
    flex-direction: column;
    align-items: flex-start;
    justify-content: center;
      .card-img{
        position:relative;
        img{
          width:calc(100%);
          object-fit: cover;
          aspect-ratio: 1 / 1;
          object-position: top;
        }}
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
      .cover-thumb{
        position:absolute;
        top:0;
        left:0;
        display:flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
        background-color: rgba(255,255,255,0.6);
        width:100%;
        height:calc(100% - 4px);
      a{color:white;
        margin-top:5px;
        padding:5px 8px;
        font-size:80%;
        border:none;
        text-decoration: none;
        text-transform: uppercase;
        &:hover{
          text-decoration: underline;
          cursor:pointer;}
        &:first-of-type{
        background-color: $primary-blue;
        }
        &:last-of-type{
        background-color: $primary-grey;
        }
      }
      span{
        color:$primary-grey;
        background-color: rgba(255,255,255,0.8);
        padding:5px;
        box-shadow: 2px 2px 3px $primary-grey;;
      }
      }
  }
</style>