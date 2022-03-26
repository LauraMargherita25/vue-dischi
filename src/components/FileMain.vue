<template>
  <main class="d-flex justify-content-center align-item-center">
        <div v-if="arrAlbums == null" class="text-light">Dati in caricamento</div> 
        <div v-else class="container d-flex align-items-start">
            <div class="row row row-cols-5 w-100">
                <file-card v-for="album in searchGenre" :key="album.title" :album-data="album"/>
            </div>
        </div>
  </main>
</template>

<script>
import FileCard from './FileCard.vue';
import axios from 'axios';

export default {
    name: "FileMain",
    data(){
        return{
            arrAlbums: null
        }
    } ,
    props: {
        searchString: String,
    },
    components: { 
        FileCard 
    },
    computed: {
        searchGenre() {
            return this.arrAlbums.filter((album) => album.genre.toLowerCase().includes(this.searchString.toLowerCase()))
        }
    },
    created() {
        setTimeout(() => {
            axios.get('https://flynn.boolean.careers/exercises/api/array/music')
            .then((response)=> {
                console.log(response)
                this.arrAlbums = response.data.response;
            })
        }, 3000);
    },
}
</script>

<style lang="scss" scoped>
main{
    height: 100%;
}
</style>

