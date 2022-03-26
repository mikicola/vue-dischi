<template>
  <main class="container-fluid">
    <div class="container d-flex">
      <div class="row row-cols-2 row-cols-md-3 row-cols-lg-5 g-2">
        <CardDisc 
        v-for="album in arrAlbum"
        :key="album.id"
        :album-data="album"
        />
        <!-- 
          creo attributo unico (album-data) passandogli l'oggetto album
          -->

        <!-- :card-poster="album.poster"
        :card-title="album.title"
        :card-author="album.author"
        :card-genre="album.genre"
        :card-year="album.year" -->
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
  //height: calc(100vh - 80px); // tolgo l'header (80px)
  // width: 100%;
  // background-color: $bg-color;
  color: white;
}

.container {
  padding: 4rem 6rem 2rem 6rem;
  // padding-top: 4rem;
}
</style>
