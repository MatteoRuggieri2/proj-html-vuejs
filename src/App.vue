<template>
  <div id="app">
    
    <Header :headerLinks="headerLinksArray" />
    <Main :courses="coursesArray" :instructors="instructorsArray" :news="latestNewsArray" />
    <!-- <Main :courses="coursesArray" :percentagesArray="percentagesLabelsArray" /> -->
    <Footer :footerDetails="footerDetailsArray" :footerCourses="footerCoursesArray" />

  </div>
</template>

<script>
import Header from "./components/Header.vue";
import Main from "./components/Main.vue";
import Footer from "./components/Footer.vue";

export default {
  name: "App",
  components: {
    Header,
    Main,
    Footer
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
      // ],
      instructorsArray: [
        {
          name: 'Mike Hart',
          img: 'instructor-mikehart.jpg',
          text: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit.'
        },
        {
          name: 'John Smith',
          img: 'instructor-johnsmith.jpg',
          text: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit.'
        },
        {
          name: 'Angela Hart',
          img: 'instructor-angelahart.jpg',
          text: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit.'
        },
      ],
      latestNewsArray: [
        {
          img: 'blog-choosecar-700x441.jpg',
          name: 'What Car to Start With?',
          date: 'February 7th, 2019',
          comments: 0,
          text: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit.'
        },
        {
          img: 'blogpost-10and2-700x441.jpg',
          name: 'Avada Driving School Expanding',
          date: 'February 7th, 2019',
          comments: 0,
          text: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit.'
        }
      ],
      footerDetailsArray: [
        {
          icon: 'fas fa-home',
          text: '12345 North Main Street, New York, NY 555555'
        },
        {
          icon: 'fas fa-phone',
          text: '1.800.555.6789'
        },
        {
          icon: 'far fa-envelope',
          text: 'info@your-domain.com'
        },
        {
          icon: 'fas fa-link',
          text: 'Theme-Fusion.com'
        }
      ],
      footerCoursesArray: ['Pass Plus', 'Intensive Course', 'Automatic', 'Instructor Training']
    }
  }

};
</script>

<style lang="scss">
@import './style/general.scss';

// Google Font
@import url('https://fonts.googleapis.com/css2?family=Open+Sans:ital,wght@0,300;0,400;0,700;1,300;1,400&display=swap');

  * {
    font-family: 'Open Sans', sans-serif;
  }

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
