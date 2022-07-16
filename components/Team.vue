<template>
	<section class="team-area pt-100 section-padding fix">
		<div class="container">
			<div class="row">
				<div class="col-12">
					<div class="section-title text-center">
						<div class="title-icon"></div>
						<h2 class="title">OUR TEAM</h2>
						<p class="paragraph">Claritas est etiam processus dynamicus, qui sequitur mutationem
							consuetudium lectorum.</p>
					</div>
				</div>
			</div>
		</div>

		<div :style="bgImg" class="team-member-inner">
			<div class="container">
				<div class="row">
					<div class="col-12">
						<div class="team-content text-center">
							<p>Claritas est etiam processus dynamicus, qui sequitur mutationem consuetudium lectorum.
								Mirum est notare quam littera gothica, quam nunc putamus parum claram, anteposuerit
								litterarum formas humanitatis per seacula quarta decima et quinta decima.</p>
						</div>
					</div>
				</div>
			</div>
		</div>

		<div class="team-member-slider">
			<div class="container">
				<div class="row">
					<div class="col-12">
						<no-ssr>
							<carousel :autoplay="true"
									  :dots="false"
									  :item="3"
									  :nav="false"
									  :responsive="{0:{items:1},576:{items:2},768:{items:3}}"
									  :smartSpeed="1000"
									  class="team-carousel"
							>
								<div v-for="(team, teams) in teams" :key="teams" class="team-member">
									<div class="member-thumb">
										<img :src="team.thumb" alt="team thumb">
										<div class="member-content">
											<h6 class="title">{{ team.title }}</h6>
											<p class="designation">{{ team.designation }}</p>
										</div>
									</div>
								</div>
							</carousel>
						</no-ssr>
					</div>
				</div>
			</div>
		</div>
	</section>
</template>

<script>
const carousel = () => typeof window !== 'undefined' ? import("vue-owl-carousel") : null;

export default {
	name: 'Team',
	components: {
		carousel
	},
	data() {
		return {
			teams: [
				{
					title: "Tony jack",
					designation: "Developer",
					thumb: require("../static/img/team/1.jpg")
				},
				{
					title: "Erik jack",
					designation: "Designer",
					thumb: require("../static/img/team/2.jpg")
				},
				{
					title: "Marlin jack",
					designation: "Marketer",
					thumb: require("../static/img/team/3.jpg")
				},
				{
					title: "Tom jack",
					designation: "SEO Specialist",
					thumb: require("../static/img/team/2.jpg")
				}
			],
			bgImg: {
				backgroundImage: `url(${require('../static/img/team-bg.jpg')})`
			}
		}
	}
}
</script>

<style lang="scss">
@import '../static/scss/variables.scss';
@import '../static/scss/components/team.scss';
</style>
