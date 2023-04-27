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
            articles: [
                {
                    title: "Train with free weigths or your body weight?",
                    text: "Lorem ipsum dolor sit amet, consectetur adipisicing elit. Praesentium eaque perferendis quam tenetur sed eos facere. Modi vel, tempora eum unde praesentium. [...]"
                },
                {
                    title: "Nutritional advice that will keep your training",
                    text: "Lorem ipsum dolor sit amet, consectetur adipisicing elit. Praesentium eaque perferendis quam tenetur sed eos facere. Modi vel, tempora eum unde praesentium. [...]"
                },
                {
                    title: "Simple principles for your next workout",
                    text: "Lorem ipsum dolor sit amet, consectetur adipisicing elit. Praesentium eaque perferendis quam tenetur sed eos facere. Modi vel, tempora eum unde praesentium. [...]"
                },
                {
                    title: "To be number on, train like you're number two",
                    text: "Lorem ipsum dolor sit amet, consectetur adipisicing elit. Praesentium eaque perferendis quam tenetur sed eos facere. Modi vel, tempora eum unde praesentium. [...]"
                },
                {
                    title: "Top 5 mistakes every gym member makes",
                    text: "Lorem ipsum dolor sit amet, consectetur adipisicing elit. Praesentium eaque perferendis quam tenetur sed eos facere. Modi vel, tempora eum unde praesentium. [...]"
                },
                {
                    title: "The myths pf shedding body fat explored",
                    text: "Lorem ipsum dolor sit amet, consectetur adipisicing elit. Praesentium eaque perferendis quam tenetur sed eos facere. Modi vel, tempora eum unde praesentium. [...]"
                },
            ]
        }
    }
}
</script>

<template>
    <section>
        <div class="ms_container">
            <SectionTitle :text="`PERFORMANCE NEWS`" />
        </div>
    </section>
</template>

<style scoped lang="scss">
@use "../src/style/general.scss";
@use "../src/style/partials/variables" as *;

section {
    background-color: $grey_primary;
    height: 1000px;
}
</style>