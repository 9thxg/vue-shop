<!--Item-list.vue-->
<template>
    <div class="cover">
        <div v-for='cnt in movies' :key='cnt.id'>
            <ItemCard v-bind="{description: cnt.description_full, genres: cnt.genres,
            id: cnt.id, language: cnt.language, image: cnt.large_cover_image, rating: cnt.rating,
            runtime: cnt.runtime, title: cnt.title, title_long: cnt.title_long}" />
        </div>
    </div>
</template>

<script>
import ItemCard from "./Item-card.vue"
import axios from 'axios'

export default {
  components: { ItemCard },
    data() {
        return{
            movies: "",
        }
    },
    
    created(){
        axios.get('https://yts.mx/api/v2/list_movies.json?sort_by=rating')
        .then(res => {
            console.log(res);
            this.movies = res.data.data.movies;
            console.log(this.movies);
        })
        .catch(err => {
            console.log(err);
        });
    }
}
</script>

<style>
    .cover {
        display: grid;
        grid-template-columns: repeat(3, minmax(0, 1fr));
        grid-template-rows: minmax(0, 1fr) minmax(0, 1fr);
        gap: 10px;
        padding: 10px;
    }
</style>