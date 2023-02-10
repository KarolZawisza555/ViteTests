<script setup>
import { ref } from "vue";

const showSpinners = ref(false);
</script>

<template>
    <div id="spinners" class="d-flex align-items-center justify-content-center">

        <button
        type="button"
        class="btn btn-primary btn-lg"
        @click="showSpinners = !showSpinners">
        {{ !showSpinners ? "Show" : "Hide" }} Spinners
    </button>
</div>
	<div
		id="spinners"
		class="d-flex align-items-center justify-content-center">
		<div v-if="showSpinners">
			<div
				class="spinner-border text-primary"
				role="status">
				<span class="visually-hidden">Loading...</span>
			</div>
			<div
				class="spinner-border text-secondary"
				role="status">
				<span class="visually-hidden">Loading...</span>
			</div>
			<div
				class="spinner-border text-success"
				role="status">
				<span class="visually-hidden">Loading...</span>
			</div>
			<div
				class="spinner-border text-danger"
				role="status">
				<span class="visually-hidden">Loading...</span>
			</div>
			<div
				class="spinner-border text-warning"
				role="status">
				<span class="visually-hidden">Loading...</span>
			</div>
			<div
				class="spinner-border text-info"
				role="status">
				<span class="visually-hidden">Loading...</span>
			</div>
			<div
				class="spinner-border text-light"
				role="status">
				<span class="visually-hidden">Loading...</span>
			</div>
			<div
				class="spinner-border text-dark"
				role="status">
				<span class="visually-hidden">Loading...</span>
			</div>
			<div
				class="spinner-grow text-primary"
				role="status">
				<span class="visually-hidden">Loading...</span>
			</div>
			<div
				class="spinner-grow text-secondary"
				role="status">
				<span class="visually-hidden">Loading...</span>
			</div>
			<div
				class="spinner-grow text-success"
				role="status">
				<span class="visually-hidden">Loading...</span>
			</div>
			<div
				class="spinner-grow text-danger"
				role="status">
				<span class="visually-hidden">Loading...</span>
			</div>
			<div
				class="spinner-grow text-warning"
				role="status">
				<span class="visually-hidden">Loading...</span>
			</div>
			<div
				class="spinner-grow text-info"
				role="status">
				<span class="visually-hidden">Loading...</span>
			</div>
			<div
				class="spinner-grow text-light"
				role="status">
				<span class="visually-hidden">Loading...</span>
			</div>
			<div
				class="spinner-grow text-dark"
				role="status">
				<span class="visually-hidden">Loading...</span>
			</div>
			<div
				class="spinner-border"
				style="width: 3rem; height: 3rem"
				role="status">
				<span class="visually-hidden">Loading...</span>
			</div>
			<div
				class="spinner-grow"
				style="width: 3rem; height: 3rem"
				role="status">
				<span class="visually-hidden">Loading...</span>
			</div>
		</div>
		<div v-if="showSpinners">
			<button
				class="btn btn-primary"
				type="button"
				disabled>
				<span
					class="spinner-grow spinner-grow-sm"
					role="status"
					aria-hidden="true"></span>
				<span class="visually-hidden">Loading...</span>
			</button>
			<button
				class="btn btn-primary"
				type="button"
				disabled>
				<span
					class="spinner-grow spinner-grow-sm"
					role="status"
					aria-hidden="true"></span>
				Loading...
			</button>
			<button
				class="btn btn-primary"
				type="button"
				disabled>
				<span
					class="spinner-border spinner-border-sm"
					role="status"
					aria-hidden="true"></span>
				<span class="visually-hidden">Loading...</span>
			</button>
			<button
				class="btn btn-primary"
				type="button"
				disabled>
				<span
					class="spinner-border spinner-border-sm"
					role="status"
					aria-hidden="true"></span>
				Loading...
			</button>
		</div>
	</div>
</template>

<style scoped></style>
