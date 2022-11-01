<template>
	<div v-if="!add && dashboard" class="w-85 center-margin mt-2">
		<article v-for="product in listings" :key="product.id" class="mt-1 leaderboard__profile">
			<span class="leaderboard__name"> {{ product.name }} </span>
			<span class="leaderboard__value">
				<span>
					<i 
						class="text-dark fa-sharp fa-solid fa-eye ml-1" 
						@click="viewProduct(product)">
					</i>
				</span>
				<span>
					<i 
						class="text-success fa-sharp fa-solid fa-pencil ml-1" 
						@click="editProduct(product)">
					</i>
				</span>
				<span>
					<i 
						class="text-danger fa-sharp fa-solid fa-minus ml-1" 
						@click="deleteProduct(product)">
					</i>
				</span>
			</span>
		</article>
		<article class="leaderboard__profile mt-1">
			<span class="leaderboard__name">New Item</span>
			<span class="leaderboard__value">
				<span>
					<i 
						class="text-success fa-sharp fa-solid fa-plus" 
						@click="addProduct()">
					</i>
				</span>
			</span>
		</article>
	</div>
	<ListingForm v-else-if="dashboard" :my_phone="phone"></ListingForm>
	<SaverMart v-else :phone="phone"/>
</template>
<script>
	import ListingForm from "./ListingForm.vue"
	import SaverMart from '../savermart/savermart.vue'
	export default{
		components: {
			ListingForm,
			SaverMart
		},
		props: ["listing","listings","dashboard"],
		data(){
			return{
				add: false,
				phone: null
			}
		},
		methods: {
			addProduct(){
				this.add = true
			},
			viewProduct(product){
				this.$emit('viewProduct')
				this.$emit('renderTemplate')
				this.phone = product
			},
			editProduct(product){
				this.phone = product
				this.add = true
			},
			deleteProduct(product){
				this.$emit("deleteListing",product)
			},
		} 
	}
</script>
<style scoped> 
	@import "./list.css";
</style>