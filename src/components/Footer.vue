<template>
    <footer>

        <!-- Footer Top -->
        <div class="footer-top">
            <div class="container">
                <div class="wrapper">

                    <!-- Column 1 -->
                    <div class="col-25">
                        <img src="../assets/img/avada-drivers-logo-2x.png" alt="Logo Avada Driving School">
                        <p>Avada Driving School is the right choice fo experienced drivers looking for a refresher course, or the brand new driver wanting to pass first time.</p>
                    </div>

                    <!-- Column 2 -->
                    <div class="col-25">
                        <h5>CONTACT DETAILS</h5>
                        <ul>
                            <li v-for="(element, index) in footerDetails" :key="index">
                                <span class="icon"><i :class="element.icon"></i></span>
                                <span>{{ element.text }}</span>
                            </li>
                        </ul>
                    </div>

                    <!-- Column 3 -->
                    <div class="col-25">
                        <h5>COURSES</h5>
                        <ul>
                            <li v-for="(element, index) in footerCourses" :key="index">
                                
                                <span>
                                    <a href="#">
                                        <span class="icon"><i class="far fa-arrow-alt-circle-right"></i></span>
                                        {{ element }}
                                    </a>
                                </span>
                            </li>
                        </ul>
                    </div>

                    <!-- Column 4 -->
                    <div class="col-25">
                        <div>
                            <img src="../assets/img/labels.png" alt="">
                        </div>
                        <div>
                            <img src="../assets/img/labels.png" alt="">
                        </div>
                        <a class="footer-btn btn btn-primary" href="#">book now</a>
                    </div>

                </div>
            </div>
        </div>

        <!-- Footer Bottom -->
        <div class="footer-bottom">
            <div class="container">
                <div class="wrapper">

                    <!-- Copyright -->
                    <div>
                        <span>
                            c Copyright 2012 - 2020 | Avada Theme By <span class="text-primary">ThemeFusion</span> | All Rights Reserved | Powered by <span class="text-primary">WordPress</span>
                        </span>
                    </div>

                    <!-- Social Icon -->
                    <div>
                        <span><i class="fab fa-facebook-f"></i></span>
                        <span><i class="fab fa-twitter"></i></span>
                        <span><i class="fab fa-youtube"></i></span>
                        <span><i class="fab fa-instagram"></i></span>
                    </div>
                </div>
            </div>
        </div>
    </footer>
</template>

<script>
export default {
    name: 'Footer',
    props: {
        footerDetails: Array,
        footerCourses: Array
    }
}
</script>

<style lang="scss" scoped>
@import '../style/variables.scss';

    footer {

        .footer-top {
            padding: 50px 0;
            background-image: url('../assets/img/footer-background-color.jpg');
            background-size: cover;
            background-position: center;
            background-repeat: no-repeat;

            // test
            color: white;

            .wrapper {
                display: flex;

                .col-25 {
                    padding: 0 20px;

                    ul {

                        li {
                            display: flex;

                            .icon {
                                margin-right: 15px;
                            }

                            a {
                                color: $primary_color;
                            }
                        }
                    }

                    
                }
            }
        }

        .footer-bottom {
            background-color: #1c1d1e;
            padding: 40px 0;

            .wrapper {
                display: flex;
                justify-content: space-between;
            }
        }
    }
</style>