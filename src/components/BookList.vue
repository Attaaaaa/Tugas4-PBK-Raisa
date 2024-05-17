<template>
  <div class="book-list">
    <h2>{{ header }}</h2>
    <ul>
      <li v-for="book in books" :key="book.id" @click="selectBook(book)" class="book-item">
        <strong>Judul:</strong> {{ book.title }}<br>
        <strong>Penulis:</strong> {{ book.author }}
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  props: ['books', 'header'],
  methods: {
    selectBook(book) {
      this.$emit('book-selected', book);
    }
  }
}
</script>

<style scoped>
/* Gaya untuk BookList.vue */
.book-list {
  max-width: 600px;
  margin: 0 auto;
}

.book-item {
  cursor: pointer;
  margin-bottom: 20px;
  padding: 10px;
  background-color: #a76e6e;
  border-radius: 5px;
  border: 1px solid rgb(124, 76, 76);
}

.book-item:hover {
  background-color: #cccccc;
}
</style>
