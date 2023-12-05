<template>
    <div>
        <img :src="promoImage" class="img-fluid" alt="promo harvest city">
    </div>
</template>

<script>
export default {
    data() {
        return {
            promoImage : ''
        }
    },
    mounted() {
        this.$axios.get('https://admharvest.harvestcity.co.id/api/get_promo_banner?id=15')
        .then((response) => {
            this.promoImage = response.data.data

            if (this.promoImage == null) {
                this.promoImage = require('~/assets/images/promo/promo-sakura-indica.webp')
            }
        })
        .catch((error) => {
            this.promoImage = require('~/assets/images/promo/promo-sakura-indica.webp')
        })
    }
}
</script>