<template>
    <footer id="footer">
        <div class="container-fluid px-0 py-5">
            <div class="container">
                <div class="row text-center align-items-center">
                    <div class="col-12 col-md-12 col-lg-6 mb-4 mb-lg-0">
                        <div class="row d-flex justify-content-center">
                            <div class="col-8">
                                <img src="~/assets/images/navbar/harvestcity-logo.png" class="img-fluid" alt="logo harvest city">
                            </div>
                        </div>
                    </div>

                    <div class="col-12 col-md-12 col-lg-6 mt-1 mt-md-0 text-center text-md-center text-lg-start footer-line">
                        <div class="row py-1 ps-0 ps-lg-5">
                            <div class="col mt-4 mt-lg-0">
                                <h2 class="fw-bold">Marketing Office:</h2>
                                <p>Depan Taman Buah Mekarsari.<br>Jl. Boulevard Harvest City No. 1<br>Transyogi KM 15.</p>
                                <!-- <div class="row mb-3">
                                    <div class="col">
                                        <h5 class="fw-bold">Follow Us On :</h5>
                                        <a href="https://www.instagram.com/harvestcity_official/">
                                            <i class="bi bi-instagram icon-size"></i>
                                        </a>
                                    </div>
                                </div> -->
                                <h5 class="fw-bold">Call Us or Whatsapp for Detail Information</h5>
                                <div class="d-block d-md-flex align-items-center">
                                    <a class="btn-wa-footer" href="https://api.whatsapp.com/send/?phone=6281807171888&text=Hallo%2C+Saya+tertarik+dengan+Harvest+City+dari+Website.+Boleh+dibantu+share+promo+dan+detailnya%3F&type=phone_number&app_absent=0">
                                        <button type="button" class="btn btn-warning px-5"><h4 class="m-0"><i class="bi bi-whatsapp"></i> 0818-0717-1888</h4></button>
                                    </a>
                                    <div class="d-block d-md-flex">
                                        <a href="https://www.instagram.com/harvestcity_official/" class="mx-0 mx-md-4">
                                            <i class="bi bi-instagram icon-size"></i>
                                        </a>
                                        <a href="#">
                                            <i class="bi bi-envelope-fill icon-size"></i>
                                        </a>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
                
                <div class="row text-center text-md-center text-lg-start mt-5">
                    <div class="col-12 col-md-12 col-lg-6 mb-4 mb-lg-0">
                        <div class="row d-flex justify-content-center justify-content-md-center justify-content-lg-start">
                            <div class="col-8 d-flex justify-content-center">
                                <div>
                                <h4 class="footer-bot">Member Of</h4>
                                <div class="row align-items-center">
                                    <div class="col-4">
                                        <img src="~/assets/images/footer/footer1.png" class="img-fluid" alt="">
                                    </div>
                                    <div class="col-4">
                                        <img src="~/assets/images/footer/footer2.png" class="img-fluid" alt="">
                                    </div>
                                    <div class="col-4">
                                        <img src="~/assets/images/footer/footer3.png" class="img-fluid" alt="">
                                    </div>
                                </div>
                            </div>
                            </div>
                        </div>
                    </div>

                    <div class="col-12 col-md-12 col-lg-6 mb-4 mb-lg-0">
                        <div class="row d-flex justify-content-center justify-content-md-center justify-content-lg-start">
                            <div class="col-12">
                                <h4 class="footer-bot">Bank Support</h4>
                                <div class="row align-items-center px-3 px-md-0">
                                    <div class="col-12 col-md-6">
                                        <img src="~/assets/images/footer/bank-1.png" class="img-fluid w-100" alt="">
                                    </div>
                                    <div class="col-12 col-md-6">
                                        <img src="~/assets/images/footer/bank-2.png" class="img-fluid w-100" alt="">
                                    </div>
                                    <div class="col-12 col-md-6">
                                        <img src="~/assets/images/footer/bank-3.png" class="img-fluid w-100" alt="">
                                    </div>
                                    <div class="col-12 col-md-6">
                                        <img src="~/assets/images/footer/bank-4.png" class="img-fluid w-100" alt="">
                                    </div>
                                    <!-- <div class="col-3">
                                        <img src="~/assets/images/footer/footer5.png" class="img-fluid" alt="">
                                    </div>
                                    <div class="col-3">
                                        <img src="~/assets/images/footer/footer6.png" class="img-fluid" alt="">
                                    </div>
                                    <div class="col-3">
                                        <img src="~/assets/images/footer/footer7.png" class="img-fluid" alt="">
                                    </div> -->
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
        <div class="container-fluid text-center footer-bg mt-3">
            <small>Copyright © 2022 PT. DWIGUNATAMA RINTISPRIMA</small>
        </div>
    </footer>
</template>

<style scoped>
#footer {
    font-family: TenorSansRegular;
}

#footer p {
    color: #A17F25;
}

#footer h2, h5 {
    color: #453246;
}

button {
    border-radius: 8px;
}

.icon-size {
    color: #A17F25;
    font-size: 30px;
}
.icon-size:hover {
    color: #453246;
    font-size: 30px;
}
.footer-bg {
    background-color: #BB9430;
    color: #eaeaea;
    font-family: MarkProLight;
    letter-spacing: 0.28em;
}
.footer-bot {
    font-family: MontserratMedium;
    border-bottom: 1px solid #A17F25;
    color: #A17F25;
}
.footer-line {
    border-left: 1px solid #000000;
}

@media screen and (max-width:980px) {
.footer-line {
    border-left: 0px solid #000000;
    border-top: 1px solid #000000;
    }
}
</style>