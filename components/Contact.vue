<template>
	<section id="support" :class="ContactStyle" :style="bgImg" class="contact-area section-padding pt-100 fix section">
		<div class="container">
			<div class="row">
				<div class="col-12">
					<div :class="['title-style-2 title-line-2', ContactStyle]" class="section-title text-center">
						<div class="title-icon"></div>
						<h2 class="title">SUPPORT CLIENTS</h2>
						<p class="paragraph">Claritas est etiam processus dynamicus, qui sequitur mutationem
							consuetudium lectorum.</p>
					</div>
				</div>
			</div>
			<div class="row support-container">
				<div class="col-md-8">
					<form action="#" class="support-form">
						<div class="input-box">
							<input class="text-field" name="name" placeholder="Your Name" type="text"/>
						</div>
						<div class="input-box">
							<input class="text-field" name="email" placeholder="Your Email" type="email"/>
						</div>
						<div class="input-box">
							<textarea class="text-field" name="message" placeholder="Your Message"></textarea>
						</div>
						<div class="input-box">
							<input class="btn-submit" type="submit" value="SEND"/>
						</div>
					</form>
				</div>
				<div class="col-md-4">
					<div class="support-info text-center">
						<div class="single-info">
							<div class="icon">
								<i class="fa fa-phone"></i>
							</div>
							<h6 class="support-title">telephones:</h6>
							<p>(+800) 123 456 789</p>
						</div>
						<div class="single-info">
							<div class="icon">
								<i class="fa fa-envelope-open-o "></i>
							</div>
							<h6 class="support-title">Address email:</h6>
							<p>demo@fantasic.com</p>
						</div>
					</div>
				</div>
			</div>
		</div>
	</section>
</template>

<script>
export default {
	name: 'Contact',
	props: ["ContactStyle"],
	data() {
		return {
			bgImg: {
				backgroundImage: `url(${require('../static/img/support-bg.jpg')})`
			}
		}
	}
}
</script>

<style lang='scss'>
@import '../static/scss/variables.scss';
@import '../static/scss/components/contact.scss';
</style>
