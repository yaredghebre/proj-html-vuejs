<script>
import SectionButton from '../SectionButton.vue';

export default {
    name: "Banner",
    components: {
        SectionButton
    }
}
</script>

<template>
    <section>
        <div class="ms_container text-white">
            <div class="row row-cols-2">
                <div class="col">
                    <h3>Achieve Your Fitness Goals</h3>
                    <p>Flexible membership packages to suit all levels of athlete and achieve your fitness goals</p>
                </div>
                <div class="col">
                    <SectionButton :text="`JOIN US`" />
                </div>
            </div>

        </div>
    </section>
</template>

<style scoped lang="scss">
@use "../src/style/general.scss";
@use "../src/style/partials/variables" as *;

section {
    background-image: url(../../assets/images/home-parallax.jpg);
    background-size: cover;
    background-position-y: -100px;

    .ms_container {
        padding: 50px 0;
        
        h3 {
            font-weight: 700;
        }
    }
}
</style>