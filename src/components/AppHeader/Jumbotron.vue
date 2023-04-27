<script>
import SectionButton from '../SectionButton.vue';

export default {
    name: "Jumbotron",
    components: {
        SectionButton
    }
}
</script>

<template>
    <div class="jumbo-container text-white d-flex flex-column align-items-center justify-content-center">
        <h1 class="">NO PAIN NO GAIN</h1>
        <p>Motivation is what gets you started. Habit is what keeps you going.</p>
        <div class="link-box mt-3">
            <SectionButton :text="`JOIN US TODAY`"/>
        </div>
    </div>
</template>

<style scoped lang="scss">
@use "../src/style/general.scss";
@use "../src/style/partials/variables" as *;

.jumbo-container {
    background-image: url(../../src/assets/images/home-banner.jpg);
    background-size: cover;
    height: 1000px;
    position: relative;
    top: 0;
    
        h1 {
            font-weight: 700;
            font-size: 6.5rem;
            letter-spacing: 5px;
        }
}
</style>