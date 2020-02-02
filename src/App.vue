<template>
  <div id="app">
    <input v-model="searchString" type="text" @keyup.enter="search" />
    <button type="submit" @click="search">Search</button>
  </div>
</template>

<script>
export default {
  name: 'app',
  data() {
    return {
      searchString: ''
    }
  },
  methods: {
    search: function() {
      window.open('https://www.google.com/search?q=' + this.searchString, '_self');
    }
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
