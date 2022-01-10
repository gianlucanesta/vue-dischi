<template>
    
    <div class="album-square">

        <div class="album-image">
            <img class="d-block mx-auto" :src="albumObj.poster" :alt="albumObj.title">
        </div>  

        <h3 class="title text-center">{{ albumObj.title }}</h3>
        <div class="author text-center">{{ albumObj.author }}</div>
        <div class="year text-center">{{ albumObj.year }}</div>
        
    </div>
    
</template>

<script>

    export default {                          
        name: 'SingleAlbum',
        props: {
        albumObj: Object
        }
    };
    
</script>

<style scoped lang="scss" >
@import '../style/variables.scss';

.album-square {
    width: 190px;
    height: 350px;
    margin: 0 20px 75px 20px;
    background-color: $primary-color;
    
    
    &-image {
        display: flex;
        flex-direction: column;
    }

    img {
        margin-top: 20px;
        width: 150px;
        align-content: center;
    }

    h3 { 
        text-transform: uppercase;
        margin-top: 20px;
        margin-bottom: 15px;
        font-size: 19px;
        font-weight: 700;
    }

    .author, .year {
        color: gray;
        font-weight: 700;
        font-size: 16px;
    }

    .year {
        font-size: 14px;
    }
    
}

.album-square:hover {
    background-color: #3d4e5f;
    cursor: pointer;
}

</style>