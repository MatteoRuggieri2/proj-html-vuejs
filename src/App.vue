<template>
  <div id="app">
    
    <Header />

  </div>
</template>

<script>
import Header from "./components/Header.vue";

export default {
  name: "App",
  components: {
    Header,
  },

  // ricordati di fare i data con le props per header e footer
  // installare fontawesome
};
</script>

<style lang="scss">
@import './style/general.scss';

</style>
