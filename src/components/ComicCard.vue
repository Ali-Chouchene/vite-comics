<script>
export default {
    name: 'ComicCard',
    props: {
        comic: Object
    }
}
</script>
<template>
    <div class="comic">
        <img :src="comic.thumb" :alt="comic.series">
        <h5>{{ comic.series }}</h5>
    </div>
</template>
<style lang="scss" scoped>
.comic {
    width: 150px;
    word-wrap: break-word;
    margin-right: 2rem;


    h5 {
        color: white;
        padding-bottom: 2rem;
        padding-top: 0.5rem;

    }

    img {

        width: 100%;
        height: 150px;
        object-fit: cover;
        object-position: top;
    }
}
</style>