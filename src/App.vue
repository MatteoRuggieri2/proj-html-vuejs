<template>
  <div id="app">
    
    <Header :headerLinks="headerLinksArray" />

  </div>
</template>

<script>
import Header from "./components/Header.vue";

export default {
  name: "App",
  components: {
    Header,
  },
  data: function() {
    return {
      headerLinksArray: [
        {
          name: 'Home',
          active: true,
          new: false
        },
        {
          name: 'About',
          active: false,
          new: false
        },
        {
          name: 'Prices',
          active: false,
          new: false
        },
        {
          name: 'Courses',
          active: false,
          new: true
        },
        {
          name: 'Locations',
          active: false,
          new: false
        },
        {
          name: 'Blog',
          active: false,
          new: false
        }
      ]
    }
  }

  // ricordati di fare i data con le props per header e footer
  // installare fontawesome
};
</script>

<style lang="scss">
@import './style/general.scss';

</style>
