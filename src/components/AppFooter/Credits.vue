<script>
export default {
    name: "Credits",
    methods: {
        scrollToTop() {
            window.scrollTo({
                top: 0
            })
        }
    }

}
</script>

<template>
    <section>
        <div class="ms_container">
            <div class="row justify-content-between align-items-center">

                <!-- FIRST COLUMN -->
                <div class="col-auto">
                    <ul class="d-flex gap-3">
                        <li><a href="#">@ Copyright 2012 - 2020</a></li>
                        <li> | </li>
                        <li><a href="#">Avada Theme by Theme Fusion</a></li>
                        <li> | </li>
                        <li><a href="#">All Rights Reserved</a></li>
                        <li> | </li>
                        <li><a href="#">Powered by WordPress</a></li>
                    </ul>
                </div>

                <!-- SECOND COLUMN -->
                <div class="col-auto">
                    <ul class="d-flex gap-3">
                        <li><a href="#"><i class="fab fa-facebook-f fa-xl"></i></a></li>
                        <li><a href="#"><i class="fab fa-twitter fa-xl"></i></a></li>
                        <li><a href="#"><i class="fab fa-instagram fa-xl"></i></a></li>
                    </ul>
                </div>
            </div>

            <!-- HOME BUTTON -->
            <a class="return-btn text-white" href="#" @click="scrollToTop()">
                <i class="fas fa-chevron-up"></i>
            </a>

        </div>


    </section>
</template>

<style scoped lang="scss">
@use "../src/style/general.scss";
@use "../src/style/partials/variables" as *;

section {
    background-color: $primary_color;

    .ms_container {
        padding: 20px 0;
        position: relative;

        .row {
            font-size: .7rem;
            color: darkgray;

            a {
                transition: .5s ease-in-out;
            }

            .col-auto {

                i {
                    padding: 20px;
                    border-radius: 3px;
                    background-color: $secondary_color;
                    transition: .5s ease-in-out;
                }

                i:hover {
                    background-color: blue;
                    transition: .5s ease-in-out;
                }
            }
        }

        .return-btn {
            position: absolute;
            right: -25%;
            bottom: 0;
            padding: 10px 20px;
            background-color: $grey_secondary;

            i {
                transition: .2s ease-in-out;

            }

            i:hover {
                scale: 1.5;
                transition: .2s ease-in-out;
            }
        }
    }
}
</style>