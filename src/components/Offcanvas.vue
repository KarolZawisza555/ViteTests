<script setup></script>

<template>
	<div
		id="offcanvas"
		class="form d-flex align-items-center justify-content-center">
		<div
			style="background-color: whitesmoke"
			class="border border-4 border-primary rounded p-5">
			<button
				class="btn btn-primary"
				type="button"
				data-bs-toggle="offcanvas"
				data-bs-target="#offcanvasExample"
				aria-controls="offcanvasExample">
				Show offcanvas left
			</button>
			<button
				class="btn btn-primary"
				type="button"
				data-bs-toggle="offcanvas"
				data-bs-target="#offcanvasTop"
				aria-controls="offcanvasTop">
				Toggle top offcanvas
			</button>

			<div
				class="offcanvas offcanvas-top"
				tabindex="-1"
				id="offcanvasTop"
				aria-labelledby="offcanvasTopLabel">
				<div class="offcanvas-header">
					<h5 id="offcanvasTopLabel">Show offcanvas top</h5>
					<button
						type="button"
						class="btn-close text-reset"
						data-bs-dismiss="offcanvas"
						aria-label="Close"></button>
				</div>
				<div class="offcanvas-body">
					Lorem ipsum dolor sit amet consectetur adipisicing elit. Et repellat
					maiores harum aperiam quibusdam consequatur repudiandae tempore saepe
					dignissimos, facilis perspiciatis, molestiae dolor ipsa sunt!
				</div>
			</div>

			<div
				class="offcanvas offcanvas-start"
				tabindex="-1"
				id="offcanvasExample"
				aria-labelledby="offcanvasExampleLabel">
				<div class="offcanvas-header">
					<h5
						class="offcanvas-title"
						id="offcanvasExampleLabel">
						Offcanvas
					</h5>
					<button
						type="button"
						class="btn-close text-reset"
						data-bs-dismiss="offcanvas"
						aria-label="Close"></button>
				</div>
				<div class="offcanvas-body">
					<div>
						Lorem ipsum dolor sit amet consectetur adipisicing elit. Et repellat
						maiores harum aperiam quibusdam consequatur repudiandae tempore
						saepe dignissimos, facilis perspiciatis, molestiae dolor ipsa sunt!
					</div>
				</div>
			</div>
		</div>
	</div>
</template>

<style scoped>
#offcanvas {
	height: 300px;
	width: 100%;
}
</style>
