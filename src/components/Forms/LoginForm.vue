<script setup>
	import { ref } from 'vue'
	import Button from '../Button/Button.vue';
	import TextInput from '../Inputs/TextInput.vue';
	import PasswordInput from '../Inputs/PasswordInput.vue';
	
	const form = ref({
		username: '',
		password: '',
	});
	
	const submitHandler = () => {
		localStorage.getItem('user');
	};
	</script>
	
	<template>
		<form class="form" @submit.prevent="submitHandler">
			<div class="form__title">Login</div>
	
			<TextInput name="username" classes="rounded" placeholder="Username" v-model:value="form.username" />
			<PasswordInput name="password" classes="rounded" placeholder="Password" v-model:value="form.password" />
	
			<Button name="Sign in" variant="secondary" classes="text-uppercase mt-4" />
		</form>
	</template>