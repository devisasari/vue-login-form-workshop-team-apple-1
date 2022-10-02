<script setup>
import Button from '../Button/Button.vue';

</script>

<template>
	<form class="form">
		<div class="form__title">Login</div>
		<div class="form__group">
			<input type="email" id="email" class="form__input rounded"  placeholder="Full Name"/>
			<label for="email" class="form__label">Boş brakılamaz</label>
		</div>

		<div class="form__group">
			<input type="phone" id="phone" class="form__input"  placeholder="Full Name"/>
			<label for="phone" class="form__label">Boş brakılamaz</label>
		</div>

		<Button name="Register" variant="primary" classes="text-uppercase mt-4" />
	</form>
</template>

<style lang="scss">
.form {
	padding: 24px;
	box-shadow: rgba(0, 0, 0, 0.35) 0px 5px 15px;
	border-radius: 12px;
	display: flex;
	flex-direction: column;
	align-items: center;
	justify-content: center;
	width: 100%;
	max-width: 400px;
	gap: 8px;
	&__title {
		margin: 32px 0;
		font-size: 32px;
		font-weight: 600;
		color: #252eff;
		width: 100%;
		text-align: center;
	}
	&__group {
		position: relative;
		width: 100%;
		display: flex;
		flex-direction: column;
	}

	&__input {
		width: 100%;
		padding: 8px 16px;
		border: none;
		border-radius: 8px;
		background-color: #fff;
		border: 3px solid #6066ff;
		transition: all 0.3s ease-in-out;

		&::placeholder {
			color: #333;
			font-size: 14px;
			font-weight: 500;
		}

		&:focus {
			border-color: rgb(196, 196, 196);
		}
	}

	&__label {
		font-size: 12px;
		margin-left: 8px;
	}
}
</style>