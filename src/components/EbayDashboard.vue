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
            @click="backButton">
              <i class="fa-sharp fa-solid fa-arrow-left"></i>
          </a>
        </div>
      </div>
    </div>
    <button 
      v-if="dashboard && showList" 
      class="center-margin mt-5 ml-5" 
      @click = "showListing('savermarts')" 
    >Saver Mart</button>    
    <ListingDetails 
      v-else
      :add="add"
      :template="template"
      :listing="listing"
      :listings="listings" 
      :dashboard="dashboard"
      @deleteListing="deleteListing"
      @addProduct="addProduct"       
      @viewProduct="viewProduct"
      @renderTemplate="renderTemplate"
      @showListing="showListing"/>
      <div v-if="this.loading" class="lds-hourglass"></div>
      <button v-if="template" @click="backButton">Back</button>
	</div>
</template>

<script>
  import axios from 'axios'
  import ListingDetails from './card/ListingDetails.vue'
	export default {
    props:["template"],
    data(){
      return{
        listingData:{
          hello: 'hello'
        },
        listings: [],
        listing: '',
        showList: true,
        dashboard: true,
        loading: false,
        add: false
      }
    },
    components: {
      ListingDetails
    },
    methods: {
      showListing(listing) {
        this.listing = listing
        this.loading = true
        axios.get(`https://ecom-minds.herokuapp.com/${listing}.json`).then( res => {
          this.listings = res.data
          this.showList = false
          this.loading  = false
        })
        .catch( err => {
          alert('Something went wrong while fetching through server. Please try again after some time')
          this.loading = false
          console.log(err)
        })
      },
      deleteListing(product){
        axios.delete(`https://ecom-minds.herokuapp.com/${this.listing}/${product.id}.json`).then(() => {
          this.showListing(this.listing)
        })
        .catch( err => {
          console.log(err)
        })
      },
      addProduct(){
        this.add = true
      },
      viewProduct(){
        this.dashboard = false
      },
      renderTemplate(){
        this.$emit('renderTemplate')
      },
      backButton(){
        if(!this.dashboard) this.dashboard = true
        else if(this.add) this.add = false
        else this.showList = true
        // this.$emit('renderTemplate')
        
        this.$emit('changeTemplate')
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
  .lds-hourglass {
    display: inline-block;
    position: absolute;
    top: 0;
    width: 100vw;
    height: 100vh;
    background: black;
    z-index: 10000;
    opacity: 0.4;
  }
  .lds-hourglass:after {
    content: " ";
    display: block;
    position: relative;
    border-radius: 50%;
    top: 42%;
    left: 46%;
    width: 0;
    height: 0;
    margin: 8px;
    box-sizing: border-box;
    border: 32px solid #fff;
    border-color: #fff transparent #fff transparent;
    animation: lds-hourglass 1.2s infinite;
  }
  @keyframes lds-hourglass {
    0% {
      transform: rotate(0);
      animation-timing-function: cubic-bezier(0.55, 0.055, 0.675, 0.19);
    }
    50% {
      transform: rotate(900deg);
      animation-timing-function: cubic-bezier(0.215, 0.61, 0.355, 1);
    }
    100% {
      transform: rotate(1800deg);
    }
  }

</style>
