<script>
import { registerRuntimeCompiler } from 'vue';

export default {
    name: "AppFooter",
    data() {
        return {
            list: [
                {
                    nomeLista: "dc comics",
                    elementiLista: [
                        {
                            name: "Characters",
                            url: "#",
                            status: false,
                        },
                        {
                            name: "Comics",
                            url: "#",
                            status: false,
                        },
                        {
                            name: "Comics",
                            url: "#",
                            status: false,
                        },
                        {
                            name: "Movies",
                            url: "#",
                            status: false,
                        },
                        {
                            name: "TV",
                            url: "#",
                            status: false,
                        },
                        {
                            name: "Games",
                            url: "#",
                            status: false,
                        },
                        {
                            name: "Videos",
                            url: "#",
                            status: false,
                        },
                        {
                            name: "News",
                            url: "#",
                            status: false,
                        },
                    ]
                },
                {
                    nomeLista: "shop",
                    elementiLista: [
                        {
                            name: "Shop DC",
                            url: "#",
                            status: false,
                        },
                        {
                            name: "Shop DC Collectibles",
                            url: "#",
                            status: false,
                        },
                    ]
                },
                {
                    nomeLista: "dc",
                    elementiLista: [
                        {
                            name: "Term Of Use",
                            url: "#",
                            status: false,
                        },
                        {
                            name: "Privacy policy(New)",
                            url: "#",
                            status: false,
                        },
                        {
                            name: "Ad Choises",
                            url: "#",
                            status: false,
                        },
                        {
                            name: "Advetising",
                            url: "#",
                            status: false,
                        },
                        {
                            name: "Jobs",
                            url: "#",
                            status: false,
                        },
                        {
                            name: "Subscription",
                            url: "#",
                            status: false,
                        },
                        {
                            name: "Talent Workshopes",
                            url: "#",
                            status: false,
                        },
                        {
                            name: "CPSC Certificates",
                            url: "#",
                            status: false,
                        },
                        {
                            name: "Rating",
                            url: "#",
                            status: false,
                        },
                        {
                            name: "Shop Help",
                            url: "#",
                            status: false,
                        },
                        {
                            name: "Contact Us",
                            url: "#",
                            status: false,
                        },
                    ]
                },
                {
                    nomeLista: "sities",
                    elementiLista: [
                        {
                            name: "DC",
                            url: "#",
                            status: false,
                        },
                        {
                            name: "MAD Magazione",
                            url: "#",
                            status: false,
                        },
                        {
                            name: "DC Kids",
                            url: "#",
                            status: false,
                        },
                        {
                            name: "DC Universe",
                            url: "#",
                            status: false,
                        },
                        {
                            name: "DC Power Visa",
                            url: "#",
                            status: false,
                        },
                    ]
                }
            ],
            footerIconList: [
                {
                    url: "#",
                    name: "facebook",
                },
                {
                    url: "#",
                    name: "twitter",
                },
                {
                    url: "#",
                    name: "youtube",
                },
                {
                    url: "#",
                    name: "pinterest",
                },
                {
                    url: "#",
                    name: "periscope",
                }
            ]
        }
    },
    methods: {
        getImagePath(img) {
            return new URL(`../assets/img/footer-${img}.png`, import.meta.url).href;
        }
    }
}
</script>

<template>
    <footer>
        <div class="footer-top">
            <div class="container">
                <div class="row">
                    <ul class="col1">
                        <li class="macro-list" v-for="elementoMacroList in list">
                            <h3>{{ elementoMacroList.nomeLista }}</h3>
                            <ul>
                                <li v-for="elemento in elementoMacroList.elementiLista">
                                    <a href="{{ elemento.url }}">{{ elemento.name }}</a>
                                </li>
                            </ul>
                        </li>
                    </ul>
                    <div class="col2">
                        <img src="../assets/img/dc-logo-bg.png" alt="">
                    </div>
                </div>
            </div>
        </div>
        <div class="footer-bottom">
            <div class="container">
                <div class="sing-up">
                    <h4>sing-up now</h4>
                </div>
                <nav class="contacts">
                    <h3>follow us</h3>
                    <ul>
                        <li v-for="elemento in footerIconList">
                            <a href="">
                                <img :src="getImagePath(elemento.name)" alt="">
                            </a>
                        </li>
                    </ul>
                </nav>
            </div>
        </div>
    </footer>
</template>

<style scoped lang="scss">
@use "../style/partials/variables" as *;

footer {
    ul {
        list-style: none;
    }

    .footer-top {
        background-image: url(../assets/img/footer-bg.jpg);
        background-size: cover;
        position: center center;
        padding: 1em 0em;
        position: relative;
        z-index: -2;

        ul {
            list-style: none;

            a {
                text-decoration: none;
                color: lighten($primary-color, 10%);
            }
        }

        .row {
            display: flex;
            justify-content: center;
            height: 300px;

            .col1 {
                width: 50%;
                display: flex;
                flex-direction: column;
                align-items: start;
                flex-wrap: wrap;

                .macro-list {
                    padding: 0.5em 0.5em;

                    h3 {
                        text-transform: uppercase;
                        padding-bottom: 0.5em;
                        color: white;
                    }
                }
            }

            .col2 {
                width: 50%;

                img {
                    width: 100%;
                    position: relative;
                    bottom: 50%;
                    right: 0%;
                }
            }
        }
    }

    .footer-bottom {
        padding: 2em 0em;
        background-color: #303030;

        .container {
            display: flex;
            justify-content: space-between;

            .sing-up {
                h4 {
                    color: white;
                    border: 2px solid $active-color;
                    text-transform: uppercase;
                    padding: 0.9em 1em;
                    cursor: pointer;
                }
            }

            .contacts {
                display: flex;
                justify-content: center;
                gap: 2em;
                align-items: center;

                h3 {
                    text-transform: uppercase;
                    font-size: 1.5rem;
                    color: $active-color;
                }

                ul {
                    display: flex;
                    gap: 1em;
                    align-items: center;
                }
            }
        }
    }
}
</style>