<template>
	<section id="department" :style="bgImg" class="department-area section-padding bg-cover section">
		<div class="container">
			<div class="row">
				<div class="col-lg-6">
					<div class="section-title title-style-5 section-title__left">
						<h2 class="title">DEPARTMENTS</h2>
						<p class="paragraph">Claritas est etiam processus dynamicus, qui sequitur mutationem
							consuetudium lectorum.</p>
					</div>
					<div class="department-faq">
						<b-card class="mb-1" no-body>
							<b-card-header header-tag="header">
								<b-button v-b-toggle.accordion-1 block href="#" variant="info"><span>0.1</span>
									Outpatient Surgery
								</b-button>
							</b-card-header>
							<b-collapse id="accordion-1" accordion="my-accordion" visible>
								<b-card-body>
									<img alt="doctor thumb" class="dep-thumb"
										 src="../static/img/home-medical/departments.jpg">
									<b-card-text>
										<h6><a href="#">Ut wisi enim ad minim veniam.</a></h6>
										<p>Nam liber tempor cum soluta nobis eleifend option congue nihil imperdiet
											doming id quod mazim placerat facer possim assum. </p>
										<a class="learn-more" href="#">Learn More</a>
									</b-card-text>
								</b-card-body>
							</b-collapse>
						</b-card>

						<b-card class="mb-1" no-body>
							<b-card-header header-tag="header">
								<b-button v-b-toggle.accordion-2 block href="#" variant="info"><span>0.2</span> Cardiac
									Clinic
								</b-button>
							</b-card-header>
							<b-collapse id="accordion-2" accordion="my-accordion">
								<b-card-body>
									<img alt="doctor thumb" class="dep-thumb"
										 src="../static/img/home-medical/departments.jpg">
									<b-card-text>
										<h6><a href="#">Ut wisi enim ad minim veniam.</a></h6>
										<p>Nam liber tempor cum soluta nobis eleifend option congue nihil imperdiet
											doming id quod mazim placerat facer possim assum. </p>
										<a class="learn-more" href="#">Learn More</a>
									</b-card-text>
								</b-card-body>
							</b-collapse>
						</b-card>

						<b-card class="mb-1" no-body>
							<b-card-header header-tag="header">
								<b-button v-b-toggle.accordion-3 block href="#" variant="info"><span>0.3</span>
									Ophthalmology Clinic
								</b-button>
							</b-card-header>
							<b-collapse id="accordion-3" accordion="my-accordion">
								<b-card-body>
									<img alt="doctor thumb" class="dep-thumb"
										 src="../static/img/home-medical/departments.jpg">
									<b-card-text>
										<h6><a href="#">Ut wisi enim ad minim veniam.</a></h6>
										<p>Nam liber tempor cum soluta nobis eleifend option congue nihil imperdiet
											doming id quod mazim placerat facer possim assum. </p>
										<a class="learn-more" href="#">Learn More</a>
									</b-card-text>
								</b-card-body>
							</b-collapse>
						</b-card>

						<b-card class="mb-1" no-body>
							<b-card-header header-tag="header">
								<b-button v-b-toggle.accordion-4 block href="#" variant="info"><span>0.4</span>
									Gynaecological Clinic
								</b-button>
							</b-card-header>
							<b-collapse id="accordion-4" accordion="my-accordion">
								<b-card-body>
									<img alt="doctor thumb" class="dep-thumb"
										 src="../static/img/home-medical/departments.jpg">
									<b-card-text>
										<h6><a href="#">Ut wisi enim ad minim veniam.</a></h6>
										<p>Nam liber tempor cum soluta nobis eleifend option congue nihil imperdiet
											doming id quod mazim placerat facer possim assum. </p>
										<a class="learn-more" href="#">Learn More</a>
									</b-card-text>
								</b-card-body>
							</b-collapse>
						</b-card>
					</div>
				</div>
			</div>
		</div>
	</section>
</template>

<script>
export default {
	name: 'Department',
	data() {
		return {
			bgImg: {
				backgroundImage: `url(${require('../static/img/home-medical/departments-bg.jpg')})`
			}
		}
	}
}
</script>
