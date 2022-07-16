<template>
	<section id="review" :style="bgImg" class="testimonial-area testimonial-style-2 section-padding fix section">
		<div class="container">
			<div class="row">
				<div class="col-12">
					<carousel :items="1"
							  :nav="false"
							  :smartSpeed="1000"
							  class="testimonial-active owl-dot-style"
					>
						<!-- testimonial item start -->
						<div v-for="(client, clients) in clients" :key="clients"
							 class="testimonial-item testimonial-style2">
							<div class="testimonial-content">
								<p>{{ client.desc }}</p>
							</div>
							<div class="testimonial-thumb">
								<img :src="client.clientThumb" alt="client thumb">
							</div>
							<h6 class="client">{{ client.name }} - <span>{{ client.designation }}</span></h6>
						</div>
						<!-- testimonial item end -->
					</carousel>
				</div>
			</div>
		</div>
	</section>
</template>

<script>
export default {
	name: 'TestimonialTwo',
	data() {
		return {
			bgImg: {
				backgroundImage: `url(${require('../static/img/bg/clients2-bg.jpg')})`
			},
			clients: [
				{
					clientThumb: require("../static/img/testimonial/1.png"),
					name: "MOHAMET LUIS",
					designation: "Web Designer",
					desc: "Claritas est etiam processus dynamicus, qui sequitur mutationem consuetudium lectorum. Mirum est notare quam littera gothica, quam nunc putamus parum claram, anteposuerit litterarum formas humanitatis per seacula quarta decima et quinta decima."
				},
				{
					clientThumb: require("../static/img/testimonial/2.png"),
					name: "ERIN MAYA",
					designation: "Web Developer",
					desc: "Claritas est etiam processus dynamicus, qui sequitur mutationem consuetudium lectorum. Mirum est notare quam littera gothica, quam nunc putamus parum claram, anteposuerit litterarum formas humanitatis per seacula quarta decima et quinta decima."
				},
				{
					clientThumb: require("../static/img/testimonial/3.png"),
					name: "KUNJO PANDE",
					designation: "Marketer",
					desc: "Claritas est etiam processus dynamicus, qui sequitur mutationem consuetudium lectorum. Mirum est notare quam littera gothica, quam nunc putamus parum claram, anteposuerit litterarum formas humanitatis per seacula quarta decima et quinta decima."
				},
			]
		}
	}
}
</script>

<style lang='scss'>
@import '../static/scss/variables.scss';
@import '../static/scss/components/testimonial.scss';
</style>
