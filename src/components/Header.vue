<template>
  <header>
    <h1>{{ title }}</h1>
  </header>
</template>

<script>
export default {
  data() {
    return {
      title: 'BookWise'
    };
  }
}
</script>

<style scoped>
/* Gaya untuk Header.vue */
header {
  background-color: rgb(85, 34, 34);
  color: rgb(255, 255, 255);
  padding: 20px;
  text-align: center;
}
</style>
