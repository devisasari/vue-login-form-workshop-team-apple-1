<script setup>
import { ref } from 'vue'

const props = defineProps(['name', 'placeholder', 'value', 'disabled', 'validate']);
const emit = defineEmits(['update:value']);

const inputType = ref('password');
const icon = ref('visibility');

const inputHandler = (e) => {
	emit('update:value', e.target.value);
};

const clickHandler = () => {
	inputType.value = inputType.value === 'password' ? 'text' : 'password';
	icon.value = icon.value === 'visibility' ? 'visibility_off' : 'visibility';
};

const validPass = () => {
	const passwordRegEx = "^(?=.*[a-z])(?=.*[A-Z])(?=.*\d)(?=.*[@$!%*?&])[A-Za-z\d@$!%*?&]{8,}$";

}
</script>

<template>

	<div class="form__group form__group--password" :class="validate ? 'valid': 'invalid'">
		<label :for="props.name" class="form__label">{{props.name}}</label>
		<span class="material-symbols-outlined" @click="clickHandler">{{ icon }}</span>
		<input :type="inputType" :id="props.name" class="form__input" @input="inputHandler" :placeholder="props.placeholder"
			:disabled="props.disabled" />
	</div>

</template>