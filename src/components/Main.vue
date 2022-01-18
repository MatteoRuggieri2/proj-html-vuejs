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


    </main>
</template>

<script>
import FirstLessonRequest from "./FirstLessonRequest.vue";

export default {
    name: 'Main',
    components: {
        FirstLessonRequest
    },
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
                    font-size: 40px;
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
    }

</style>