<script setup>
import { ref } from 'vue'
import RegisterForm from '@components/Forms/RegisterForm.vue';
import LoginForm from '@components/Forms/LoginForm.vue';
const show = ref(false);
const showForm = (value) => {
	show.value = value;
};
</script>
	
<template>
	<div class="container">
		<transition name="fade">
			<template v-if="show">
				<LoginForm />
			</template>
			<template v-else>
				<RegisterForm @show="showForm" />
			</template>
		</transition>
	</div>
</template>
	
<style lang="scss">
.container {
	display: flex;
	flex-direction: row;
	align-items: center;
	justify-content: center;
	min-height: 100vh;
}
</style>