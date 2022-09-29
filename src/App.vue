<template>
  <div id="app">
    <ListingPage />
  </div>
</template>

<script>
import ListingPage from './components/ListingPage.vue'

export default {
  name: 'App',
  components: {
    ListingPage
  }
}
</script>

<style>
 *{
  margin: 0px;
  padding:0px;
  box-sizing: border-box;
 }
 body{
  background-color: #F1F3F6;
 }
</style>
