<template>
  <div id="app">
    
    <Header :headerLinks="headerLinksArray" />
    <Main :courses="coursesArray" />
    <!-- <Main :courses="coursesArray" :percentagesArray="percentagesLabelsArray" /> -->

  </div>
</template>

<script>
import Header from "./components/Header.vue";
import Main from "./components/Main.vue";

export default {
  name: "App",
  components: {
    Header,
    Main,
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
      ],
      coursesArray: [
        {
          name: 'Pass Plus',
          img: 'courses-passplus.jpg'
        },
        {
          name: 'Intensive Course',
          img: 'course-intensive.jpg'
        },
        {
          name: 'Instructors',
          img: 'courses-instructor.jpg'
        },
      ],
      // percentagesLabelsArray: [
      //   {
      //     name: 'pass rate',
      //     percentage: '95%'
      //   },
      //   {
      //     name: 'referral rate',
      //     percentage: '100%'
      //   },
      //   {
      //     name: 'accident rate',
      //     percentage: '0%'
      //   }
      // ]
    }
  }

  // ricordati di fare i data con le props per header e footer
  // installare fontawesome
};
</script>

<style lang="scss">
@import './style/general.scss';

  // Personalizzazione scrollbar
  ::-webkit-scrollbar{
    width:0.5em;
    height:0.5em;
    background: rgb(255, 255, 255);
  }
  ::-webkit-scrollbar-thumb{
    border-radius:4px;
    background-color: $primary_color;
    // border: none;
    border: 1px solid white;
  }
  ::-webkit-scrollbar-thumb:hover{
    background-color: rgb(49, 172, 0);
    // border: none;
    border: 1px solid white;
  }
  
  ::-webkit-scrollbar-thumb:active{
    background-color:rgb(40, 141, 0);
    border: none;
  }

</style>
