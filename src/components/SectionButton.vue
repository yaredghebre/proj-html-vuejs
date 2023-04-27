<script>
export default {
    name: "SectionButton",
    props: {
        text: String
    }
}
</script>

<template>
    <div class="text-center">
        <button type="button" class="btn btn-outline-light px-4 py-2 mt-3 ms_button">{{ text }}</button>
    </div>
</template>

<style scoped lang="scss">
@use "../src/style/general.scss";
@use "../src/style/partials/variables" as *;

.ms_button {
    font-size: 1.1rem;
    border-radius: 0;
}
</style>