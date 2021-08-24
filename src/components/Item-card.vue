<template>
    <router-link :to="{
        name: 'Item',
        params: { number: this.number},
        }"
        style=text-decoration:none;>
        <v-card elevation="2">
            <v-img height="250" />
            <v-divider></v-divider>
            <v-card-title>Number : {{number}}</v-card-title>
        </v-card>
    </router-link>
</template>

<script>
export default {
    props: {
        number: {
            type: Number,
            require:true,
        }
    }
}
</script>

<style>

</style>