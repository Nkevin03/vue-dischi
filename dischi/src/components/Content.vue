<template>
    <div v-if="Albums" class="container">
    <Card v-for="(album, i) in Albums" :key="`album_${i}`"
        :poster="album.poster" :title="album.title" :author="album.author" :year="album.year" :genre="album.genre"/>
    </div>
</template>

<script>
import Card from '@/components/Card.vue';
import axios from 'axios';
export default {
    name: 'Albums',
    components: {
        Card ,
    },
    data() {
        return {
            Albums: null,
        };
    },
    created() {
        this.getAlbums();
    },
    methods: {
        getAlbums() {
            axios.get('https://flynn.boolean.careers/exercises/api/array/music').then(received => {
                this.Albums = received.data.response;
            });
        },
    },
}
</script>

<style scoped lang="scss">
    .container{
        display: flex;
        flex-wrap: wrap;
        justify-content: center;
        width: 90%;
        margin: 0 auto;
    }
</style>