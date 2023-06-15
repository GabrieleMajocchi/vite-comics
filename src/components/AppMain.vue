<script>
    export default {
        name: 'AppMain',
        data() {
            return {
                
            }
        },
        methods: {
            
        },
    }
</script>

<template>
    <main class="">
        <div class="products d-flex align-item-center">
            <h2 class="fw-bold m-auto w-75"> --> Content goes here &lt;-- </h2>
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

    .products{
        height: 170px;
        background-color: $bgMain;
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
