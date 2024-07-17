<template>
	<section>
		<div id="view-more">
			<p>MOVIE</p>
			<p>VIEW MORE</p>
		</div>
		<swiper
			:modules="modules"
			:slidesPerView="1"
			:spaceBetween="50"
			:loop="true"
			:autoplay="{ delay: 3000 }"
			:breakpoints="{
				'940': {
					slidesPerView: 2,
					spaceBetween: 30
				},
				'1200': {
					slidesPerView: 3,
					spaceBetween: 30
				}
			}"
		>
			<swiper-slide v-for="(img, index) in imgsRef" :key="img.src" @click="openLightbox(index)" v-slot="data">
				<img :src="img" alt="Movie Image" @click="openLightbox(index)" />
			</swiper-slide>
		</swiper>
		<VueEasyLightbox :visible="visibleRef" :imgs="imgsRef" :index="indexRef" @hide="onHide" />
	</section>
</template>
<script setup>
// Import Swiper Vue.js components
import { Swiper, SwiperSlide } from "swiper/vue";
// Import Swiper styles
import "swiper/css/bundle";
// import required modules
import { Autoplay } from "swiper/modules";
const modules = [Autoplay];

import movie01 from "../assets/movie01.jpg";
import movie02 from "../assets/movie02.jpg";
import movie03 from "../assets/movie03.jpg";
import movie04 from "../assets/movie04.jpg";
import movie05 from "../assets/movie05.jpg";
const imgsRef = [movie01, movie02, movie03, movie04, movie05];

import VueEasyLightbox, { useEasyLightbox } from "vue-easy-lightbox";
import "vue-easy-lightbox/external-css/vue-easy-lightbox.css";
const { visibleRef, indexRef, show, onHide } = useEasyLightbox({
	imgs: imgsRef
});
const openLightbox = (index) => {
	indexRef.value = index;
	show();
};
</script>

<style scoped lang="scss">
section {
	padding-top: 70px;
	padding-bottom: 47vw;
	width: 100%;
	height: 650px;
	background: linear-gradient(180deg, transparent 80%, white 80%);
	backdrop-filter: blur(5px);
	overflow: hidden;
	#view-more {
		display: flex;
		flex-wrap: wrap;
		justify-content: space-between;
		align-items: flex-start;
		p {
			margin: 0 0 25px;
			padding: 0 5%;
			font-family: aktiv-grotesk, sans-serif;
			font-weight: 400;
			font-style: normal;
			color: #fff;
			font-size: 16px;
			letter-spacing: 0.3em;
		}
		p:nth-child(2) {
			font-size: 11px;
		}
	}
	.swiper {
		width: 125%;
		height: 450px;
		position: relative;
		top: 10%;
		left: 50%;
		transform: translateX(-50%);
	}

	.swiper-slide img {
		width: 100%;
		height: 100%;
		object-fit: contain;
	}
}
</style>
