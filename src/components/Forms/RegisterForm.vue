<script setup>
	import { ref } from 'vue'
	
	import Button from '../Button/Button.vue';
	import TextInput from '../Inputs/TextInput.vue';
	import EmailInput from '../Inputs/EmailInput.vue';
	import PasswordInput from '../Inputs/PasswordInput.vue';
	import NumberInput from '../Inputs/NumberInput.vue';
	
	const emit = defineEmits(['show']);
	
	const form = ref({
		fullname: '',
		email: '',
		password: '',
		confirmPassword: '',
	});
	
	const submitHandler = () => {
		localStorage.setItem('user', JSON.stringify(form.value));
	};
	const clickHandler = () => {
		emit('show', true)
	};
	</script>
		
	<template>
		<form class="form" @submit.prevent="submitHandler">
			<div class="form__title">Register</div>
	
			<TextInput name="Fullname" placeholder="Fullname" v-model:value="form.fullname" />
			<EmailInput name="Email" placeholder="Email" v-model:value="form.email" />
			<NumberInput name="Phone" placeholder="Phone" v-model:value="form.phone" />
			<PasswordInput name="Password" placeholder="Password" v-model:value="form.password" />
			<PasswordInput name="Confirm Password" placeholder="Confirm Password" v-model:value="form.confirmPassword" />
	
			<Button name="Register" variant="primary" classes="w-100 mt-4" />
			<Button name="Have account ? Sing in" variant="secondary" classes="w-100 mt-1" @click="clickHandler" />
		</form>
	</template>