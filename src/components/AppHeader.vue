<script>
export default {
  name:'AppHeader'
}
</script>

<template>
  <header>
    <div class="container d-flex">
      <div class="logo">
        <a href="#"><img src="/dc-logo.png" alt="DC Logo"></a>
      </div>
      <nav>
        <ul class="d-flex">
          <li><a href="#">Characters</a></li>
          <li><a href="#">Comics</a></li>
          <li><a href="#">Movies</a></li>
          <li><a href="#">TV</a></li>
          <li><a href="#">Games</a></li>
          <li><a href="#">Collectibles</a></li>
          <li><a href="#">Videos</a></li>
          <li><a href="#">Fans</a></li>
          <li><a href="#">News</a></li>
          <li><a href="#">Shop</a></li>
        </ul>
      </nav>
    </div>
    
  </header>
</template>


<style lang="scss" scoped>
  @use '../style/partials/variables' as *;
  @use '../style/partials/mixin' as *;

  header{
    background-color: white;
    height:85px;
    .logo{
      padding:8px;
      height:85px;
      width:85px;
    }
    nav{
      height:85px;
      ul{
      list-style: none;
      height:100%;
      li{
        display:flex;
        align-items:center;
        margin-left:18px;
        height:100%;
        border-bottom:4px solid white;
        &:hover , &.active{
            border-bottom:4px solid $primary-blue;
          }
        &:hover a{
          color:$primary-blue;
        }
        a{
          text-decoration: none;
          color:$primary-grey;
          text-transform: uppercase;
          font-size:80%;
          font-weight: bold;
         }
      }
      
    }
    }
    
  }
</style>