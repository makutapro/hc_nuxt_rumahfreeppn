<template>
    <div class="container text-center py-5">
        <h2 class="fs-1">Sakura Indica</h2>
        <h5>SITEPLAN</h5>
        <div class="row mb-4 d-flex justify-content-center align-items-center">
            <div class="col-12 col-md-8 mt-5">
                <img :src="siteplan" class="img-fluid w-100" alt="siteplan sakura indica harvest city">
            </div>
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            siteplan : ''
        }
    },
    mounted() {
        this.$axios.get('https://admharvest.harvestcity.co.id/get_siteplan?id=15')
        .then((response) => {
            this.siteplan = response.data.data

            if (this.siteplan == null) {
                this.siteplan = require('~/assets/images/siteplan/siteplan-sakuraindica.jpeg')
            }
        })
        .catch((error) => {
            this.siteplan = require('~/assets/images/siteplan/siteplan-sakuraindica.jpeg')
        })

        // data-aos="fade-left" data-aos-duration="2000"
        // AOS.init();
    }
}
</script>