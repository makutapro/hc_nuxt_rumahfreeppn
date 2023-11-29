<template>
    <section id="residential" class="container-fluid px-2 px-md-3 py-5">
        <div class="container text-center">
            <h2 class="mb-0">AVAILABLE UNIT</h2>

            <div class="row d-flex justify-content-center">
                <div class="col-12 col-md-10">
                    <div class="row g-0 bg-white bg-card position-relative my-5">
                <div class="col-md-6 mb-md-0">
                    <div id="carousel-harumi" class="carousel slide">
                        <div class="carousel-inner">
                            <div class="carousel-item active">
                                <img src="~/assets/images/residential/harumi.png" class="img-fluid w-100 img-card h-100 object-fit-cover cursor-pointer" @click="() => showImg(0)">
                            </div>
                            <div class="carousel-item">
                                <img src="~/assets/images/residential/harumi.png" class="img-card cursor-pointer" @click="() => showImg(0)">
                            </div>
                        </div>
                        <button class="carousel-control-prev" type="button" data-bs-target="#carousel-harumi" data-bs-slide="prev">
                            <span class="carousel-control-prev-icon" aria-hidden="true"></span>
                            <span class="visually-hidden">Previous</span>
                        </button>
                        <button class="carousel-control-next" type="button" data-bs-target="#carousel-harumi" data-bs-slide="next">
                            <span class="carousel-control-next-icon" aria-hidden="true"></span>
                            <span class="visually-hidden">Next</span>
                        </button>
                    </div>
                  <!-- <img src="~/assets/images/residential/standar.png" class="img-fluid w-100 img-card h-100 object-fit-cover"> -->
                </div>
                <div class="col-md-6 p-4 p-md-5 text-center">
                    <h1 class="mt-0 p-2 p-md-4 display-6 fw-bold text-center mb-0"><span class="fs-3 fw-normal">Tipe</span> Harumi</h1>
                    <div class="mb-5">
                        <!-- <div class="d-flex justify-content-between align-items-center">
                            <p class="fs-3 fw-light">Land Area</p>
                            <p class="fs-3 fw-bold">66 <sup class="fw-light">m2</sup></p>
                        </div>
                        <div class="d-flex justify-content-between align-items-center">
                            <p class="fs-3 fw-light">Floor Area</p>
                            <p class="fs-3 fw-bold">30 <sup class="fw-light">m2</sup></p>
                        </div> -->
                        <div class="row">
                            <div class="col-12">
                                <p class="fs-3 fw-light mb-0">LT / LB</p>
                                <p class="fs-2 fw-semibold mb-0">32 <sup class="fw-semibold">m2</sup> / 60 <sup class="fw-semibold">m2</sup></p>
                            </div>
                        </div>
                    </div>
                    <img src="~/assets/images/residential/feature.png" class="img-fluid">
                </div>
            </div>
            
            <div class="row g-0 bg-white bg-card position-relative my-5">
                <div class="col-md-6 mb-md-0">
                    <div id="carousel-megame" class="carousel slide">
                        <div class="carousel-inner">
                            <div class="carousel-item active">
                                <img src="~/assets/images/residential/megame.png" class="img-fluid w-100 img-card h-100 object-fit-cover cursor-pointer" @click="() => showImg(1)">
                            </div>
                            <div class="carousel-item">
                                <img src="~/assets/images/residential/megame.png" class="img-fluid w-100 img-card h-100 object-fit-cover cursor-pointer" @click="() => showImg(1)">
                            </div>
                        </div>
                        <button class="carousel-control-prev" type="button" data-bs-target="#carousel-megame" data-bs-slide="prev">
                            <span class="carousel-control-prev-icon" aria-hidden="true"></span>
                            <span class="visually-hidden">Previous</span>
                        </button>
                        <button class="carousel-control-next" type="button" data-bs-target="#carousel-megame" data-bs-slide="next">
                            <span class="carousel-control-next-icon" aria-hidden="true"></span>
                            <span class="visually-hidden">Next</span>
                        </button>
                    </div>
                </div>
                <div class="col-md-6 p-4 p p-md-5 text-center">
                    <h1 class="mt-0 p-2 p-md-4 display-6 fw-bold text-center"> <span class="fs-3 fw-normal">Tipe</span> Megame</h1>
                    <div class="mb-5">
                        <!-- <div class="d-flex justify-content-between align-items-center">
                            <p class="fs-3 fw-light">Land Area</p>
                            <p class="fs-3 fw-bold">60 <sup class="fw-light">m2</sup></p>
                        </div>
                        <div class="d-flex justify-content-between align-items-center">
                            <p class="fs-3 fw-light">Floor Area</p>
                            <p class="fs-3 fw-bold">23 <sup class="fw-light">m2</sup></p>
                        </div> -->
                        <div class="row">
                            <div class="col-12">
                                <p class="fs-3 fw-light mb-0">LT / LB</p>
                                <p class="fs-2 fw-semibold mb-0">37 <sup class="fw-semibold">m2</sup> / 72 <sup class="fw-semibold">m2</sup></p>
                            </div>
                        </div>
                    </div>
                    <img src="~/assets/images/residential/feature.png" class="img-fluid">
                </div>
            </div>
                </div>
            </div>

         
            
            <!-- <div class="row d-flex justify-content-center">
                <div class="col-12 col-md-4 col-lg-4 mt-5">
                        <div class="card">
                            <img src="~/assets/images/residential/cluster-1.webp" class="card-img-top img-fluid" alt="">
                            <small class="mt-3 mb-1"><span class="cluster px-3 py-1">Cluster</span></small>
                            <h4 class="card-title py-1 mb-0 fw-bold"><span class="title">Neo Salvia</span></h4>
                            <div class="card-body">
                                <small><span class="startprice">CICILAN MULAI</span></small>
                                <h2 class="mb-0 price card-text fw-bold">Rp. 4 Jt-an</h2>
                            </div>
                        </div>
                </div>
                <div class="col-12 col-md-4 col-lg-4 mt-5">
                    <div class="card">
                            <img src="~/assets/images/residential/cluster-2.webp" class="card-img-top img-fluid" alt="">
                            <small class="mt-3 mb-1"><span class="cluster px-3 py-1">Cluster</span></small>
                            <h4 class="card-title py-1 mb-0 fw-bold"><span class="title">Sakura Indica</span></h4>
                            <div class="card-body">
                                <small><span class="startprice">CICILAN MULAI</span></small>
                                <h2 class="mb-0 price card-text fw-bold">Rp. 2 Jt-an</h2>
                            </div>
                        </div>
                </div>
                <div class="col-12 col-md-4 col-lg-4 mt-5">
                    <div class="card">
                            <img src="~/assets/images/residential/cluster-3.png" class="card-img-top img-fluid" alt="">
                            <small class="mt-3 mb-1"><span class="cluster px-3 py-1">Cluster</span></small>
                            <h4 class="card-title py-1 mb-0 fw-bold"><span class="title">Ridge Crystal</span></h4>
                            <div class="card-body">
                                <small><span class="startprice">CICILAN MULAI</span></small>
                                <h2 class="mb-0 price card-text fw-bold">Rp. 4 Jt-an</h2>
                            </div>
                        </div>
                </div>
            </div> -->
        </div>
        <no-ssr>
            <vue-easy-lightbox :visible="visible" :imgs="images[img]" :index="index" @hide="onHide" rotateDisabled="true"></vue-easy-lightbox>
        </no-ssr>
    </section>
</template>

<script>
import VueEasyLightbox from 'vue-easy-lightbox'

export default{
    components: {
        VueEasyLightbox
    },
    data(){
        return{
            clusHome:[],
            firstHome:[],
            images: [
                [
                    require('~/assets/images/residential/harumi.png'),
                    require('~/assets/images/residential/harumi.png'),
                ],
                [
                    require('~/assets/images/residential/megame.png'),
                    require('~/assets/images/residential/megame.png'),
                ],
            ],
            img: 0,
            index: 0,
            visible: false,
        }
    },
    created(){
     this.$axios.get('https://admharvest.harvestcity.co.id/api/homecluster')
      .then((response) => {
        this.clusHome = response.data.data
       }),
       this.$axios.get('https://admharvest.harvestcity.co.id/api/firstcluster')
      .then((response) => {
        this.firstHome = response.data.data
       })
    },
    mounted(){
        window.scrollTo(0, 0)
    },
    methods: {
        showImg(img, index) {
            this.img = img;
            this.index = index;
            this.visible = true;
        },
        onHide() {
            this.visible = false;
        },
    },
}

</script>

<style scoped>
#residential {
    background-color: #4A324B;
}

#residential h1 {
    font-family: TenorSansRegular;
}

#residential h2 {
    letter-spacing: 0.18em;
    color: #FFB800;
}

#residential h4 {
    /* background-color: #BB9430; */
    font-family: BodoniModaSemiBold;
    color: #eaeaea; 
}

#residential h5 {
    color: #5C1B73;
}

.carousel, .carousel-inner, .carousel-item {
    height: 100%;
}

.carousel-inner {
    border-top-left-radius: 80px;
}

.carousel-control-next-icon {
    background-image: url(../assets/images/residential/arrow-right.png);
    background-size: cover;
    width: 28px;
    height: 29px;
}

.carousel-control-prev-icon {
    background-image: url(../assets/images/residential/arrow-left.png);
    background-size: cover;
    width: 28px;
    height: 29px;
}

.bg-card {
    border-top-left-radius: 80px;
    border-bottom-right-radius: 80px;
}

.card {
    background-color: #472354;
    border-radius: 24px;
    border: none;
}

a {
    text-decoration: none;
}
.btn-outline-warning{
    color: #323232;
    border: 1px solid #323232;
}

.cursor-pointer {
    cursor: pointer;
}
</style>