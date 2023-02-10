<script setup>
import { reactive } from "vue";
import Home from "./components/Home.vue";
import Offcanvas from "./components/Offcanvas.vue";
import Form from "./components/Form.vue";
import SliderImages from "./components/SliderImages.vue";
import Spinners from "./components/Spinners.vue";
import Accordin from "./components/Accordin.vue";
import MyNavbar from "./components/MyNavbar.vue";
import Alerts from "./components/Alerts.vue";
import Badges from "./components/Badges.vue";
import Collapse from "./components/Collapse.vue";
import Modal from "./components/Modal.vue";
import Progress from "./components/Progress.vue";

const state = reactive({
	elementsNavBarArray: [
		"home",
		"form",
		"sliderimages",
		"offcanvas",
		"spinners",
		"alerts",
	],
	sliderImagesArray: [
		{ title: "title1", description: "description", image: "" },
		{ title: "title2", description: "description", image: "" },
		{ title: "title3", description: "description", image: "" },
		{ title: "title4", description: "description", image: "" },
	],
});
</script>

<template>
	<div class="container-xxl">
		<MyNavbar :elements="state.elementsNavBarArray" />
		<Home />
		<Form />
		<SliderImages :sliderImagesArray="state.sliderImagesArray" />
		<Offcanvas />
		<Spinners />
		<Accordin />
		<Progress />
		<Alerts />
		<Badges />
		<Collapse />
		<Modal />
		<Toast />
	</div>
</template>

<style scoped></style>
