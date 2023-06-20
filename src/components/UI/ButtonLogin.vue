<template>
	<button :class="border && 'border'">
		{{ text }}
	</button>
</template>
<script setup>
	const { text, border } = defineProps(['text', 'border']);
</script>
<style scoped>
	button {
		padding: 15px 0;
		width: 120px;
		border-radius: 10px;
		border: none;
		background-color: transparent;
		font-size: 16px;
		color: var(--mediumGray);
	}

	button:hover {
		cursor: pointer;
		color: var(--almostBlack);
	}

	.border {
		border: solid 2px var(--mediumGray);
	}

	.border:hover {
		border: solid 2px var(--almostBlack);
	}
</style>
