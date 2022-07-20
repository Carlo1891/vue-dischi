<template>

    <div>

        <div v-if="!loading" class="row">
            <Cards v-for="album in albums" :key="album.id" :object="album"/>
        </div>

        <div v-else>
            <Load/>
        </div>

    </div>

</template>

<script>

    import Cards from './Cards.vue';
    import Load from './Load.vue';
    import axios from 'axios';
    export default {
        name: 'Albums',
        components: {
    Cards,
    Load,
    },
            data () {
                return {
                albums: [],
                loading: true,
                };
            },
            methods: {
                getAlbums () {
                    axios.get ('https://flynn.boolean.careers/exercises/api/array/music')
                    .then (response => {
                    this.albums = response.data.response;
                    console.log (this.albums);
                    this.loading = false;
                })
                .catch (error => {
                    console.warn (error);
                });
                
                },
            },
            created () {
                this.getAlbums ();
        }    

    }

</script>

<style scoped lang="scss">
    @import "../assets/styles/variables.scss";
</style>
