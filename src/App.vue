<script setup>
import { reactive } from "vue";
import Info from "./components/Info.vue";
import Home from "./components/Home.vue";
import Form from "./components/Form.vue";
import About from "./components/About.vue";
import MyNavbar from "./components/MyNavbar.vue";

const state = reactive({ elementsArray: ["home", "form", "about", "info"] });
</script>

<template>
	<div class="">
		<MyNavbar :elements="state.elementsArray" />
		<Home />
		<Form />
		<About />
		<Info />
		<!-- <MyButton color="secondary" /> -->
	</div>
</template>

<style scoped></style>
