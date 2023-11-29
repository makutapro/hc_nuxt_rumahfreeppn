<template>
    <section id="brosur" class="container-fluid px-0 py-5">
        <div class="container text-center">
            <div class="row">
                <div class="col-md-6">
                    
                    <PromoBanner />

                </div>
                <div class="col-md-6 d-flex justify-content-center align-items-center mt-5 mt-md-0 divider">
                    <div>
                        <h3 class="mt-4 mt-md-0">Dapatkan Informasi lengkap Harvest City,<br>silahkan download E-Brochure di bawah ini.</h3>
                        <button type="button" class="btn btn-warning fs-5 py-2 px-5 mt-3" @click="showModal = true">DOWNLOAD SEKARANG</button>
                    </div>
                
                </div>
            </div>
    

        </div>
        <PopUpForm v-show="showModal" @close-modal="showModal = false" />
    </section>
</template>

<script>
    export default{
        data(){``
            return {
                showModal: false
        }
    }
}
</script>

<style scoped>
#brosur {
    background-color: #4A324B;
    color: #fff;
}

#brosur h3 {
    color: #fff;
    font-family: TenorSansRegular;
}

.divider {
    border-left: 1px solid #A17F25;
}

button {
    border-radius: 8px;
    font-family: TenorSansRegular;
}

@media (max-width: 768px) {
    .divider {
        border-left: 0px;
        border-top: 1px solid #A17F25;
        margin-bottom: 10px;
    }
}

</style>