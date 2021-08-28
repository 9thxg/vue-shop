<!--Item-card.vue-->
<template>
    <router-link :to="{
        name: 'Item',
        params: { description: this.description, genres: this.genres, language: this.language,
        image: this.image, rating: this.rating, runtime: this.runtime, title: this.title, title_long: this.title_long},
        }"
        style=text-decoration:none;>
        <v-card elevation="2">
            <v-img :src="image" max-height="3000"/>
            <v-divider></v-divider>
            <v-card-title style="font-size:2vmin; text-align:center;">{{ title_long }}</v-card-title>
        </v-card>
    </router-link>
</template>

<script>
export default {
    props: {
        description: {
            type: String,
        },
        genres: {
            
        },
        id: {
            type: Number,
        },
        language: {
            type: String,
        },
        image: {
            type: String,
        },
        rating: {
            type: Number,
        },
        runtime: {
            type: Number,
        },
        title: {
            type: String,
        },
        title_long: {
            type: String,
        },
    },
}
</script>

<style>

</style>