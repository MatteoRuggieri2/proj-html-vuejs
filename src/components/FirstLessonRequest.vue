<template>
    <div class="wrapper">
        <div class="first-lesson-request">
            <h2>First Lesson Free!</h2>
            <span class="request-description">When you make a block booking with us your first lesson is included free.</span>
            <input class="input-100" type="text" placeholder="Your Name*">
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
            border: 1px solid black;
            padding: 50px 40px;
            text-align: center;
            background-color: white;
            border-radius: 10px;
            position: absolute;
            top: -120px;
            left: 0;

            h2 {
                margin-bottom: 40px;
            }

            .request-description {
                display: inline-block;
                margin-bottom: 30px;
            }
        }
    }

</style>