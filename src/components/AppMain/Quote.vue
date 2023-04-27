<script>
export default {
    name: "Quote"
}
</script>

<template>
    <section>
        <div class="ms_container text-white text-center d-flex flex-column align-items-center">
            <p class="mb-4">"I fear not the man who has practiced 10,000 kicks once, but I fear the man who has practiced one kick 10,000 times"</p>
            <img src="../../assets/images/divider-white-xx.png" alt="">
            <h5 class="mt-4">BRUCE LEE &#8226; QUOTE OF THE DAY</h5>
        </div>
    </section>
</template>

<style scoped lang="scss">
@use "../src/style/general.scss";
@use "../src/style/partials/variables" as *;

section {
    // height: 1000px;
    background-image: url(../../src/assets/images/home-testimonial-bg.jpg);
    background-position: center;
    background-size: cover;
    

    .ms_container {

        width: 50%;
        p {
            font-weight: 500;
            font-size: 2.5rem;
        }

        h5 {
            font-weight: 700;
        }
    }
}
</style>