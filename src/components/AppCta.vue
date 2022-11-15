<script>
export default {
  name:'AppCta',
  data(){
    return{
      ctaObjects:[
        {
          text:'DIGITAL COMICS',
          imgName: 'digital-comics.png'
        },
        {
          text:'DC MERCHANDISE',
          imgName: 'merchandise.png'
        },
        {
          text:'SUBSCRIPTION',
          imgName: 'subscriptions.png'
        },
        {
          text:'COMIC SHOP LOCATOR',
          imgName: 'shop-locator.png'
        }
      ]
    }
  },
  methods:{
    getImgPath(img){
      return new URL(`../assets/buy-comics-${img}`,import.meta.url).href
    }
  }
}
</script>

<template>
  <div class="cta-strip">
    <div class="container">
 
        <ul class="d-flex">
          <li v-for="(ctaObject,index) in ctaObjects" :key="index">
            <img :src="getImgPath(ctaObject.imgName)" :alt="ctaObject.imgName"><span>{{ctaObject.text}}</span>
          </li>
        </ul>
    
    </div>
  </div>
</template>


<style lang="scss" scoped>
  @use '../style/partials/variables' as *;
  @use '../style/partials/mixin' as *;

  .cta-strip{
    background-color: $primary-blue;
    height:150px;
    width:100%;
    .container{
      padding:80px 0;
      height:150px;
      ul{
        height:100%;
        width:100%;
        li{
          display:flex;
          align-items: center;
          margin:10px;
          img{
            height:60px;
          }
          span{
            font-weight: 300;
            font-size:90%;
            margin-left:10px;
            margin-right:10px;
          }
        }
      }
    }
  }
</style>