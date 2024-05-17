<template>
  <div id="app">
    <Header />
    <BookList :books="books" :header="listHeader" @book-selected="selectBook" />
    <Book v-if="selectedBook" :book="selectedBook" />
  </div>
</template>

<script>
import Header from './components/Header.vue';
import BookList from './components/BookList.vue';
import Book from './components/Book.vue';

export default {
  components: {
    Header,
    BookList,
    Book
  },
  data() {
    return {
      listHeader: 'Daftar Buku',
      books: [
        { id: 1, title: 'Sherlock Holmes', author: 'Sir Arthur Conan Doyle', year: 1887 },
        { id: 2, title: 'Percy Jackson & the Olympians', author: 'Rick Riordan', year: 2005  },
        { id: 3, title: 'School for Good and Evil', author: 'Soman Chainani', year: 2013 }
      ],
      selectedBook: null
    };
  },
  methods: {
    selectBook(book) {
      this.selectedBook = book;
    }
  }
}
</script>

<style>
/* Gaya untuk App.vue */
#app {
  font-family: Arial, sans-serif;
}
</style>
