<template>
	<header :class="{'sticky': scrolled}" class="header-main bg-ebony">
		<div class="container">
			<div class="row">
				<div class="col-12">
					<div class="menu-wrap">
						<div class="brand-logo">
							<router-link to="">
								<img alt="Brand Logo" src="../static/img/hosting/logo/logo.png">
							</router-link>
						</div>
						<div id="hamburger" @click="display_menu()">
							<span></span>
							<span></span>
							<span></span>
						</div>
						<ul class="main-menu">
							<li><a class="activee" href="#home" @click="close_menu()">Home</a></li>
							<li><a href="#about" @click="close_menu()">About</a></li>
							<li><a href="#service" @click="close_menu()">Service</a></li>
							<li><a href="#pricing" @click="close_menu()">Pricing</a></li>
							<li><a href="#review" @click="close_menu()">Testimonial</a></li>
							<li><a href="#chooseus" @click="close_menu()">Why Choose Us</a></li>
							<li><a href="#blog" @click="close_menu()">Blog</a></li>
						</ul>
					</div>
				</div>
			</div>
		</div>
	</header>
</template>

<script>
export default {
	name: 'Navbar',
	data() {
		return {
			load: false,
			limitPosition: 200,
			scrolled: false,
			lastPosition: 500
		}
	},
	methods: {
		// responsive menu script
		display_menu: function () {
			var body = document.getElementsByTagName("body")[0];
			(!body.classList.contains("display_menu")) ? body.classList.add("display_menu") : body.classList.remove("display_menu");
		},
		close_menu: function () {
			var body = document.getElementsByTagName("body")[0];
			body.classList.remove('display_menu');
		},
		loaded: function () {
			document.getElementsByTagName("body")[0].style.overflowY = "hidden";
			this.load = true;
		},

		// sticky menu script
		handleScroll() {
			if (this.lastPosition < window.scrollY && this.limitPosition < window.scrollY) {
				this.scrolled = true;
				// move up!
			}

			if (this.lastPosition > window.scrollY) {
				this.scrolled = true;
				// move down
			}

			this.lastPosition = window.scrollY;
			this.scrolled = window.scrollY > 50;
		}
	},
	created() {
		window.addEventListener("scroll", this.handleScroll);
	},
	destroyed() {
		window.removeEventListener("scroll", this.handleScroll);
	},

	mounted() {
		(function () {
			scrollTo();
		})();

		function scrollTo() {
			const links = document.querySelectorAll('.main-menu li a');
			links.forEach(each => (each.onclick = scrollAnchors));
		}

		function scrollAnchors(e, respond = null) {
			const distanceToTop = el => Math.floor(el.getBoundingClientRect().top);
			e.preventDefault();
			var targetID = (respond) ? respond.getAttribute('href') : this.getAttribute('href');
			const targetAnchor = document.querySelector(targetID);
			if (!targetAnchor) return;
			const originalTop = distanceToTop(targetAnchor);
			window.scrollBy({top: originalTop - 75, left: 0, behavior: 'smooth'});
			const checkIfDone = setInterval(function () {
				const atBottom = window.innerHeight + window.pageYOffset >= document.body.offsetHeight - 0;
				if (distanceToTop(targetAnchor) === 0 || atBottom) {
					targetAnchor.tabIndex = '-1';
					targetAnchor.focus();
					clearInterval(checkIfDone);
				}
			}, 800);
		}

		//scroll spy js
		window.addEventListener('load', function () {
			var section = document.querySelectorAll(".main-container > *");
			var sections = {};
			var i = 0;

			Array.prototype.forEach.call(section, function (e) {
				sections[e.id] = e.offsetTop - 85;
			});

			window.onscroll = function () {
				var scrollPosition = document.documentElement.scrollTop || document.body.scrollTop;

				for (i in sections) {
					if (sections[i] <= scrollPosition) {
						document.querySelector('.activee').setAttribute('class', ' ');
						document.querySelector('a[href*=' + i + ']').setAttribute('class', 'activee');
					}
				}
			};
		});
	}
}

</script>

<style lang='scss'>
@import '../static/scss/variables.scss';
@import '../static/scss/components/header.scss';
</style>
