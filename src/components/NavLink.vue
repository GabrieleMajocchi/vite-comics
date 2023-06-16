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

<style lang="scss">

</style>