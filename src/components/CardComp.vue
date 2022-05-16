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
  width: calc(100% / 6 - 40px);
  margin: 5px 20px;

  .image-card{
    width: 100%;
  }
}
</style>