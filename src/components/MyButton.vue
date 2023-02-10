<script setup>
defineProps({
	color: {
		type: String,
		default: "primary",
	},
});
</script>

<template>
	<button
		type="button"
		:class="`btn btn-${color}`">
		Primary
	</button>
</template>

<style scoped></style>
