<script setup>
const props = defineProps(['name', 'variant', 'classes']);
</script>
	
<template>
	<button :class="[props.classes, 'btn btn-'+props.variant]">{{props.name}}</button>
</template>

<style lang="scss">
.btn {
	padding: 9px 32px;
	border: none;
	cursor: pointer;
	transition: all 0.2s ease-in-out;
	font-weight: 500;

	&-primary {
		background-color: #8b54ff;
		color: #fff;
		border-radius: 16px;

		&:hover {
			background-color: #613ab2;
		}
	}

	&-secondary {
		background-color: #6066ff;
		color: #fff;
		border-radius: 16px;

		&:hover {
			background-color: #4347b2;
		}
	}
}
</style>