<template>
    <div class="news">
        <img :src="require(`../assets/img/${singleNews.img}`)" :alt="singleNews.name">
        <h4>{{ singleNews.name }}</h4>
        <div class="info-news">
            <span>{{ singleNews.date }}</span>
            <span> | </span>
            <span class="comments">{{ singleNews.comments }} Comments</span>
        </div>
        <p>{{ singleNews.text }}</p>
    </div>
</template>

<script>
export default {
    name: 'News',
    props: {
        singleNews: Object
    }
}
</script>

<style lang="scss" scoped>
@import '../style/variables.scss';

    .news {
        width: 100%;
        margin: 0 15px 40px;
        padding-bottom: 30px;
        text-align: center;

        img {
            margin-bottom: 15px;
        }

        h4 {
            color: $primary_color;
            margin-bottom: 10px;
            font-size: 24px;
        }

        .info-news {
            margin-bottom: 20px;
            font-size: 12px;

            .comments {
                color: $primary_color;
            }
        }

        p {
            font-size: 16px;
        }
    }

</style>