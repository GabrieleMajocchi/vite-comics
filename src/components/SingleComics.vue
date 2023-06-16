<script>
export default {
    name: 'NavLink',
    props: {comicslist: Object,
    },
    data() {
        return {
            
        }
    },
}
</script>

<template>
    <div class="comics">
        <span class="fw-bold fs-2">{{comicslist.price}}</span>
        <img :src="comicslist.thumb" :alt="comicslist.series">
        <p class="comics-title">{{(comicslist.series).toUpperCase()}}</p>
    </div>
</template>

<style lang="scss" scoped>
    @use '../styles/partials/mixing.scss' as *;
    @use '../styles/partials/variables.scss' as *;
    
    .comics{
        width: calc(100% / 6 - 1rem);
        color: $textWhite;
        margin: 3rem 1rem 0 0;
        position: relative;
        cursor: pointer;
        &:hover img{
            opacity: 0.2;
        }
        span{
            position: absolute;
            top: 50%;
            left: 50%;
            translate: (-50% -50%);
            display: none;
            z-index: 1;
        }
        &:hover span{
            display: block;
        }
    }
    .comics img{
        width: 100%;
        aspect-ratio: 1;
        object-fit: cover;
        object-position: top;
    }

</style>