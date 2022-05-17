<template>
  <main>

    <!-- Titolo contenitore -->
    <div class="gb-container">
      <div class="title-content">current series</div>
    </div>
    <!-- /Titolo contenitore -->

    <!-- Card Component -->
    <div class="gb-container container-cards d-flex flex-wrap">

      <CardComp 
      v-for="(cardItem, index) in arrayCards" :key="`card-${index}`" 
      :card="cardItem"
      />

    </div>
  <!-- /Card Component -->

  <div class="gb-container  text-center">
    <button type="button" class="btn btn-primary gb-btn">Load More</button>
  </div>

  </main>
</template>

<script>
import CardComp from "./CardComp.vue";
import arrayCards from "../assets/data/array-cards";

export default {
  name: "MainComp",
  components: { 
    CardComp 
  },

  data(){
    return{
      arrayCards
    }
  }
}
</script>

<style lang="scss" scoped>
@import '../assets/style/vars';

main{
  padding: 40px 0;
  color: white;
  background-color: #1C1C1C;
  
  // .gb-container{
  //   position: relative;
  // }

  .title-content{
    // position: absolute;
    // top: -55;
    // left: 0;
    display: inline-block;
    text-transform: uppercase;
    color: white;
    background-color: $primary-color;
    padding: 5px 10px;
    font-weight: 500;
    margin-bottom: 20px;
  }

  .gb-btn{
    // display: inline-block;
    margin: 0 auto;
    text-transform: uppercase;
    background-color: $primary-color;
    padding: 5px 40px;
  }
}
</style>