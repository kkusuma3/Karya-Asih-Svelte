<script>
	let imgLogo = '/images/logo.png'
	import '../node_modules/materialize-css/dist/css/materialize.min.css';
	import '../node_modules/materialize-css/dist/js/materialize.min.js';

</script>

<style>
	a:hover {
		text-decoration: none;
	}
	nav {
		background-color: white;
	}
	@media (max-width: 600px) {
        .imgLogo {
			width: 50vw;
			padding: 0.2em 0;
		}
    }
	.imgLogo {
		max-width: 15vw;
	}
	.homeTab, .homeTabContact {
		color: rgba(35, 68, 141, 1);
		font-size: 1.2rem;
		border-bottom: 2px solid transparent;
	}
	.homeTab:hover {
		border-bottom: 3px solid #23448D;
	}
	.tabContact {
		background-color: white;
	}
	.btn-floating {
		margin: 0 10px;
	}
</style>

<div class="navbar-fixed">
	<nav>
		<div class="row">
			<a data-scroll href="#home" class="brand-logo center col s12 l3 offset-s2 push-l1"><img class="imgLogo" src={imgLogo} alt = 'logo'></a>
			<ul class="right hide-on-med-and-down col s7 offset-s1">
				<li class="col s3">
					<a data-scroll href="#services" class="center homeTab">Services</a>
				</li>
				<li class="col s3">
					<a data-scroll href="#clients" class="center homeTab">Our Clients</a>
				</li>
				<li class="col s3">
					<a data-scroll href="#about" class="center homeTab">About Us</a>
				</li>
				<li class="col s3 tabContact">
					<div class="center">
						<a data-scroll href="#contact" class="pulse btn-floating">
							<i class="small material-icons iconContact">call</i>
						</a>
						<span class="homeTabContact">Contact Us</span>
					</div>
				</li>
			</ul>
		</div>
	</nav>
</div>
