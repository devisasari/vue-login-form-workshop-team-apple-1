<script setup>
	const props = defineProps(['name', 'placeholder', 'value', 'disabled']);
	const emit = defineEmits(['update:value']);
	
	const inputHandler = (e) => {
		emit('update:value', e.target.value);
	};
	</script>
	<template>
		<div class="form__group">
			<input type="email" :id="props.name" class="form__input" @input="inputHandler" :placeholder="props.placeholder"
				:disabled="props.disabled" />
			<label :for="props.name" class="form__label">{{props.name}}</label>
		</div>
	</template>