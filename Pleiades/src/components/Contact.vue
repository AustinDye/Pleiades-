<template>
    <div id="contact" class="row g-0" v-scrollanimation>
        <div class="col-12"><h1>contact us today</h1></div>
    </div>
    <div class="container justify-content-center align-items-center d-flex" v-scrollanimation>
      <div class="row ">
        <div class="col-6 contact-info justify-content-center align-items-center d-flex flex-column" v-scrollanimation>
          <h5>Pleiades Projectworks LLC</h5>
          <p><b>Email: </b> info@pleiadesprojectworks.com </p>
          <p>Monday - Friday</p>
        </div>
        <div class="col-6 contact-form d-flex  justify-content-center align-items-center d-flex flex-column p-5" v-scrollanimation>
     
            <form
            class=""
              :action="FORM_ENDPOINT"
              @submit="handleSubmit"
              method="POST"
              target="_blank"
            >
              <div class="">
                <input type="text" placeholder="Your name" name="name" required />
                <input type="email" placeholder="Email" name="email" required />
                <textarea placeholder="Your message" name="message" required />
              </div>
              <button type="submit">Send us a message</button>
             
            </form>
        
            <div v-if="submitted">
              <h2>Thanks you!</h2>
              <div>We'll be in touch soon.</div>
            </div>
      
        </div>
      </div>
    
</div>
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

  <style scoped lang="scss">

  .before-enter {
    opacity: 0;
    transform: translateX(50%);
    transition: all 0.5s ease;
  }
  
  .enter {
    opacity: 1;
    transition-delay: 0.1s;
    transform: translateX(0);
  }
    .container{
        
     
  
        height: 65vh;
        border-radius: 25px;
        margin-bottom: 7vh;
        

        @media (max-width: 480px) {
            width: 90%;
          
             
         }
    }

    h1{
        margin-top: 7vh;
        margin-bottom: 7vh;
        color: white;
        font-size: 8em;
        font-family: geo-medium;
        padding-bottom: 5vh;
        text-align: center;
    
        @media (max-width: 480px) {
           font-size: 5em;
           margin-bottom: 15vh;
        }
    
         /* Media Query for Tablets Ipads portrait mode */
       
      
    }

    h5{
      color: white;
      font-size: 2em;
      font-family: geo-light;
    }

    p{
      color: white;
      font-size: 1em;
      font-family: geo-light;
    }

    input{
        padding: .5em;
    
       
        
        
  
    }

    #contact h1{
      @media (max-width: 300px) {
       
        font-size: 5em;
        margin-bottom: 38.5vh;
       }
    }

    .contact-form{
      background-color: white;
      padding: 2em;
      width: 50%;
      height: 65vh;
      border-radius: 0px 25px 25px 0px;
       @media (max-width: 500px) {
        height: 100%;
        width: 100%;
        border-radius: 0px 0px 25px 25px;
        margin-bottom: 7vh;
       }

     
    }

    .contact-info{
      background-color: black;
   
      height: 65vh;
      border-radius: 25px 0px 0px 25px;
      @media (max-width: 480px) {
        height: 100%;
        width: 100%;
        padding: 2em;
        
  
     }
     @media (max-width: 500px) {
     
      border-radius: 25px 25px 0px 0px;
   
     }
      
    }

    button{
        background: linear-gradient(
          90deg,
          black 0%,
          black 50%,
          rgba(251, 7, 217, 1) 75%,
          rgba(255, 0, 0, 1) 100%
      );
        border-radius: 25px;
        box-shadow: none;
        border: none;
        outline: none;
        width: 50%;
        padding: .5em;
        color: white;
        transition: all 1s;
    }

    button:hover{
      background: black;
    transition: all 1s;
    }

    textarea{
        height: 30vh;
        width: 100%;
        margin-top: 1em;
        margin-bottom: 1em;

        @media (max-width: 480px) {
            width:100%;
    
          
         }
    }

    .row{
      width: 100vw;
    }

    @media (max-width: 380px){
      #contact{
        margin-bottom: 5em;
      }
    }
  </style>