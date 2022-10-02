<script setup>
import { ref } from 'vue'
const props = defineProps(['name', 'placeholder', 'value', 'disabled', 'classes']);
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

</script>
<template>
	<div class="form__group form__group--password">
		<input :type="inputType" :id="props.name" class="form__input" :class="props.classes" @input="inputHandler"
			:placeholder="props.placeholder" :disabled="props.disabled" />
		<label :for="props.name" class="form__label">{{props.name}}</label>
		<span class="material-symbols-outlined" @click="clickHandler">{{ icon }}</span>
	</div>
</template>