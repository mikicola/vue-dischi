<template>
  <main class="container-fluid">
    <div class="container d-flex">
      <div class="row">
        <CardDisc />
      </div>
    </div>
  </main>
</template>

<script>
import CardDisc from "./CardDisc.vue";
import axios from 'axios';

export default {
  name: "MainSpotify",
  data(){
    return{
      arrAlbum: null,
    }
  },
  components: {
    CardDisc,
  },
  created(){
    axios.get('https://flynn.boolean.careers/exercises/api/array/music')
    .then((axiosResponse) => {
      console.log(axiosResponse);
      this.arrAlbum = axiosResponse.data.response
      console.log(this.arrAlbum);
    })
  }
};
</script>

<style lang="scss" scoped>
@import "../assets/styles/partials/variables.scss";
main {
  height: calc(100vh - 80px); // tolgo l'header (80px)
  width: 100%;
  background-color: $bg-color;
  color: white;
}

.container {
  padding: 4rem 6rem 0 6rem;
}
</style>
