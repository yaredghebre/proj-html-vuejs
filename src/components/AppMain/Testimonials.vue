<script>
import SectionTitle from '../SectionTitle.vue';

export default {
    name: "Testimonials",
    components: {
        SectionTitle
    },
    data() {
        return {
            currentIndex: 0,
            cards: [
                {
                    image: "../src/assets/images/review_1-compressor.jpg",
                    review: '"The trainers at Avada Gym have helped me reach my fitness goals beyond anything I could have hoped for. I love it!"',
                    name: "Tara Smith"
                },
                {
                    image: "../src/assets/images/review_3-compressor-2.jpg",
                    review: '"The atmosphere at Avada Gym is amazing, the people are even better. All in all, it is a great place to work out"',
                    name: "Simon Chel"
                },
                {
                    image: "../src/assets/images/review_2-compressor.jpg",
                    review: '"The facilities at Avada Gym stood out to me the most. They are well maintained and have high quality equipment"',
                    name: "Jen Wirth"
                },
                {
                    image: "../src/assets/images/review_4-compressor-2.jpg",
                    review: '"No bad things to say about Avada Gym, they are top notch at every corner and truly take care of their customers."',
                    name: "Jeff Glum"
                },
            ]
        }
    },
}
</script>

<template>
    <section>
        <div class="ms_container">
            <SectionTitle :text="`REAL WORLD RESULTS`" />
            <div class="row row-cols-2 outer-row">
                <div v-for="card in cards" class="col text-white outer-col">
                    <div class="row row-cols-2 text-white inner-row">
                        <div class="col inner-col d-flex">
                            <img :src="card.image" alt="immagine card">
                        <div class="col inner-col">
                            <p class="text-secondary font-italic">{{ card.review }}</p>
                            <h6 class="text-secondary">{{ ' - ' + card.name }}</h6>
                        </div>
                        </div>
                    </div>
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

    .outer-row {
        gap: 40px;

        .outer-col {
            width: calc(50% - 20px);
            padding: 20px;
            background-color: $grey_secondary;

            .inner-row {
                .inner-col {
                    width: 100%;
                    gap: 30px;

                    p {
                        font-style: italic;
                    }

                    h6 {
                        font-weight: 700;
                    }

                }
            }
        }
    }
}
</style>