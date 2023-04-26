<script>
    import AppHeader from "./components/AppHeader/AppHeader.vue";
    import AppMain from "./components/AppMain/AppMain.vue";
    import AppFooter from "./components/AppFooter/AppFooter.vue";

    export default {
      components: {
        AppHeader,
        AppMain,
        AppFooter
      }
    }

</script>

<template>
    <AppHeader />
    <AppMain />
    <AppFooter />
</template>

<style lang="scss">
@use "./style/general.scss";

</style>