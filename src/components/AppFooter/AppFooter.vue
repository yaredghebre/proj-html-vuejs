<script>
import Banner from './Banner.vue';
import Contacts from './Contacts.vue';
import Credits from './Credits.vue';

export default {
    name: "AppFooter",
    components: {
        Banner,
        Contacts,
        Credits
    }
}
</script>

<template>
    <Banner />
    <Contacts />
    <Credits />
</template>

<style scoped lang="scss">
@use "../src/style/general.scss";
@use "../src/style/partials/variables" as *;
@use "../src/style/partials/mixins" as *;
</style>