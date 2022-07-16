<template>
	<section :style="bgImg" class="call-to-action bg-cover">
		<div class="container">
			<div class="row align-items-center">
				<div class="col-md-8">
					<div class="call-action-content">
						<h3 class="title">Are You Ready to Buy this theme!</h3>
						<p class="desc">Duis autem vel eum iriure dolor in hendrerit in vulputate velit esse molestie
							consequat</p>
					</div>
				</div>
				<div class="col-md-4">
					<div class="call-button">
						<a class="btn btn-round" href="#">Puchase Now</a>
					</div>
				</div>
			</div>
		</div>
	</section>
</template>

<script>
export default {
	name: 'CallToAction',
	data() {
		return {
			bgImg: {
				backgroundImage: `url(${require('../static/img/home-medical/puchase-bg.jpg')})`
			}
		}
	}
}
</script>

<style>

</style>
