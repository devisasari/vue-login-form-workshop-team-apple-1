<script setup>
import { computed } from 'vue'
const props = defineProps(['name', 'placeholder', 'value', 'disabled', 'classes']);
const emit = defineEmits(['update:value']);
const validate = computed(() => {
	return props.value != '' ? 'valid' : 'invalid';
});
const inputHandler = (e) => {
	emit('update:value', e.target.value);
};
</script>
<template>
	<div class="form__group">
		<input type="text" :id="props.name" class="form__input" :class="props.classes" @input="inputHandler"
			:placeholder="props.placeholder" :disabled="props.disabled" />
		<label :for="props.name" class="form__label">{{props.name}}</label>
	</div>
</template>