<template>
    <div>
    <!-- popup form -->
    <!-- <div class="modal fade modal-sm" id="popupform" data-bs-backdrop="static" data-bs-keyboard="false" tabindex="-1" aria-labelledby="staticBackdropLabel" aria-hidden="true"> -->
    <div class="modal-overlay" id="popupform">
        <div class=" modal1 modal-dialog modal-dialog-centered">
            <div class="modal-content px-0">
                <!-- <div class="modal-header">

                   
                </div> -->
                <div class="modal-body p-0">
                  
                        <button type="button" class="btn-close" @click="$emit('close-modal')" aria-label="Close"></button>
      

                
                    <form id="form-popup-regular_1" >
                        <img class="img-fluid d-block w-100" src="~/assets/images/banner/banner.webp" alt="">
                        <div class="row px-3 py-3">
                            
                            <div class="col">
                                <div>
                                    <h5>Isi Form untuk Dapatkan Info & Promo Eksklusif</h5>
                                </div>
                                <div class="mb-3">
                                    <input type="text" class="form-control" id="nama" v-model="NamaProspect" placeholder="NAMA" required>
                                </div>
                                <div class="mb-3">
                                    <input type="number" class="form-control" id="hp" v-model="Hp" placeholder="NOMOR WHATSAPP" required>
                                </div>
                                <div class="mb-3">
                                    <input type="email" class="form-control" id="email" v-model="EmailProspect" placeholder="EMAIL" required>
                                </div>
                                <div class="mb-3">
                                    <small><i>*Kami tidak memberikan data anda ke pihak manapun</i></small>
                                </div>
                                <div class="mb-3">
                                    <button type="button" @click="onSubmit" class="btn btn-promo btn-warning btn-block w-100 ">KLAIM PROMONYA SEKARANG</button>
                                </div>

                                <!-- success alert -->
                                <div v-if="infoSuccess" class="alert alert-success d-flex align-items-center" role="alert">
                                    <svg class="bi flex-shrink-0 me-2" width="24" height="24" role="img" aria-label="Success:"><use xlink:href="#check-circle-fill"/></svg>
                                    <div>
                                        {{  infoSuccess }}
                                    </div>
                                </div>
                                
                                <!-- error alert -->
                                <div  v-if="infoError" class="alert alert-danger d-flex align-items-center" role="alert">
                                    <svg class="bi flex-shrink-0 me-2" width="24" height="24" role="img" aria-label="Danger:"><use xlink:href="#exclamation-triangle-fill"/></svg>
                                    <div>
                                        {{  infoError }}
                                    </div>
                                </div>
                                
                              
                            </div>
                        </div>
                    </form>

                    


                   

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
          NamaProspect: '',
          EmailProspect:'',
          Hp: '',
          KodePT: '',
          KodeProject: '',
          TipeSelected: '',
          VerifiedStatus: '',
          infoSuccess:null,
          infoError:null,
          show: true,
          status: '',  
    
        }
      },

      methods: {
          onSubmit() {

            let formData = new FormData()
            formData.append('NamaProspect', this.NamaProspect)
            formData.append('EmailProspect', this.EmailProspect)
            formData.append('Hp', this.Hp) 
            //   formData.append('Message', 'Saya tertarik dengan Unit '+this.TipeSelected)
            formData.append('KodePT', 'DR') 
            formData.append('KodeProject', 'HC') 
            formData.append('Campaign', 'Sakura Indica')
            formData.append('utm_source', this.utm_source)
            formData.append('utm_medium', this.utm_medium)
            formData.append('utm_campaign', this.utm_campaign)
            formData.append('VerifiedStatus', '0') 
              
              let config = {
              headers: {
  
                  'Content-type': 'application/json', //must
  
                      },
                  }
  
                  this.$axios.post('https://api.makutapro.id/prospect/website', formData, config)
                  .then((response) => {   
                      this.status=response.data.meta.status
            
                      if (this.status=='success'){
                          this.infoSuccess = 'Terimakasih, sales representatif kami akan segera menghubungi Anda!'
                          this.NamaProspect = ''
                          this.EmailProspect = ''
                          this.Hp = ''
                          this.TipeSelected = ''
                      }
                    
                  })
                  .catch((error) => {
                      this.infoError = 'Data Anda gagal terkirim, silahkan menghubungi Kami melalui whatsapp'
                  });   
          }
      }
    }
</script>

<style scoped>
#form-popup-regular_1 {
    background-color: #fff;
    border-radius: 15px;
}

#form-popup-regular_1 img {
    border-top-left-radius: 15px;
    border-top-right-radius: 15px;
}

#popupform h5 {
    font-family: MontserratBold;
    font-size: 14px;
}

#popupform p {
    font-family: MontserratMedium;
    font-size: 12px;
}
.btn-close {
    position: absolute;
    z-index: 1;
    right: 12px;
    top: 12px;
    background-color: #fff;
    border-radius: 50%;
    padding: 10px;
    box-shadow: #666;
    opacity: 1;

}
.form-control:focus {
    border-color: #223631;
    box-shadow: 0 0 0 0.2rem rgba(34, 54, 49, 0.25);
} 
.modal-sm {
    left:40%;
}

.modal-overlay {
  position: fixed;
  width: 100%;
  z-index: 1050;
  top: 0;
  bottom: 0;
  left: 0;
  right: 0;
  display: flex;
  justify-content: center;
  background-color: rgba(0,0,0,0.7);
  color: #666;
}
.modal1 {

  z-index: 99999;
  max-width: 400px;
}
small {
    font-size:10px;
    font-family: InterRegular;
}
/* .btn-warning {
    color: #eaeaea;
    background-color: #BB9430;
    border-color: #BB9430;
    font-family: MontserratSemiBold;
}
.btn-warning:hover {
    color: #BB9430;
    background-color: #eaeaea;
    border-color: #BB9430;
    font-family: MontserratSemiBold;
} */

::placeholder {
    font-size: x-small;
}
</style>