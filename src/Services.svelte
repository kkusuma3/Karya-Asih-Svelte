<script>
    let imgCleaning = '/images/img-table.jpg';
    let imgPhoto = '/images/img-photocopy.jpg';
    const services = [
        {
            icon: 'format_paint',
            title: 'Cleaning Services',
            description: 'Jasa cleaning service spesialis langsung ke kantor anda.',
            content : [
                'Layanan Terpadu yang meliputi pembersihan lantai, langit-langit,dinding, toilet, hingga permbersihan karpet, marmer dan coating vynil.',
                'Layanan Pembersihan Kaca Gedung dan Gondola.',
                'Layanan Pertamanan berupa pemeliharaan, perawatan, dan kebersihan taman'
            ],
            image: imgCleaning
        },
        {
            icon: 'work',
            title: 'Business Support Services',
            description: 'Jasa bantuan menyediakan tenaga kerja tambahan untuk meningkatan produktifitas.',
            content : 'Untuk meningkatkan efisiensi dan efektifitas kinerja perusahaan anda, Karya Asih menawarkan Business Support Services dengan menyediakan tenaga terampil, terdidik, dan berintegritas tinggi untuk kebutuhan operator telpon, messenger, office boy / tea girls, mailroom, pantry services, locker services, factory helper, production helper, meeting room services, dan lain-lain.',
            image: imgPhoto
        }
    ]
</script>

<style>
    h5 {
        font-size: 2.1em;
    }
    h6 {
        font-size: 1.4em;
    }
    li, p {
        font-size: 1.1em;
    }
    .column {
        padding: 1em 0;
    }
    .bgGray {
        background-color: rgba(206, 206, 206, 0.5);
    }
    .flexColumn {
        display: flex;
        flex-direction: column;
        align-items: flex-start;
    }
    .fontPrimary {
        color: #23448D;
    }
    .cardService {
        width: 90%;
        padding: 1em;
    }
    .imageContainer {
        max-height: 70vh;
        border-radius: 30px;
    }
    .vl {
        padding: 0.5em 1em;
        margin: 1em 0;
        border-left: thick solid rgba(35,68,141,0.5);
        border-radius: 5px;
        font-size: 1.2em;
    }
    .vr {
        padding-right: 1em;
        margin: 1em 0;
        border-right: thick solid rgba(35,68,141,0.5);
        border-radius: 5px;
        font-size: 1.2em;
    }
</style>

<div id="services" class="column bgGray fontPrimary">
    <div class="row cardService">
        <div class="row">
            <div class="col s12 l6 push-l1 flexColumn">
                <h5><strong>{services[0].title}</strong></h5>
                <h6>{services[0].description}</h6>
                <ul>
                    {#each services[0].content as cont}
                    <li class="vl">{cont}</li>
                    {/each}
                </ul>
            </div>
            <img class="col s8 l3 push-l2 imageContainer" src={services[0].image} alt="something">
        </div>
    </div>
    <div class="row cardService">
        <div class="row">
            <img class="col s8 l3 push-l1 imageContainer" src={services[1].image} alt="something">
            <div class="col s12 l7 push-l2 flexColumn">
                <h5><strong>{services[1].title}</strong></h5>
                <h6>{services[1].description}</h6>
                <p class="vr">{services[1].content}</p>
            </div>
        </div>
    </div>
</div>