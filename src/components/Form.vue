<script setup></script>

<template>
	<div
		id="form"
		class="form d-flex align-items-center justify-content-center">
		<div
			style="background-color: whitesmoke"
			class="border border-4 border-primary rounded p-5">
			<form>
				<div class="mb-3">
					<h1 class="mb-4">Login</h1>
					<label
						for="exampleInputEmail1"
						class="form-label"
						>Email address</label
					>
					<input
						type="email"
						class="form-control"
						id="exampleInputEmail1"
						aria-describedby="emailHelp" />
					<div
						id="emailHelp"
						class="form-text">
						We'll never share your email with anyone else.
					</div>
				</div>
				<div class="mb-3">
					<label
						for="exampleInputPassword1"
						class="form-label"
						>Password</label
					>
					<input
						type="password"
						class="form-control"
						id="exampleInputPassword1" />
				</div>
				<div class="mb-3 form-check">
					<input
						type="checkbox"
						class="form-check-input"
						id="exampleCheck1" />
					<label
						class="form-check-label"
						for="exampleCheck1"
						>Check me out</label
					>
				</div>
				<button
					type="submit"
					class="btn btn-secondary">
					Login
				</button>
			</form>
		</div>
	</div>
</template>

<style scoped>
#form {
	height: 800px;
	width: 100%;
}
</style>
