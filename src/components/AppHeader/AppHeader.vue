<script>
import SectionButton from '../SectionButton.vue';

export default {
    name: "AppHeader",
    components: {
        SectionButton
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
    },
    
    // FUNZIONE PER IL CLICK SUI LINK
    methods: {
        setActiveLink(index) {
            this.links.forEach((link, i) => {
                if (i === index) {
                    link.current = true;
                } else {
                    link.current = false;
                }
            });
        }
    }
}
</script>

<template>
    <header>

        <!-- NAVBAR -->
        <nav class="d-flex justify-content-between align-items-center p-5">
            <div class="logo">
                <a href="#"><img src="../../assets/images/gym_logo_1x.png" alt=""></a>
            </div>
            <nav>
                <ul class="nav-links text-white d-flex gap-5">
                    <li v-for="(link, index) in links" :class="link.current ? 'active' : ''">
                        <a :href="link.url" @click="setActiveLink(index)">{{ link.text }}</a>
                    </li>
                </ul>
            </nav>
        </nav>

        <!-- JUMBOTRON -->
        <section class="jumbotron">
            <div class="jumbo-container text-white d-flex flex-column align-items-center justify-content-center">
                <h1 class="">NO PAIN NO GAIN</h1>
                <p>Motivation is what gets you started. Habit is what keeps you going.</p>
                <div class="link-box mt-3">
                    <SectionButton :text="`JOIN US TODAY`" />
                </div>
            </div>
        </section>

    </header>
</template>

<style scoped lang="scss">
@use "../src/style/general.scss";
@use "../src/style/partials/variables" as *;
@use "../src/style/partials/mixins" as *;

header {
    background-image: url(../../src/assets/images/home-banner.jpg);
    background-repeat: no-repeat;
    background-size: cover;

    nav {

        a {
            transition: .3s ease-in-out;
        }

        .active {
            color: $red_primary;
        }
    }

    .jumbo-container {
        height: 800px;

        h1 {
            font-weight: 700;
            font-size: 6.5rem;
            letter-spacing: 4px;
        }

        h1:hover {
            animation: blur .3s ease-in-out alternate;
        }

        @keyframes blur {
            0% {
                text-shadow: 0 0 5px white, 0 0 10px white, 0 0 15px white, 0 0 20px $red_primary, 0 0 25px $red_primary, 0 0 30px $red_primary;
                color: transparent;
            }

            100% {
                text-shadow: none;
                color: $red_primary;
            }
        }
    }
}
</style>

