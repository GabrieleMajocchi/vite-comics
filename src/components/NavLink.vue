<script>
export default {
    name: 'NavLink',
    props: {link: Object},
}
</script>

<template>
    <li class="position-relative">
        <a class="fw-bold" :href="link.ref">{{(link.name).toUpperCase()}}</a>
        <div class="blubox"></div>
    </li>
</template>

<style lang="scss" scoped>
    @use '../styles/partials/mixing.scss' as *;
    @use '../styles/partials/variables.scss' as *;
    
    li{
        margin-right: 1rem;
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