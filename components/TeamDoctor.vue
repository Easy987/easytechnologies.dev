<template>
	<section id="team" class="team-area section-padding fix section">
		<div class="container">
			<div class="row">
				<div class="col-12">
					<div class="section-title title-style-5 text-center">
						<h2 class="title">OUR GIFTED DOCTORS</h2>
						<p class="paragraph">Claritas est etiam processus dynamicus, qui sequitur mutationem
							consuetudium lectorum.</p>
					</div>
				</div>
			</div>
			<div class="row">
				<div class="col-12">
					<carousel :autoplay="true"
							  :dots="false"
							  :item="3"
							  :loop="true"
							  :margin="30"
							  :nav="false"
							  :responsive="{0:{items:1},576:{items:2},768:{items:3}}"
							  :smartSpeed="300"
							  class="doctor-team-carousel"
					>
						<div v-for="(doctor, doctors) in doctors" :key="doctors" class="doctor-member">
							<div class="doctor-thumb">
								<img :src="doctor.thumb" alt="doctor thumb">
								<div class="doctor-content">
									<h6 class="title">{{ doctor.title }}</h6>
									<p class="designation">{{ doctor.designation }}</p>
								</div>
							</div>
						</div>
					</carousel>
				</div>
			</div>
		</div>
	</section>
</template>

<script>
export default {
	name: 'TeamDoctor',
	data() {
		return {
			doctors: [
				{
					title: "ERICK MARTEN",
					designation: "Deltal Specialist",
					thumb: require("../static/img/home-medical/team/1.jpg")
				},
				{
					title: "MARLIN JACK",
					designation: "Deltal Specialist",
					thumb: require("../static/img/home-medical/team/2.jpg")
				},
				{
					title: "JHONSON DOE",
					designation: "Deltal Specialist",
					thumb: require("../static/img/home-medical/team/3.jpg")
				},
				{
					title: "TOM DOE",
					designation: "Deltal Specialist",
					thumb: require("../static/img/home-medical/team/2.jpg")
				}
			]
		}
	}
}
</script>

<style lang="scss">
@import '../static/scss/variables.scss';
@import '../static/scss/components/team.scss';
</style>
