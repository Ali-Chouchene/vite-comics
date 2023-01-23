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
        <label>
            <h3>{{ comic.series }}</h3>
            <h4>price: {{ comic.price }}</h4>
        </label>
        <h5>{{ comic.series }}</h5>
    </div>
</template>
<style lang="scss" scoped>
.comic {
    width: calc(90% / 6);
    word-wrap: break-word;
    cursor: pointer;


    &:hover {
        filter: grayscale(100%);
    }

    &:hover label {
        display: block;
    }


    h5 {
        color: white;
        padding-bottom: 2rem;
        padding-top: 0.5rem;

    }

    img {

        width: 100%;
        height: 180px;
        object-fit: cover;
        object-position: top;
        position: relative;
    }

    label {
        background-color: rgba(0, 0, 0, 0.404);
        position: absolute;
        top: 30px;
        left: 0;
        height: 50%;
        width: 100%;
        color: white;
        display: none;
        text-align: center;
        line-height: 30px;
        cursor: pointer;

    }
}
</style>