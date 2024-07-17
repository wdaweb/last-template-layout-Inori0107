<template>
	<swiper
		:modules="modules"
		:slidesPerView="1"
		:spaceBetween="30"
		:loop="true"
		:autoplay="{ delay: 3000 }"
		:pagination="{
			clickable: true
		}"
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
		<swiper-slide><img src="../assets/event01.jpeg" /></swiper-slide>
		<swiper-slide><img src="../assets/event02.jpeg" /></swiper-slide>
		<swiper-slide><img src="../assets/event03.jpeg" /></swiper-slide>
		<swiper-slide><img src="../assets/event04.jpeg" /></swiper-slide>
		<swiper-slide><img src="../assets/event05.jpeg" /></swiper-slide>
		<swiper-slide><img src="../assets/event06.jpeg" /></swiper-slide>
		<swiper-slide><img src="../assets/event07.jpeg" /></swiper-slide>
	</swiper>
</template>
<script setup>
// Import Swiper Vue.js components
import { Swiper, SwiperSlide } from "swiper/vue";

// Import Swiper styles
import "swiper/css/bundle";
import "swiper/css/pagination";

// import required modules
import { Autoplay, Pagination } from "swiper/modules";

const modules = [Autoplay, Pagination];
</script>

<style scoped lang="scss">
.swiper {
	height: 380px;
	background: #fff;
	padding: 30px;
}

.swiper-slide img {
	width: 100%;
	height: 100%;
	object-fit: contain;
	transition: transform 0.3s;
}

:deep(.swiper-pagination-bullet) {
	border-radius: 2px;
	width: 30px;
	height: 5px;
	margin-right: 14px;
	background-color: darken($color: #f0f0f0, $amount: 30);

	&.swiper-pagination-bullet-active {
		background-color: #acd0d1;
	}
}
</style>
