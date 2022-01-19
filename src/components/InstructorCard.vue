<template>
    <div class="instructor-card">
        <div class="card-primary">
            <img :src="require(`../assets/img/${singleInstructor.img}`)" :alt="singleInstructor.name">
            <h4>{{ singleInstructor.name }}</h4>
            <div class="icon-container">
                <span>--icon--</span>
                <span>--icon--</span>
                <span>--icon--</span>
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

    .instructor-card {
        // width: calc(100% / 3);
        width: 32%;

        .card-primary {
            padding: 40px;

            img {
                margin-bottom: 40px;
            }

            h4 {
                margin-bottom: 10px;
            }

            .icon-container {
                margin-bottom: 10px;
            }

            p {
                text-align: center;
            }
        }
    }

</style>