<script>
export default {
    name: "Contacts"

}
</script>

<template>
    <section>
        <div class="ms_container text-white">
            <div class="row row-cols-4">

                <!-- FIRST COLUMN -->
                <div class="col">
                    <h6 class="text-secondary mb-4">COME FIND US</h6>
                    <ul class="list-unstyled">
                        <li>12345 North Main Street</li>
                        <li>New York, NY 555555</li>
                        <li>Phone: <a href="">1.800.555.6789</a></li>
                        <li>Email: <a href="">info@your-domain.com</a></li>
                    </ul>
                </div>

                <!-- SECOND COLUMN -->
                <div class="col">
                    <h6 class="text-secondary mb-4">RECENT POSTS</h6>
                    <ul class="list-unstyled">
                        <li class="ms_list-style border-bottom border-secondary py-3"><a href="">Train with free weights or your body weight?</a> </li>
                        <li class="ms_list-style border-bottom border-secondary py-3"><a href="">Nutritional advice that will keep you training</a> </li>
                    </ul>

                </div>

                <!-- THIRD COLUMN -->
                <div class="col">
                    <h6 class="text-secondary mb-4">OPENING TIMES</h6>
                    <ul class="list-unstyled">
                        <li>Weekdays Monday - Friday</li>
                        <li class="text-secondary">09:00 - 19:00</li>
                    </ul>
                    <ul class="list-unstyled mt-2">
                        <li>Weekends Saturday - Sunday</li>
                        <li class="text-secondary">09:00 - 21:00</li>
                    </ul>
                </div>

                <!-- FOURTH COLUMN -->
                <div class="col">
                    <img src="../../assets/images/gym_ad-compressor.jpg" alt="">
                </div>
            </div>
        </div>
    </section>
</template>

<style scoped lang="scss">
@use "../src/style/general.scss";
@use "../src/style/partials/variables" as *;

section {
    background-color: $grey_secondary;

    .ms_container {
        font-size: .8rem;

        a {
            transition: 0.5s ease-in-out;
        }

        .ms_list-style {
            list-style-type: ">";
        }

        li {
            color: darkgray;
        }
    }
}
</style>