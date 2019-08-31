<script>
    const imgCall = '/images/Call.svg';
    const imgEmail = '/images/Email.svg';
    const imgLocation = '/images/Location.svg';
    const contact = [
        {
            'title': 'Telepon Kami',
            'content': '(021) 452-8035',
            'img': imgCall,
            'icon': 'call',
            'link': 'tel:021-452-8035',
        },
        {
            'title': 'Email Kami',
            'content': 'hendra@karya-asih.com',
            'img': imgEmail,
            'icon': 'email',
            'link': 'mailto:hendra@karya-asih.com'
        },
        {
            'title': 'Kunjungi Kantor Kami',
            'content': 'Jl. Raya Kelapa Hibrida QK 1/17 Kelapa Gading, Jakarta 14240',
            'img': imgLocation,
            'icon': 'directions',
            'link': 'https://goo.gl/maps/tUdfvgMrdLsN3k4K6',
        }
    ]
</script>
<style>
    .column {
        padding: 1vh 10vw;
    }
    .imgContactUs{
        width: 15vw;
        border-radius: 15px;
    }
    .btn {
        background-color: rgba(35, 68, 141, 1);
        color: white;
        border-radius: 15px;
    }
    a {
        text-decoration: none;
    }
    .fontContent {
        font-size: 1.2em;
        height: 3em;
    }
</style>
<div id="contact" class="column section">
    <h3 class="center">Tunggu apalagi? Hubungi Kami!</h3>
    <div class="row">
        {#each contact as con}
        <div class="col s4 center flexColumn">
            <img class="imgContactUs" src={con.img} alt="Phone Call Image">
            <p class="fontContent">{con.content}</p>
            <a href={con.link} class="waves-effect waves-light btn" target="_blank">
                <i class="material-icons left">{con.icon}</i>
                {con.title}
            </a>
        </div>
        {/each}
    </div>
</div>