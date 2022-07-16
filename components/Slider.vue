<template>
	<section id="home" :style="bgImg" class="slider-section hero-style-1 section">
		<div class="container">
			<div class="row">
				<div class="col-12">
					<no-ssr>
						<carousel :autoplay="true"
								  :items="1"
								  :loop="true"
								  :nav="false"
								  :smartSpeed="1000"
								  class="hero-carousel owl-dot-style owl-dot-style__2"
						>
							<!-- single slider item -->
							<div v-for="(slider, sliders) in sliders" :key="sliders" class="hero-slider-item">
								<div class="row align-items-center">
									<div class="col-xl-6 col-lg-5 col-md-5">
										<div class="slider-thumb">
											<img :src="slider.sliderThumb" alt="slider thumb">
										</div>
									</div>
									<div class="col-xl-6 col-lg-7 col-md-7">
										<div class="slider-content">
											<h2 class="slider-title">{{ slider.sliderTitle }}</h2>
											<p class="slider-desc">{{ slider.sliderDesc }}</p>
											<div class="slider-btn">
												<a class="read-more active" href="#"><i class="fa fa-apple"></i> Apple
													Store</a>
												<a class="read-more" href="#"><i class="fa fa-android"></i> Google Play</a>
											</div>
										</div>
									</div>
								</div>
							</div>
							<!-- single slider end -->
						</carousel>
					</no-ssr>
				</div>
			</div>
		</div>
	</section>
</template>

<script>
const carousel = () => typeof window !== 'undefined' ? import("vue-owl-carousel") : null;

export default {
	name: 'Slider',
	components: {
		carousel
	},
	data() {
		return {
			bgImg: {
				backgroundImage: `url(${require('../static/img/home-bg.jpg')})`
			},
			sliders: [
				{
					sliderThumb: require("../static/img/slider/1.png"),
					sliderTitle: 'AWESOME MOBILE APP',
					sliderDesc: 'An awesome Vue template for App landing and App Store site'
				},
				{
					sliderThumb: require("../static/img/slider/2.png"),
					sliderTitle: 'AWESOME MOBILE APP',
					sliderDesc: 'An awesome Vue template for App landing and App Store site'
				},
				{
					sliderThumb: require("../static/img/slider/3.png"),
					sliderTitle: 'AWESOME MOBILE APP',
					sliderDesc: 'An awesome Vue template for App landing and App Store site'
				},
			]
		}
	}
}
</script>
