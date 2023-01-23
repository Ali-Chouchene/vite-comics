<script>
export default {
    data() {
        return {
            socials: [
                {
                    text: 'facebook',
                    img: 'footer-facebook.png'
                },
                {
                    text: 'twitter',
                    img: 'footer-twitter.png',
                },
                {
                    text: 'youtube',
                    img: 'footer-youtube.png',
                },
                {
                    text: 'pinterest',
                    img: 'footer-pinterest.png',
                },
                {
                    text: 'periscope',
                    img: 'footer-periscope.png',
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
    <div class="f-b-bg">
        <div class="container">
            <div class="f-b">
                <div>
                    <button>
                        <h3>SIGN-UP NOW!</h3>
                    </button>
                </div>
                <nav>

                    <ul>
                        <h3>FOLLOW US</h3>
                        <li v-for="(social) in socials"><a href="#"><img :src="buildImgUrl(social.img)"
                                    :alt="social.text"></a>
                        </li>
                    </ul>
                </nav>
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>
@use "../../assets/scss/mixin" as *;

* {
    font-family: "Open Sans", sans-serif;
}

.f-b-bg {
    position: fixed;
    bottom: 0;
    right: 0;
    left: 0;
    z-index: 2;
    background-color: rgb(48, 48, 48);
}

.f-b {
    height: 13vh;
    @include dflex-jcsb;

    button {
        padding: 15px 20px;
        color: white;
        background-color: transparent;
        border: 2px solid dodgerblue;
        cursor: pointer;

        &:hover {
            background-color: dodgerblue;
            color: black;
        }
    }

    ul {
        list-style: none;
        display: flex;
        align-items: center;

        h3 {
            color: dodgerblue;
            padding-right: 10px;
        }

        li {
            height: 100%;

            a {
                text-decoration: none;
                padding: 1rem;
                font-size: 17px;
                font-weight: 600;
                width: 15%;
                aspect-ratio: 3/2;
                object-fit: contain;
                mix-blend-mode: color-dodge;
                margin: 0;

                &:hover {
                    box-shadow: 5px 5px 5px 5px dodgerblue;
                }

            }
        }
    }

}
</style>