<template>
  <main>
      <div class="container">
        <div class="row">
            <file-card v-for="album in arrAlbums" :key="album.title"/>
        </div>
      </div>
  </main>
</template>

<script>
import FileCard from './FileCard.vue'

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
}
</script>

<style lang="scss" scoped>

</style>

