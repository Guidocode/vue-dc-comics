<template>
  <div class="light-blue-band py-5">
    <div class="gb-container">
      <ul class="d-flex justify-content-between m-0 px-5">

        <li v-for="(voceMenu, index) in vociMenu" :key="`menu-${index}`">
          <a class="d-flex align-items-center" href="#">
            <!-- ERRORE -->
            <div class="icon" 
            :style="{backgroundImage: 'url('+ require(`../assets/img/${voceMenu.image}`)+')'}"></div>
            <span>{{voceMenu.name}}</span>
          </a>
        </li>
          
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  name: 'LightBlueBand',

  data(){
    return {
      vociMenu: [
        {
          image: 'buy-comics-digital-comics.png',
          name: 'digital comics'
        },
        {
          image: 'buy-comics-merchandise.png',
          name: 'dc merchandise'
        },
        {
          image: 'buy-comics-subscriptions.png',
          name: 'subscription'
        },
        {
          image: 'buy-comics-shop-locator.png',
          name: 'comics shop locator'
        },
        {
          image: 'buy-dc-power-visa.svg',
          name: 'dc power visa'
        },
      ]
    }
  }
}
</script>

<style lang="scss" scoped>
@import '../assets/style/vars';
@import '../assets/style/mixins';

.light-blue-band{
  background-color: $primary-color;

  ul{
    a{
      display: inline-block;
      color: white;
      font-size: .7rem;
      @include linkStyle();
      margin-right: 5px;
      

      .icon{
        display: inline-block;
        width: 60px;
        height: 50px;
        margin-right: 5px;
        background-size: contain;
        background-repeat: no-repeat;
        background-position: center;
      }
    }
  }
}
</style>