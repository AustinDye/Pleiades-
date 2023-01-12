<template>
    <div class="row g-0 m-0">
        <div class="col-12"><h1>contact us today</h1></div>
    </div>
    <div class="container justify-content-center align-items-center d-flex">
      <div class="row justify-content-center align-items-center">
        <div class="col-6 contact-info justify-content-center align-items-center d-flex flex-column">
          <h5>Pleiades Projectworks LLC</h5>
          <p><b>Email: </b> austindye@pleiadesprojectworks.com </p>
          <p>Monday - Friday</p>
        </div>
        <div class="col-6 contact-form d-flex justify-content-center align-items-center d-flex flex-column p-5">
     
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
              </div>
      
              <div class="d-flex flex-column justify-content-center align-items-center">
                <textarea placeholder="Your message" name="message" required />
                
                  <button type="submit">Send us a message</button>
               
              </div>
             
             
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
        margin-left:2.5em;
       
        
        
  
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
        background-color: rgb(0, 0, 0);
      
        box-shadow: none;
        border: none;
        outline: none;
        width: 50%;
        padding: .5em;
        color: white;
    }

    textarea{
        height: 30vh;
        width: 20vw;
        margin: 1em;

        @media (max-width: 480px) {
            width: 80%;
            margin: 1em;
          
         }
    }
  </style>