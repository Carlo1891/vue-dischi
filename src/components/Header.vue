<template>

    <div class="top-bar container-fluid">
        <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTB_Fl5K0DJ05-29U3KPUT6ZIisAHO9fUAuXA&usqp=CAU" alt="logo-spotify">
    </div>

</template>

<script>

    export default {
        name: 'Header',
    }

</script>

<style scoped lang="scss">
    
    @import "../assets/styles/variables.scss";

    .top-bar {
        background-color: $topBarColor;
        height: 100px;
    }

</style>
