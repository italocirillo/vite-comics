<script>
import Card from './Card.vue';

export default {
    name: "AppCardHero",
    components: {
        Card,
    },
    data() {
        return {
            cards: [
                {
                    thumb: 'https://www.coverbrowser.com/image/action-comics/1-1.jpg',
                    price: '$19.99',
                    series: 'Action Comics',
                    type: 'comic book',
                },
                {
                    thumb: 'https://www.panini.it/media/catalog/product/cache/a5b5dd3adfe0d321084804c738f29601/M/1/M1BLLA015ISBN_0.jpg',
                    price: '$3.99',
                    series: 'American Vampire 1976',
                    type: 'comic book',
                },
                {
                    thumb: 'https://media.wired.com/photos/593384dad80dd005b42b2817/master/w_2560%2Cc_limit/Aquaman-16.jpg',
                    price: '$16.99',
                    series: 'Aquaman',
                    type: 'graphic novel',
                },
                {
                    thumb: 'https://d29xot63vimef3.cloudfront.net/image/batgirl/1-1.jpg',
                    price: '$2.99',
                    series: 'Batgirl',
                    type: 'comic book',
                },
                {
                    thumb: 'https://static.posters.cz/image/750/locandine-film-in-plexiglass-batman-prowl-comic-cover-i69653.jpg',
                    price: '$3.99',
                    series: 'Batman',
                    type: 'comic book',
                },
                {
                    thumb: 'https://static.wikia.nocookie.net/marvel_dc/images/5/50/Batman_Beyond_v.1_1.jpg',
                    price: '$2.99',
                    series: 'Batman Beyond',
                    type: 'comic book',
                },
                {
                    thumb: 'https://static.wikia.nocookie.net/marvel_dc/images/0/0d/Batman_Superman_Vol_1_1.jpg',
                    price: '$3.99',
                    series: 'Batman/Superman',
                    type: 'comic book',
                },
                {
                    thumb: 'https://static.wikia.nocookie.net/marvel_dc/images/c/cf/Batman_Superman_Annual_Vol_2_1.jpg',
                    price: '$4.99',
                    series: 'Batman/Superman Annual',
                    type: 'comic book',
                },
                {
                    thumb: 'https://static.wikia.nocookie.net/marvel_dc/images/5/54/Batman_The_Joker_War_Zone_Vol_1_1.jpg',
                    price: '$5.99',
                    series: 'Batman: The Joker War Zone',
                    type: 'comic book',
                },
                {
                    thumb: 'https://static.wikia.nocookie.net/marvel_dc/images/6/64/Batman_Three_Jokers_Collected.jpg',
                    price: '$6.99',
                    series: 'Batman: Three Jokers',
                    type: 'comic book',
                },
                {
                    thumb: 'https://static.wikia.nocookie.net/marvel_dc/images/f/f8/Batman_White_Knight_Presents_Harley_Quinn_Vol_1_1.jpg',
                    price: '$4.99',
                    series: 'Batman: White Knight Presents: Harley Quinn',
                    type: 'comic book',
                },
                {
                    thumb: 'https://static.wikia.nocookie.net/marvel_dc/images/c/c8/Catwoman_Vol_2_1.jpg',
                    price: '$16.99',
                    series: 'Catwoman',
                    type: 'graphic novel',
                },
            ]
        }
    },
}
</script>

<template>
    <main class="app-card-hero">
        <div class="jumbotron">
            <img src="../assets/img/jumbotron.jpg" alt="">
        </div>
        <div class="container">
            <button class="button current-series">
                <a href="#">
                    <h1>Current series</h1>
                </a>
            </button>
            <div class="row">
                <Card v-for="(card, index) in cards" :key="index" :img="card.thumb" :title="card.series" />
            </div>
            <div class="load-more">
                <button class="button">
                    <a href="#">load more</a>
                </button>
            </div>
        </div>
    </main>
</template>

<style scoped lang="scss">
@use "../style/partials/variables" as*;

main {
    background-color: $sfondo-nero;
    padding: 7em 0em 2em 0em;
    text-align: start;

    h1 {
        color: white;
        font-size: 1rem;
    }

    .jumbotron {
        height: 40vh;

        img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            object-position: top center;
        }
    }

    .row {
        padding: 2em 0em;
        display: flex;
        justify-content: center;
        flex-wrap: wrap;
    }

    .load-more {
        text-align: center;
    }

    .button {
        background-color: $active-color;
        border-style: none;
        cursor: pointer;
        padding: 1em 3em;

        a {
            text-decoration: none;
            color: white;
            text-transform: uppercase;
            font-size: 0.8em;
            font-weight: 900;
        }

        &.current-series {
            padding: 1em;
            position: relative;
            transform: translate(0%, -50%);
        }
    }

}
</style>