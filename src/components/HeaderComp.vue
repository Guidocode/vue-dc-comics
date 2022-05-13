<template>

  <header>
    <div class="logo">
      <img src="../assets/img/dc-logo.png" alt="Logo">
    </div>

    <nav>
      <ul>
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
  // display: flex;
  // justify-content: space-between;
  // align-items: center;
  height: 80px;
  line-height: 76px;

  .logo{
    float: left;
    width: 60px;
    height: 60px;
  }

  nav{
    float: right;
    ul{
      display: flex;
      margin: 0;
    }

    li{
      padding: 0 15px;
    }

    a{
      display: inline-block;
      color: black;
      font-size: .7rem;
      font-weight: 600;
      @include linkStyleNav();
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