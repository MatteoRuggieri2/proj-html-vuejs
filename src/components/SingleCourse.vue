<template>
    <div class="single-course">
        <img :src="require(`../assets/img/${singleCourse.img}`)" :alt="singleCourse.name">
        <h3>{{ singleCourse.name }}</h3>
        <a class="btn btn-bckg-blue" href="#">Learn More</a>
    </div>
</template>

<script>
export default {
    name: 'SingleCourse',
    props: {
        singleCourse: Object
    }
}
</script>

<style lang="scss" scoped>
@import '../style/variables.scss';

    .single-course {
        // background-color: mediumturquoise;
        // border: 1px solid black;
        padding: 0 20px;
        text-align: center;
        color: $third_color;

        img {
            margin-bottom: 20px;
        }

        h3 {
            margin-bottom: 15px;
        }
    }
</style>