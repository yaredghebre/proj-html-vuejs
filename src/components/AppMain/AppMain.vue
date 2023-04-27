<script>
import Intro from './Intro.vue';
import Membership from './Membership.vue';
import Features from './Features.vue';
import Testimonials from './Testimonials.vue';
import Facilities from './Facilities.vue';
import Quote from './Quote.vue';
import Trainers from './Trainers.vue';
import Blog from './Blog.vue';

export default {
    name: "AppMain",
    components: {
        Intro,
        Membership,
        Features,
        Testimonials,
        Facilities,
        Quote,
        Trainers,
        Blog
    }
}
</script>

<template>
    <Intro />
    <Membership />
    <Features />
    <Testimonials />
</template>

<style scoped lang="scss">
@use "../src/style/general.scss";
@use "../src/style/partials/variables" as *;
@use "../src/style/partials/mixins" as *;
</style>