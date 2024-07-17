<template>
	<!-- component <sidebar> -->
	<sectionSideMenu></sectionSideMenu>
	<section id="bg_pic">
		<img :src="bg_picture" />
	</section>
	<!-- component <Carousel> -->
	<sectionCarousel></sectionCarousel>
	<!-- component <News> -->
	<sectionNews></sectionNews>
	<!-- component <Movie> -->
	<sectionMovie></sectionMovie>
	<!-- component <Footer> -->
	<sectionFooter></sectionFooter>
	<ScrollTop />
</template>

<script setup>
import sectionSideMenu from "./components/sectionSideMenu.vue";
import sectionCarousel from "./components/sectionCarousel.vue";
import sectionNews from "./components/sectionNews.vue";
import sectionFooter from "./components/sectionFooter.vue";
import sectionMovie from "./components/sectionMovie.vue";
import bg_picture from "./assets/bg_picture.jpeg";
import "./style/main.scss";
import AOS from "aos";
import "aos/dist/aos.css";
AOS.init({
	once: true
});
</script>

<style scoped lang="scss">
:deep(.p-scrolltop-icon) {
	color: aqua;
}
</style>
