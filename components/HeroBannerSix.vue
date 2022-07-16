<template>
	<section id="home" :style="bgImg" class="slider-section hero-style-6">
		<div class="container">
			<div class="row">
				<div class="col-12">
					<carousel :autoplay="true"
							  :dots="false"
							  :items="1"
							  :nav="false"
							  :smartSpeed="1000"
							  class="hero-carousel"
					>
						<!-- single slider item -->
						<div class="hero-slider-item">
							<div class="row align-items-center">
								<div class="col-md-7">
									<div class="slider-content">
										<h3 class="slider-subtitle"><b>FROM $3.00</b> /per month</h3>
										<h2 class="slider-title">UNLIMITED WEB HOSTING</h2>
										<ul class="hero-pricing-list">
											<li>Unlimited Disk Space, Bandwidth</li>
											<li>FREE Search & Marketing Credits</li>
											<li>FREE Domain Registration</li>
											<li>FREE Security Suite</li>
										</ul>
										<div class="slider-btn">
											<a class="btn btn-round" href="#">LEARN MORE</a>
										</div>
									</div>
								</div>
								<div class="col-md-5">
									<div class="slider-thumb">
										<img alt="slider thumb" src="../static/img/hosting/slider/1.png">
									</div>
								</div>
							</div>
						</div>
						<!-- single slider end -->

						<!-- single slider item -->
						<div class="hero-slider-item">
							<div class="row align-items-center">
								<div class="col-md-7">
									<div class="slider-content">
										<h3 class="slider-subtitle"><b>FROM $3.00</b> /per month</h3>
										<h2 class="slider-title">UNLIMITED WEB HOSTING</h2>
										<ul class="hero-pricing-list">
											<li>Unlimited Disk Space, Bandwidth</li>
											<li>FREE Search & Marketing Credits</li>
											<li>FREE Domain Registration</li>
											<li>FREE Security Suite</li>
										</ul>
										<div class="slider-btn">
											<a class="btn btn-round" href="#">LEARN MORE</a>
										</div>
									</div>
								</div>
								<div class="col-md-5">
									<div class="slider-thumb">
										<img alt="slider thumb" src="../static/img/hosting/slider/2.png">
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
				backgroundImage: `url(${require('../static/img/hosting/slider/slide-bg.jpg')})`
			}
		}
	}
}
</script>
