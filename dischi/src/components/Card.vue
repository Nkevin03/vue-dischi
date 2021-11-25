<template>
    <div class="album">
        <div class="album-info">
            <div class="card_img">
                <img :src="poster">
            </div>
            <div class="card-info">
                <h2>{{title}}</h2>
                <h3>{{author}}</h3>
                <h4>{{genre}}</h4>
                <h4>{{year}}</h4>
            </div>
        </div>
    </div>
</template>

<script>
export default {
name: 'Albumcard',
    props: {
        poster: String,
        title: String,
        author: String,
        genre: String,
        year: String,
    },
}
</script>

<style scoped lang="scss">
    @import '@/styles/variables.scss';

    .album{
        display: flex;
        justify-content: center;
        padding: 10px;
        margin: 15px;
        background-color: $third-color;
        width: calc(100% / 6);
    }
    .album-info{
        text-align: center;

        img{
            width: 100%;
        }
        .card-info{
            color: $text;
        }
    }
</style>