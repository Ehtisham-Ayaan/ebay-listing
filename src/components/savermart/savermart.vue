<template>
  <div>
    <NavBar />
    <ListingPage :phone="phone"/>
    <FooTer />
  </div>
</template>

<script>
  import NavBar from './modules/NavBar.vue'
  import ListingPage from './modules/ListingPage.vue'
  import FooTer from './modules/FooTer.vue'

  export default {
    name: 'App',
    props: ["phone"],
    components: {
      NavBar,
      ListingPage,
      FooTer
    },
    mounted(){
      console.log(this.phone)
    },
    methods: {
      
    }
  }
</script>

<style>
</style>
