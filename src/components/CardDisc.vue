<template>
  <div class="card-album flex-row text-center col-6 col-md-4 col-lg-3">
      <img class="img-fluid" src="https://www.onstageweb.com/wp-content/uploads/2018/09/bon-jovi-new-jersey.jpg" alt="">
      <h2 class="pt-4">new jersey</h2>
      <h3 class="pt-2">Bon Jovi</h3>
      <h4>1988</h4>
  </div>
</template>

<script>
export default {
    name: 'CardDisc'
}
</script>

<style lang="scss" scoped>
@import '../assets/styles/partials/variables.scss';
  .card-album{
    background-color: $primary-color;
    padding: 10px;
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
