<template>
	<section id="home" :style="bgImg" class="slider-section hero-style-2 hero-style-3 section">
		<div class="hero-slider-item">
			<div class="container">
				<div class="row align-items-center">
					<div class="col-lg-6 col-md-6 order-2 order-md-1">
						<div class="slider-content slider-content__style-3">
							<h2 class="slider-title">SOFTWARE DEVELOPMENT MADE EASY</h2>
							<p class="slider-desc">We make what you've dreamed of.</p>
						</div>
					</div>
					<div class="col-lg-6 col-md-6 order-1 order-md-2">
						<div class="slider-banner-thumb slide-animate">
							<img alt="slider thumb" src="../static/img/slider/home3-slide1.png">
						</div>
					</div>
				</div>
			</div>
		</div>
	</section>
</template>

<script>
export default {
	name: 'HeroBanner',
	data() {
		return {
			bgImg: {
				backgroundImage: `url(${require('../static/img/bg/home3-bg.jpg')})`
			}
		}
	}
}
</script>
