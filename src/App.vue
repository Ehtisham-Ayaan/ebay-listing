<template>
  <div id="app" class="font">
    <NavBar />
    <ListingPage id="page" />
    <button @click="compiling" >Compile to Html</button>
    <FooTer />
  </div>
</template>

<script>
  import NavBar from './components/NavBar.vue'
  import ListingPage from './components/ListingPage.vue'
  import FooTer from './components/FooTer.vue'
  import file from './assets/example.txt'
  import fileDownload from 'js-file-download'

  export default {
    name: 'App',
    components: {
      NavBar,
      ListingPage,
      FooTer
    },
    methods: {
      async compiling(){



        let pageHTML = document.getElementById('app');
        let downloadHTML = pageHTML
        // let tempEl = document.createElement('a');

        let html = "<head><title>Ebay</title><link href='https://fonts.googleapis.com/css?family=Poppins' rel='stylesheet'><style>"+ file +"</style></head><body>"+
                    downloadHTML.outerHTML +
                    "</body>"

        // console.log(html.toString())

        fileDownload(html, 'filename.html');

        // tempEl.href = 'data:attachment/html,' +  encodeURI(html)
        // tempEl.target = '_blank';
        // tempEl.download = 'thispage.html';
        // tempEl.click();
      },
    }
  }
</script>

<style>
  @import "./components/css/utils.css";
  @import "./components/css/utlisr.css";
 *{
    margin: 0px;
    padding:0px;
    box-sizing: border-box;
  }
  body{
    background-color: #F1F3F6;
  }
</style>
