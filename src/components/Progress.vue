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
			class="progress-bar bg-success"
			:style="valueProgres2"></div>
	</div>
	<div
		class="progress"
		role="progressbar"
		aria-label="Example with label"
		aria-valuenow="25"
		aria-valuemin="0"
		aria-valuemax="100">
		<div
			class="progress-bar"
			:style="valueProgres3">
			{{ state.progress3 }} %
		</div>
	</div>
	<div
		class="progress my-1"
		role="progressbar"
		aria-label="Danger example"
		aria-valuenow="100"
		aria-valuemin="0"
		aria-valuemax="100">
		<div
			:class="colorBar"
			:style="valueProgres3"></div>
	</div>
	<p class="new h1">NEW FEATURE VUE 3 V-bind in css clasess</p>
	<p class="newFeatureVue3">{{ state.color }}</p>
</template>
<script setup>
import { reactive, onMounted, computed } from "vue";
const state = reactive({
	progress: 0,
	progress2: 0,
	progress3: 0,
	randomColor: "#fffffff",
});
function getRandomColor() {
	const letters = "0123456789ABCDEF";
	let color = "#";
	for (let i = 0; i < 6; i++) {
		color += letters[Math.floor(Math.random() * 16)];
	}
	return color;
}
onMounted(() => {
	setInterval(() => {
		state.progress = (state.progress + 2) % 100;
		state.progress2 = (state.progress2 + 4) % 100;
		state.progress3 = (state.progress3 + 3) % 100;
	}, 500);
	setInterval(() => {
		state.color = getRandomColor();
	}, 1000);
});
const randomBackgroundColor = computed(() => {
	return `width: ${state.progress}%`;
});
const valueProgres = computed(() => {
	return `width: ${state.progress}%`;
});
const valueProgres2 = computed(() => {
	return `width: ${state.progress2}%`;
});
const valueProgres3 = computed(() => {
	return `width: ${state.progress3}%`;
});
// ---------------------------------------------------------------------------
// Generate by Chat GPT
// ---------------------------------------------------------------------------
const colorBar = computed(() => {
	if (state.progress3 >= 75) return "progress-bar bg-success";
	else if (state.progress3 >= 50) return "progress-bar bg-info";
	else if (state.progress3 >= 25) return "progress-bar bg-warning";
	else return "progress-bar bg-danger";
});
</script>
<style>
.newFeatureVue3 {
	background-color: v-bind(state.color);
}
.new {
	color: v-bind(state.color);
}
</style>
