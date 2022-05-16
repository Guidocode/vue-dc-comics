<template>
  <main>

    <div class="gb-container">
      <div class="title-content">current series</div>
    </div>

    <div class="gb-container container-cards d-flex flex-wrap">

      <CardComp 
      v-for="(cardItem, index) in arrayCards" :key="`card-${index}`" 
      :card="cardItem"
      />

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

  .title-content{
    display: inline-block;
    text-transform: uppercase;
    color: white;
    background-color: $primary-color;
    padding: 5px 10px;
    font-weight: 500;
    margin-bottom: 20px;
  }
}
</style>