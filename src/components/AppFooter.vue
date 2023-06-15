<script>
    export default {
        name: 'AppFooter',
        data() {
            return {
                dcComics: [
                    {ref: '#', name: 'Characters'},
                    {ref: '#', name: 'Comics'},
                    {ref: '#', name: 'Movies'},
                    {ref: '#', name: 'TV'},
                    {ref: '#', name: 'Games'},
                    {ref: '#', name: 'Collectibles'},
                    {ref: '#', name: 'Videos'},
                    {ref: '#', name: 'Fans'},
                    {ref: '#', name: 'News'},
                ],
                dc: [
                    {ref: '#', name: 'Terms Of Use'},
                    {ref: '#', name: 'Privacy policy (New)'},
                    {ref: '#', name: 'Ad Choices'},
                    {ref: '#', name: 'Advertising'},
                    {ref: '#', name: 'Jobs'},
                    {ref: '#', name: 'Subscriptions'},
                    {ref: '#', name: 'Talent Workshops'},
                    {ref: '#', name: 'CPSC Certificates'},
                    {ref: '#', name: 'Ratings'},
                    {ref: '#', name: 'Shop Help'},
                    {ref: '#', name: 'Contact Us'},
                    {ref: '#', name: ''},
                ],
                sites: [
                    {ref: '#', name: 'DC'},
                    {ref: '#', name: 'MAD Magazine'},
                    {ref: '#', name: 'DC Kids'},
                    {ref: '#', name: 'Dc Universe'},
                    {ref: '#', name: 'DC Power Visa'},
                ],
            }
        },
        methods: {
            
        },
    }
</script>

<template>
    <footer>
        <div class="background">
            <div class="top-footer d-flex w-75 m-auto position-relative">

                <div class="link-section">
                    <h3>DC COMICS</h3>
                    <ul v-for="section in dcComics">
                        <li>
                            <a :href="section.ref">{{ section.name }}</a>
                        </li>
                    </ul>
                    <h3>SHOP</h3>
                    <ul>
                        <li>
                            <a href="#">Shop DC</a>
                        </li>
                        <li>
                            <a href="#">Shop DC Collectibles</a>
                        </li>
                    </ul>
                </div>

                <div class="link-section">
                    <h3>DC</h3>
                    <ul v-for="section in dc">
                        <li>
                            <a :href="section.ref">{{ section.name }}</a>
                        </li>
                    </ul>
                </div>

                <div class="link-section">
                    <h3>SITES</h3>
                    <ul v-for="section in sites">
                        <li>
                            <a :href="section.ref">{{ section.name }}</a>
                        </li>
                    </ul>
                </div>

                <div class="dc position-absolute"></div>
            </div>
        </div>
        
        <div class="lower-footer  d-flex w-75 m-auto position-relative align-items-center justify-content-between">
            <div class="button">
                <a href="#" class="fw-bold">SIGN-UP NOW!</a>
            </div>
            <div class="socials d-flex">
                <p class="fw-bold">FOLLOW US</p>
                <img src="../assets/img/footer-facebook.png" alt="">
                <img src="../assets/img/footer-twitter.png" alt="">
                <img src="../assets/img/footer-youtube.png" alt="">
                <img src="../assets/img/footer-pinterest.png" alt="">
                <img src="../assets/img/footer-periscope.png" alt="">
            </div>
        </div>
    </footer>
</template>

<style lang="scss">
    @use '../styles/partials/mixing.scss' as *;
    @use '../styles/partials/variables.scss' as *;

    footer{
        background-color: $bgFooter;
    }

    .background{
        background-image: url(../assets/img/footer-bg.jpg);
        background-repeat: no-repeat;
        background-size: cover;
    }

    .top-footer{
        color: $textWhite;
        padding: 2rem 0 4rem 0;
        overflow: hidden;
        div{
            margin-right: 2rem;
        }
        div h3{
            margin: 1rem 0;
            font-weight: bold;
            font-size: 1rem;
        }
        div ul{
            margin: 0;
            padding: 0;
        }
        div li a{
            color: $textGrey;
            text-decoration: none;
            &:hover{
                color: $dcColor;
            }
        }
        .dc{
            background-image: url(../assets/img/dc-logo-bg.png);
            width: 700px;
            height: 700px;
            background-repeat: no-repeat;
            background-size: contain;
            right: 50px;
            top: -130px;
        }
    }

    .lower-footer{
        height: 100px;
        div a{
            color: $textWhite;
            padding: 0.5rem 1rem;
            border: 2px solid $dcColor;
            &:hover{
                color: $dcColor;
            }
        }
        div p{
            color: $dcColor;
            font-size: 1.3rem;
            margin: 0 1.3rem;
        }
        div img{
            height: 40px;
            aspect-ratio: 1;
            margin: 0 0.8rem;
            cursor: pointer;
        }
    }
</style>
