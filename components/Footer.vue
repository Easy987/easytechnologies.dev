<template>
	<footer>
		<div :class="FooterStyle" class="footer-main dark-bg section-padding">
			<div class="container">
				<div class="row">
					<div class="col-12">
						<div class="footer-content text-center">
							<ul class="footer-social-link">
								<li v-for="(social, socials) in socials" :key="socials">
									<a :href="social.link" target="_blank">
										<i :class=social.icon></i>
									</a>
								</li>
							</ul>
							<h3 class="footer-title">THANKS FOR STOPPING BY OUR WEBSITE!</h3>
							<p>Claritas est etiam processus dynamicus, qui sequitur mutationem .</p>
						</div>
					</div>
				</div>
			</div>
		</div>
		<div :class="FooterStyle" class="footer-bottom black-bg">
			<div class="container">
				<div class="row">
					<div class="col-md-6 order-2 order-md-1">
					</div>
					<div class="col-md-6 order-1 order-md-2">
						<div class="useful-link">
							<a href="#">Our Team</a>
							<a href="#">Sight Map</a>
							<a href="#">Sign In</a>
						</div>
					</div>
				</div>
			</div>
		</div>
	</footer>
</template>

<script>
export default {
	name: 'Footer',
	props: ["FooterStyle"],
	data() {
		return {
			socials: [
				{
					icon: "fa fa-facebook",
					link: "https://www.facebook.com/"
				},
				{
					icon: "fa fa-twitter",
					link: "https://twitter.com/"
				},
				{
					icon: "fa fa-behance",
					link: "https://www.behance.net/"
				},
				{
					icon: "fa fa-dribbble",
					link: "https://dribbble.com/"
				}
			]
		}
	}
}
</script>

<style lang='scss'>
@import '../static/scss/variables.scss';
@import '../static/scss/components/footer.scss';
</style>
