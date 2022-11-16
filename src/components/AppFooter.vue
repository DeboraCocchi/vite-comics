<script>
export default {
  name:'AppFooter'
}
</script>

<template>
  <footer>
    <div class="top">
      <div class="container">
        <div class="col">
          <h3>DC Comics</h3>
          <ul>
            <li><a href="#">Characters</a></li>
            <li><a href="#">Comics</a></li>
            <li><a href="#">Movies</a></li>
            <li><a href="#">TV</a></li>
            <li><a href="#">Games</a></li>
            <li><a href="#">Videos</a></li>
            <li><a href="#">News</a></li>
          </ul>
          <h3>Shop</h3>
          <ul>
            <li><a href="#">Shop DC</a></li>
            <li><a href="#">Shop DC Collectibles</a></li>
          </ul>
        </div>
        <div class="col">
          <h3>DC</h3>
          <ul>
            <li><a href="#">Terms of use</a></li>
            <li><a href="#">Privacy Policy (New)</a></li>
            <li><a href="#">Ad Choices</a></li>
            <li><a href="#">Advertising</a></li>
            <li><a href="#">Jobs</a></li>
            <li><a href="#">Subscriptions</a></li>
            <li><a href="#">Talent Workshops</a></li>
            <li><a href="#">CPSC Certificates</a></li>
            <li><a href="#">Ratings</a></li>
            <li><a href="#">Shop help</a></li>
            <li><a href="#">Contact Us</a></li>
          </ul>
        </div>
        <div class="col">
          <h3>Sites</h3>
          <ul>
            <li><a href="#">DC</a></li>
            <li><a href="#">MAD Magazine</a></li>
            <li><a href="#">DC Kids</a></li>
            <li><a href="#">DC Universe</a></li>
            <li><a href="#">DC Power Visa</a></li>
          </ul>
        </div>
        <div class="big-logo"></div>
      </div>
      
    </div>
    <div class="bottom">
      <div class="container d-flex">
        <div class="button"><a href="#">SIGN UP NOW!</a></div>
        <div class="socials">
          <span>Follow US</span>
          <ul>
            <li><a href="#"><img src="../assets/footer-facebook.png" alt=""></a></li>
            <li><a href="#"><img src="../assets/footer-twitter.png" alt=""></a></li>
            <li><a href="#"><img src="../assets/footer-youtube.png" alt=""></a></li>
            <li><a href="#"><img src="../assets/footer-pinterest.png" alt=""></a></li>
            <li><a href="#"><img src="../assets/footer-periscope.png" alt=""></a></li>
          </ul>
        </div>
      </div>
    </div>
  </footer>
</template>


<style lang="scss" scoped>
  @use '../style/partials/variables' as *;
  @use '../style/partials/mixin' as *;

  .top{
    background-image: url('../assets/footer-bg.jpg');
    min-height: 400px;
    background-size: cover;
    overflow-y: scroll;
      .container{
        position:relative;
        padding:40px 0 80px;
        display:flex;
        align-items:flex-start;
        .col{
          width:140px;
          height:100%;
          margin-right:20px;
          h3{
            text-transform: uppercase;
            margin:8px 0;
            font-size: 140%;
            &:nth-of-type(2){
              margin-top:20px;
            }
          }
          a{
            color:$primary-lightgrey;
            text-decoration: none;
            font-size:85%;
            &:hover{
              color:white;
            }
          }
    }
    .big-logo{
      background-image: url('../assets/dc-logo-bg.png');
      opacity:0.7;
      width:450px;
      height:450px;
      background-size: cover;
      position:absolute;
      top:-38px;
      right:0;
      display:inline;
    }
    }
  }
  .bottom{
    height:100px;
    width:100%;
    background-color:$primary-grey;
    position:fixed;
    bottom:0;
    left:0;
    z-index:1;
    .container{
      height:100%;
      .button{
        border:2px solid $primary-blue;
        padding:10px 8px;
        a{
          text-decoration: none;
          color:white;
          font-size:90%;
          &:hover{
            text-decoration: underline;
          }
        }
      }
      .socials{
        display:flex;
        align-items: center;
        span{
          color:$primary-blue;
          text-transform: uppercase;;
        }
        ul{
        display:flex;
        height:100%;
          a{
            margin-left:15px;
          }
        }
      }
    }
      
  }
</style>