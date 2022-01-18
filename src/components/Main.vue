<template>
    <main>

        <!-- Jumbotron -->
        <div class="jumbotron">
            <div class="container">
                <div class="wrapper">

                    <!-- Jumbo-text -->
                    <div class="jumbo-text">
                        <h1>Drive with Avada</h1>
                        <h3>We offer the finest driving tuition money can buy</h3>
                    </div>

                </div>
            </div>
        </div>

        <!-- Section - First Lesson -->
        <section class="first-lesson-sect">
            <div class="container">
                <div class="wrapper">
                    <div class="col-45">
                        <h2>Get Behind The Wheel</h2>
                        <h4>Lorem ipsum dolor sit amet Temconsectetur adipisicing elit. Quaerat, tempore sed. dolor sit amet consectetur adipisicing elit.</h4>
                        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Quaerat, tempore sed. Tempore eligendi, alias ipsam neque perspiciatis qui blanditiis illo non, perferendis omnis labore officia nisi inventore molestias magnam voluptas.Lorem ipsum dolor sit amet consectetur adipisicing elit. Quaerat, tempore sed. Tempore eligendi, alias ipsam neque perspiciatis qui blanditiis illo non, perferendis omnis labore officia nisi inventore molestias magnam voluptas.</p>
                    </div>
                    <div class="col-45">
                        <FirstLessonRequest />
                    </div>
                </div>
            </div>
        </section>

        <!-- Section - Courses -->
        <section class="courses-sect">
            
            <!-- Number Banner -->
            <div class="number-banner">
                <div class="container">
                    <div class="wrapper">
                        <div>
                            <h2>Start Learning to Drive Today</h2>
                            <h3>Give us a call to shedule your first driving lesson</h3>
                        </div>
                        <div>
                            <span>--icon-- </span>
                            <h2 class="telephone-number">1-800-555-555</h2>
                        </div>
                    </div>
                </div>
            </div>

            <!-- Courses -->
            <div class="courses">
                <div class="container">
                    <div class="wrapper">

                        <!-- Course Info Tab -->
                        <div class="col-40">
                            <div class="course-info-tab">
                                <h2>Courses</h2>
                                <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Aliquid labore eligendi esse quibusdam modi, iusto amet tempore obcaecati est aspernatur minus quas quod nisi incidunt excepturi numquam maxime officia sapiente.</p>
                                <a class="btn btn-primary" href="#">course information</a>
                                <img class="new-tag-img" src="../assets/img/new-corner.jpg" alt="Tag 'New'">
                            </div>
                        </div>

                        <!-- Courses Container -->
                        <div class="col-60">
                            <div class="courses-container">
                                <SingleCourse v-for="(element, index) in courses" :key="index" :singleCourse="element" />
                            </div>
                        </div>
                    </div>

                    <!-- Percentage Cards -->
                    <div class="percentage-card-container">
                        <div class="col-30">
                            <div class="card">
                                <div class="circle">95%</div>
                                <div class="percentage-name">pass rate</div>
                            </div>
                        </div>
                        <div class="center">
                            <div class="card">
                                <div class="circle">100%</div>
                                <div class="percentage-name">referral rate</div>
                            </div>
                        </div>
                        <div class="col-30">
                            <div class="card">
                                <div class="circle">0%</div>
                                <div class="percentage-name">accident rate</div>
                            </div>
                        </div>
                    </div>
                </div>
                
                <svg class="latestnews-bottom" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1440 320">
                    <path fill="#ffffff" fill-opacity="1" d="M0,192L720,288L1440,192L1440,320L720,320L0,320Z"></path>
                </svg>
                
            </div>

        </section>


    </main>
</template>

<script>
import FirstLessonRequest from "./FirstLessonRequest.vue";
import SingleCourse from "./SingleCourse.vue";

export default {
    name: 'Main',
    components: {
        FirstLessonRequest,
        SingleCourse,
    },
    props: {
        courses: Array,
        percentagesArray: Array
    }
}
</script>

<style lang="scss" scoped>
@import '../style/variables.scss';

    main {

        // Jumbotron
        .jumbotron {
            // min-height: 80vh;
            background-image: url('../assets/img/homepage-hero-background.jpg');
            background-size: cover;
            background-position: center;
            background-repeat: no-repeat;

            .wrapper {

                .jumbo-text {
                    padding: 40vh 0 30vh;
                    color: $secondary_color;

                    h1 {
                        font-size: 60px;
                        margin-bottom: 20px;
                    }

                    h3 {
                        font-size: 30px;
                    }
                }
            }
        }

        // Section - First Lesson
        .first-lesson-sect {

            .wrapper {
                display: flex;
                justify-content: space-between;

                h2 {
                    margin-bottom: 30px;
                    font-size: $section_title_font_size;
                }

                h4 {
                    margin-bottom: 20px;
                    font-size: 24px;
                }

                p {
                    font-size: 18px;
                }
            }
        }

        // Section - Courses
        .courses-sect {

            .number-banner {
                padding-top: 80px;
                padding-bottom: 100px;
                color: $secondary_color;
                background-image: url('../assets/img/horizontal-cta-background.jpg');
                background-size: cover;
                background-position: center;
                background-repeat: no-repeat;

                .wrapper {
                    display: flex;
                    justify-content: space-between;
                    align-items: center;

                    h2 {
                        font-size: $section_title_font_size;
                    }

                    .telephone-number {
                        display: inline-block;
                    }
                }
            }

            .courses {
                padding: 80px 0 150px;
                background-image: url('../assets/img/promise-background.jpg');
                background-size: cover;
                background-position: bottom;
                background-repeat: no-repeat;
                position: relative;

                .wrapper {
                    display: flex;

                    .course-info-tab {
                        // margin: 50px 0;
                        padding: 50px;
                        text-align: center;
                        background-color: white;
                        border: 1px solid black;
                        border-radius: 10px;
                        overflow: hidden;
                        position: relative;
                        bottom: 120px;
                        left: 0;

                        h2 {
                            margin-bottom: 40px;
                            font-size: $section_title_font_size;
                        }

                        p {
                            margin-bottom: 30px;
                        }

                        .new-tag-img {
                            display: block;
                            width: 15%;
                            position: absolute;
                            top: 0;
                            left: 0;
                        }
                    }

                    .courses-container {
                        padding: 0 20px;
                        display: flex;
                    }
                }

                .percentage-card-container {
                    display: flex;
                    justify-content: space-between;
                    position: absolute;
                    top: 75%;
                    left: 50%;
                    transform: translateX(-50%);
                    z-index: 2;

                    // test
                    // background-color: darkcyan;
                    // border: 2px solid red;

                    .center {
                        flex-grow: 1;
                        margin: 0 10px;
                    }

                    .card {
                        background-color: white;
                        display: flex;
                        flex-direction: column;
                        align-items: center;
                        padding: 50px;
                        border-top: 6px solid $primary_color;
                        border-radius: 10px;
                        box-shadow: 0 4px 8px 0 gray, 0 6px 20px 0 gray;

                        // test
                        // border: 1px solid black;

                        .circle {
                            margin-bottom: 50px;
                            width: 11vw;
                            height: 11vw;
                            border-radius: 50%;
                            border: 10px solid $primary_color;
                            display: flex;
                            align-items: center;
                            justify-content: center;
                        }
                    }
                }

                .latestnews-bottom {
                    display: block;
                    position: absolute;
                    bottom: 0;
                    left: 0;
                }
            }

        }
    }

</style>