<script>
import SectionTitle from '../SectionTitle.vue';

export default {
    name: "Facilities",
    components: {
        SectionTitle
    },
    data() {
        return {
            thumbs: [
                {
                    image: "../src/assets/images/home-image1.jpg",
                    url: "#",
                    active: false
                },
                {
                    image: "../src/assets/images/home-image2.jpg",
                    url: "#",
                    active: false
                },
                {
                    image: "../src/assets/images/home-image3.jpg",
                    url: "#",
                    active: false
                },
                {
                    image: "../src/assets/images/home-image4.jpg",
                    url: "#",
                    active: false
                },
                {
                    image: "../src/assets/images/home-image54.jpg",
                    url: "#",
                    active: false
                },
                {
                    image: "../src/assets/images/home-image6.jpg",
                    url: "#",
                    active: false
                },
            ]
        }
    }
}
</script>

<template>
    <section>
        <div class="ms_container">
            <SectionTitle :text="`HIGH PERFORMANCE FACILITIES`" />
            <div class="row row-cols-3 mt-5 justify-content-between">
                <div v-for="thumb in thumbs" class="col ">
                    <img :src="thumb.image" alt="">
                </div>
            </div>
        </div>
    </section>
</template>

<style scoped lang="scss">
@use "../src/style/general.scss";
@use "../src/style/partials/variables" as *;

section {
    background-color: $grey_primary;

    .row {
        gap: 40px;
    
        .col {
            width: calc(100% / 3 - 30px);
        }
    }
}
</style>