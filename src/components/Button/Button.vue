<script setup>
const props = defineProps(['name', 'variant', 'classes']);
</script>
	
<template>
	<button :class="[props.classes, 'btn btn-'+props.variant]">{{props.name}}</button>
</template>

<style lang="scss">
.btn {
	padding: 16px 32px;
	border: none;
	cursor: pointer;
	transition: all 0.2s ease-in-out;

	&-primary {
		background-color: #8b54ff;
		color: white;

		&:hover {
			background-color: #613ab2;
		}
	}
}
</style>