<script>
    import NavBar from './NavBar.svelte';
    import Services from './Services.svelte';
    import Clients from './Clients.svelte';
    import AboutUs from './AboutUs.svelte';
    import ContactUs from './ContactUs.svelte';
    import Footer from './Footer.svelte';
    const imgParallax = '/images/img-parallax.jpg';
    
</script>

<style>
    a {
        background-color: rgba(35, 68, 141, 1);
        color: white;
        border-radius: 15px;
    }
    a:hover {
        text-decoration: none;
	}
    h2 {
        animation: fadein 2s;
    }
    h4 {
        animation: fadein 4s;
    }
    @keyframes fadein {
        from { opacity: 0; }
        to   { opacity: 1; }
    }
    .container { 
        width: 100%;
        max-width: 100%;
    }
    .parallax-container{
        height: 95vh;
    }
</style>

<div id="home" class="container">
    <NavBar/>
    <div class="parallax-container center valign-wrapper">
            <div class="row">
            <div class="col s12 white-text">
                <h2 class="white-text teal-text lighten-2">Penyedia <strong>Layanan Kebersihan</strong> Terpadu</h2>
                <h4>Ahli Cleaning Services daerah Jakarta sejak 1989</h4>
                <a data-scroll class="waves-effect waves-light btn-large lighten-2" href="#contact">Daftar Sekarang</a>
            </div>
        </div>
        <div class="parallax"><img width='100%' src={imgParallax} alt="Cleaning"></div>
    </div>
    <Services/>
    <Clients/>
    <AboutUs/>
    <ContactUs/>
    <Footer/>
</div>