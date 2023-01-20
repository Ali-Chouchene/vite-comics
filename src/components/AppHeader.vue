<script>
export default {
    data() {
        return {
            currentI: 0,
            links: [
                {
                    text: 'Characters',
                    url: '#',
                    current: false,
                },
                {
                    text: 'Comics',
                    url: '#',
                    current: true,
                },
                {
                    text: 'Movies',
                    url: '#',
                    current: false,
                },
                {
                    text: 'TV',
                    url: '#',
                    current: false,
                },
                {
                    text: 'Games',
                    url: '#',
                    current: false,
                },
                {
                    text: 'Collectibles',
                    url: '#',
                    current: false,
                },
                {
                    text: 'Videos',
                    url: '#',
                    current: false,
                },
                {
                    text: 'Fans',
                    url: '#',
                    current: false,
                },
                {
                    text: 'News',
                    url: '#',
                    current: false,
                },
                {
                    text: 'Shop',
                    url: '#',
                    current: false,
                },
            ],
        }
    },
    computed: {
        currentActive() {
            this.links.forEach(link => {
                link.current = false;
            })
            return this.links[this.currentI].current = true;
        }
    },
    methods: {
        setCurrent(index) {
            this.currentI = index;
        },

    }
}

</script>

<template>
    <header>
        <div class="container">
            <div class="h-nav">
                <figure>
                    <img src="../assets/img/dc-logo.png" alt="DC-logo">
                </figure>
                <nav>
                    <ul>
                        <li v-for="(link, i) in links" @click="setCurrent(i)"><a :href="link.url"
                                :class="{ 'active': link.current }">{{ link.text }}</a>
                        </li>
                    </ul>
                </nav>
            </div>
        </div>
    </header>
</template>

<style lang="scss" scoped>
@use "../assets/scss/mixin" as *;

* {
    font-family: "Open Sans", sans-serif;
}

header {
    height: 15vh;
    padding: 1rem;
}

.h-nav {
    @include dflex-jcsb;

    img {
        cursor: pointer;
    }

}

ul {
    list-style: none;
    display: flex;

    li {
        height: 100%;

        a {
            text-decoration: none;
            padding: 1rem;
            font-size: 17px;
            font-weight: 600;

            &:hover {
                color: dodgerblue;
            }

        }
    }
}
</style>