<template>
	<section :style="bgImg" class="video-section section-padding pt-100 fix">
		<div class="container">
			<div class="row align-items-center">
				<div class="col-lg-6 order-2 order-lg-1">
					<div class="video-player">
						<figure class="embed-responsive embed-responsive-16by9">
							<iframe :src="video" allow="autoplay; encrypted-media" allowfullscreen></iframe>
						</figure>
					</div>
				</div>
				<div class="col-lg-6 order-1 order-lg-2">
					<div class="bestapp-content-inner text-center">
						<div class="section-title text-center">
							<div class="title-icon"></div>
							<h2 class="title text-white">EMBED VIDEO SUPPORT LEFT, RIGHT OR FULL WIDTH</h2>
							<p>Claritas est etiam processus dynamicus, qui sequitur mutationem consuetudium
								lectorum.</p>
						</div>
						<div class="bestapp-content-text pb-0">
							<p>Claritas est etiam processus dynamicus, qui sequitur mutationem consuetudium lectorum.
								Mirum est notare quam littera gothica, quam nunc putamus parum claram, anteposuerit
								litterarum formas humanitatis per seacula quarta decima et quinta decima.</p>
							<ul class="video-list">
								<li><i class="fa fa-check-square-o"></i> Perfect layout</li>
								<li><i class="fa fa-check-square-o"></i> Sweet moves</li>
							</ul>
						</div>
					</div>
				</div>
			</div>
		</div>
	</section>
</template>

<script>
export default {
	name: 'Video',
	data() {
		return {
			video: "https://www.youtube.com/embed/iaj8ktgL3BY",
			bgImg: {
				backgroundImage: `url(${require('../static/img/video-bg.jpg')})`
			}
		}
	}
}
</script>

<style lang='scss'>
@import '../static/scss/variables.scss';
@import '../static/scss/components/video.scss';
</style>
