<script>
  import AppHeader from './components/AppHeader.vue';
  import AppMain from './components/AppMain.vue';
  import AppFooter from './components/AppFooter.vue';
  
  export default {
    name: 'AppVue',
    components:{
        AppHeader,
        AppMain,
        AppFooter
      }
  }
</script>

<template>
  <div class="page">
    <AppHeader/>
    <AppMain/>
    <AppFooter/>
  </div>
</template>

<style lang="scss">
  @use './styles/partials/mixing.scss' as *;
  @use './styles/partials/variables.scss' as *;
  @import './styles/general.scss';
  
  body{
    background-color: $bgColor;
  }
</style>
