<template>
  <main>
      <div class="container">
        <div class="row row row-cols-5">
            <file-card v-for="album in arrAlbums" :key="album.title" :album-data="album"/>
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
            arrAlbums: [
                {
                    poster:	"https://www.onstageweb.com/wp-content/uploads/2018/09/bon-jovi-new-jersey.jpg",
                    title:	"New Jersey",
                    genre:	"Rock",
                    year:	"1988",
                },
                {
                    poster:	"https://www.onstageweb.com/wp-content/uploads/2018/09/bon-jovi-new-jersey.jpg",
                    title:	"New Jersey",
                    genre:	"Rock",
                    year:	"1988",
                },
                {
                    poster:	"https://www.onstageweb.com/wp-content/uploads/2018/09/bon-jovi-new-jersey.jpg",
                    title:	"New Jersey",
                    genre:	"Rock",
                    year:	"1988",
                },
                {
                    poster:	"https://www.onstageweb.com/wp-content/uploads/2018/09/bon-jovi-new-jersey.jpg",
                    title:	"New Jersey",
                    genre:	"Rock",
                    year:	"1988",
                },
                {
                    poster:	"https://www.onstageweb.com/wp-content/uploads/2018/09/bon-jovi-new-jersey.jpg",
                    title:	"New Jersey",
                    genre:	"Rock",
                    year:	"1988",
                }
            ]
        }
    } ,
    components: { 
        FileCard 
    },
    created() {
        axios.get('https://flynn.boolean.careers/exercises/api/array/music')
         .then((response)=> {
             console.log(response)
         })
    },
}
</script>

<style lang="scss" scoped>

</style>

