<template>
	<section :style="bgImg" class="best-app-area section-padding2 pb-0 fix">
		<div class="container">
			<div class="row">
				<div class="col-xl-6 col-lg-6">
					<div class="bestapp-content-inner bestappThree">
						<div class="section-title title-style-2 shape">
							<h2 class="title text-white">best mobile app</h2>
							<p>Claritas est etiam processus dynamicus, qui sequitur mutationem consuetudium
								lectorum.</p>
						</div>
						<div class="bestapp-content-text">
							<p>Claritas est etiam processus dynamicus, qui sequitur mutationem consuetudium lectorum.
								Mirum est notare quam littera gothica, quam nunc putamus parum claram, anteposuerit
								litterarum formas humanitatis per seacula quarta decima et quinta decima.</p>
							<a class="read-more active" href="#"><i class="fa fa-apple"></i> Apple Store</a>
							<a class="read-more" href="#"><i class="fa fa-android"></i> Google Play</a>
						</div>
					</div>
				</div>
				<div class="col-xl-6 col-lg-6">
					<div class="bestapp-thumb">
						<img alt="bestapp thumb" src="../static/img/bestapp3.png">
					</div>
				</div>
			</div>
		</div>
	</section>
</template>

<script>
export default {
	name: 'Bestapp',
	data() {
		return {
			bgImg: {
				backgroundImage: `url(${require('../static/img/bg/bestapp3-bg.jpg')})`
			}
		}
	}
}
</script>

<style lang='scss'>
@import '../static/scss/variables.scss';
@import '../static/scss/components/best-app.scss';
</style>
