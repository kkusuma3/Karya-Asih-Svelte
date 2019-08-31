<script>
    const logo = '/images/logo_transparent.png';
    const pillars = [
        {
            'title' : 'Fokus',
            'description' : 'Sejak berdiri, Karya Asih selalu mengutamakan bidang Cleaning Service dan Business Suport Services sehingga lebih berpengalaman dan spesialis.',
            'icon' : '/images/img-focus.jpg'
        },
        {
            'title' : 'Kompetitif',
            'description' : 'Karya Asih mampu bersaing secara kualitas dan harga untuk sumber daya manusia, sarana dan perlengkapan.',
            'icon' : '/images/img-competitive.jpg'
        },
        {
            'title' : 'Handal',
            'description' : 'Karya Asih didukung tenaga kerja yang terlatih dan professional sesuai standar yang diinginkan.',
            'icon' : '/images/img-handal.jpg'
        }
    ]
    const visiMisi = [
        {
            'title' : 'Visi',
            'description' : 'Memberikan layanan dengan sumber daya manusia yang terampil, berpengalaman, profesional, serta didukung fasilitas perlengkapan dengan kualitas terbaik.'
        },
        {
            'title' : 'Misi',
            'description' : 'Menjadi perusahaan yang fokus dan terdepan dalam memberikan layanan Cleaning Services dan Business Support Services dengan standardisasi optimum.'
        }
    ]
</script>

<style>
    .column { 
        background-color: rgba(206, 206, 206, 0.5);
        padding: 1vh 10vw;
    }
    .imageLogo {
        width: 30vw;
    }
    .cardPillar {
        display: flex;
        flex-direction: column;
    }
    .imgPillar {
        border-radius: 15px;
        max-width: calc(100% - 1em);
        height: 35vh;
    }
    .fontPillarTitle {
        font-size: 1.4em;
        font-weight: bold;
        margin-bottom: 0;
    }
    .fontPillarDesc {
        font-size: 1em;
    }
    .fontVMDesc{
        margin-left: 1em;
    }
    .vl {
        padding: 0.2em;
        margin: 0.4em 0;
        border-left: thick solid rgba(35,68,141,0.5);
        border-radius: 5px;
        transition: box-shadow 0.5s;
        box-shadow: 0px 11px 51px 3px white;
    }
</style>

<div id="about" class="column section">
    <h4>About Us</h4>
    <div class="row section">
        <div class="col s12 m6">
            <p> Sejak berdiri, Karya Asih telah membuktikan dirinya sebagai perusahaan yang berpengalaman di bidang Cleaning Services dan Busines Support Services untuk perkantoran, pabrik, dan pusat perbelanjaan. Berbagai apresiasi telah kami dapatkan dalam melayani beragam mitra kami, mulai dari perusahaan berskala nasional hingga perusahaan internasional.</p>
            <p>Bukan hanya pengalaman, Karya Asih dipilih menjadi mitra oleh berbagai perusahaan terkemuka karena memiliki sistem dan budaya perusahaan terbaik di bidangnya.</p>
        </div>
        <div class="col s12 m3 push-m2">
            <img src={logo} alt="Karya asih logo" class="imageLogo">
        </div>
    </div>
    <div class="row section">
        {#each pillars as pillar}
            <div class="col s12 l4 cardPillar">
                <img class="imgPillar" src={pillar.icon} alt="Pillar Karya Asih">
                <p class="fontPillarTitle">{pillar.title}</p>
                <p class="fontPillarDesc">{pillar.description}</p>
            </div>
        {/each }
    </div>
    <div class="row section">
        {#each visiMisi as vm}
            <div class="row">
                <div class="col s6 l2">
                    <h4>{vm.title}</h4>
                </div>
                <div class="col s12 l10">
                    <div class="vl">
                        <p class="fontVMDesc">{vm.description}</p>
                    </div>
                </div>
            </div>
        {/each }
    </div>
</div>