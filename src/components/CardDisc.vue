<template>
  <div class="card-album flex-row text-center">
  
      <img class="img-fluid" :src="albumData.poster" :alt="albumData.title">
      <h2 class="pt-4">{{ albumData.title }}</h2>
      <h3 class="pt-2">{{ albumData.author }}</h3>
      <h4>{{ albumData.year }}</h4>
      </div>
  
</template>

<script>
export default {
    name: 'CardDisc',
    props: {
      albumData: Object // è album-data del main 
    }
}
</script>

<style lang="scss" scoped>
@import '../assets/styles/partials/variables.scss';
  .card-album{
    background-color: $primary-color;
    padding: 10px;
    // margin: 10px;
    img{
      // width: 150px;
    }
    h2{
      text-transform: uppercase;
      font-size: 1.3rem;
    }
    h3{
      font-size: 1.2rem;
    }
    h4{
      font-size: 1rem;
    }
    h3, h4{
      color: #637074;
    }
  }
</style>
