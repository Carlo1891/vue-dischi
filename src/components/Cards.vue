<template>

    <div class="music-cards col-2 p-2">

        <img :src="object.poster" :alt="object.poster" class="img-fluid">
        <h2 class="text-white text-center">{{object.title}}</h2>

        <span>{{object.author}}</span>
        <span>{{object.year}}</span>

    </div>

</template>

<script>

    export default {
        name: 'Albums',
        props: {
            object: {
                type: object,
                required: true,
            }
        }
    }

</script>

<style scoped lang="scss">

    @import "../assets/styles/variables.scss";

    .music-cards {
        background-color: $topBarColor;
        height: 200px;
        span {
            color: $otherColor;
        }
    }
</style>
