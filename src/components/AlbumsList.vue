<template>
    <div class="container overflow-auto py-5">
        <div class="row row-cols-5 g-3">
            <div class="col" v-for="album in albums" :key="album.title">
                <TheAlbum :info="album"></TheAlbum>
            </div>
        </div>
    </div>
</template>

<script>
    import TheAlbum from "./TheAlbum.vue";
    import axios from 'axios';

    export default {
        name: 'AlbumsList',
        components: { TheAlbum },

        data() {
            return {
                dataUrl: 'https://flynn.boolean.careers/exercises/api/array/music',
                albums: [],
            };
        },

        methods: {
            fetchAlbums() {
                axios.get(this.dataUrl).then((response) => {
                    this.albums = response.data.response;
                });
            },
        },

        mounted() {
            this.fetchAlbums();
        },
    } 
</script>

<style lang="scss" scoped>

</style>