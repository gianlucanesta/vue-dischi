<template>
    <div>
        <select @change="selectGenre" v-model="genreValue" name="" id="select-genre">
            <option value="Rock">Rock</option>
            <option value="Pop">Pop</option>
            <option value="Metal">Metal</option>
            <option value="Jazz">Jazz</option>
        </select>
    </div>
</template>

<script>
export default {
    name: "Genere",
    data:function() {
        return {
            genreValue: ''
        };
    },
    methods: {
        selectGenre: function () {
            alert(this.genreValue);
        }
    }
}
</script>

<style scoped lang="scss" >
@import '../style/variables.scss';

#select-genre {
    margin-top: 5%;
    margin-bottom: 5%;
    margin-left: 10%;
}    

</style>
