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
    <main class="d-flex align-items-center">
        <h1 class="w-75 m-auto fw-bold"> --> Content goes here &lt;-- </h1>
    </main>
</template>

<style lang="scss" scoped>
    @use '../styles/partials/mixing.scss' as *;
    @use '../styles/partials/variables.scss' as *;

    main{
        height: 200px;
        background-color: $bgMain;
    }

    h1{
        color: $textWhite;
    }
</style>
