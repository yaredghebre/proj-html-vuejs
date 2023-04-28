<script>
export default {
    name: "Features",
    components: {

    },
    data() {
        return {
            cards: [
                {
                    icon: "fas fa-link-slash",
                    title: "Strength & Conditioning",
                    text: "Lorem ipsum dolor sit amet consectetur, adipisicing elit. Sed necessitatibus, fuga quo ab tempore aperiam minus quae magni tenetur laboriosam corporis."
                },
                {
                    icon: "fas fa-bicycle",
                    title: "Fitness & Cardio",
                    text: "Lorem ipsum dolor sit amet consectetur, adipisicing elit. Sed necessitatibus, fuga quo ab tempore aperiam minus quae magni tenetur laboriosam corporis."
                },
                {
                    icon: "fab fa-skyatlas",
                    title: "Flexibility & Rest",
                    text: "Lorem ipsum dolor sit amet consectetur, adipisicing elit. Sed necessitatibus, fuga quo ab tempore aperiam minus quae magni tenetur laboriosam corporis."
                },
                {
                    icon: "fas fa-heart-pulse",
                    title: "Health & Diet",
                    text: "Lorem ipsum dolor sit amet consectetur, adipisicing elit. Sed necessitatibus, fuga quo ab tempore aperiam minus quae magni tenetur laboriosam corporis."
                },
            ]
        }
    }
}
</script>

<template>
    <section>
        <div class="ms_container">
            <div class="row row-cols-4 text-white text-center">
                <div v-for="card in cards" class="col">
                    <div class="icon-container "><i class="mb-5" :class="card.icon"></i></div>
                    <h6>{{ card.title }}</h6>
                    <img src="../../assets/images/divider-x-red.png" alt="Divider Icon">
                    <p class="text-secondary mt-2">{{ card.text }}</p>
                </div>
            </div>
        </div>
    </section>
</template>

<style scoped lang="scss">
@use "../src/style/general.scss";
@use "../src/style/partials/variables" as *;

section {
    background-image: url(../../assets/images/gym_bkgd_bw-compressor.jpg);
    background-position-y: -100px;
    background-size: cover;

    .col {
        padding: 20px;
    
        .icon-container {
            display: inline;
            border: 1px solid $secondary_color;
            color: $secondary_color;
            border-radius: 50%;
            padding: 15px;
            font-size: 2rem;
            cursor: pointer;
            transition: 0.5s ease-in-out;
        }

        &:hover .icon-container {
            color: red;
            transform: scale(1.5);
        }

        h6 {
            transition: 0.5s ease-in-out;
        }

        &:hover h6 {
            color: $secondary_color;
        }
    }
}
</style>
