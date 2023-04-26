<script>
import SectionTitle from '../SectionTitle.vue';

export default {
    name: "Intro",
    components: {
        SectionTitle
    }
}
</script>

<template>
    <section>
        <div class="ms_container text-center">
            <SectionTitle :text="`WORLD CLASS Fitness`" />
            <p class="text-secondary">At Avada Gym, everything we do from top to bottom is of the highest quality to ensure
                we're equipped to help you reach your goals of a healthy and fit lifestyle.</p>
        </div>
    </section>
</template>

<style scoped lang="scss">
@use "../src/style/general.scss";
@use "../src/style/partials/variables" as *;
@use "../src/style/partials/mixins" as *;

section {
    background-color: $grey_primary;

    .ms_container {
        position: relative;
    }

    .ms_container::after {
        @include triangle(50px, $grey_primary, -30px, 50%);
    }
}
</style>