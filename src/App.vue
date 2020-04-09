<template>
  <div id="app">

    <div class="body">
        <div class="search-body">
          <input class="search-box" v-model="searchString" type="text" @keyup.enter="search" />
          <button class="search-button" type="submit" @click="search">Google Search</button>
          <img class="search-icon" src="https://www.thinkafrica.fi/wp-content/uploads/2019/04/search-icon.png">
          <img class="google-logo" src="https://www.google.com/images/branding/googlelogo/1x/googlelogo_color_272x92dp.png">
        </div>

        <div class="footer">
          <a href ="https://www.google.com/intl/en_us/ads/">Advertising</a>
          <a href ="https://www.google.com/services/">Business</a>
          <a href="https://google.com/search/howsearchworks/">How Search works</a>
        </div>
    </div>

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

.search-body {
  position: relative;
}

.search-box {
  margin-top: 250px;
  height: 47px;
  width: 583px;
  border: 1px solid #dfe1e5;
  border-radius: 40px;
  font-family: 'Roboto';
  padding-left: 50px;
}
.search-box:hover {
  box-shadow: 0 1px 6px 0 rgba(32, 33, 36, .28);
}

.search-icon {
  height: 20px;
  width: 20px;
  display: flex;
  position: absolute;
  left: 450px;
  top: 265px;
}

.search-button {
  position: absolute;
  display: flex;
  left: 600px;
  margin-top: 20px;
  padding: 10px 15px;
  border: none;
  border-radius: 5px;
  background-color: rgb(240, 240, 240);
  color: rgb(90, 90, 90);
}
.search-button:hover {
  border: 3px black;
}

.google-logo {
  position: absolute;
  top: 0;
  left: 0;
  padding-left: 600px;
  padding-top: 125px;
}

.footer {
  position: absolute;
  align-items: center;
  bottom: 0;
  left: 0;
  text-decoration: none;
  display: flex;
  font-size: 15px;
  background-color: rgb(238, 238, 238);
  width: 100%;
  height: 35px;
}

a {
  text-decoration: none;
  color: rgb(100, 100, 100);
  margin-left: 50px;
}


</style>