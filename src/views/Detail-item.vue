<template>
  <div>
      <h1>This page is Number {{number}} Item</h1>
  </div>
</template>

<script>
export default {
    name: 'Item',
    props: {
        number: {
            type: Number,
            require: true,
        }
    }
}
</script>

<style>

</style>