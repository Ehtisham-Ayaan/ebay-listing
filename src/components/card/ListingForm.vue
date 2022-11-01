<template>
	<div class="main-block">
		<form class="my-5">
			<div class="info">
				<input class="fname" type="text" name="name" v-model="phone.name" placeholder="Phone Name">
				<input type="text" name="name" v-model="phone.display" placeholder="Display">
				<input type="text" name="name" v-model="phone.ram" placeholder="Ram">
				<input type="text" name="name" v-model="phone.battery" placeholder="Battery">
				<input type="text" name="name" v-model="phone.back_camera" placeholder="Back Camera">
				<input type="text" name="name" v-model="phone.release_date" placeholder="Release Date">
				<input type="text" name="name" v-model="phone.sim_support" placeholder="Sim Support">
				<input type="text" name="name" v-model="phone.phone_dimension" placeholder="Phone Dimensions">
				<input type="text" name="name" v-model="phone.phone_weight" placeholder="Phone Weight">
				<input type="text" name="name" v-model="phone.operating_system" placeholder="Operating System">
				<input type="text" name="name" v-model="phone.processor" placeholder="Processor">
				<input type="text" name="name" v-model="phone.gpu" placeholder="GPU">
				<input type="text" name="name" v-model="phone.screen_size" placeholder="Screen Size">
				<input type="text" name="name" v-model="phone.screen_resolution" placeholder="Screen Resolution">
				<input type="text" name="name" v-model="phone.screen_type" placeholder="Screen Type">
				<input type="text" name="name" v-model="phone.screen_protection" placeholder="Screen Protection">
				<input type="text" name="name" v-model="phone.front_camera" placeholder="Front Camera">
				<input type="text" name="name" v-model="phone.front_flashlight" placeholder="Front Flashlight">
				<input type="text" name="name" v-model="phone.front_video_recording" placeholder="Front Video Recording">
				<input type="text" name="name" v-model="phone.back_flaslight" placeholder="Back Flashlight">
				<input type="text" name="name" v-model="phone.back_video_recording" placeholder="Back Video Recording">
				<input type="text" name="name" v-model="phone.internal_memory" placeholder="Internal Memory">
				<input type="text" name="name" v-model="phone.battery_type" placeholder="Battery Type">
				<select v-model="phone.card_slot">
					<option value="card" disabled selected>Card Slot</option>
					<option value="true">Yes</option>
					<option value="false">No</option>
				</select>
				<select v-model="phone.bluetooth">
					<option value="bluetooth" disabled selected>Bluetooth</option>
					<option value="true">Yes</option>
					<option value="false">No</option>
				</select>
				<select v-model="phone.G3">
					<option value="3g" disabled selected>3G</option>
					<option value="true">Yes</option>
					<option value="false">No</option>
				</select>
				<select v-model="phone.G4">
					<option value="4g" disabled selected>4G</option>
					<option value="true">Yes</option>
					<option value="false">No</option>
				</select>
				<select v-model="phone.G5">
					<option value="5g" disabled selected>5G</option>
					<option value="true">Yes</option>
					<option value="false">No</option>
				</select>
				<select v-model="phone.radio">
					<option value="radio" disabled selected>Radio</option>
					<option value="true">Yes</option>
					<option value="false">No</option>
				</select>
				<select v-model="phone.wifi">
					<option value="wifi" disabled selected>Wi-Fi</option>
					<option value="true">Yes</option>
					<option value="false">No</option>
				</select>
				<select v-model="phone.nfc">
					<option value="nfc" disabled selected>NFC</option>
					<option value="true">Yes</option>
					<option value="false">No</option>
				</select>
				<div class="d-flex flex-wrap w-100">
					<span class="text-white"> FAQ </span>
					<div v-for="faq in phone.faq" :key="faq.id" class="fname ml-2 w-100">
						<input class="" type="text" name="name" v-model="faq.question" placeholder="Question">
						<input class="ml-3" type="text" name="name" v-model="faq.answer" placeholder="Answer">
						<i @click="addFaq" class="text-white fa-sharp fa-solid fa-plus"></i>
						<i @click="deleteFaq(faq)" class="text-white fa-sharp fa-solid fa-minus ml-1"></i>
					</div>
				</div>
				<div class="d-flex flex-wrap w-100">
					<span class="text-white"> What’s in the Box </span>
					<div v-for="box in phone.box" :key="box.id" class="fname ml-2 w-100">
						<input class="" type="text" name="name" v-model="box.in_box" placeholder="In Box">
						<i @click="addFaq('box')" class="text-white fa-sharp fa-solid fa-plus"></i>
						<i @click="deleteFaq('box', box)" class="text-white fa-sharp fa-solid fa-minus ml-1"></i>
					</div>
				</div>
				<div class="d-flex flex-wrap w-100">
					<span class="text-white"> Condition </span>
					<div v-for="cond in phone.cond" :key="cond.id" class="fname ml-2 w-100">
						<input class="" type="text" name="name" v-model="cond.condition" placeholder="Condition">
						<i @click="addFaq('cond')" class="text-white fa-sharp fa-solid fa-plus"></i>
						<i @click="deleteFaq('cond', cond)" class="text-white fa-sharp fa-solid fa-minus ml-1"></i>
					</div>
				</div>
			</div>
			<button @click="submit" class="button">Submit</button>
		</form>
	</div>
</template>
<script>
	import axios from "axios"
	export default{
		props:["my_phone"],
		data(){
			return {
				phone: {
					card_slot: 'card',
					bluetooth: 'bluetooth',
					radio: 'radio',
					G3: '3g',
					G4: '4g',
					G5: '5g',
					nfc: 'nfc',
					wifi: 'wifi',
					faq: [{
						question: '',
						answer: ''
					}],
					box: [{
						in_box: ''
					}],
					cond: [{
						condition: ''
					}]
				},
				editing: false
			}
		},
		mounted(){
			if(this.my_phone){
				this.phone = this.my_phone
				this.phone.faq = JSON.parse(this.phone.faq)
				this.phone.box = JSON.parse(this.phone.box)
				this.phone.cond = JSON.parse(this.phone.cond)
				this.editing = true
			}
		},
		methods: {
			addFaq(data){
				if(data == "box") this.phone.box.push({ in_box: '' })
				else if (data == "cond")this.phone.cond.push({	condition: ''	})
				else {
					this.phone.faq.push({
						question: '',
						answer: ''
					})
				}
			},
			deleteFaq(data, value){
				if (data == "box"){
					const index = this.phone.box.map(object => object).indexOf(value)
					if(this.phone.box.length > 1) this.phone.box.splice(index, 1)
				}
				else if (data == "cond"){
					const index = this.phone.cond.map(object => object).indexOf(value)
					if(this.phone.cond.length > 1) this.phone.cond.splice(index, 1)
				}
				else{
					const index = this.phone.faq.map(object => object).indexOf(value)
					if(this.phone.faq.length > 1) this.phone.faq.splice(index, 1)
				}
			},
			submit(){
				this.phone.faq = JSON.stringify(this.phone.faq)
				this.phone.box = JSON.stringify(this.phone.box)
				this.phone.cond= JSON.stringify(this.phone.cond)
				if(this.editing && this.my_phone){
					axios.put(`https://ecom-minds.herokuapp.com/savermarts/${this.my_phone.id}.json`, this.phone)	
					.catch( err => {
						console.log(err)
					})
				} else {
					axios.post(`https://ecom-minds.herokuapp.com/savermarts.json`, this.phone)
					.catch( err => {
						console.log(err)
					})
				}
			}
		}
	}
</script>
<style scoped>
	@import "./my_form.css";
</style>
