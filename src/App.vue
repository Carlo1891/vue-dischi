<template>

    <div id="app">
        <Header/>
        <Main/>
    </div>

</template>

<script>

    import Header from "./components/Header.vue";
    import Main from "./components/Main.vue";

    export default {
        name: 'App',
        comments: {
            Header,
            Main
        }
    }

</script>

<style lang="scss">

    @import "assets/styles/variables.scss";
    @import "~bootstrap/dist/css/bootstrap.css";
    
</style>
