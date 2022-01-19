<template>
    <div class="instructor-card">
        <div class="card-primary">
            <img :src="require(`../assets/img/${singleInstructor.img}`)" :alt="singleInstructor.name" :title="singleInstructor.name">
            <h4>{{ singleInstructor.name }}</h4>
            <div class="icon-container">
                <span><a href="#"><i class="fab fa-facebook-f"></i></a></span>
                <span><a href="#"><i class="fab fa-twitter"></i></a></span>
                <span><a href="#"><i class="fab fa-instagram"></i></a></span>
            </div>
            <p>{{ singleInstructor.text }}</p>
        </div>
    </div>
</template>

<script>
export default {
    name: 'InstructorCard',
    props: {
        singleInstructor: Object
    },
    methods: {
        // centerColumn: function(index) {
        //     if(index === 1) {
        //          DA FARE CON STILE INLINE
        //         .card-primary{
        //             width: 34px;
        //             margin: 0 10px;
        //         }
        //     }
        // }
    }
}
</script>

<style lang="scss" scoped>
@import '../style/variables.scss';

    .instructor-card {
        // width: calc(100% / 3);
        width: 32%;

        .card-primary {
            padding: 40px;
            box-shadow: 0px 13px 20px 0 rgb(156, 156, 156);
            color: $primary_text_color;

            img {
                margin-bottom: 40px;
            }

            h4 {
                margin-bottom: 10px;
                color: $title_text_color;
                font-size: 25px;
            }

            .icon-container {
                margin-bottom: 10px;

                a {
                    margin: 0 10px;
                }
            }

            p {
                text-align: center;
                font-size: 15px;
                line-height: 30px;
            }
        }
    }

</style>