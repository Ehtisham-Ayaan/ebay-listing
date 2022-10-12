<template>
  <div id="app" class="font">
    <NavBar />
    <ListingPage id="page" />
    <!-- <button @click="compiling" >Compile to Html</button> -->
  </div>
</template>

<script>
  import NavBar from './components/NavBar.vue'
  import ListingPage from './components/ListingPage.vue'

  export default {
    name: 'App',
    components: {
      NavBar,
      ListingPage
    },
    methods: {
      compiling(){
        let pageHTML = document.getElementById('app');
        let downloadHTML = pageHTML
        let tempEl = document.createElement('a');

        let html = '<head><title>Ebay</title><link rel="stylesheet" href="mystyle.css"/></head><body>'+
                    downloadHTML.outerHTML +
                    '</body>'

        tempEl.href = 'data:attachment/html,' + encodeURI(html)
        tempEl.target = '_blank';
        tempEl.download = 'thispage.html';
        tempEl.click();
      },
    }
  }
</script>

<style>
  @import "./components/css/utils.css";
 *{
    margin: 0px;
    padding:0px;
    box-sizing: border-box;
  }
  body{
    background-color: #F1F3F6;
  }
</style>
