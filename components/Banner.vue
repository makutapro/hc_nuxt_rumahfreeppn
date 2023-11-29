<template>
    <section id="banner" class="container-fluid px-0">
        <!-- <div class="d-none d-md-none d-lg-block"> -->
        <div class="d-none d-md-block">
            <img :src="bannerDesktop" class="img-fluid w-100" alt="banner harvest city">
            <div class="container-md">
                <div class="container over-text mt-3 mt-md-0 w-100">
                    <div class="row">
                        <div class="col-12 col-md-6 text-center text-md-start">
                            <h1 class="h1">PERUMAHAN EKSKLUSIF<br>FASILITAS TERLENGKAP</h1>
                        </div>
                        <div class="col-12 col-md-6 d-none d-md-block">
                            <h2 class="h2">Kawasan Terbesar di Cibubur</h2>
                            <ul>
                                <li><p class="mb-0">Perkembangan infrastruktur skala kota</p></li>
                                <li><p>Trendsetter perumahan di koridor Cibubur</p></li>
                            </ul>
                        </div>
                    </div>
                </div>
            </div>
        </div>

        <div class="d-block d-md-none">
            <img :src="bannerMobile" class="img-fluid w-100" alt="banner harvest city">
            <div class="over-text mt-3 mt-md-0">
                <div class="row">
                    <div class="col-12 text-center">
                        <h1 class="h1">PERUMAHAN EKSKLUSIF<br>FASILITAS TERLENGKAP</h1>
                    </div>
                    <div class="col-12 text-center mt-2">
                        <h2 class="h2 mb-0">Kawasan Terbesar di Cibubur</h2>
                        <p class="mb-0"><i class="bi bi-check2-circle text-success me-2"></i>Perkembangan infrastruktur skala kota</p>
                        <p><i class="bi bi-check2-circle text-success me-2"></i>Trendsetter perumahan di koridor Cibubur</p>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>

<script>
export default {
    data() {
        return {
            bannerDesktop : '',
            bannerMobile : '',
        }
    },
    mounted() {
        this.$axios.get('https://admharvest.harvestcity.co.id/api/get_banner?id=15')
        .then((response) => {
            if (response.data.data == null) {
                this.bannerDesktop = require('~/assets/images/banner/banner.webp')
                this.bannerMobile = require('~/assets/images/banner/banner-mobile.webp')
            }
            else {
                this.bannerDesktop = response.data.data.banner_desktop ?? require('~/assets/images/banner/banner.webp')
                this.bannerMobile = response.data.data.banner_mobile ?? require('~/assets/images/banner/banner-mobile.webp')
            }
        })
        .catch((error) => {
            this.bannerDesktop = require('~/assets/images/banner/banner.webp')
            this.bannerMobile = require('~/assets/images/banner/banner-mobile.webp')
        })
    }
}
</script>

<style scoped>
#banner {
    overflow-x: hidden;
}

#banner h1 {
    font-family: TenorSansRegular;
    font-weight:bold;
    color: #453246;
}

#banner h2 {
    font-family: MontserratSemiBold;
    color: #A17F25;
}

#banner p {
    font-family: MontserratRegular;
    color: #453246;
}
.container-fluid {
    position: relative;
}
.over-text {
    position: absolute;
    top: 15%;
}
.over-text-md {
    position: absolute;
    bottom: 0;
}
.padding {
    padding-top: 120px;
}
.padding-md {
    padding-top: 150px;
}

@media (max-width: 767px) {
    h1 {
        font-size: calc(1rem + 1.5vw);
    }

    h2 {
        font-size: calc(.7rem + 1.5vw);
    }

    p {
        font-size: calc(.5rem + 1.5vw);
    }

    .over-text {
        position: absolute;
        top: calc(15% - 10px);
        left: 0;
        right: 0;
    }
}
</style>