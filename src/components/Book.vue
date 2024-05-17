<template>
  <div>
    <h3>{{ book.title }}</h3>
    <p>Penulis: {{ book.author }}</p>
    <p>Tahun Terbit: {{ book.year }}</p>
  </div>
</template>

<script>
export default {
  props: ['book']
}
</script>

<style scoped>
/* Gaya untuk Book.vue */
div {
  max-width: 600px;
  margin: 20px auto;
  padding: 20px;
  background-color: #b68282;
  border-radius: 5px;
  border: 1px solid rgb(177, 122, 122);
}
</style>
