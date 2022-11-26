<template>
  <div id="app" class="font">
    <EbayDashboard 
      :template="template" 
      @changeTemplate="changeTemplate"
      @renderTemplate="renderTemplate"/>
    <button v-if="template" @click="compiling" >Compile to Html</button>
  </div>
</template>

<script>
  import EbayDashboard from './components/EbayDashboard.vue'
  import file from './assets/example.txt'
  import fileDownload from 'js-file-download'

  export default {
    name: 'App',
    components: {
      EbayDashboard
    },
    data(){
      return{
        template: false
      }
    },
    computed:{
      myTemplate(){
        return this.template
      }
    },
    watch: {
      myTemplate:{
        handler(value){
          this.template = value
        }
      }
    },
    methods: {
      async compiling(){
        let pageHTML = document.getElementById('app');
        let downloadHTML = pageHTML
        let html = "<head><title>Ebay</title><link href='https://fonts.googleapis.com/css?family=Poppins' rel='stylesheet'><style>"+ file +"</style></head><body>"+
                    downloadHTML.outerHTML +
                    "</body>"
        fileDownload(html, 'filename.html');
      },
      changeTemplate(){
        this.template = false
      },
      renderTemplate(){
        this.template = true
      }
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
