<template>
	<nav>
		<section class="logo-header">
			<Logo />
		</section>
		<section class="menu-section">
			<Menu />
			<Login />
		</section>

		<div class="icon-mobile" @click="toggleMenu">
			<img
				src="/images/icon-menu.svg"
				alt="icon open menu"
				v-if="stateMobileIcon"
			/>
			<img src="/images/icon-close-menu.svg" alt="icon open menu" v-else />
		</div>
	</nav>
</template>
<script setup>
	import { ref } from '@vue/reactivity';
	import { Menu, Logo, Login } from './Navbar';

	const stateMobileIcon = ref(true);

	const toggleMenu = () => {
		const menu = document.querySelector('.menu-section');
		menu.classList.toggle('show');
		stateMobileIcon.value = !stateMobileIcon.value;

		if (menu.classList.contains('show')) {
			document.body.style.overflow = 'hidden';
		} else {
			document.body.style.overflow = 'auto';
		}
	};
</script>

<style scoped>
	nav {
		display: flex;
		align-items: center;
		padding: 20px 0;
	}

	.menu-section {
		display: flex;
		align-items: center;
		justify-content: space-between;
		width: 100%;
		gap: 1rem;
	}

	.icon-mobile {
		z-index: 1;
		display: none;
	}

	.show {
		opacity: 1 !important;
	}

	.logo-header{
		z-index: 1;
	}

	@media (max-width: 991px) {
		nav {
			padding: 40px 0 20px 0;
			align-items: flex-start;
		}

		.icon-mobile {
			display: block;
			position: absolute;
			top: 30px;
			right: 20px;
		}

		.menu-section {
			opacity: 0;
			right: 10px;
			position: absolute;
			height: 100%;
			width: 55%;
			background-color: var(--almostWhite);
		}
	}
</style>
