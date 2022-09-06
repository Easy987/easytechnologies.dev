<template>
	<section id="home" :style="bgImg" class="slider-section hero-style-2 hero-style-4 section">
		<div class="hero-slider-item">
			<div class="container">
				<div class="row align-items-center">
					<div class="col-md-7 order-2 order-md-1">
						<div class="slider-content slider-content__style-4">
							<h2 class="slider-title">SOFTWARE DEVELOPMENT MADE EASY</h2>
							<p class="slider-desc">An awesome Vue template for App landing and App Store site</p>
						</div>
					</div>
					<div class="col-md-5 order-1 order-md-2">
						<div class="slider-banner-thumb">
							<img alt="slider thumb" src="../static/img/slider/home4-slide1.png">
						</div>
					</div>
				</div>
			</div>
		</div>
	</section>
</template>

<script>
export default {
	name: 'HeroBannerFour',
	data() {
		return {
			bgImg: {
				backgroundImage: `url(${require('../static/img/bg/home4-bg.jpg')})`
			}
		}
	}
}
</script>
