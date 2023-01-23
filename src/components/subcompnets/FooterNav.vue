<script>
export default {
    data() {
        return {
            cards: [
                {
                    text: 'DIGITAL COMICS',
                    img: 'buy-comics-digital-comics.png',
                },
                {
                    text: 'DC MERCHANDISE',
                    img: 'buy-comics-merchandise.png',
                },
                {
                    text: 'SUBSCRIPTION',
                    img: 'buy-comics-subscriptions.png',
                },
                {
                    text: 'COMIC SHOP LOCAL',
                    img: 'buy-comics-shop-locator.png',
                },
                {
                    text: 'DC POWER VISA',
                    img: 'buy-dc-power-visa.svg',
                }
            ],
        }
    },
    methods: {
        buildImgUrl(img) {
            const url = new URL(`../../assets/img/${img}`, import.meta.url);
            console.log(url.href)
            return url.href;

        }
    }
}

</script>

<template>
    <div class="bg">
        <div class="container">
            <div class="row">
                <div v-for="card in cards" class="col">
                    <img :src="buildImgUrl(card.img)" alt="">
                    <h5>{{ card.text }}</h5>
                </div>
            </div>

        </div>
    </div>
</template>

<style lang="scss" scoped>
@use "../../assets/scss/mixin" as *;

.bg {
    position: sticky;
    top: 0;
    left: 0;
    right: 0;
    z-index: 1;
    height: 150px;
    background-color: rgb(2, 130, 249);

    .container {
        height: 100%;

        .row {
            @include dflex-jcsa;
            height: 100%;

            .col {
                height: 100%;
                @include dflex-aic;
                color: white;


                h5 {
                    cursor: pointer;

                    &:hover {
                        color: black;
                    }
                }

                img {
                    height: 60px;
                    width: 50px;
                }
            }
        }
    }



}
</style>