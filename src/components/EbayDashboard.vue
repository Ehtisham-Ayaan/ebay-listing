<template>
	<div>
    <div v-if="dashboard" class="header header-font bg-light py-1">
      <div class="logo">
        <img class="ml-5 mt-1" width="150" src="../assets/logoM.png"/>
      </div>
      <div class="links upper-case text-white">
        <div class="link mr-5">
          <a 
            href="#" 
            class="text-dark" 
            @click="showList = true">
              <i class="fa-sharp fa-solid fa-arrow-left"></i>
          </a>
          <a href="#" class="text-dark">-</a>
        </div>
      </div>
    </div>
    <ListingCard 
      v-if="dashboard && showList" 
      class="w-85 center-margin mt-5 ml-5" 
      @showListing = "showListing" 
    />    
    <ListingDetails 
      v-else
      :listing="listing"
      :listings="listings" 
      :dashboard="dashboard"
      @deleteListing = "deleteListing"
      @viewProduct = "viewProduct"
      @renderTemplate = "renderTemplate"/>
	</div>
</template>

<script>
  import ListingCard from './card/ListingCard.vue'
  import axios from 'axios'
  import ListingDetails from './card/ListingDetails.vue'
	export default {
    data(){
      return{
        listingData:{
          hello: 'hello'
        },
        listings: [],
        listing: '',
        showList: true,
        dashboard: true
      }
    },
    components: {
      ListingCard,
      ListingDetails
    },
    methods: {
      showListing(listing) {
        this.listing = listing
        axios.get(`https://ecom-minds.herokuapp.com/${listing}.json`).then( res => {
          console.log(res)
          this.listings = res.data
          this.showList = false
        })
        .catch( err => {
          console.log(err)
        })
      },
      deleteListing(product){
        axios.delete(`http://127.0.0.1:3000/${this.listing}/${product.id}.json`).then(() => {
          this.showListing(this.listing)
        })
        .catch( err => {
          console.log(err)
        })
      },
      viewProduct(){
        this.dashboard = false
      },
      renderTemplate(){
        this.$emit('renderTemplate')
      }
    }
	}
</script>

<style scoped>
  .logo{
    width: 25%;
    float: left;
  }
  .links{
    display: flex;
    width: 75%;
    float: left;
    justify-content: flex-end;
    font-Weight: 500;
    font-size: 14px;
    line-height: 21px;
  }
  a{
    text-decoration: none;
  }
  .header{
    display: flex;
    align-items: center;
    font-size: 42px;
    line-height: 63px;
    font-size: 42px;
    line-height: 63px;
    padding-top: 0.5rem;
    padding-bottom: 0.5rem;
  }
</style>
