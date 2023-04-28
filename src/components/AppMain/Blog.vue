<script>
import SectionTitle from '../SectionTitle.vue';
import SectionButton from '../SectionButton.vue';

export default {
    name: "Blog",
    components: {
        SectionTitle,
        SectionButton
    },
    data() {
        return {
            articlesFirstRow: [
                {
                    image: "../src/assets/images/blog1.jpg",
                    title: "Train with free weigths or your body weight?",
                    text: "Lorem ipsum dolor sit amet, consectetur adipisicing elit. Praesentium eaque perferendis quam tenetur sed eos facere. Modi vel, tempora eum unde praesentium. [...]"
                },
                {
                    image: "../src/assets/images/blog4.jpg",
                    title: "To be number on, train like you're number two",
                    text: "Lorem ipsum dolor sit amet, consectetur adipisicing elit. Praesentium eaque perferendis quam tenetur sed eos facere. Modi vel, tempora eum unde praesentium. [...]"
                }
            ],
            articlesSecondRow: [
                {
                    image: "../src/assets/images/blog6.jpg",
                    title: "Nutritional advice that will keep your training",
                    text: "Lorem ipsum dolor sit amet, consectetur adipisicing elit. Praesentium eaque perferendis quam tenetur sed eos facere. Modi vel, tempora eum unde praesentium. [...]"
                },
                {
                    image: "../src/assets/images/trainer3.jpg",
                    title: "Top 5 mistakes every gym member makes",
                    text: "Lorem ipsum dolor sit amet, consectetur adipisicing elit. Praesentium eaque perferendis quam tenetur sed eos facere. Modi vel, tempora eum unde praesentium. [...]"
                }

            ],
            articlesThirdRow: [
                {
                    image: "../src/assets/images/trainer4.jpg",
                    title: "Simple principles for your next workout",
                    text: "Lorem ipsum dolor sit amet, consectetur adipisicing elit. Praesentium eaque perferendis quam tenetur sed eos facere. Modi vel, tempora eum unde praesentium. [...]"
                },
                {
                    image: "../src/assets/images/trainer1.jpg",
                    title: "The myths pf shedding body fat explored",
                    text: "Lorem ipsum dolor sit amet, consectetur adipisicing elit. Praesentium eaque perferendis quam tenetur sed eos facere. Modi vel, tempora eum unde praesentium. [...]"
                }
            ]
        }
    }
}
</script>

<template>
    <section>
        <div class="ms_container">
            <SectionTitle :text="`PERFORMANCE NEWS`" />
            <div class="row row-cols-3 justify-content-around parent-row mb-5">

                <!-- FIRST ROW -->
                <div class="row row-cols-2 outer-row flex-column mt-5 gap-5">
                    <div v-for="card in articlesFirstRow" class="col outer-col ">
                        <div class="row row-cols-2 inner-row text-white flex-column">
                            <div class="col inner-col">
                                <img :src="card.image" alt="Immagine Blog">

                                <!-- effetto hover -->
                                <div class="overlay d-flex justify-content-center align-items-center gap-4">
                                    <a href=""><i class="fas fa-link fa-2xl"></i></a>
                                    <a href=""><i class="fas fa-magnifying-glass fa-2xl"></i></a>
                                </div>
                                <!-- / effetto hover -->

                            </div>
                            <div class="col inner-col p-3">
                                <h6>{{ card.title }}</h6>
                                <p class="mt-1 text-secondary">{{ card.text }}</p>
                            </div>
                        </div>
                    </div>
                </div>

                <!-- SECOND ROW -->
                <div class="row row-cols-2 outer-row flex-column mt-5 gap-5">
                    <div v-for="card in articlesSecondRow" class="col outer-col ">
                        <div class="row row-cols-2 inner-row text-white flex-column">
                            <div class="col inner-col">
                                <img :src="card.image" alt="Immagine Blog">

                                <!-- effetto hover -->
                                <div class="overlay d-flex justify-content-center align-items-center gap-4">
                                    <a href=""><i class="fas fa-link fa-2xl"></i></a>
                                    <a href=""><i class="fas fa-magnifying-glass fa-2xl"></i></a>
                                </div>
                                <!-- / effetto hover -->

                            </div>
                            <div class="col inner-col p-3">
                                <h6>{{ card.title }}</h6>
                                <p class="mt-1 text-secondary">{{ card.text }}</p>
                            </div>
                        </div>
                    </div>
                </div>

                <!-- THIRD ROW -->
                <div class="row row-cols-2 outer-row flex-column mt-5 gap-5">
                    <div v-for="card in articlesThirdRow" class="col outer-col ">
                        <div class="row row-cols-2 inner-row text-white flex-column">
                            <div class="col inner-col">
                                <img :src="card.image" alt="Immagine Blog">

                                <!-- effetto hover -->
                                <div class="overlay d-flex justify-content-center align-items-center gap-4">
                                    <a href=""><i class="fas fa-link fa-2xl"></i></a>
                                    <a href=""><i class="fas fa-magnifying-glass fa-2xl"></i></a>
                                </div>
                                <!-- / effetto hover -->

                            </div>
                            <div class="col inner-col p-3">
                                <h6>{{ card.title }}</h6>
                                <p class="mt-1 text-secondary">{{ card.text }}</p>
                            </div>
                        </div>
                    </div>
                </div>
            </div>

            <SectionButton :text="`READ ALL ARTICLES`" />

        </div>
    </section>
</template>

<style scoped lang="scss">
@use "../src/style/general.scss";
@use "../src/style/partials/variables" as *;

section {
    background-color: $grey_primary;

    .ms_container {
        position: relative;

        .parent-row {
            gap: 30px;

            .outer-row {
                .outer-col {
                    width: 100%;

                    .inner-row {
                        background-color: $grey_secondary;

                        .inner-col {
                            position: relative;
                            width: 100%;
                            font-size: .8rem;
                            padding: 0;

                            .overlay {
                                position: absolute;
                                top: 0;
                                left: 0;
                                width: 100%;
                                height: 100%;
                                background-color: $red_primary;
                                opacity: 0;
                                transition: .3s ease-in-out;
                            }
                        }

                        .inner-col:hover .overlay {
                            opacity: .7;

                            a {
                                transition: .2s ease-in-out;
                            }

                            a:hover {
                                color: white;
                                scale: 1.5;
                            }

                        }
                    }
                }
            }
        }
    }

}
</style>