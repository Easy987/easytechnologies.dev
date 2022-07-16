<template>
	<section id="screenshot" :style="bgImg" class="screenshot-style-2 section-padding bg-cover section">
		<div class="container">
			<div class="row">
				<div class="col-12">
					<div class="section-title title-style-2">
						<h2 class="title">SCREENSHOTS</h2>
						<p class="paragraph">Claritas est etiam processus dynamicus, qui sequitur mutationem <br>consuetudium
							lectorum.</p>
					</div>
				</div>
			</div>
			<div class="row">
				<div class="col-12">
					<div class="screenshot-gallery text-center">
						<swiper :options="swiperOption">
							<swiper-slide>
								<div class="scr-thumb">
									<img alt="screenshot thumb" src="../static/img/screenshot/scr-1.jpg">
								</div>
							</swiper-slide>
							<swiper-slide>
								<div class="scr-thumb">
									<img alt="screenshot thumb" src="../static/img/screenshot/scr-2.jpg">
								</div>
							</swiper-slide>
							<swiper-slide>
								<div class="scr-thumb">
									<img alt="screenshot thumb" src="../static/img/screenshot/scr-3.jpg">
								</div>
							</swiper-slide>
							<swiper-slide>
								<div class="scr-thumb">
									<img alt="screenshot thumb" src="../static/img/screenshot/scr-2.jpg">
								</div>
							</swiper-slide>
							<swiper-slide>
								<div class="scr-thumb">
									<img alt="screenshot thumb" src="../static/img/screenshot/scr-3.jpg">
								</div>
							</swiper-slide>
							<!-- Optional controls -->
							<div slot="button-prev" class="swiper-button-prev"></div>
							<div slot="button-next" class="swiper-button-next"></div>
						</swiper>
					</div>
				</div>
			</div>
		</div>
	</section>
</template>

<script>

export default {
	name: 'ScreenshotTwo',
	data() {
		return {
			bgImg: {
				backgroundImage: `url(${require('../static/img/bg/screenshot-bg.jpg')})`
			},
			swiperOption: {
				speed: 600,
				loop: true,
				slidesPerView: 3,
				effect: 'coverflow',
				// grabCursor: true,
				centeredSlides: true,
				coverflowEffect: {
					rotate: -25,
					stretch: 0,
					depth: 100,
					modifier: 1,
					slideShadows: false,
				},
				navigation: {
					nextEl: '.swiper-button-next',
					prevEl: '.swiper-button-prev'
				},
				breakpoints: {
					768: {
						spaceBetween: 60
					},
					576: {
						slidesPerView: 2,
						spaceBetween: 20
					}
				}
			}
		}
	}
}

</script>
