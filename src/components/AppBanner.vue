<script>

export default {
    name: "AppBanner",
    data() {
        return {
            bannerList: [
                {
                    url: "#",
                    src: "buy-comics-digital-comics.png",
                    name: "digital comics",
                },
                {
                    url: "#",
                    src: "buy-comics-merchandise.png",
                    name: "dc merchandise",
                },
                {
                    url: "#",
                    src: "buy-comics-subscriptions.png",
                    name: "subscription",
                },
                {
                    url: "#",
                    src: "buy-comics-shop-locator.png",
                    name: "comic shop locator",
                },
                {
                    url: "#",
                    src: "buy-dc-power-visa.svg",
                    name: "dc power visa",
                },

            ]
        }
    },
    methods: {
        getImagePath(img) {
            return new URL(`../assets/img/${img}`, import.meta.url).href;
        }
    }
}
</script>

<template>
    <div class="banner">
        <div class="container">
            <ul>
                <li v-for="element in bannerList">
                    <a :href="element.url">
                        <img :src="getImagePath(element.src)" :alt="element.name">
                        <p>{{ element.name }}</p>
                    </a>
                </li>
            </ul>
        </div>
    </div>
</template>

<style scoped lang="scss">
@use "../style/partials/variables" as *;

.banner {
    background-color: $active-color;
    padding: 2em 0em;

    ul {
        width: 100%;
        list-style: none;
        display: flex;
        justify-content: space-between;
        align-items: center;

        a {
            text-decoration: none;
            color: white;
        }

        li {
            width: calc(100%/5);

            a {
                display: flex;
                justify-content: center;
                align-items: center;
                gap: 1em;

                img {
                    width: 16%;
                }

                p {
                    text-transform: uppercase;
                    font-weight: 300;
                    font-size: 0.8rem;
                }
            }
        }

    }
}
</style>