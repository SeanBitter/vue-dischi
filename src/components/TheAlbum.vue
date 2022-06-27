<template>
        <div class="p-3 text-center cards-container">
            <div>
                <img :src="info.poster" :alt="info.title" class="img-card">
            </div>
            <h5 class="py-2 text-center">{{info.title.toUpperCase()}}</h5>
            <h6>{{info.author}}</h6>
            <h6>{{info.year}}</h6>
        </div>
</template>

<script>
export default {
    name: 'TheAlbum',
    props: {
        info: Object,
    }
}
</script>

<style lang="scss" scoped>
@import "../assets/scss/variables";
.cards-container {
    background-color: $secondary;
    height: 100%;

    h6 {
        color: grey;
    }

    .img-card {
        width: 100%;
        aspect-ratio: 1;
    }
}

</style>