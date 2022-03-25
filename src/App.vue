<template>
  <div id="app">
    <HeaderSpotify />
    <MainSpotify />
    <CardDisc />
  </div>
</template>

<script>
import HeaderSpotify from './components/HeaderSpotify.vue';
import MainSpotify from './components/MainSpotify.vue';
import CardDisc from './components/CardDisc.vue';

export default {
  name: 'App',
  components: {
    HeaderSpotify,
    MainSpotify,
    CardDisc,
  }
}
</script>

<style lang="scss">
  @import "./assets/styles/style.scss";
  @import "~bootstrap/scss/bootstrap";
  
</style>
