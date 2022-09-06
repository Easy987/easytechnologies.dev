<template>
	<div class="main-container">
		<!-- Navbar section -->
		<Navbar NavbarStyle2="header-style-3"/>

		<!-- slider section -->
		<HeroBannerThree/>

		<!-- about section -->
		<About/>

		<!-- best app section -->
		<Bestapp/>

		<!-- features section -->
		<Features/>

		<!-- testimonial section -->
		<Testimonial/>

		<!-- screenshot area -->
		<Screenshot/>

		<!-- video section -->
		<Video/>

		<!-- team section -->
		<Team/>

		<!-- download section -->
		<Download/>

		<!-- contact section -->
		<Contact/>

		<!-- footer section -->
		<Footer/>

	</div>
</template>

<script>
import Navbar from '../components/Navbar'
import HeroBannerThree from '../components/HeroBannerThree'
import About from '../components/About'
import Bestapp from '../components/Bestapp'
import Features from '../components/Features'
import Testimonial from '../components/Testimonial'
import Screenshot from '../components/Screenshot'
import Video from '../components/Video'
import Team from '../components/Team'
import Download from '../components/Download'
import Contact from '../components/Contact'
import Footer from '../components/Footer'

export default {
	name: 'app',
	components: {
		Navbar,
		HeroBannerThree,
		About,
		Bestapp,
		Features,
		Testimonial,
		Screenshot,
		Video,
		Team,
		Download,
		Contact,
		Footer
	}
}
</script>
<style>
@import '../static/css/font-awesome.min.css';
@import '../static/css/pe-icon-7-stroke.css';
</style>

<style lang="scss">
@import "../static/scss/_variables.scss";
@import "../static/scss/_mixins.scss";
@import "../static/scss/_typography.scss";
@import "../static/scss/_spacing.scss";
@import "../static/scss/_common.scss";
@import "../static/scss/_components.scss";
</style>

