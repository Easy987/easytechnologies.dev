<template>
	<div :style="bgImg" class="puchase-area bg-cover">
		<div class="container">
			<div class="row align-items-center">
				<div class="col-md-8">
					<div class="puchase">
						<h3>Are You Ready to Buy this theme!</h3>
						<p>Duis autem vel eum iriure dolor in hendrerit in vulputate velit esse molestie consequat</p>
					</div>
				</div>
				<div class="col-md-4">
					<div class="puchase-button text-md-right">
						<a class="btn btn-round btn-2 btn-2--bg" href="#">Puchase Now</a>
					</div>
				</div>
			</div>
		</div>
	</div>
</template>

<script>
export default {
	data() {
		return {
			bgImg: {
				backgroundImage: `url(${require('../static/img/hosting/puchase-bg.jpg')})`
			},
		}
	}
};
</script>

<style lang="scss" scoped>
@import '../static/scss/variables.scss';

.puchase-area {
	padding: 80px 0;
	// responsive
	@media #{$xs-device}{
		padding: 62px 0;
	}
}

.puchase {
	@media #{$sm-device}{
		margin-bottom: 20px;
	}

	h3 {
		color: #fff;
		font-size: 24px;
		font-weight: 700;
		margin-bottom: 20px;
	}

	p {
		color: #fff;
		font-style: italic;
	}
}
</style>
