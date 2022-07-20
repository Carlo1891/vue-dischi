<template>

    <div class="main-content">

        <div class="col-12 p-3">
            <Albums/>
        </div>

    </div>

</template>

<script>

    import Albums from './Albums.vue';
    export default {
        name: 'Main',
        components: {
            Albums,
        }
    }

</script>

<style scoped lang="scss">

    @import "../assets/styles/variables.scss";

    .main-content {
        background-color: $mainBarColor;
        height: 800px;
    }
</style>
