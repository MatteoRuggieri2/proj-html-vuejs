<template>
    <footer>
        <!-- Footer Bottom -->
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
                        <h5>title</h5>
                        <ul>
                            <li>
                                <span><i>-icon-</i></span>
                                <span>text</span>
                            </li>
                        </ul>
                    </div>

                    <!-- Column 3 -->
                    <div class="col-25">
                        <h5>title</h5>
                        <ul>
                            <li>
                                <span>-icon-</span>
                                <span>text</span>
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
                        <a href="#"></a>
                    </div>

                </div>
            </div>
        </div>

        <!-- Footer Bottom -->
        <div class="footer-bottom">
            <div class="container">

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
                }
            }
        }
    }
</style>