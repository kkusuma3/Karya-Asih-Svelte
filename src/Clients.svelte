<script>
    const imgParallax = '/images/img-cleaning.jpg';
    const clients = [
        {
            title: 'Justus Usahamandiri',
            imageSrc: '/images/clients/justus.jpg',
            link: 'http://justus.co.id/',
            address: 'Wisma Justus - Jl. Danau Sunter Utara No.27-28, RT.10/RW.11, Sunter Jaya',
            since: '2013'
        },
        {
            title: 'Justus Kimia Raya',
            imageSrc: '/images/clients/justus-kimia.jpg',
            link: 'http://justus.co.id/',
            address: 'Wisma Justus - Jl. Danau Sunter Utara No.27-28, RT.10/RW.11, Sunter Jaya',
            since: '2018'
        },
        {
            title: 'Justus Sakti Raya',
            imageSrc: '/images/clients/justus-sakti.jpg',
            link: 'http://justus.co.id/',
            address: 'Wisma Justus - Jl. Danau Sunter Utara No.27-28, RT.10/RW.11, Sunter Jaya',
            since: '2018'
        },
        {
            title: 'Sunter Indah Permai',
            imageSrc: '/images/clients/bina.png',
            link: 'http://www.ptsip.co.id',
            address: 'GRHA SIP, Jl. Danau Indah Raya C2 No. 4',
            since: '2012'
        },
        {
            title: 'Astra Honda Motors',
            imageSrc: '/images/clients/astra.png',
            link: 'https://www.astra-honda.com/',
            address: 'Jl. Laksda Yos Sudarso – Sunter I Jakarta 14350, Indonesia',
            since: '1989'
        },
        {
            title: 'Tatamulia Nusantara Indah',
            imageSrc: '/images/clients/tata.jpg',
            link: 'https://www.tatamulia.co.id/',
            address: 'Sentul Workshop',
            since: '2016'
        },

    ]
</script>

<style>
    #clients {
        margin: 3em 0;
    }
    a:hover {
        text-decoration: none;
    }
    h3{
        font-size: 3em;
        color: black;
    }
    .card {
        width: 20vw;
        border-radius: 15px;
    }
    .card:hover{
        box-shadow: 0px 11px 51px 3px rgba(35,68,141,0.5);
    }
    .card-content p {
        color: #23448D;
        text-align: center;
    }
    .flexRow {
        display: flex;
        flex-wrap: wrap;
        flex-direction: row;
        justify-content: space-evenly;
        align-items: center;
        margin: 0 10vw;
    }
    .imgClient{
        max-height: 35vh;
        padding: 1em;
    }
</style>

<div id="clients">
    <div class="column">
        <h3 class="center">Dipercaya Oleh</h3>
        <div class="section flexRow">
            {#each clients as client}
                <a href={client.link} target="_blank">
                     <div class="card">
                        <div class="card-image waves-effect waves-block waves-light">
                            <img class="imgClient" src={client.imageSrc} alt="Company logo">
                        </div>
                        <div class="card-content">
                            <p>Since <strong>{client.since}</strong></p>
                        </div>
                    </div>
                </a>
            {/each }
        </div>
    </div>
</div>