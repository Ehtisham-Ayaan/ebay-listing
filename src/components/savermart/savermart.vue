<template>
  <div>
    <NavBar />
    <ListingPage />
    <FooTer />
  </div>
</template>

<script>
  import NavBar from './modules/NavBar.vue'
  import ListingPage from './modules/ListingPage.vue'
  import FooTer from './modules/FooTer.vue'

  export default {
    name: 'App',
    components: {
      NavBar,
      ListingPage,
      FooTer
    },
    methods: {
      
    }
  }
</script>

<style>
</style>
