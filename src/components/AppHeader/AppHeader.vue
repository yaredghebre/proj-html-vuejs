<script>
import Jumbotron from './Jumbotron.vue';

export default {
    name: "AppHeader",
    components: {
        Jumbotron
    },
    data() {
        return {
            links: [
                {
                    text: "HOME",
                    url: "#",
                    current: true,
                },
                {
                    text: "ABOUT US",
                    url: "#",
                    current: false,
                },
                {
                    text: "FACILITIES",
                    url: "#",
                    current: false,
                },
                {
                    text: "MEMBERSHIP",
                    url: "#",
                    current: false,
                },
                {
                    text: "TESTIMONIALS",
                    url: "#",
                    current: false,
                },
                {
                    text: "BLOG",
                    url: "#",
                    current: false,
                },
            ]
        }
    }
}
</script>

<template>
    <header class="d-flex justify-content-between align-items-center p-5">
        <div class="logo">
            <img src="../src/assets/images/gym_logo_1x.png" alt="Header Logo">
        </div>
        <nav>
            <ul class="nav-links text-white d-flex gap-5">
                <li v-for="link in links" :class="link.current ? 'active' : ''">
                    <a :href="link.url">{{ link.text }}</a>
                </li>
            </ul>
        </nav>
    </header>
    <Jumbotron />
</template>

<style scoped lang="scss">
@use "../src/style/general.scss";
@use "../src/style/partials/variables" as *;
@use "../src/style/partials/mixins" as *;

header {
    width: 100%;
    z-index: 100;
    position: fixed;
    .active {
        color: $secondary_color;
    }
}

</style>