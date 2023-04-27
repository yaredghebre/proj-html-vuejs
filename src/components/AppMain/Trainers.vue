<script>
import SectionTitle from '../SectionTitle.vue';
import SectionButton from '../SectionButton.vue';

export default {
    name: "Trainers",
    components: {
        SectionTitle,
        SectionButton
    },
    data() {
        return {
            trainers: [
                {
                    image: "../src/assets/images/trainer1.jpg",
                    name: "Anna Baker",
                    position: "Personal Trainer",
                    bio: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Recusandae eius sequi est dolorum odit accusamus, tempora doloremque eaque eveniet.",
                    socials: [
                        {
                            icon: "fab fa-facebook-f fa-xl",
                            URL: "https://www.facebook.com/",
                        },
                        {
                            icon: "fab fa-twitter fa-xl",
                            URL: "https://www.twitter.com/",
                        },
                        {
                            icon: "fab fa-instagram fa-xl",
                            URL: "https://www.instagram.com/",
                        }
                    ]
                },
                {
                    image: "../src/assets/images/trainer3.jpg",
                    name: "Anne Warren",
                    position: "Personal Trainer",
                    bio: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Recusandae eius sequi est dolorum odit accusamus, tempora doloremque eaque eveniet.",
                    socials: [
                        {
                            icon: "fab fa-facebook-f fa-xl",
                            URL: "https://www.facebook.com/",
                        },
                        {
                            icon: "fab fa-twitter fa-xl",
                            URL: "https://www.facebook.com/",
                        },
                        {
                            icon: "fab fa-instagram fa-xl",
                            URL: "https://www.instagram.com/",
                        }
                    ]
                },
                {
                    image: "../src/assets/images/trainer4.jpg",
                    name: "Peter Rice",
                    position: "Personal Trainer",
                    bio: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Recusandae eius sequi est dolorum odit accusamus, tempora doloremque eaque eveniet.",
                    socials: [
                        {
                            icon: "fab fa-facebook-f fa-xl",
                            URL: "https://www.facebook.com/",
                        },
                        {
                            icon: "fab fa-twitter fa-xl",
                            URL: "https://www.facebook.com/",
                        },
                        {
                            icon: "fab fa-instagram fa-xl",
                            URL: "https://www.instagram.com/",
                        }
                    ]
                },
            ]
        }
    }
}
</script>

<template>
    <section>
        <div class="ms_container">
            <SectionTitle :text="`MEET OUR TRAINERS`" />
            <div class="row row-cols-3 outer-row justify-content-between mb-5">
                <div v-for="card in trainers" class="col outer-col text-white">
                    <div class="row row-cols-2 inner-row text-white flex-column">
                        <div class="col inner-col">
                            <img :src="card.image" alt="Immagine Trainer">
                        </div>
                        <div class="col inner-col p-4">
                            <h6>{{ card.name }}</h6>
                            <h6>{{ card.position }}</h6>
                            <p class="mt-5 text-secondary">{{ card.bio }}</p>
                            <div class="social-icons mt-5 d-flex gap-2">
                                <a v-for="social in card.socials" href="">
                                    <i :class="social.icon"></i>
                                </a>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
            <SectionButton :text="`VIEW ALL TRAINERS`" />
        </div>
    </section>
</template>

<style scoped lang="scss">
@use "../src/style/general.scss";
@use "../src/style/partials/variables" as *;
@use "../src/style/partials/mixins" as *;

section {
    background-color: $grey_secondary;

    .ms_container {
        position: relative;

        .outer-row {
            .outer-col {
                width: calc(100% / 3 - 40px);
                background-color: $grey_primary;

                .inner-row {
                    .inner-col {
                        width: 100%;
                        font-size: .8rem;
                        padding: 0;

                        .social-icons {
                            transition: 0.5s ease-in-out;

                            i {
                                background-color: $grey_secondary;
                                padding: 20px;
                                transition: 0.5s ease-in-out;
                            }
                        }
                    }
                }
            }
        }
    }

    .ms_container::after {
        @include triangle(50px, $grey_secondary, -30px, 50%);
    }


}
</style>

