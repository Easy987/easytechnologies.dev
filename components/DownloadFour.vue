<template>
	<section :style="bgImg" class="download-area-five bg-cover">
		<div class="container">
			<div class="row">
				<div class="col-lg-6">
					<div class="download-wrapper-five section-padding">
						<div class="section-title title-style-5 text-center">
							<h2 class="title">DOWNLOAD OUR LATEST APP</h2>
							<p class="paragraph-light">Claritas est etiam processus dynamicus, qui sequitur mutationem
								consuetudium lectorum.</p>
						</div>
						<div class="download-content-five">
							<p>Claritas est etiam processus dynamicus, qui sequitur mutationem consuetudium lectorum.
								Mirum est notare quam littera gothica, quam nunc putamus parum claram, anteposuerit
								litterarum formas .</p>
						</div>
						<div class="button-set text-center">
							<a class="btn btn-round" href="#"><i class="fa fa-apple"></i> Apple Store</a>
							<a class="btn btn-round" href="#"><i class="fa fa-android"></i> Google Play</a>
						</div>
					</div>
				</div>
				<div class="col-lg-6">
					<div class="app-thumb">
						<img alt="app thumb" src="../static/img/home-medical/app.png">
					</div>
				</div>
			</div>
		</div>
	</section>
</template>

<script>
export default {
	name: 'Download',
	data() {
		return {
			bgImg: {
				backgroundImage: `url(${require('../static/img/home-medical/download-bg.jpg')})`
			}
		}
	}
}
</script>

<style lang='scss'>
@import '../static/scss/variables.scss';
@import '../static/scss/components/download.scss';
</style>
