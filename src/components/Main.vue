<template>
	<section class="main-content">
		<div class="title">
			<h1>Make remote work</h1>
			<p>
				Get your team in sync, no matter your location. Streamline processes,
				create team rituals, and watch productivity soar.
			</p>
			<button class="learn-button">Learn more</button>
			<Sponsors />
		</div>
		<div class="banner-image">
			<img
				src="/images/image-hero-desktop.png"
				class="hero-image"
				alt="hero image snap"
			/>
		</div>
	</section>
</template>
<script setup>
	import { Sponsors } from './UI';
</script>
<style scoped>
	.main-content {
		display: flex;
		align-items: center;
		justify-content: center;
		gap: 10rem;
		margin-top: 70px;
	}

	h1 {
		font-size: 102px;
		max-width: 700px;
		margin: 0;
	}

	p {
		max-width: 550px;
		font-size: 19px;
		line-height: 29px;
		color: var(--mediumGray);
	}

	.title {
		display: flex;
		flex-direction: column;
		align-items: flex-start;
		gap: 1rem;
	}

	.banner-image {
		max-width: 500px;
	}

	.banner-image img {
		width: 100%;
	}

	.learn-button {
		background-color: var(--almostBlack);
		color: var(--almostWhite);
		border: none;
		padding: 20px 25px;
		font-size: 21px;
		border: 2px solid;
		border-radius: 20px;
	}

	.learn-button:hover {
		background-color: var(--almostWhite);
		color: var(--almostBlack);
		border: 2px solid var(--almostBlack);
		cursor: pointer;
	}

	@media (max-width: 991px) {
		.main-content {
			flex-direction: column-reverse;
			gap: 5rem;
			margin-top: 30px;
		}

		.hero-image {
			content: url('/images/image-hero-mobile.png');
		}

		.title {
			align-items: center;
		}

		h1 {
			font-size: 32px;
		}

		p {
			text-align: center;
			font-size: 16px;
		}
	}
</style>
