<template>
	<section class="login">
		<ButtonLogin text="Login" />
		<ButtonLogin text="Register" :border="true" />
	</section>
</template>
<script setup>
	import { ButtonLogin } from '../UI';
</script>
<style scoped>
	.login {
		display: flex;
		gap: 1rem;
	}

	@media (max-width: 991px) {
		.login {
			position: absolute;
			flex-direction: column;
			top: 350px;
			right: 50px;
		}
	}
</style>
