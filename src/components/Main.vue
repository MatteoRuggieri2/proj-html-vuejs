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

                        <!-- Courses -->
                        <div class="col-60">
                            <SingleCourse />
                        </div>
                    </div>
                </div>
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
        SingleCourse
    },
    props: {
        courses: Array
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
                padding: 80px 0;
                background-image: url('../assets/img/promise-background.jpg');
                background-size: cover;
                background-position: bottom;
                background-repeat: no-repeat;

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
                }
            }

        }
    }

</style>