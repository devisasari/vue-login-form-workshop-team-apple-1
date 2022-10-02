<script setup>
const props = defineProps(['name', 'variant', 'classes']);
</script>
	
<template>
	<button :class="[props.classes, 'btn btn-'+props.variant]">{{props.name}}</button>
</template>

<style lang="scss">
.btn {
	padding: 0.5rem 1rem;
	border-radius: 0.25rem;
	border: none;
	cursor: pointer;
	font-size: 1rem;
	font-weight: 600;
	transition: all 0.2s ease-in-out;

	&:hover {
		transform: translateY(-2px);
	}
}
</style>