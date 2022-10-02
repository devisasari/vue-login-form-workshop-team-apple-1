<script setup>
import LoginForm from './components/Forms/LoginForm.vue';
// import RegisterForm from './components/Forms/RegisterForm.vue';
</script>

<template>
	<div class="container">
		<LoginForm />
		<!-- <RegisterForm /> -->
	</div>
</template>

<style lang="scss">
.container {
	display: flex;
	flex-direction: column;
	align-items: center;
	justify-content: center;
	min-height: 100vh;
}
</style>
