<template>
  <header class="container-fluid">
    <div class="container d-flex justify-content-between">
      <img
        src="https://upload.wikimedia.org/wikipedia/commons/7/71/Spotify.png"
        alt="Logo Spotify"/>

      <select class="genre-selector">
        <option selected>Seleziona genere</option>
        <option value="Rock">Rock</option>
        <option value="pop">pop</option>
        <option value="metal">metal</option>
      </select>
    </div>
  </header>
</template>

<script>
export default {
  name: "HeaderSpotify",
};
</script>

<style lang="scss" scoped>
@import "../assets/styles/partials/variables.scss";
header {
  background-color: $primary-color;
}
img {
  height: 60px;
  margin: 10px;
}

.genre-selector{
  background-color:  $primary-color;
  color: white;
}
</style>
