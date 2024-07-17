<template>
	<header data-aos="fade-down" data-aos-duration="1500">
		<a href="#"><img src="../assets/xs_logo.jpg" /></a>
		<div id="phone">
			<span
				>ME <br />
				NU</span
			>
		</div>
	</header>
	<div id="pc">
		<span
			>ME <br />
			NU</span
		>
		<img src="../assets/logo.png" data-aos="fade-right" data-aos-duration="2000" />
	</div>
</template>

<script setup>
import AOS from "aos";
import "aos/dist/aos.css";

AOS.init({
	once: true
});
</script>

<style scoped lang="scss">
@import "../style/main.scss";

header {
	position: relative;
	z-index: 1000;
	background: #fff;
	width: 100%;
	height: 60px;
	img {
		margin-left: 45px;
	}
	#phone {
		background: #acd0d1;
		position: absolute;
		top: 0;
		right: 0;
		width: 60px;
		height: 60px;
		span {
			display: block;
			padding: 11px 0px 8px 18px;
			color: #fff;
			letter-spacing: 0.6rem;
			font-size: 12px;
			line-height: 1.5;
		}
	}
	@include lg {
		display: none;
	}
}
#pc {
	display: none;
	@include lg {
		z-index: 1000;
		display: block;
		background: #acd0d1;
		position: fixed;
		top: 0;
		left: 0;
		width: 60px;
		height: 100vh;
		span {
			display: block;
			height: 60px;
			padding: 11px 0px 8px 16px;
			color: #fff;
			letter-spacing: 0.6rem;
			font-size: 12px;
			line-height: 1.5;
			border-bottom: 1px solid #fff;
		}
		img {
			width: 150px;
			height: 150px;
			position: absolute;
			top: 0px;
			left: 60px;
		}
	}
}
</style>
