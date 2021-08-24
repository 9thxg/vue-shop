<template>
    <div class="cover">
        <div v-for='n in 10' :key='n'>
            <ItemCard :number='n' />
        </div>
    </div>
</template>

<script>
import ItemCard from "./Item-card.vue"

export default {
  components: { ItemCard },
    data() {
        return{
            
        }
    }
}
</script>

<style>
    .cover {
        display: grid;
        grid-template-columns: repeat(3, 1fr);
        gap: 10px;
        padding: 10px;
    }
</style>