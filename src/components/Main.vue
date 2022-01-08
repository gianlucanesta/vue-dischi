<template>
    <section>
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

export default {
    name: 'Main',
    components: {
        SingleAlbum,
        Loader,
    }, 
    data: function () {
    return {
      albums: [],
    };
  },
    created: function() {
        axios.get('https://flynn.boolean.careers/exercises/api/array/music')
        
        .then((response) => {
            // console.log(response);
            this.albums = response.data.response;
        });
    }                            

}
</script>

<style scoped lang="scss" >

    .row{
        display: flex;
        justify-content: center;
    }

</style>