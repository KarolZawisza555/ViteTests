<script setup>
defineProps({
	color: {
		type: String,
		default: "primary",
	},
	elements: {
		type: Array,
		default: [],
	},
});
</script>

<template>
	<nav class="navbar navbar-expand-lg navbar-light bg-light">
		<div class="container-fluid">
			<a class="navbar-brand" href="#">Bootstrap5 Vue3</a>
			<button class="navbar-toggler" type="button" data-bs-toggle="collapse"
				data-bs-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false"
				aria-label="Toggle navigation">
				<span class="navbar-toggler-icon"></span>
			</button>
			<div class="collapse navbar-collapse" id="navbarSupportedContent">
				<ul class="navbar-nav me-auto mb-2 mb-lg-0">
					<li class="nav-item dropdown">
						<a class="nav-link dropdown-toggle" href="#" id="navbarDropdown" role="button"
							data-bs-toggle="dropdown" aria-expanded="false">
							Go to
						</a>
						<ul class="dropdown-menu" aria-labelledby="navbarDropdown">
							<li v-for="item in elements" :key="item.index">
								<a class="dropdown-item" :href="`#${item}`">{{ item }}</a>
							</li>
						</ul>
					</li>
				</ul>
			</div>
		</div>
	</nav>
</template>

<style scoped>

</style>
