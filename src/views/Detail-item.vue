<template>
  <div class="layout">
      <v-img :src="image" max-width="200"></v-img>
      <div>
        <h1>{{title}}</h1>
        <h3>{{runtime}}m</h3>
      </div>
      
      <div>
        <h2>Rating {{rating}} </h2>
        <v-rating
            v-model="rate"
            color="green"
            half-increments
            readonly
            length="5"
            size="32"
        ></v-rating>
      </div>
      
      <div>
        <h2>Genres </h2>
        <h3>{{ genres }}</h3>
      </div>
      
      <div>
        <h3>{{ description }}</h3>
      </div>
  </div>
</template>

<script>
export default {
    data() {
        return{
            rate: 0,
        }
    },
    name: 'Item',
    props: {
        description: {
            type: String,
        },
        genres: {
            
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
    created(){
        this.rate = this.rating/2;
    }
}
</script>

<style>
    .layout {
        display: flex;
        justify-content: center;
        align-items: center;
    }
</style>