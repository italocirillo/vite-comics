<script>
export default {
    name: "AppHeader",
    data() {
        return {
            links: [
                {
                    text: "characters",
                    url: "#",
                    current: false,
                },
                {
                    text: "comics",
                    url: "#",
                    current: true,
                },
                {
                    text: "movies",
                    url: "#",
                    current: false,
                },
                {
                    text: "tv",
                    url: "#",
                    current: false,
                },
                {
                    text: "games",
                    url: "#",
                    current: false,
                },
                {
                    text: "collectibles",
                    url: "#",
                    current: false,
                },
                {
                    text: "videos",
                    url: "#",
                    current: false,
                },
                {
                    text: "fans",
                    url: "#",
                    current: false,
                },
                {
                    text: "news",
                    url: "#",
                    current: false,
                },
                {
                    text: "shop",
                    url: "#",
                    current: false,
                },
            ]
        }
    }
}
</script>

<template>
    <header>
        <div class="container">
            <div class="sezione-logo">
                <a href="#">
                    <img class="logo" src="../assets/img/dc-logo.png" alt="">
                </a>
            </div>
            <nav>
                <ul>
                    <li v-for="link in links" :class="link.current ? 'active' : ''">
                        <a href=" {{ link.url }}">{{ link.text }}</a>
                    </li>
                </ul>
            </nav>
        </div>
    </header>
</template>

<style scoped lang="scss">
@use "../style/partials/variables" as*;

header {
    width: 100%;
    background-color: white;
    position: fixed;
}

header .container {
    height: 120px;
    z-index: 1;
    display: flex;
    justify-content: space-between;

    .sezione-logo {
        padding: 0.5em 0em;
        width: 20%;
    }

    nav {
        width: 80%;
        display: flex;
        align-items: center;

        ul {
            list-style: none;
            height: 100%;
            line-height: 100%;
            display: flex;
            align-items: center;

            li {
                height: 100%;
                display: flex;
                align-items: center;
                cursor: pointer;

                a {
                    text-decoration: none;
                    color: $primary-color;
                    font-weight: 900;
                    text-transform: uppercase;
                    padding: 0em 1em;
                }

                &.active a,
                &:hover a {
                    color: $active-color;
                }

                &.active,
                &:hover {
                    border-bottom: 2px solid $active-color;
                }
            }
        }
    }
}
</style>