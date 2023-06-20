<template>
	<div class="sponsors">
		<img src="/images/client-databiz.svg" alt="client databiz image" />
		<img src="/images/client-audiophile.svg" alt="client audiophile image" />
		<img src="/images/client-meet.svg" alt="client meet image" />
		<img src="/images/client-maker.svg" alt="client maker image" />
	</div>
</template>
<style scoped>
	.sponsors {
		display: flex;
		justify-content: space-between;
		align-items: center;
		width: 100%;
		gap: 1rem;
		margin-top: 50px;
	}

	.sponsors img {
		width: 100%;
	}

	@media (max-width: 991px) {
		.sponsors {
			margin-bottom: 30px;
		}
		.sponsors img {
			width: auto;
		}
	}

	@media (max-width: 400px) {
		.sponsors {
			flex-direction: column;
			gap: 2rem;
		}
	}
</style>
