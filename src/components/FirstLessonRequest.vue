<template>
    <div class="wrapper">
        <div class="first-lesson-request box-shadow">
            <h2>First Lesson Free!</h2>
            <span class="request-description">When you make a block booking with us your first lesson is included free.</span>
            <div class="input-name">
                <input class="input-100" type="text" placeholder="Your Name*">
                <img src="../assets/img/image.png" alt="elemento decorativo">
            </div>
            <input class="input-100" type="email" placeholder="Email*">
            <input class="input-100" type="text" placeholder="Telephone">
            <input class="input-100" type="text" placeholder="Location">
            <a class="btn btn-primary" href="#">request a callback</a>
        </div>
    </div>
</template>

<script>
export default {
    name: 'FirstLessonRequest'
}
</script>

<style lang="scss" scoped>
@import '../style/variables.scss';

    .wrapper {
        position: relative;

        .first-lesson-request {
            padding: 50px 40px;
            text-align: center;
            background-color: white;
            border-radius: 10px;
            position: absolute;
            top: -120px;
            left: 0;

            h2 {
                font-size: 30px;
                margin-bottom: 40px;
                color: $primary_color;
            }

            .request-description {
                display: inline-block;
                margin-bottom: 30px;
                font-size: 15px;
                line-height: 30px;
                color: $primary_text_color;
            }

            .input-name {
                position: relative;

                img {
                    width: 18px;
                    position: absolute;
                    top: 50%;
                    right: 10px;
                    transform: translateY(-50%);
                }
            }
        }
    }

</style>