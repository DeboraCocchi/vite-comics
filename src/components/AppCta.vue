<script>
export default {
  name:'AppCta',
  data(){
    return{
      ctaObjects:[
        {
          text:'DIGITAL COMICS',
          imgName: 'comics-digital-comics.png'
        },
        {
          text:'DC MERCHANDISE',
          imgName: 'comics-merchandise.png'
        },
        {
          text:'SUBSCRIPTION',
          imgName: 'comics-subscriptions.png'
        },
        {
          text:'COMIC SHOP LOCATOR',
          imgName: 'comics-shop-locator.png'
        },
        {
          text:'DC POWER VISA',
          imgName: 'dc-power-visa.svg'
        },
      ]
    }
  },
  methods:{
    getImgPath(img){
      return new URL(`../assets/buy-${img}`,import.meta.url).href
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
          img:last-of-type{
              height:45px;
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