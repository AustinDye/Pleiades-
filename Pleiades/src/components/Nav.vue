<template>
    <nav id="nav" class="navbar navbar-dark fixed-top">
        <div class="container-fluid ">
            
          <img class="navbar-brand" src="../assets/img/logo-top.svg" alt="">
          <a id="serv-link" class="d-none d-md-flex" href="#services">Services</a>
          <a id="why-link" class="d-none d-md-flex" href="#whyus">Why Choose Us?</a>
          <a id="work-link" class="d-none d-md-flex" href="#works">Our Work</a>
          <button class="navbar-toggler" type="button" data-bs-toggle="offcanvas" data-bs-target="#offcanvasDarkNavbar" aria-controls="offcanvasDarkNavbar">
            <span class="">Get Started</span>
          </button>
          <div class="offcanvas d-flex justify-content-center align-items-center offcanvas-end p-5" tabindex="-1" id="offcanvasDarkNavbar" aria-labelledby="offcanvasDarkNavbarLabel">
                        
            <button type="button" class="btn-close d-flex justify-content-center align-items-center mb-5" data-bs-dismiss="offcanvas" aria-label="Close">close</button>
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
                          <input class="p-1 m-1 " type="email" placeholder="Email" name="email" required />
                          <textarea class="p-1 m-1" placeholder="Your message" name="message" required />
                          
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

    mounted() {

        let nav = document.getElementById('nav');
        let serv = document.getElementById('serv-link');
        let why = document.getElementById('why-link');
        let work = document.getElementById('work-link');
        

        window.addEventListener('scroll', function(e) {
            let scroll = window.pageYOffset || document.documentElement.scrollTop || document.body.scrollTop || 0;

            if(scroll > 400 && scroll < 1000){
                nav.style.opacity = 1;
                window.history.pushState("object or string", "Title", "/#services");
            }

            if(scroll > 2800 && scroll < 3600){
                window.history.pushState("object or string", "Title", "/#whyus");
              
            }

            if(scroll > 3600 && scroll < 4000){
                window.history.pushState("object or string", "Title", "/#works");
                
            }

            if(scroll > 4000){
                window.history.pushState("object or string", "Title", "/#contact");
               
            }
            

       

           
        });

        },
    
  
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

#nav{
    opacity: 0;
}


.navbar{
    background-color: black;
    margin:  auto;
  

    font-family: geo-light;
    font-weight: 900;
    outline: .1em solid rgba(255, 255, 255, 0.302);
    transition: all 500ms;
    

    @media (max-width: 820px) {

        margin-top: 0;
        width: 100vw;
        margin-left: 0;
        margin-right: 0;
        border-radius:0;
        outline: none;
       
     }

  
}
a{
  font-family: geo-light;
  font-weight: 500;
  font-size: 1.3em;
  color: rgba(255, 255, 255, 0.713);
  text-decoration: none;
  transition: .5s ;
  
}

a:hover{
  color: white;
  border-bottom: 1px white solid;
  font-size: 1.4em;
}

.navbar-brand{
    padding: 1em;
    height: 20%;
    width: 20%;
    
    @media (max-width: 380px) {
    
        height: 50%;
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
    background: linear-gradient(
      90deg,
      black 0%,
      black 50%,
      rgba(251, 7, 217, 1) 75%,
      rgba(255, 0, 0, 1) 100%
    );
      box-shadow: none;
      border: none;
      outline: none;
      margin-top:1vh;
      width: 100%;
      padding: .5em;
      color: white;
      border-radius: 25px;

    

      
  }

  textarea{
    width: 100%;
    height: 15vh;
 

      @media (max-width: 480px) {
          width: 100%;
  
        
       }
  }

  .offcanvas{
   border-radius: 25px;
   max-height: 90vh;
   margin-top: 10vh;

   @media (max-width: 280px) {
    border-radius: 0;
    max-height: 100vh;
    margin-top:0;

  }
   
  }

  .btn-close{
    background: none;
    background-color: black;
    opacity: 1;
    color: white;
    font-size: 1.2em;
    border-radius: 25px;
    padding: .5em;
    width: 100%;
    margin-top: 10vh;

    @media (max-width: 280px) {
      width: 100%;
    
    }

    
    
  }

  .navbar-toggler{
    border: none;
    
    border-radius:60px;
    padding: .5em;
    margin-right: 5vw;
    font-size: 1.4em;
    font-family: geo-light;
    background:none;
    color: rgb(255, 255, 255);
    transition: all .5s;
  
    
    @media (max-width: 380px) {
        font-size: .8em;
        height: 40px;
        width: 30%;
   
      }
   

}

.navbar-toggler:hover{
    border: rgba(255, 255, 255, 0.445) solid .1em;
}

.navbar-toggler:active{
  border: rgba(255, 255, 255, 0.445) solid .1em;
}

.navbar-toggler:visited{
  border: rgba(255, 255, 255, 0.445) solid .1em;
}

</style>