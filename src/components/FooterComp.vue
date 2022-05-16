<template>
  <footer>
    
    <!-- Footer top -->
    <div class="footer-top">
      <div class="gb-container">
        <div class="container-fluid">
          <div class="row row-cols-2">

            <!-- COLONNE FOOTER DINAMICHE -->
            <div class="columns">
              <div class="row row-cols-3 py-4">

                <div class="col">
                  <h6>dc comics</h6>
                  <ul>
                    <li v-for="(dcComicsItem, index) in dcComicsMenu" :key="`dcComicsItem-${index}`">
                      <a :href="dcComicsItem.href">{{dcComicsItem.name}}</a>
                    </li>
                  </ul>

                  <h6>shop</h6>
                  <ul>
                    <li v-for="(shopItem, index) in shopMenu" :key="`shopItem-${index}`">
                      <a :href="shopItem.href">{{shopItem.name}}</a>
                    </li>
                  </ul>
                </div>

                <div class="col">
                  <h6>dc</h6>
                  <ul>
                    <li v-for="(dcItem, index) in dcMenu" :key="`dcItem-${index}`">
                      <a :href="dcItem.href">{{dcItem.name}}</a>
                    </li>
                  </ul>
                </div>

                <div class="col">
                  <h6>sites</h6>
                  <ul>
                    <li v-for="(sitesItem, index) in sitesMenu" :key="`sitesItem-${index}`">
                      <a :href="sitesItem.href">{{sitesItem.name}}</a>
                    </li>
                  </ul>
                </div>
              </div>
            </div>
            <!-- /COLONNE FOOTER DINAMICHE -->

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

        <!-- NAV SOCIAL DINAMICA -->
        <nav class="d-flex align-items-center">
          <h6 class="mb-0">follow us</h6>
          <ul class="d-flex mb-0">
            <li v-for="(socialItem, index) in social" :key="`socialItem-${index}`">
              <a :href="socialItem.href"><img :src="require(`../assets/img/${socialItem.image}`)" :alt="socialItem.name"></a>
            </li>
          </ul>
        </nav>
        <!-- /NAV SOCIAL DINAMICA -->

      </div>
      
    </div>
    <!-- /Footer bottom -->
    
  </footer>
</template>

<script>
import dcComicsMenu from '../assets/data/dccomics-items-footer'
import shopMenu from '../assets/data/shop-items-footer'
import dcMenu from '../assets/data/dc-items-footer'
import sitesMenu from '../assets/data/sites-items-footer'
import social from '../assets/data/social-footer'

export default {
  name: 'FooterComp',

  data(){
    return{
      dcComicsMenu,
      shopMenu,
      dcMenu,
      sitesMenu,
      social
    }
  }
}
</script>

<style lang="scss" scoped>
footer{
@import '../assets/style/vars';
@import '../assets/style/mixins';

  // FOOTER TOP
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
          color: $primary-color;
        }
      }
    }

    .logo{
      margin-top: -50px;
      width: 100%;
    }
  }

  // FOOTER BOTTOM
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
        transition: .2s;
        &:hover{
          filter: brightness(.7);
        }
      }
    }
  }
}
</style>