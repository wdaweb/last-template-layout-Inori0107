<template>
	<section>
		<div id="news" data-aos="fade-up" data-aos-duration="2000">
			<h1>NEWS</h1>
			<p>VIEW MORE</p>
		</div>
		<div id="ad" data-aos="fade-up" data-aos-duration="2000">
			<ul>
				<li>
					<a href="https://yorushika.com/news/detail/11611?lang=zh-tw">
						<p class="date">2024.06.20 <span class="artists">suis</span></p>
						<p class="title">新潮文庫“文鳥・夢十夜/夏目漱石”的限定封面發售決定</p>
					</a>
				</li>
				<li>
					<a href="https://yorushika.com/news/detail/11610?lang=zh-tw">
						<p class="date">2024.06.14 <span class="artists">suis</span></p>
						<p class="title">suis的個人訪談刊登在《ROCKIN'ON JAPAN》8月號上</p>
					</a>
				</li>
				<li>
					<a href="https://yorushika.com/news/detail/11609?lang=zh-tw">
						<p class="date">2024.06.12 <span class="artists">YORUSHIKA</span></p>
						<p class="title">suis將作為嘉賓出演J-WAVE的《TOKIO HOT 100》</p>
					</a>
				</li>
			</ul>
		</div>
	</section>
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
section {
	width: 100%;
	display: flex;
	flex-direction: column;
	align-items: center;
	height: 500px;
	background: #fff;
	padding: 20px 0 60px 0;
	font-family: sans-serif;
	#news {
		display: flex;
		justify-content: space-between;
		width: 100%;
		height: 50px;
		padding: 0 40px 0 40px;
		letter-spacing: 0.3rem;
		h1 {
			margin: 0 0 25px;
			padding: 0 20px;
			font-weight: 400;
			color: #222;
			font-size: 16px;
		}
		p {
			margin: 0 0 25px;
			padding-right: 20px;
			font-size: 12px;
		}
	}
	#ad {
		width: 100%;
		height: 360px;
		padding-right: 40px;
		li {
			list-style-type: none;
			border-top: 1px solid #eaeaea;
			&:last-child {
				border-bottom: 1px solid #eaeaea;
			}
			a {
				padding: 15px 20px;
				cursor: pointer;
				display: flex;
				flex-direction: column;
				width: 100%;
				height: 120px;
				text-decoration: none;
				color: #000;
				.date {
					font-size: 13px;
					color: #222;
					letter-spacing: 0.2rem;
					span {
						font-size: 10px;
						color: #fff;
						background: #acd0d1;
						padding: 3px 6px 3px 8px;
						margin-left: 10px;
					}
				}
			}
		}
	}
	@include lg {
		flex-direction: row;
		padding-right: 10%;
		#news {
			text-align: center;
			display: block;
			width: 30%;
			height: 300px;
			padding-top: 40px;
			padding-left: 10%;
			h1 {
				font-size: 22px;
				padding-left: 0;
			}
		}
		#ad {
			width: 70%;
			height: 360px;
			a {
				flex-direction: row !important;
				.date {
					width: 30%;
					line-height: 5;
					margin-top: 6px;
				}
				.title {
					line-height: 5;
					width: 70%;
					margin: 0;
				}
			}
		}
	}
}
</style>
