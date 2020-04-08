<template>
  <div id="app">

    <div class= "body">
        <div class= "searchbody">
      <input class ="searchbox" v-model="searchString" type="text" @keyup.enter="search" />
      <button id = "searchbutton" type="submit" @click="search">Google Search</button>
      <link href="https://fonts.googleapis.com/css?family=Roboto&display=swap" rel="stylesheet">
      <img id="searchicon" src ="https://www.thinkafrica.fi/wp-content/uploads/2019/04/search-icon.png">
      <img id="googlelogo" src = "https://www.google.com/images/branding/googlelogo/1x/googlelogo_color_272x92dp.png">
    </div>

    <div class= "footer">
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

.searchbody {
  position: relative;
}

.searchbox {
  margin-top: 250px;
  margin-right: 50px;
  height: 47px;
  width: 583px;
  border: 1px solid #dfe1e5;
  border-radius: 40px;
  font-family: 'Roboto';
}
.searchbox:hover {
  box-shadow: 0 1px 6px 0 rgba(32, 33, 36, .28);
}

#searchicon {
  height: 20px;
  width: 20px;
  display: flex;
  position: absolute;
  top: 0;
  left: 0;
  padding-left: 460px;
  padding-top: 265px;
}

#searchbutton {
  position: absolute;
  display: flex;
  margin-left: 600px;
  margin-top: 20px;
  padding: 10px 15px;
  border: none;
  border-radius: 5px;
  background-color: rgb(240, 240, 240);
  color: rgb(90, 90, 90);
}
#searchbutton:hover {
  border: 3px black;
}

#googlelogo {
  position: absolute;
  top: 0;
  left: 0;
  padding-left: 600px;
  padding-top: 125px;
}

.footer {
  margin-top: 350px;
  margin-left: -1080px;
  text-decoration: none;
  display: inline-block;
  font-size: 15px;
  background-color: rgb(238, 238, 238);
  width: 345vh;
  height: 35px;
}

a {
  text-decoration: none;
  color: rgb(100, 100, 100);
  margin-left: 50px;
}


</style>