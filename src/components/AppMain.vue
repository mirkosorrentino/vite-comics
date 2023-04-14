<script>
import AppComic from './AppComic.vue';

export default {
    name: "AppMain",
    components: {
        AppComic
    },

    data() {
        return {
            comics: [
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
    }
}
</script>

<template>
    <main>
        <div class="container">
            <div class="current-series-tag main-btns">Current Series</div>
            <div class="grid">
                <AppComic v-for="(comic, index) in comics" :key="index" :image="comic.thumb" :title="comic.series" :alt="comic.type"/>
            </div>
            <a href=""><div class="load-more-btn main-btns">Load more</div></a>
        </div>
    </main>
</template>

<style lang="scss" scoped>
@use "../style/general.scss" as *;
@use "../style/partials/mixins" as *;
@use "../style/partials/variables" as *;

main {
    width: 100%;
    background-color: $main-section-color;
    padding: 20px 0 60px;
    position: relative;

    .main-btns {
        font-weight: 600;
        color: white;
        text-transform: uppercase;
        display: inline-block;
        padding: 5px 10px;
        position: absolute;
        background-color: $banners-color;
    }
    
    .current-series-tag {
        z-index: 100;
        top: -10px;
        left: 10.5%;
    }
    .load-more-btn {
        font-size: .7rem;
        text-align: center;
        bottom: 20px;
        left: 50%;
        transition: translate(0 -50%);
    }
    .grid {
        @include flex(row, center, stretch);
        flex-wrap: wrap;

        .col {
            width: calc(100% / 6);
            text-align: center;
        }
    }
}
</style>