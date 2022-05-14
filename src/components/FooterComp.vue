<template>
  <footer>
    
    <!-- Footer top -->
    <div class="footer-top">
      <div class="gb-container">
        <div class="container-fluid">
          <div class="row row-cols-2">

            <div class="columns">
              <div class="row row-cols-3 py-4">

                <div class="col">
                  <h6>dc comics</h6>
                  <ul>
                    <li><a href="#">characters</a></li>
                    <li><a href="#">comics</a></li>
                    <li><a href="#">movies</a></li>
                    <li><a href="#">tv</a></li>
                    <li><a href="#">games</a></li>
                    <li><a href="#">videos</a></li>
                    <li><a href="#">news</a></li>
                  </ul>

                  <h6>shop</h6>
                  <ul>
                    <li><a href="#">shop dc</a></li>
                    <li><a href="#">shop dc collectibles</a></li>
                  </ul>
                </div>

                <div class="col">
                  <h6>dc</h6>
                  <ul>
                    <li><a href="#">Terms Of Use</a></li>
                    <li><a href="#">Privacy policy (New)</a></li>
                    <li><a href="#">Ad choices</a></li>
                    <li><a href="#">advertising</a></li>
                    <li><a href="#">jobs</a></li>
                    <li><a href="#">subscriptions</a></li>
                    <li><a href="#">talent workshops</a></li>
                    <li><a href="#">cpsc certificates</a></li>
                    <li><a href="#">ratings</a></li>
                    <li><a href="#">shop help</a></li>
                    <li><a href="#">contact us</a></li>
                  </ul>
                </div>

                <div class="col">
                  <h6>sites</h6>
                  <ul>
                    <li><a href="#">dc</a></li>
                    <li><a href="#">mad magazine</a></li>
                    <li><a href="#">dc kids</a></li>
                    <li><a href="#">dc universe</a></li>
                    <li><a href="#">dc power visa</a></li>
                  </ul>
                </div>
              </div>
            </div>

            <div class="col">
              <img class="logo" src="../assets/img/dc-logo-bg.png" alt="">
            </div>

          </div>
        </div>
      </div>
    </div>
    <!-- /Footer top -->


    <!-- Footer bottom -->
    <div class="footer-bottom">

      <div class="gb-container d-flex justify-content-between align-items-center">
        <button type="button" class="btn btn-outline-primary gb-btn">sing-up now!</button>

        <nav class="d-flex align-items-center">
          <h6 class="mb-0">follow us</h6>
          <ul class="d-flex mb-0">
            <li><a href="#"><img src="../assets/img/footer-facebook.png" alt="facebook"></a></li>
            <li><a href="#"><img src="../assets/img/footer-twitter.png" alt="twitter"></a></li>
            <li><a href="#"><img src="../assets/img/footer-youtube.png" alt="youtube"></a></li>
            <li><a href="#"><img src="../assets/img/footer-pinterest.png" alt="pinterest"></a></li>
            <li><a href="#"><img src="../assets/img/footer-periscope.png" alt="periscope"></a></li>
          </ul>
        </nav>
      </div>
      
    </div>
    <!-- /Footer bottom -->
    
  </footer>
</template>

<script>
export default {
  name: 'FooterComp'
}
</script>

<style lang="scss" scoped>
footer{
@import '../assets/style/vars';
@import '../assets/style/mixins';

  .footer-top{
    max-height: 350px;
    background-image: url(../assets/img/footer-bg.jpg);
    background-size: cover;
    background-position: center;
    overflow: hidden;

    .columns{
      color: white;

      ul{
        padding-left: 0;
      }

      h6{
        text-transform: uppercase;
      }

      a{
        text-transform: capitalize;
        text-decoration: none;
        font-size: .7rem;
        color: #979291;
        &:hover{
          text-decoration: underline;
          color: white;
        }
      }
    }

    .logo{
      margin-top: -50px;
      width: 100%;
    }
  }

  .footer-bottom{
    height: 80px;
    background-color: #303030;

    .gb-container{
      height: 100%;
    }

    .gb-btn{
      border: 2px solid $primary-color;
      border-radius: none;
      color: white;
      text-transform: uppercase;
      &:hover{
        background-color: $primary-color;
      }
    }

    nav{
      h6{
        text-transform: uppercase;
        color: $primary-color;
      }

      li{
        padding: 0 5px;
      }

      a img{
        width: 25px;
      }
    }
  }
}
</style>