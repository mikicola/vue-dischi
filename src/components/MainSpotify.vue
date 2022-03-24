<template>
  <main class="bg-primary">
    <div class="container">
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
</style>
