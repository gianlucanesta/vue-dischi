<template>
    <section>
        <div class="container">
            <Genere />
        </div>

        <div class="container d-flex justify-content-center text-white"> 
            
            <div  v-if="albums.length > 0" class="row row-cols-2 row-cols-lg-5">

                <SingleAlbum v-for="(element, index) in albums" :key="index" :albumObj="element"/> 

            </div>
            
            <Loader v-else/> 
        </div>
    </section>
</template>

<script>
import axios from 'axios';
import SingleAlbum from './SingleAlbum.vue';
import Loader from './Loader.vue';
import Genere from './Genere.vue';

export default {
    name: 'Main',
    components: {
        SingleAlbum,
        Loader,
        Genere,
    }, 
    data: function () {
    return {
      albums: [],
    };
  },
    methods: {
        getAlbums: function() {
            axios.get('https://flynn.boolean.careers/exercises/api/array/music')
            
            .then((response) => {
                // console.log(response);
                this.albums = response.data.response;
            });
        } 
    },
    created: function() {
        this.getAlbums();
    }                           

}
</script>

<style scoped lang="scss" >

    .row{
        display: flex;
        justify-content: center;
    }

</style>