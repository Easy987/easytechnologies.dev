<template>
	<section :class="downloadThree" :style="bgImg" class="download-area section-padding fix downloadTwo">
		<div class="container">
			<div class="row align-items-center">
				<div class="col-md-6">
					<div class="section-title title-style-2 shape pb-0">
						<h2 class="title text-white">GET IT NOW</h2>
						<p>Claritas est etiam processus dynamicus, qui sequitur mutationem consuetudium lectorum.</p>
					</div>
				</div>
				<div class="col-md-6">
					<div class="button-set button-set__style-2">
						<a class="read-more active" href="#"><i class="fa fa-apple"></i> Apple Store</a>
						<a class="read-more" href="#"><i class="fa fa-android"></i> Google Play</a>
					</div>
				</div>
			</div>
		</div>
	</section>
</template>

<script>
export default {
	name: 'DownloadTwo',
	props: ["downloadThree"],
	data() {
		return {
			bgImg: {
				backgroundImage: `url(${require('../static/img/bg/clients2-bg.jpg')})`
			}
		}
	}
}
</script>

<style lang='scss'>
@import '../static/scss/variables.scss';
@import '../static/scss/components/download.scss';
</style>
