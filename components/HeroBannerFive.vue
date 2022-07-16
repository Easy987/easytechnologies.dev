<template>
	<section id="home" :style="bgImg" class="slider-section slider-style-5 section">
		<div class="container">
			<div class="row">
				<div class="col-12">
					<carousel :autoplay="true"
							  :dots="false"
							  :items="1"
							  :loop="true"
							  :nav="false"
							  :smartSpeed="1000"
							  class="hero-carousel"
					>
						<!-- single slider item -->
						<div v-for="(slider, sliders) in sliders" :key="sliders" class="hero-slider-item">
							<div class="row align-items-center">
								<div class="col-xl-7 col-lg-7 col-md-7">
									<div class="slider-content">
										<div class="slider-logo">
											<img :src="slider.logo" alt="slider logo">
										</div>
										<h6 class="slider-subtitle">{{ slider.subtitle }}</h6>
										<h2 class="slider-title">{{ slider.sliderTitle }}</h2>
										<p class="slider-desc">{{ slider.sliderDesc }}</p>
										<div class="slider-btn">
											<a class="btn btn-round" href="#">LEARN MORE</a>
										</div>
									</div>
								</div>
								<div class="col-xl-5 col-lg-5 col-md-5">
									<div class="slider-thumb">
										<img :src="slider.sliderThumb" alt="slider thumb">
									</div>
								</div>
							</div>
						</div>
						<!-- single slider end -->
					</carousel>
				</div>
			</div>
		</div>
	</section>
</template>

<script>
export default {
	name: 'HeroBannerFive',
	data() {
		return {
			bgImg: {
				backgroundImage: `url(${require('../static/img/home-medical/slider/1-bg.jpg')})`
			},
			sliders: [
				{
					sliderThumb: require("../static/img/home-medical/slider/1.png"),
					logo: require("../static/img/home-medical/slider/slider-logo.png"),
					subtitle: 'THE BEST HOSPITALITY VUE TEMPLATE FOREVER!',
					sliderTitle: 'FANTASIC HEALTH SYSTEM',
					sliderDesc: 'Nam liber tempor cum soluta nobis eleifend option congue nihil imperdiet doming id quod mazim placerat facer possim assum.'
				},
				{
					sliderThumb: require("../static/img/home-medical/slider/2.png"),
					logo: require("../static/img/home-medical/slider/slider-logo.png"),
					subtitle: 'THE BEST HOSPITALITY VUE TEMPLATE FOREVER!',
					sliderTitle: 'FANTASIC HEALTH SYSTEM',
					sliderDesc: 'Nam liber tempor cum soluta nobis eleifend option congue nihil imperdiet doming id quod mazim placerat facer possim assum.'
				},
			]
		}
	}
}
</script>
