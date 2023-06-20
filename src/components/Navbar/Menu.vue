<template>
	<ul class="menu">
		<li>
			<a href="#" @click="handleShowFeaturesMenu"
				>Features <img src="/images/icon-arrow-down.svg" alt="icon arrow down"
			/></a>
			<SubMenuFeatures v-if="dropdownState.showFeaturesMenu" />
		</li>
		<li>
			<a href="#" @click="handleShowCompanyMenu"
				>Company <img src="/images/icon-arrow-down.svg" alt="icon arrow down"
			/></a>
			<SubMenuCompany v-if="dropdownState.showCompanyMenu" />
		</li>
		<li><a href="#">Careers</a></li>
		<li><a href="#">About</a></li>
	</ul>
</template>
<script setup>
	import { reactive } from '@vue/reactivity';
	import { SubMenuFeatures, SubMenuCompany } from '../Navbar';

	const dropdownState = reactive({
		showFeaturesMenu: false,
		showCompanyMenu: false,
	});

	const handleShowFeaturesMenu = () => {
		dropdownState.showFeaturesMenu = !dropdownState.showFeaturesMenu;
	};

	const handleShowCompanyMenu = () => {
		dropdownState.showCompanyMenu = !dropdownState.showCompanyMenu;
	};
</script>
<style scoped>
	.menu {
		display: flex;
		gap: 2.5rem;
		margin-left: 50px;
	}

	a {
		display: flex;
		align-items: center;
		gap: 0.4rem;
	}

	@media (max-width: 991px) {
		.menu {
			position: absolute;
			flex-direction: column;
			top: 100px;
			right: 50px;
		}
	}
</style>
