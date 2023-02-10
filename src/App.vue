<script setup>
import { reactive } from "vue";
import Info from "./components/Info.vue";
import Home from "./components/Home.vue";
import Offcanvas from "./components/Offcanvas.vue";
import Form from "./components/Form.vue";
import SliderImages from "./components/SliderImages.vue";
import Spinners from "./components/Spinners.vue";
import MyNavbar from "./components/MyNavbar.vue";

const state = reactive({
  elementsNavBarArray: ["home", "form", "about", "info", "sliderimages"],
  sliderImagesArray: [
    { title: "title1", description: "description", image: "" },
    { title: "title2", description: "description", image: "" },
    { title: "title3", description: "description", image: "" },
    { title: "title4", description: "description", image: "" },
  ],
});
</script>

<template>
  <div class="">
    <MyNavbar :elements="state.elementsNavBarArray" />
    <Home />
    <Form />
    <SliderImages :sliderImagesArray="state.sliderImagesArray" />
    <Offcanvas />
    <Spinners />
    <!-- <Info /> -->
  </div>
</template>

<style scoped>

</style>
