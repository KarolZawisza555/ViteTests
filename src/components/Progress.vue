<template>
	<div
		class="progress my-1"
		role="progressbar"
		aria-label="Animated striped example"
		aria-valuenow="50"
		aria-valuemin="10"
		aria-valuemax="100">
		<div
			class="progress-bar progress-bar-striped progress-bar-animated"
			:style="valueProgres"></div>
	</div>
	<div
		class="progress my-1"
		role="progressbar"
		aria-label="Basic example"
		aria-valuenow="0"
		aria-valuemin="0"
		aria-valuemax="100">
		<div
			class="progress-bar"
			:style="valueProgres"></div>
	</div>
</template>
<script setup>
import { reactive, onMounted, computed } from "vue";
const state = reactive({ progress: 0 });
onMounted(() => {
	setInterval(() => {
		state.progress = (state.progress + 2) % 100;
	}, 500);
});
const valueProgres = computed(() => {
	return `width: ${state.progress}%`;
});
</script>
<style></style>
