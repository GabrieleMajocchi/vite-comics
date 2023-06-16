<script>
import NavLink from './NavLink.vue'
    export default {
        name: 'AppHeader',
        components:{
            NavLink,
        },
        data() {
            return {
                links: [
                    {ref: '#', name: 'Characters'},
                    {ref: '#', name: 'Comics'},
                    {ref: '#', name: 'Movies'},
                    {ref: '#', name: 'TV'},
                    {ref: '#', name: 'Games'},
                    {ref: '#', name: 'Collectibles'},
                    {ref: '#', name: 'Videos'},
                    {ref: '#', name: 'Fans'},
                    {ref: '#', name: 'News'},
                    {ref: '#', name: 'Shop'},
                ]
            }
        },
        methods: {
            
        },
    }
</script>

<template>
    <header class="d-flex">
        <div class="d-flex align-items-center m-auto justify-content-around my-3 w-75">
            <img src="../assets/img/dc-logo.png" alt="">
            <ul v-for="link in links" class="m-auto">
                <NavLink :link="link"/>
            </ul>
        </div>
    </header>
</template>

<style lang="scss" scoped>
    @use '../styles/partials/mixing.scss' as *;
    @use '../styles/partials/variables.scss' as *;

    header{
        width: 100vw;
        background-color: $bgWhite;
    }

    img{
        width: 80px;
        margin-right: 500px;
    }

    a{
        font-size: 0.9rem;
        color: $textGrey;
    }
    li:hover .blubox{
            display: block;
        }
    .blubox{
        display: none;
        background-color: $bgDc;
        height: 5px;
        width: 100%;
        position: absolute;
        bottom: -44px;
    }

</style>
