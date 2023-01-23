<script>
import FooterNav from './subcompnets/FooterNav.vue';
import FooterBottom from './subcompnets/FooterBottom.vue';
export default {
    components: { FooterNav, FooterBottom },
}

</script>

<template>
    <footer>
        <FooterNav />

        <div class="container">
            <div class="f-main">
                <div class="more-info">
                    <div>
                        <h3>DC COMICS</h3>
                        <ul>
                            <li><a href="#">Characters</a></li>
                            <li><a href="#">Comics</a> </li>
                            <li><a href="#">Movies</a> </li>
                            <li><a href="#">TV</a> </li>
                            <li><a href="#">Games</a> </li>
                            <li><a href="#">Videos</a> </li>
                            <li><a href="#">News</a> </li>
                        </ul>
                        <h3>SHOP</h3>
                        <ul>
                            <li><a href="#">Shop DC</a></li>
                            <li><a href="#">Shop DC Collectibles</a> </li>

                        </ul>
                    </div>
                    <div>
                        <h3>DC</h3>
                        <ul>
                            <li><a href="#">Terms Of Use</a></li>
                            <li><a href="#">Privacy Policy (New)</a> </li>
                            <li><a href="#">Ad Choice</a> </li>
                            <li><a href="#">Advertising</a> </li>
                            <li><a href="#">Jobs</a> </li>
                            <li><a href="#">Subscriptions</a> </li>
                            <li><a href="#">Talent Workshops</a> </li>
                            <li><a href="#">CSPC Certificates</a> </li>
                            <li><a href="#">Ratings</a> </li>
                            <li><a href="#">Shop Help</a> </li>
                            <li><a href="#">Contact Us</a> </li>
                        </ul>
                    </div>
                    <div>
                        <h3>SITES</h3>
                        <ul>
                            <li><a href="#">DC</a></li>
                            <li><a href="#">MAD Magazine</a> </li>
                            <li><a href="#">DC Kids</a> </li>
                            <li><a href="#">DC Universe</a> </li>
                            <li><a href="#">DC Power Visa</a> </li>
                        </ul>
                    </div>

                </div>
                <div class="f-logo">
                    <img src="../assets/img/dc-logo-bg.png" alt="dc-logo">
                </div>
            </div>
        </div>
        <FooterBottom />

    </footer>
</template>

<style lang="scss" scoped>
@use "../assets/scss/mixin" as *;


footer {
    // padding-top: 60px;
    position: relative;
    height: calc(100vh - 32vh);
    background-image: url(../assets/img/footer-bg.jpg);
    background-repeat: no-repeat;
    background-position: top;
    background-size: cover;

    .more-info {
        width: 35%;
        margin-top: 20px;
        display: flex;
        gap: 2.3rem;
        flex-wrap: wrap;
        align-content: flex-start;

        h3 {
            color: white;
            margin: 0.7rem 0;
        }

        ul {
            list-style: none;

            li {

                a {
                    text-decoration: none;
                    color: gray;
                    font-weight: 500;
                    line-height: 25px;
                    font-size: small;

                    &:hover {
                        color: dodgerblue
                    }
                }

            }
        }
    }

    img {
        position: absolute;
        top: 60px;
        right: 300px;
        z-index: 0;
    }
}
</style>