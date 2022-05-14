<template>

  <header class="gb-container">
    <div class="logo">
      <img src="../assets/img/dc-logo.png" alt="Logo">
    </div>

    <nav>
      <ul class="d-flex m-0">
        <li v-for="(voceNav, index) in vociNav" :key="`nav-${index}`">
          <a :class="{'active' : voceNav.isActive}" :href="voceNav.href">{{voceNav.name}}</a>
        </li>
      </ul>
    </nav>
  </header>

</template>

<script>
export default {
  name: 'HeaderComp',

  data(){
    return {
      vociNav: [
        {
          name: 'characters',
          href: '#',
          isActive: false
        },
        {
          name: 'comics',
          href: '#',
          isActive: true
        },
        {
          name: 'movies',
          href: '#',
          isActive: false
        },
        {
          name: 'tv',
          href: '#',
          isActive: false
        },
        {
          name: 'games',
          href: '#',
          isActive: false
        },
        {
          name: 'collectibles',
          href: '#',
          isActive: false
        },
        {
          name: 'videos',
          href: '#',
          isActive: false
        },
        {
          name: 'fans',
          href: '#',
          isActive: false
        },
        {
          name: 'news',
          href: '#',
          isActive: false
        },
        {
          name: 'shop',
          href: '#',
          isActive: false
        },
      ],

      indexActiveItemNav: 0,
    }
  
  },

  methods: {

    // toggleActive(indice){

    //   this.indexActiveItemNav = indice;
    //   console.log(this.indexActiveItemNav);

    //   this.vociNav[this.indexActiveItemNav].isActive = !this.vociNav[this.indexActiveItemNav].isActive;
    // }
  }
}
</script>

<style lang="scss" scoped>
@import '../assets/style/vars';
@import '../assets/style/mixins';

header{
  height: 100px;
  line-height: 94px;

  .logo{
    float: left;
    width: 70px;
    height: 70px;
    img{
      width: 100%;
    }
  }

  nav{
    float: right;

    li{
      padding: 0 15px;
    }

    a{
      display: inline-block;
      color: black;
      font-size: .7rem;
      font-weight: 600;
      @include linkStyle();
      &:hover,
      &.active{
        border-bottom: 4px solid $primary-color;
        color: $primary-color;
      }
     
    }
  }
}
</style>

{'active':item.isActive}