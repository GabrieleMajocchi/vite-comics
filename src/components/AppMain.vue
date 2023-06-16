<script>
import SingleComics from './SingleComics.vue'
    export default {
        name: 'AppMain',
        components: {
            SingleComics,
        },
        data() {
            return {
                currentseries: [
                    {thumb: "https://www.coverbrowser.com/image/action-comics/1-1.jpg",
                    price: "$19.99",
                    series: "Action Comics",
                    type: "comic book",},
                    {thumb: "https://www.panini.it/media/catalog/product/cache/a5b5dd3adfe0d321084804c738f29601/M/1/M1BLLA015ISBN_0.jpg",
                    price: "$3.99",
                    series: "American Vampire 1976",
                    type: "comic book",},
                    {thumb: "https://media.wired.com/photos/593384dad80dd005b42b2817/master/w_2560%2Cc_limit/Aquaman-16.jpg",
                    price: "$16.99",
                    series: "Aquaman",
                    type: "graphic novel",},
                    {thumb: "https://d29xot63vimef3.cloudfront.net/image/batgirl/1-1.jpg",
                    price: "$2.99",
                    series: "Batgirl",
                    type: "comic book",},
                    {thumb: "https://static.posters.cz/image/750/locandine-film-in-plexiglass-batman-prowl-comic-cover-i69653.jpg",
                    price: "$3.99",
                    series: "Batman",
                    type: "comic book",},
                    {thumb: "https://static.wikia.nocookie.net/marvel_dc/images/5/50/Batman_Beyond_v.1_1.jpg",
                    price: "$2.99",
                    series: "Batman Beyond",
                    type: "comic book",},
                    {thumb: "https://static.wikia.nocookie.net/marvel_dc/images/0/0d/Batman_Superman_Vol_1_1.jpg",
                    price: "$3.99",
                    series: "Batman/Superman",
                    type: "comic book",},
                    {thumb: "https://static.wikia.nocookie.net/marvel_dc/images/c/cf/Batman_Superman_Annual_Vol_2_1.jpg",
                    price: "$4.99",
                    series: "Batman/Superman Annual",
                    type: "comic book",},
                    {thumb: "https://static.wikia.nocookie.net/marvel_dc/images/5/54/Batman_The_Joker_War_Zone_Vol_1_1.jpg",
                    price: "$5.99",
                    series: "Batman: The Joker War Zone",
                    type: "comic book",},
                    {thumb: "https://static.wikia.nocookie.net/marvel_dc/images/6/64/Batman_Three_Jokers_Collected.jpg",
                    price: "$6.99",
                    series: "Batman: Three Jokers",
                    type: "comic book",},
                    {thumb: "https://static.wikia.nocookie.net/marvel_dc/images/f/f8/Batman_White_Knight_Presents_Harley_Quinn_Vol_1_1.jpg",
                    price: "$4.99",
                    series: "Batman: White Knight Presents: Harley Quinn",
                    type: "comic book",},
                    {thumb: "https://static.wikia.nocookie.net/marvel_dc/images/c/c8/Catwoman_Vol_2_1.jpg",
                    price: "$16.99",
                    series: "Catwoman",
                    type: "graphic novel",},
                ],
            }
        },
        methods: {
            
        },
    }
</script>

<template>
    <main class="">
        <div class="jumbotron"></div>
        <div class="products">
            <div class="box m-auto w-75 d-flex align-item-center justify-content-between flex-wrap position-relative">
                <div class="current-series fw-bold">CURRENT SERIES</div>
                <SingleComics v-for="comics in currentseries" :comicslist="comics"/>>
                <a href="#" class="load-more fw-bold m-auto">LOAD MORE</a>
            </div>
        </div>
        <div class="blubox d-flex align-item-center justify-content-center">
            <div class="element d-flex align-items-center px-5">
                <img src="../assets/img/buy-comics-digital-comics.png" alt="">
                <p>DIGITAL COMICS</p>
            </div>
            <div class="element d-flex align-items-center px-5">
                <img src="../assets/img/buy-comics-merchandise.png" alt="">
                <p>DC MERCHANDISE</p>
            </div>
            <div class="element d-flex align-items-center px-5">
                <img src="../assets/img/buy-comics-subscriptions.png" alt="">
                <p>SUBSCRIPTION</p>
            </div>
            <div class="element d-flex align-items-center px-5">
                <img src="../assets/img/buy-comics-shop-locator.png" alt="">
                <p>COMIC SHOP LOCATOR</p>
            </div>
            <div class="element d-flex align-items-center px-5">
                <img src="../assets/img/buy-dc-power-visa.svg" alt="">
                <p>DC POWER VISA</p>
            </div>
        </div>
    </main>
</template>

<style lang="scss" scoped>
    @use '../styles/partials/mixing.scss' as *;
    @use '../styles/partials/variables.scss' as *;
    .jumbotron{
        width: 100%;
        height: 400px;
        background-image: url('../assets/img/jumbotron.jpg');
        background-repeat: no-repeat;
        background-size: cover;
    }
    .products{
        background-color: $bgMain;
        padding-bottom: 1rem;
    }
    .current-series, .load-more{
        background-color: $bgDc;
        color: $textWhite;
        padding: 0.5rem 1rem;
        top: -30px;
    }
    .current-series{
        position: absolute;
        font-size: 1.5rem;
        top: -30px;
    }
    .blubox{
        height: 200px;
        background-color: $bgDc;
    }

    h2{
        color: $textWhite;
    }

    .element img{
        height: 50px;
    }

    .element p{
        color: $textWhite;
        padding-left: 1rem;
        margin-bottom: 0;
    }
</style>
