<template>
  <div>

    <HeaderComp />

    <JumbotronComp />

    <MainComp />

    <LightBlueBand />

    <FooterComp />
    
  </div>
</template>

<script>
import HeaderComp from "./components/HeaderComp.vue";
import MainComp from "./components/MainComp.vue";
import FooterComp from "./components/FooterComp.vue";
import LightBlueBand from "./components/LightBlueBand.vue";
import JumbotronComp from "./components/JumbotronComp.vue";


export default {
  name: 'App',
  components: {
    HeaderComp,
    MainComp,
    FooterComp,
    LightBlueBand,
    JumbotronComp
}
}
</script>

<style lang="scss">
@import './assets/style/vars';
@import './assets/style/general';
@import './assets/style/utilities';

</style>
