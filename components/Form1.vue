<template>
    <div id="form1" class="container-fluid px-0 py-5 position-relative">
        <div class="container text-center">
            <div class="row ">
                <div class="col-md-6">
                    <!-- <img src="~/assets/images/promo/banner.webp" class="img-fluid" alt="promo harvest city"> -->

                    <PromoBanner />

                </div>
                <div class="d-none d-md-block">
                    <div class="col-md-6 px-5 mt-5 mt-md-0 position-absolute py-5 d-flex align-items-center form-box">
                    <div class="d-block">
                        <h5 class="h5">Isi Form untuk Dapatkan Info & Promo Eksklusif Perumahan HARVEST CITY</h5>
                        <form id="form-klaim-promo" @submit="onSubmit">
                            <div class="row font-form mt-3">
                                <div class="col-12 mt-2">
                                    <!-- success alert -->
                                    <div v-if="infoSuccess" class="alert alert-success d-flex align-items-center m-3 text-center" role="alert">
                                        {{  infoSuccess }}
                                    </div>

                                    <!-- error alert -->
                                    <div  v-if="infoError" class="alert alert-danger d-flex align-items-center m-3 text-center" role="alert">
                                        {{  infoError }}
                                    </div>
                                </div>

                                <div class="col-12 col-md-6 mt-2">
                                    <input type="text" class="form-control" v-model="form.nama" id="nama" placeholder="NAMA">
                                </div>
                                <div class="col-12 col-md-6 mt-2">
                                    <input type="email" class="form-control" v-model="form.email" id="email" placeholder="EMAIL ANDA">
                                </div>
                                <div class="col-12 col-md-6 mt-2">
                                    <input type="number" class="form-control" v-model="form.hp" id="hp" placeholder="NOMOR WHATSAPP">
                                </div>
                                <div class="col-12 col-md-6 mt-2">
                                    <select v-model="form.message" class="form-control form-select">
                                        <option value='' selected disabled>PILIH TIPE RUMAH</option>
                                        <option value="SANVITALIA">SANVITALIA</option>
                                        <option value="SOLANDRA">SOLANDRA</option>
                                    </select>
                                </div>
                                <div class="col-12 mt-3">
                                    <small class="fst-italic">*Kami tidak memberikan data anda ke pihak manapun</small>
                                </div>
                                <div class="col-12 mt-3">
                                    <button type="submit" class="btn btn-warning btn-klaim-promo px-3">KLAIM PROMONYA SEKARANG</button>
                                </div>
                            </div>
                        </form>
                    </div>
                </div>
                </div>

                <div class="d-block d-md-none">
                    <div class="col-md-6 px-5 mt-4 mt-md-0 py-5 d-flex align-items-center">
                        <div class="d-block">
                            <h5 class="h5">Isi Form untuk Dapatkan Info & Promo Eksklusif Perumahan HARVEST CITY</h5>
                            <form id="form-klaim-promo" @submit="onSubmit">
                                <div class="row font-form mt-3">

                                    <div class="col-12 mt-2">
                                        <!-- success alert -->
                                        <div v-if="infoSuccess" class="alert alert-success d-flex align-items-center m-3 text-center" role="alert">
                                            {{  infoSuccess }}
                                        </div>

                                        <!-- error alert -->
                                        <div  v-if="infoError" class="alert alert-danger d-flex align-items-center m-3 text-center" role="alert">
                                            {{  infoError }}
                                        </div>
                                    </div>
                                    <div class="col-12 col-md-6 mt-2">
                                        <input type="text" class="form-control" v-model="form.nama" id="nama" placeholder="NAMA">
                                    </div>
                                    <div class="col-12 col-md-6 mt-2">
                                        <input type="email" class="form-control" v-model="form.email" id="email" placeholder="EMAIL ANDA">
                                    </div>
                                    <div class="col-12 col-md-6 mt-2">
                                        <input type="number" class="form-control" v-model="form.hp" id="hp" placeholder="NOMOR WHATSAPP">
                                    </div>
                                    <div class="col-12 col-md-6 mt-2">
                                        <select v-model="form.message" class="form-control form-select">
                                            <option value='' selected disabled>PILIH TIPE RUMAH</option>
                                            <option value="SANVITALIA">SANVITALIA</option>
                                            <option value="SOLANDRA">SOLANDRA</option>
                                        </select>
                                    </div>
                                    <div class="col-12 mt-3">
                                        <small class="fst-italic">*Kami tidak memberikan data anda ke pihak manapun</small>
                                    </div>
                                    <div class="col-12 mt-3">
                                        <button type="submit" class="btn btn-warning btn-klaim-promo px-3">KLAIM PROMONYA SEKARANG</button>
                                    </div>
                                </div>
                            </form>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>
<script>
  export default {
    data() {
      return {
        form: {
          nama: '',
          email: '',
          hp: '',
          message: '',
        },
      
        utm_source : '',
        utm_medium: '',
        utm_campaign: '',

        show: true,
        status:null,
        infoSuccess:null,
        infoError:null

      }
    },
    created() {
        if (this.$route.query.utm_source) {
            this.utm_source = this.$route.query.utm_source
        }

        if (this.$route.query.utm_medium) {
            this.utm_medium = this.$route.query.utm_medium
        }

        if (this.$route.query.utm_campaign) {
            this.utm_campaign = this.$route.query.utm_campaign
        }

    },
    methods: {
      onSubmit(event) {
         event.preventDefault()

        if (this.form.nama == '' || this.form.email == '' || this.form.hp == '' || this.form.message == '') {
            this.infoError = 'Form harus diisi semua'
            return
        }

         let formData = new FormData()
            formData.append('NamaProspect', this.form.nama)
            formData.append('Hp', this.form.hp)
            formData.append('EmailProspect', this.form.email)
            formData.append('Message', this.form.message)
            formData.append('KodePT', 'DR')
            formData.append('KodeProject', 'HC')
            formData.append('Campaign', 'Sakura Indica')
            formData.append('utm_source', this.utm_source)
            formData.append('utm_medium', this.utm_medium)
            formData.append('utm_campaign', this.utm_campaign)

            // formData.append('Campaign', '')
            // formData.append('KodePT', 'MKT')
            // formData.append('KodeProject', 'TEST')
            formData.append('VerifiedStatus', '1')

            let config = {
                headers: {
                    'Access-Control-Allow-Origin': '*',
                    'Content-type': 'application/json', //must
                    'Access-Control-Allow-Methods': 'GET, POST',
                    'Access-Control-Allow-Headers': 'X-Requested-With',
                    'Set-Cookie' : 'cross-site-cookie=whatever, flavor=choco, SameSite=None, Secure',
                },
            }
          
            this.$axios.post('https://api.makutapro.id/prospect/website', formData, config)
            .then((response) => {                    
                    this.status = response.data.status
                    this.show = false
                    if(this.status == 400){
                        this.infoError = 'No.Hp Anda sudah terdaftar di sistem kami, silahkan hubungi Kami melalui telephone / whatsapp'
                        // alert(this.infoError)
                        this.nama = ''
                        this.hp = ''
                    }else if(this.status == 402){
                        this.infoError = 'Nomer Hp harus berupa angka'
                        // alert(this.infoError)
                        this.nama = ''
                        this.hp = ''
                    }else {
                        this.infoSuccess = 'Terimakasih, sales representatif kami akan segera menghubungi Anda!'
                        // alert(this.infoSuccess)
                        this.nama = ''
                        this.hp = ''
                    }  
            })
            .catch((error) => {
                // let { data } = error
                this.status = error.status
                this.show = false
                this.infoError = 'Data Anda gagal terkirim, silahkan menghubungi Kami melalui whatsapp'
                alert(this.infoError)
                this.nama = ''
                this.hp = ''
            })
      },
     
    }
  }
</script>

<style scoped>
#form1 {
    background-color: #4A324B;
    font-family: TenorSansRegular;
    color: #fff;
}
#form1 ::placeholder,
select .form-control {
    font-size: x-small;
    color: #5C1B73;
}

.form-box {
    background: linear-gradient(180deg, #BA9616 0%, #A27F25 100%);
    top: -50px;
    right: calc((100vw - 100%) + 10vw);
    height: calc(100% + 50px);
    width: calc(100% - 60vw);
    border-top-left-radius: 22px;
    border-top-right-radius: 22px;
}

.font-form {
    font-family: InterRegular;
}
.form-select {
    font-size: x-small;
    color: #5C1B73;
    font-family: InterRegular;
    padding-top: 10px;
    padding-bottom: 10px;
}
.form-control {
    background-color: #E9E9E9;
}
h5 {
    color: #E9E9E9;
}
</style>