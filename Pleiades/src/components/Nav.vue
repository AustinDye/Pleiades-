<template>
    <nav class="navbar navbar-dark  fixed-top">
        <div class="container-fluid ">
            
          <a class="navbar-brand" href="#">Pleiades Projectworks</a>
          <button class="navbar-toggler" type="button" data-bs-toggle="offcanvas" data-bs-target="#offcanvasDarkNavbar" aria-controls="offcanvasDarkNavbar">
            <span class="">Get Started</span>
          </button>
          <div class="offcanvas offcanvas-end p-5" tabindex="-1" id="offcanvasDarkNavbar" aria-labelledby="offcanvasDarkNavbarLabel">
                        
            <button type="button" class="btn-close d-flex justify-content-center align-items-center mb-5 p-3" data-bs-dismiss="offcanvas" aria-label="Close">close</button>
            <div class="container justify-content-center align-items-center d-flex">
                
                <div class="row justify-content-center align-items-center">
                    
                  <div class="col-12 contact-info justify-content-center align-items-center d-flex flex-column">
                    
                    <h5>Pleiades Projectworks LLC</h5>
                    <p><b>Email: </b> info@pleiadesprojectworks.com </p>
                    <p>Monday - Friday</p>
                  </div>
                  <div class="col-12 contact-form d-flex justify-content-center align-items-center d-flex flex-column p-5">
               
                      <form
                      class=""
                        :action="FORM_ENDPOINT"
                        @submit="handleSubmit"
                        method="POST"
                        target="_blank"
                      >
                        <div class="">
                          <input class="p-1 m-1" type="text" placeholder="Your name" name="name" required />
                          <input class="p-1 m-1 mb-2 " type="email" placeholder="Email" name="email" required />
                        </div>
                
                        <div class="d-flex flex-column justify-content-center align-items-center">
                          <textarea placeholder="Your message" name="message" required />
                          
                            <button class="button" type="submit">Send us a message</button>
                         
                        </div>
                       
                       
                      </form>
                  
                      <div v-if="submitted">
                        <h2>Thanks you!</h2>
                        <div>We'll be in touch soon.</div>
                      </div>
                
                  </div>
                </div>
              
          </div>
          </div>
        </div>
      </nav>
</template>

<script>
     export default {
    name: "App",
    data: () => ({
      submitted: false,
      FORM_ENDPOINT: "https://public.herotofu.com/v1/35805ee0-912b-11ed-a003-6f0b76086b1c",
    }),
  
    methods: {
      handleSubmit() {
        setTimeout(() => {
          this.submitted = true;
        }, 100);
      },
    },
  };
</script>

<style lang="scss" scoped>
.navbar{
    margin-top: 85vh;
    width: 30%;
    background-color: black;
    margin-left: 35%;
    margin-right: 35%;
    border-radius:60px;
    font-family: geo-light;
    font-weight: 900;
    outline: .1em solid rgba(255, 255, 255, 0.302);

    @media (max-width: 820px) {

        margin-top: 0;
        width: 100vw;
        margin-left: 0;
        margin-right: 0;
        border-radius:0;
        outline: none;
   
  
     }

  
}

.navbar-brand{
    padding: 1em;
    @media (max-width: 380px) {
        font-size: 1em;
        height: 40px;
        width: 50%;
   
      }
 
    
}



.text-bg-dark{
    background-color: black;
    background: black;
    color: black;
}


.contact-form{
    background-color: white;
    padding: 2em;
   

   
  }

  .contact-info{
    background-color: black;
    padding: 2em;
    color: white;
    border-radius: 2px;
    @media (max-width: 820px) {

   
      padding: 2em;
      

   }
  
    
  }

 

  .button{
      background-color: rgb(0, 0, 0);
      box-shadow: none;
      border: none;
      outline: none;
      margin-top:5vh;
      width: 100%;
      padding: .5em;
      color: white;
  }

  textarea{
    width: 100%;
    height: 60%;
 

      @media (max-width: 480px) {
          width: 80%;
          margin: 1em;
        
       }
  }

  .offcanvas{
   border-radius: 25px;
   max-height: 90vh;
   
  }

  .btn-close{
    background-color: black;
    background: black;
    color: white;
    font-size: 1.2em;
    border-radius: 2px;
    width: 3em;
    
  }

  .navbar-toggler{
    border-radius:60px;
    width: 30%;
    height: 60px;
    font-size: 1em;
    font-family: geo-light;
    background: black;
    color: rgba(255, 255, 255, 0.702);
    border: solid rgba(255, 255, 255, 0.175) 2px;
    @media (max-width: 380px) {
        font-size: .8em;
        height: 40px;
        width: 30%;
   
      }
   

}
</style>