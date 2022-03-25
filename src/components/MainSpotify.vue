<template>
  <main class="container-fluid">
    <div class="container d-flex pt-5 px-5">
      <CardDisc />
    </div>
  </main>
</template>

<script>
import CardDisc from "./CardDisc.vue";
export default {
  name: "MainSpotify",
  components: {
    CardDisc,
  },
};
</script>

<style lang="scss" scoped>
@import '../assets/styles/partials/variables.scss';
main{
  height: 100hv;
  widows: 100%;
  background-color: $bg-color;
  color: white;
}

</style>
