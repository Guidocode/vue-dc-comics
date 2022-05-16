<template>
  
  <div class="gb-card">
    <div class="image-card">
      <img :src="card.thumb" :alt="card.series">
    </div>
    <div class="title-card">{{card.series}}</div>
  </div>

</template>

<script>
export default {
  name: 'CardComp',
  props:{
    card: Object
  },
}
</script>

<style lang="scss" scoped>
.gb-card{
  width: calc(100vw / 8 - 20px);
  margin: 5px 10px 20px;
  cursor: pointer;
  transition: .3s;
  &:hover{
    filter:contrast(3);
  }
  // DA RIVEDERE I CALC
  .image-card{
    height: calc(100vw / 8 - 40px);
    overflow: hidden;
    margin-bottom: 10px;
  }

  .image-card img{
    width: 100%;
  }

  .title-card{
    text-transform: uppercase;
    font-size: .7rem;
  }
}
</style>