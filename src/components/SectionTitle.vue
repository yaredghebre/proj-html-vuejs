<script>
export default {
    name: "SectionTitle",
    props: {
        text: String
    }
}
</script>

<template>
    <h2 class="text-white mb-4">{{ text }}</h2>
    <img class="mb-4" src="../assets/images/divider-xx-red.png" alt="">
</template>

<style scoped lang="scss">
@use "../src/style/general.scss";
@use "../src/style/partials/variables" as *;

h2 {
    font-weight: 700;
}
</style>