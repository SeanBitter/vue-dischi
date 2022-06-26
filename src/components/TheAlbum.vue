<template>
    <div>
        <div>
            <div>
                <img :src="info.poster" :alt="info.title" height="120" weight="120">
            </div>
            <h2>{{info.title}}</h2>
            <h6>{{info.author}}</h6>
            <h6>{{info.year}}</h6>
        </div>
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
</style>