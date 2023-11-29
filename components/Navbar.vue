<template>
    <header class="position-relative z-3">
        <!-- <nav class="navbar navbar-expand-lg bg-body-light shadow-sm">
            <div class="container-fluid ">
                <a class="navbar-brand" href="#">
                    <img src="~assets/images/navbar/logo.webp" alt="LOGO" width="100">
                </a>
                <div class="ms-auto">
                    <a href="https://api.whatsapp.com/send?phone=6281717883000&text=Hallo%2C%20Saya%20tertarik%20dengan%20Kota%20Legenda%20dari%20Website.%20Boleh%20dibantu%20share%20promo%20dan%20detailnya%3F" target="_blank" class="btn btn-primary btn-call-us px-3">HUBUNGI KAMI</a>
                </div>
            </div>
        </nav> -->

        <div class="bg-transparent p-0 position-absolute w-100">
            <div class="container d-flex justify-content-center align-items-center">
                <a class="navbar-brand p-0" href="/">
                    <img src="~assets/images/navbar/logo.webp" class="img-fluid logo" alt="LOGO" width="150">
                </a>

                <div class="ms-auto">
                    <a href="https://api.whatsapp.com/send/?phone=6281807171888&text=Hallo%2C+Saya+tertarik+dengan+Harvest+City+dari+Website.+Boleh+dibantu+share+promo+dan+detailnya%3F&type=phone_number&app_absent=0" target="_blank" class="btn btn-warning fs-5 px-3 px-md-5">0818 0717 1888</a>
                </div>
            </div>
        </div>

    </header>
</template>

<style scoped>

#navbar {
    transition: 0.5s;
    font-family: TenorSansRegular;
    background:rgba(255, 255, 255, 0.5);
}

#btn-hubungi-kami {
    text-decoration: none;
}

@media screen and (max-width:768px) {
    .logo {
        width: 35%;
    }

    .btn-warning {
        width: 8rem;
        font-size: 12px !important;
    }
}
</style>