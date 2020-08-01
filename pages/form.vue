<template>
	<div>
		<nuxt-link to='/'><button class="btn-round" style="padding-top:0;" >&#8592;</button></nuxt-link>
		<span class="back-btn">
			Back to Home
		</span>
		<br>
		<br>
		<div 
		style="position:absolute;
		top:50%;left:50%;
		transform:translate(-50%,-50%);">
		<form @submit.prevent="submitted" accept-charset="utf-8">
			
			<input type="text" id="name-input" v-bind:requried="true" v-model="name" placeholder="Name">
			<br>
			<br>
			<input type="email"  id= "email-input" v-bind:requried="true" v-model="email" placeholder="Email">
			<br>
			<br>
			<select id="select-board" v-model = "board" v-bind:requried="true">
				<option  disabled selected>Board</option>
				<option >CBSE</option>
				<option >ICSE</option>
			</select>
			<br>
			<br>
			<button type="submit">Submit</button>
			
		</form>
	</div>

</div>
</template>

<script>
import isEmail from 'validator/lib/isEmail';
export default {

	data(){
		return{
			name:"",
			email:"",
			board:"Board"
		}
	},
	methods:{
		submitted(){
			
			document.getElementById('select-board').style.border = '1px solid black';
			document.getElementById('email-input').style.border = '1px solid black';
			document.getElementById('name-input').style.border = '1px solid black';

			if(this.board==="Board"){
				document.getElementById('select-board').style.border = '1px solid red';
				return;
			}
			if(!isEmail(this.email)){
				document.getElementById('email-input').style.border = '1px solid red';
				return;
			}
			if(this.name===""){
				document.getElementById('name-input').style.border = '1px solid red';
				return;
			}

			alert('Form Submitted');

			
		}
	}


}
</script>
<style>
input{
	height:30px;
	outline:0px;
	border:1px solid;
	padding-left:5px;
}
select{
	width:178px;
	height:30px;
}
.back-btn{
	font-family:
	'Quicksand',
	'Source Sans Pro',
	-apple-system,
	BlinkMacSystemFont,
	'Segoe UI',
	Roboto,
	'Helvetica Neue',
	Arial,
	sans-serif;
	font-weight: 300;
	color: #35495e;
	letter-spacing: 1px;
	font-size:20px;
}
</style>